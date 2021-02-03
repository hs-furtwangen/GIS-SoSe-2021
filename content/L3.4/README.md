## _V_ **3.4** Datenbankzugriff über Server

### MongoDB in Node
Bisher wurde die Datenbank noch direkt über die MongoShell angesprochen. Damit wir aber die Datenbank ohne manuelles Zutun verwenden können, müssen wir diese mit unserem Node.JS Server verbinden. Was bisher von Hand mit der MongoShell erledigt wurde, soll also das Node.js-Programm bewerkstelligen. Hierzu muss Node zunächst um die entsprechenden Module für die Arbeit mit MongoDB erweitert werden. Führen Sie also die Kommandos `npm install @types/mongodb` sowie `npm install mongodb` auf der obersten Ebene ihres GIS-Projektes / Repositories aus. 

Die Datei `package.json` sollte nun neue Einträge unter `dependencies` aufweisen, welche auf die Module und Versionen von MongoDB verweisen. Damit weiß dann auch z.B. Heroku, mit welchen Modulen das Projekt arbeitet, ohne dass diese Module im Github-Repository mitgeliefert werden. Überprüfen Sie zudem noch einmal die Datei `.gitignore`, damit nicht versehentlich diese Module in Ihre Versionskontrolle geraten.

Das Node-Modul `mongodb` stellt verschiedene Standardobjekte zur Verfügung, mit denen die Datenbankoperationen innerhalb der Node-Umgebung ausgeführt werden können. Wie zuvor die Module `http` und `url` wird auch `mongodb` importiert, in diesem Fall z.B. als `Mongo`: 
```typescript
import * as Mongo from "mongodb";
```

### MongoClient
Stellt, wie zuvor die MongoShell, innerhalb der Node-Umgebung eine Verbindung mit dem Datenbanksystem her. Ein neues MongoClient-Objekt erwartet für seine Erzeugung als Parameter eine URL und gegebenenfalls noch Zusatzoptionen. Die Methode `connect` des Mongo Clients liefert eine Promise, auf deren Erfüllung gewartet werden kann.

```typescript
let mongoClient: Mongo.MongoClient = new Mongo.MongoClient(_url, options);
await mongoClient.connect();
```

### Collection
Eine Variable von diesem Typ referenziert direkt eine Collection der Datenbank. Darauf können dann die aus der MongoShell bekannten Operationen ausgeführt werden. 
```typescript
let orders: Mongo.Collection = mongoClient.db("Test").collection("Students");
orders.insert({...});
```

### Implementation

>**Hinweis zu den Videos:** Auch dieses mal gilt wieder: Die Videos kommen aus dem EIA2 Kurs, darum sind evtl. manche Dinge für Sie nicht 1 zu 1 übernehmbar. Die darin vorgestellten Konzepte sind jedoch wichtig und hilfreich für diese Woche. 

<div align="center"><video controls width="30%"> 
  <source src="http://games.hs-furtwangen.de/EIA2_Video/L07_V3_Implementation.mp4" type="video/mp4"> 
<a href="http://games.hs-furtwangen.de/EIA2_Video/L07_V3_Implementation.mp4">Video</a>
</video>    
</div>

### Test
> - Starten Sie den Server in einem dritten Terminalfenster. MongoDB sollte den Verbindungsversuch erkennen und eine zweite Connection anzeigen.
> - Starten Sie den Client in einem kleinen neuen Browserfenster. Am besten ordnen Sie die Fenster so an, so dass Ihr Bildschirm nun horizontal und vertikal halbiert erscheint. 
> - Setzen Sie mit dem Client mehrere unterschiedliche Anfragen ab und beobachte die Ausgaben im Serverfenster. 
> - Fragen Sie mit der MongoShell die Collection "Orders" der Datenbank "Cocktail" ab um zu schauen, ob die Bestellungen/Datensätze eingetragen wurden (oder eben welche Benennung Sie gewählt haben).
> - Ersetzen Sie nun im Servercode den URL zum Datenbankserver mit dem von ihrer remote DB kopierten Connection-String (s. L10). Sie können ihn sich auch unter Clusters->Connect noch einmal anzeigen lassen.
> - Starten Sie ihren lokalen Server neu. Setzen Sie mit dem Client weitere Datensätze ab und prüfen Sie in Atlas ob die Datensätze in der Online-Datenbank ankommen.

