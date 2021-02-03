## _P_ **2.4** JSON und Local Storage

### Aufgabe 1

**a)** Konvertieren Sie die Variable in der `data.ts` Datei, in der Sie zuvor die Daten gespeichert haben, in einen JSON string und schreiben Sie eine Funktion in Ihrem Hauptprogramm, welches die Daten aus dem JSON String in ein Objekt ihres Interfaces / ihrer Klasse konvertiert. An dieser Stelle sollte die Seite wieder genau so funktionieren wie die Woche davor.

**b)** Speichern Sie die Daten über die ausgwählten Möglichkeiten in den Cache des Browsers, entweder über localStorage, sessionStorage oder Cookies.

**c)** Sorgen Sie dafür, dass jede Kategorie auf einer eigenen Seite auswählbar wird. Versuchen Sie dabei sich an den "Code kopieren ist schlecht" Grundsatz zu halten (vorallem für den TS Code, weniger für den HTML Code). Dafür bieten sich zwei Vorgehensweisen an:
1. Entweder Sie kopieren die HTML Seiten und finden einen Weg, wie sie dem Typescript miteilen können, welche Seite gerade geöffnet ist / welche Kategorie geladen werden soll oder 
2. Sie finden eine Möglichkeit, auf der gleichen Seite die drei Unterschiedlichen Kategorien _eine nach der anderen, und nur eine auf einmal_ anzuzeigen.

**d)** Sofern noch nicht passiert, zeigen Sie auf der Auswahlseite an, welche Teilaspekte bereits in vorherigen Schritten ausgewählt wurden.


### Aufgabe 2

Entwickeln Sie eine weitere Seite, auf die nachdem (je) ein Element aus allen Kategorieren ausgewählt wurde weitergeleitet wird. Auf dieser Seite sollte die grafische Darstellung zusammengeführt werden. Nutzen Sie dazu die Daten die Sie im Browser Cache abgelegt haben sowie die Daten aus der `daten.ts` Datei.