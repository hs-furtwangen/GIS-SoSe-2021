# **3** Server und Datenbanken

In diesem Kapitel soll das Zusammenspiel zwischen Client, Server und Datenbank gelernt und umgesetzt werden. 

Im Praktikum wird eine Seite erstellt, auf der sich Nutzer mit ihren Daten (Name, Nachnahme, E-mail, Adresse etc.) und einem Passwort über ein Formular registrieren können. Über einen Button werden diese Daten an Ihren Heroku-Server geschickt. Dieser prüft ob bereits ein Account mit der angegebenen E-mail Adresse existiert. Falls nein, legt er den neuen User in Ihrer MongoDB ab. Falls ja gibt er eine Antwort an den Client zurück, die dort angezeigt wird, sodass der User weiß, dass die E-Mail bereits belegt ist. 

Erstellen Sie einen Button auf einer verlinkten Unterseite, der eine Anfrage an den Server schickt und alle Namen aller User in der Datenbank dem Client zurückgibt. Dieser zeigt diese dann an. 

Erstellen Sie eine weitere Unterseite auf der sich ein Nutzer einloggen kann. Hier wird per Formular die Mail des Nutzers und sein Passwort zum Server geschickt. Der Server überprüft ob es die Kombination aus Passwort und E-Mail gibt und gibt eine entsprechende Nachricht an den Client zurück, der diese dann anzeigt.

## **3.1** Serveranbindung

- Formulare
- FormData
- URL
- NodeJS

## **3.2** Server Request Verarbeitung

- URL Modul
- Request Handling
- (POST Request)  

## **3.3** Datenbanken Grundlagen

- Datenbanken Einführung
- Datenbank lokal
- Datenbank online

## **3.4** Datenbankzugriff über den Server

- Datenbank und Node.js Kommunikation
- Pipeline: HTML → Server → Datenbank