<div align="center"><video controls width="30%"> 
  <source src="http://games.hs-furtwangen.de/EIA2_Video/L07_V4_Test.mp4" type="video/mp4"> 
<a href="http://games.hs-furtwangen.de/EIA2_Video/L07_V4_Test.mp4"><img src="../X01_Appendix/Img/video.jpg" width="25%"/></a>
</video>    
</div>

### Ausbau 
> - Um es einfacher zu machen, zwischen lokaler und remote DB zu wechseln, können Sie folgendes tun: Erweiteren Sie ihren Server derart, dass beim Start ein Argument entgegen genommen (z.B. eine der beiden Zeichenketten "local" und "remote") und anhand dessen entschieden wird, ob die lokale oder die Online-Datenbank genutzt wird. ([Info Commandline Argumente Auslesen](https://nodejs.org/en/knowledge/command-line/how-to-parse-command-line-arguments/): Sie brauchen nur die ganz einfachen Basics, und können darum nach dem zweiten Beispiel aufhören zu lesen)
>   - Lassen Sie nun Heroku Ihren Server bauen. Passen Sie dazu die Steuerdatei `package.json` so an, dass der Pfad zum neuen Server eingetragen ist und bei der Startanweisung das Argument mitgegeben wird z.B. 
  ```typescript
  "scripts": {
    "start": "node PfadZumServer/Server.js remote"
  },
  ```
> - Implementieren Sie eine Funktion retrieveOrders, welche mit `orders.find()` alle Bestellungen ausliest und ein Array von `Orders` zurückliefert. Nutzen Sie dazu die asynchrone Funktion `toArray()` des von `find()` zurückgegebenen Cursor-Objektes.
> - Implementieren Sie eine Erweiterung der Funktion `handleRequest`, so dass retrieveOrders aufgerufen und das Ergebnis als (JSON-)Zeichenkette in die Serverantwort eingefügt wird, wenn der Server dazu aufgefordert wird, z.B. mit dem Query-String `command=retrieve`, oder unter einem eigenen Pfad `/retrieve`. Eine Clientsoftware könnte damit die Datensätze abrufen.

### Typescript Dokumentation

https://www.typescriptlang.org/

---

## **?!** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A-Termin)

Zusammenfassung von: [&lt;TawsTm&gt;](https://github.com/TawsTm)

### Aufgrund von MogoDB in GIS-Ordner aktualisiert sich der Live Server ständig?
Ihr könnt die html-Datei einfach direkt öffnen, da ihr den Live-Server gerade nicht braucht. Für die Endabgabe müsst ihr schauen, dass ihr die DB nicht in denselben Ordner legt, wenn ihr einen Live-Server benutzt.

### Server Datenbank Wer spricht mit wem?
Wir haben unseren Client Server und die Datenbank. Der Server bei Heroku der Client bei Github und die DB bei Mongo. Anfrage von Client an Server, der es verarbeitet und es an die Datenbank weiterleitet. Die Datenbank kommuniziert mit dem Server und der Server gibt im Anschluss an den Client die Antwort.

### Die Anfrage an den Server läuft über eine URL?
Ja, hier kommen GET und POST ins Spiel.

### Wie ist MongoDB aufgebaut?
MongoDB besteht aus einem Clusterkopf, in dem die Datenbanken drin sind, in einer Datenbank können Collections sein. In den Collections finde ich meine Dateien als JavaScript bzw. JSON-Objekte wieder.

### Wie ist es mit Username und Passwort anlegen?
Es geht eine Anfrage an den Server und dieser verarbeitet die eingegebenen Daten und speichert diese im Falle von Richtigkeit in der Datenbank und gibt im besten Fall dem Client eine Rückmeldung.

