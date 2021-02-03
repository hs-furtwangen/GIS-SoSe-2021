## _P_ **2.5** Kommunikation

**a)** Ändern Sie ihre `data.ts` Datei so um, dass sie ausschließlich aus den JSON Daten besteht (und damit zur `data.json` wird).

**b)** Ändern Sie die Funktion, welche bisher die JSON Daten eingelesen hat, so um, dass diese zunächst über `fetch` aus dem Internet geladen werden. An diesem Punkt sollte die Seite wieder genauso wie letzte Woche funktionieren.

**c)** Fügen Sie der "Display Seite" (die in der alle ausgewählten Dinge gemeinsam am Ende angezeigt werden) eine Funktion hinzu, welche die Daten, die im Browsercache gespeichert sind, an die URL `https://gis-communication.herokuapp.com` verschickt und dessen JSON Antwort wohlformatiert auf Ihrer Webseite anzeigt. _Die Antwort auf die erste Anfrage kann unter Umständen bis zu 15 Sekunden dauern, da der Server erst hochfahren muss._

Die möglichen Antworten der Seite sind entweder:

```json
{
  "error": "<Fehlermeldung hier>"
}
``` 
oder

```json
{
  "message": "<Nachricht des Servers hier>"
}
```

Formatieren Sie die Ausgaben unterschiedlich, je nach dem ob `error` oder `message` zurückgegeben wird.

Nutzen Sie diesen Codeschnipsel, um die Daten zu versenden (Erklärung dazu gibt es in der [Lektion nächste Woche](../L3.1)). Um die Antwort auszulesen, muss die letzte Zeile dieses Schnipsels verändert werden, wie es in der Lektion diese Woche dargestellt wurde. Außerdem müssen Sie `browserCacheData` mit dem Speichermedium Ihrer Wahl ersetzen. `broswerCacheData` sollte ein (komplexes) JS Objekt sein, also nicht nur eine Zahl oder String. 

```ts
let query: URLSearchParams = new URLSearchParams(<any>browserCacheData);
url = url + "?" + query.toString();
await fetch(url);
```


<!-- 
>**Bei Problemen/Unklarheiten:** können Sie ins Praktikum kommen oder per Discord/Mail fragen stellen.

Erstellen Sie ein neues Verzeichnis und kopieren Sie die Dateien der letzten Aufgabe hinein. 

Die Aufgabe baut auf der Shop Aufgabe der letzten 3 Wochen auf. 

Ziel der Praktikumsaufgabe ist es Daten über mehrere HTML Seiten hinweg speichern zu können. In dieser Aufgabe geht es darum zu speichern, welche Artikel von einem Kunden in den Warenkorb gelegt wurden. Außerdem sollen die auf der Website angezeigten Artikel per JSON geladen werden. 

>### **Achtung!:** Beachten Sie die [<ins>Coding Style Guidelines</ins>](https://hs-furtwangen.github.io/GIS-WiSe-2020-2021/codingstyle/). Code der diesen Guidelines nicht entpricht wird nicht akzeptiert! Code der W3 Errors oder JS-Errors aufweist wird ebenfalls nicht akzeptiert! Verstöße führen zu einer Ampelstufe 🚦

### Teilaufgabe 1

Bisher werden Ihre Artikel über ein Array, welches direkt im Code liegt, eingelesen. Änderungen sind nur dann möglich wenn Sie das Array direkt bearbeiten. Ein besserer Weg ist es deshalb, die Daten und den Code voneinander zu trennen. Auf diese Art und Weise können jederzeit Artikel hinzugefügt oder aus dem Shop genommen werden, ohne dass der Code verändert werden muss.

Erstellen Sie eine JSON Datei mit allen Ihren Artikeln. Sie können dies von Hand oder mithilfe von online JSON Generatoren durchführen oder indem Sie folgenden Hinweis beachten.

>**Hinweis:** Damit Sie die JSON nicht von Hand befüllen müssen, können Sie mithilfe von `JSON.stringify(data_array)` aus Ihrem Daten-Array ein JSON Dokument erzeugen.

Lesen Sie nun die einzelnen Artikel, welche vorher in einem Array gespeichert waren aus der neuen JSON Datei aus. 

>**Hinweis:** Die `fetch()` Methode funktioniert nur auf Servern. Wenn Sie also wie gewohnt die HTML Datei nur lokal auf Ihrer Maschine in den Browser ziehen, funktioniert `fetch()` nicht. Verwenden Sie eine Live-Server Erweiterung in VSCode (besser) oder laden Sie Ihre Aufgabe für diesen Teil hoch (schlechter) und testen Sie dann.

Erzeugen Sie anhand der eingelesenen Daten die Artikel auf Ihrer Webseite.

>**Hinweis:** Es gibt mehrere Wege wie Sie die Kategorie eines Artikels in einer JSON Datei speichern können. Sie können z.B. jeden Artikel mit einer "Kategorie-ID" versehen und die Artikel beim Einlesen der JSON sortieren, falls Sie das noch nicht getan haben.

### Teilaufgabe 2

Verwenden Sie hierfür den [localStorage](https://www.w3schools.com/jsref/prop_win_localstorage.asp) (oder die Cookies). Wenn ein User der Website einen Artikel über einen der "Kaufen" Buttons in den Warenkorb legt, soll der jeweilige Artikel im local Storage gespeichert werden. 

Legen Sie eine Warenkorb Seite an (falls Sie noch keine haben). Auf der Warenkorb Seite werden alle Artikel die ein User per Button in den Warenkorb gelegt hat dynamisch per Code generiert und angezeigt. Auf der Warenkorb Seite wird außerdem der Gesamtpreis der Bestellung angezeigt. 

User haben die Mögkichkeit einzelne Artikel zu entfernen. Jeder dynamisch generierte Artikel hat einen "Entfernen/Löschen" Button/Text.

User können ihren gesamten Warenkorb löschen. Hierfür gibt es ebenfalls einen Button, der den localStorage leert und die Artikel aus dem Warenkorb entfernt. 

### Bonusaufgabe (keine Pflicht)

User können einen Artikel mehrmals in den Warenkorb legen (z. B. 5 Äpfel). Im Warenkorb kann die Anzahl der Artikel eines Typs geändert werden. -->
