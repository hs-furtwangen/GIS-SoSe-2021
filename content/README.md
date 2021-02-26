## **1** HTML und CSS

In diesem ersten Kapitel geht es HTML und CSS, also die Basiselemente der Gestaltung einer Webseite.

In den Praktikumsabgaben zu diesem Kapitel entsteht eine wohlgestaltete Portofolio-Webseite, mit der Sie sich präsentieren und die sich aus mehreren HTML-Documenten sowie einer oder mehrerer CSS-Dateien zusammensetzt (ohne JS).

### **1.1** Arbeitsumgebung und Grundlagen HTML

- Einführung in die Thematik
- Vorbereitung / Tools
- HTML Basics
- HTML Bilder und Verweise

### **1.2** HTML Elemente

- HTML Audio und Video
- HTML Struktur
- Browser und Web Inspector

### **1.3** Grundlagen CSS

- Einführung
- Eigenschaften
- Selektoren
- Kaskadierung und Vererbung
- *Box Model* und Maßeinheiten

### **1.4** Vertiefung CSS

- Komplexe Selektoren
- Positionierung, Flussverhalten und Layout
- Responsive Design
- *Transition* und *Animation*

---

## **2** TypeScript

In diesem zweiten großen Abschnitt des Praktikums werden wir uns ganz dem Einstieg und der Entwicklung mit Typescript widmen.

Im Praktikums soll nach anfänglichen Fingerübungen eine Webseite umgesetzt werden, die dem Nutzer erlaubt – ähnlich wie bei einem Klappbuch – ein Bild aus drei oder mehr verschiedenen Teilen zusammenzusetzen, für die jeweils mehrere Varianten zur Auswahl stehen. Es könnte sich z.B. um das Bild eines Menschen handeln, das sich aus einem Kopf, einem Rumpf und Beinen zusammensetzt, oder auch eines Tieres, einer Rakete oder einer Topfpflanze.  
Zu jedem der Teile kann auf einer eigenen Unterseite eine von verschiedenen Varianten ausgewählt werden - also z.B. eine Seite um den Kopf auszuwählen, eine für den Rumpf und eine für die Beine.  
Auf einer weiteren Seite wird das Gesamtbild als eine Kombination der ausgewählten Varianten grafisch (z.B. img / canvas) präsentiert. Diese Seite soll nach erfolgter Auswahl angezeigt werden.  
Die Auswahlmöglichkeiten sollen dynamisch aus einer JSON-Datei geladen und auf der Seite angezeigt werden. Außerdem muss die Umsetzung so dynamisch sein, dass bei (geringfügigen) Änderungen in der JSON Datei die Seite sich automatisch beim nächsten Laden anpasst. Die Nutzung passender Interfaces (oder Klassen) ist dabei unverzichtbar.  
Der aktuelle Status der Auswahl wird über Local Storage (oder Cookies) gespeichert und die schließlich ausgewählte Kombination der Varianten an einen Server übermittelt und dessen Antwort in geeigneter, nutzerfreundlicher Form auf der Gesamtbild-Seite ausgegeben.

### **2.1** Einstieg JavaScript und TypeScript

- Arbeitsumgebung
- Variablen
- Typen
- Operatoren
- Funktionen
- Schleifen

### **2.2** Weiterführende Konzepte Typescript

- Vorgehensweisen und best practices
- Arrays
- Interfaces
- Objekte
- Canvas

### **2.3** DOM Manipulation und Eventhandling

- DOM Klassenhierarchie  
- DOM Manipulation
- Events
- Event Handling
- Event Listener

### **2.4** JSON und Local Storage

- JSON
- Local Storage / Cookies

### **2.5** Kommunikation

- fetch
- Promise
- async / await

---

## **3** Server und Datenbanken

In diesem Kapitel soll das Zusammenspiel zwischen Client, Server und Datenbank gelernt und umgesetzt werden. 

Im Praktikum wird eine Seite erstellt, auf der sich Nutzer mit ihren Daten (Name, Nachnahme, E-mail, Adresse etc.) und einem Passwort über ein Formular registrieren können. Über einen Button werden diese Daten an Ihren Heroku-Server geschickt. Dieser prüft ob bereits ein Account mit der angegebenen E-mail Adresse existiert. Falls nein, legt er den neuen User in Ihrer MongoDB ab. Falls ja gibt er eine Antwort an den Client zurück, die dort angezeigt wird, sodass der User weiß, dass die E-Mail bereits belegt ist. 

Erstellen Sie einen Button auf einer verlinkten Unterseite, der eine Anfrage an den Server schickt und alle Namen aller User in der Datenbank dem Client zurückgibt. Dieser zeigt diese dann an. 

Erstellen Sie eine weitere Unterseite auf der sich ein Nutzer einloggen kann. Hier wird per Formular die Mail des Nutzers und sein Passwort zum Server geschickt. Der Server überprüft ob es die Kombination aus Passwort und E-Mail gibt und gibt eine entsprechende Nachricht an den Client zurück, der diese dann anzeigt.

### **3.1** Serveranbindung

- Formulare
- FormData
- URL
- NodeJS

### **3.2** Server Request Verarbeitung

- URL Modul
- Request Handling
- (POST Request)  

### **3.3** Datenbanken Grundlagen

- Datenbanken Einführung
- Datenbank lokal
- Datenbank online

### **3.4** Datenbankzugriff über den Server

- Datenbank und Node.js Kommunikation
- Pipeline: HTML → Server → Datenbank
