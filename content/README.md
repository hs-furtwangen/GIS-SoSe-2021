# **1** HTML und CSS

In diesem ersten Kapitel geht es HTML und CSS, also die Basiselemente der Gestaltung einer Webseite, zu denen in den folgenden Kapiteln ([2](#2-typescript) und [3](#3-server-und-datenbanken)), die Programmierung – mit *TypeScript* – sowie die Anbindung an Server und Datenbank – mit *Node.js* und *MongoDB* – hinzukommt.

Zunächst geht es in der Einführung allerdings darum eine funktionsfähige Arbeitsumgebung an den Start zu bringen.

---

## **1.1** Arbeitsumgebung und Grundlagen HTML

- Einführung in die Thematik
- Vorbereitung / Tools
- HTML Basics
- HTML Bilder und Verweise

*[**V** **1.1** **7. Oktober** (Vorlesungsmaterialien)](L1.1)*
*[**P** **1.1** **9. Oktober** (Praktikumsaufgabe)](P1.1)*

---

## **1.2** HTML Elemente

– HTML Audio und Video
- HTML Struktur
- Browser und Web Inspector

*[**V** **1.2** **14. Oktober** (Vorlesungsmaterialien)](L1.2)*
*[**P** **1.2** **16. Oktober** (Praktikumsaufgabe)](P1.2)*

---

## **1.3** Grundlagen CSS

- Einführung
- Eigenschaften
- Selektoren
- Kaskadierung und Vererbung
- *Box Model* und Maßeinheiten

*[**V** **1.3** **21. Oktober** (Vorlesungsmaterialien)](L1.3)*
*[**P** **1.3** **23. Oktober** (Praktikumsaufgabe)](P1.3)*

---

## **1.4** Vertiefung CSS

- Komplexe Selektoren
- Positionierung, Flussverhalten und Layout
- Responsive Design
- *Transition* und *Animation*

*[**V** **1.4** **28. Oktober** (Vorlesungsmaterialien)](L1.4)*
*[**P** **1.4** **30. Oktober** (Praktikumsaufgabe)](P1.4)*

---

## **A|1** Praktikumsabgabe zum Kapitel 1

Die Praktikumsabgabe zu diesem Kapitel ist eine wohlgestaltete Portofolio-Webseite mit, der Sie sich präsentieren und die sich aus mehreren HTML-Documenten sowie einer oder mehrerer CSS-Dateien zusammensetzt (ohne JS). Die zu beachtenen Details finden Sie in den Teilaufgaben [P 1.2](P1.2), [P 1.3](P1.3), [P 1.4](P1.4) mit (*) gekennzeichnet.

#### Abgabe zum 1. November 2020
*[zur Praktikumsabgabe zum Kapitel 1 (auf FELIX)](https://felix.hs-furtwangen.de/auth/RepositoryEntry/3994517970/CourseNode/102499789173212){:target="_blank"}*

---

# **2** TypeScript

In diesem zweiten großen Abschnitt des Praktikums werden wir uns ganz dem Einstieg und der Entwicklung mit Typescript widmen.

---

## **2.1** Einstieg JavaScript und TypeScript

- Arbeitsumgebung
- Variablen
- Typen
- Operatoren
- Funktionen
- Schleifen

*[**V** **2.1** **4. November** (Vorlesungsmaterialien)](L2.1)*
*[**P** **2.1** **6. November** (Praktikumsaufgabe)](P2.1)*

---

## **2.2** Weiterführende Konzepte Typescript

- Vorgehensweisen und best practices
- Arrays
- Interfaces
- Objekte
- Canvas

*[**V** **2.2** **11. November** (Vorlesungsmaterialien)](L2.2)*
*[**P** **2.2** **13. November** (Praktikumsaufgabe)](P2.2)*

---

## **2.3** DOM Manipulation und Eventhandling

- DOM Klassenhierarchie  
- DOM Manipulation
- Events
- Event Handling
- Event Listener

*[**V** **2.3** **18. November** (Vorlesungsmaterialien)](L2.3)*
*[**P** **2.3** **20. November** (Praktikumsaufgabe)](P2.3)*

---

## **2.4** JSON und Local Storage

- JSON
- Local Storage / Cookies

*[**V** **2.4** **25. November** (Vorlesungsmaterialien)](L2.4)*
*[**P** **2.4** **27. November** (Praktikumsaufgabe)](P2.4)*

---

## **2.5** Kommunikation

- fetch
- Promise
- async / await

*[**V** **2.5** **2. Dezember** (Vorlesungsmaterialien)](L2.5)*
*[**P** **2.5** **4. Dezember** (Praktikumsaufgabe)](P2.5)* 

---

## **A|2** Praktikumsabgabe zum Kapitel 2

In diesem Kapitel soll nach anfänglichen Einstiegsaufgaben eine Webseite umgesetzt werden, die dem Nutzer erlaubt – ähnlich wie bei einem Klappbuch – ein Bild aus drei oder mehr verschiedenen Teilen zusammenzusetzen, für die jeweils mehrere Varianten zur Auswahl stehen. Es könnte sich z.B. um das Bild eines Menschen handeln, das sich aus einem Kopf, einem Rumpf und Beinen zusammensetzt, oder auch eines Tieres, einer Rakete oder einer Topfpflanze.  
Zu jedem der Teile kann auf einer eigenen Unterseite eine von verschiedenen Varianten ausgewählt werden - also z.B. eine Seite um den Kopf auszuwählen, eine für den Rumpf und eine für die Beine.  
Auf einer weiteren Seite wird das Gesamtbild als eine Kombination der ausgewählten Varianten grafisch (z.B. img / canvas) präsentiert. Diese Seite soll nach erfolgter Auswahl angezeigt werden.  
Die Auswahlmöglichkeiten sollen dynamisch aus einer JSON-Datei geladen und auf der Seite angezeigt werden. Außerdem muss die Umsetzung so dynamisch sein, dass bei (geringfügigen) Änderungen in der JSON Datei die Seite sich automatisch beim nächsten Laden anpasst. Die Nutzung passender Interfaces (oder Klassen) ist dabei unverzichtbar.  
Der aktuelle Status der Auswahl wird über Local Storage (oder Cookies) gespeichert und die schließlich ausgewählte Kombination der Varianten an einen Server übermittelt und dessen Antwort in geeigneter, nutzerfreundlicher Form auf der Gesamtbild-Seite ausgegeben.

_Code, der sich nicht an die [Code Guidelines](../codingstyle) hält, mit ganz besonderem Augenmerk auf Formatierung, Typisierung und Benennung, ist nicht akzeptabel!_

#### Abgabe zum 6. Dezember 2020
*[zur Praktikumsabgabe zum Kapitel 2 (auf FELIX)](https://felix.hs-furtwangen.de/url/RepositoryEntry/3994517970/CourseNode/102761918774206){:target="_blank"}*

---

# **3** Server und Datenbanken

## **3.1** Serveranbindung

- Formulare
- FormData
- URL
- NodeJS

*[**V** **3.1** **9. Dezember** (Vorlesungsmaterialien)](L3.1)*
*[**P** **3.1** **11. Dezember** (Praktikumsaufgabe)](P3.1)* 

---

## **3.2** Server Request Verarbeitung

- URL Modul
- Request Handling
- (POST Request)  

*[**V** **3.2** **16. Dezember** (Vorlesungsmaterialien)](L3.2)*
*[**P** **3.2** **18. Dezember** (Praktikumsaufgabe)](P3.2)* 

---

## **3.3** Datenbanken Grundlagen

- Datenbanken Einführung
- Datenbank lokal
- Datenbank online

*[**V** **3.3** **13. Januar** (Vorlesungsmaterialien)](L3.3)*
*[**P** **3.3** **15. Januar** (Praktikumsaufgabe)](P3.3)* 

---

## **3.4** Datenbankzugriff über den Server

- Datenbank und Node.js Kommunikation
- Pipeline: HTML → Server → Datenbank

*[**V** **3.4** **20. Januar** (Vorlesungsmaterialien)](L3.4)*
*[**P** **3.4** **22. Januar** (Praktikumsaufgabe)](P3.4)* 

---

## **A|3** Praktikumsabgabe zum Kapitel 3

In diesem Kapitel soll das Zusammenspiel zwischen Client, Server und Datenbank gelernt und umgesetzt werden. 

Erstellen sie eine Seite auf der sich Nutzer mit ihren Daten (Name,Nachnahme, E-mail, Adresse etc.) und einem Passwort über ein Formular registrieren können. Über einen Button werden diese Daten an Ihren Heroku-Server geschickt. Dieser prüft ob bereits ein Account mit der angegebenen E-mail Adresse existiert. Falls nein, legt er den neuen User in Ihrer MongoDB ab. Falls ja gibt er eine Antwort an den Client zurück, die dort angezeigt wird, sodass der User weiß, dass die E-Mail bereits belegt ist. 

Erstellen Sie einen Button auf einer verlinkten Unterseite, der eine Anfrage an den Server schickt und alle Namen aller User in der Datenbank dem Client zurückgibt. Dieser zeigt diese dann an. 

Erstellen Sie eine weitere Unterseite auf der sich ein Nutzer einloggen kann. Hier wird per Formular die Mail des Nutzers und sein Passwort zum Server geschickt. Der Server überprüft ob es die Kombination aus Passwort und E-Mail gibt und gibt eine entsprechende Nachricht an den Client zurück, der diese dann anzeigt.

#### Abgabe zum 24. Januar 2021
*[zur Praktikumsabgabe zum Kapitel 3 (auf FELIX)](https://felix.hs-furtwangen.de/url/RepositoryEntry/3994517970/CourseNode/102761918835934){:target="_blank"}*

---
