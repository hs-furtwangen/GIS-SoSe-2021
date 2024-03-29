<!-- # Über die Prüfungsabgabe -->

Zu diesem ersten Teil der Modulprüfung stehen Ihnen zwei Aufgabenstellungen zur Wahl (siehe *Aufgaben zur Wahl*), die Sie selbstständig bearbeiten sollen. Die Lösung der Aufgabe ist im besten Fall eine lauffähige Anwendung, die der jeweiligen Beschreibung genügt (siehe *Über die Prüfungsabgabe*).

Die Bewertung der Aufgabenlösungen folgt einem einheitlichen Kriterienkatalog (siehe *Bewertungskriterien*). Sie werden in der mündlichen Prüfung aufgefordert die Details der Implementierung Ihrer Lösung zu erläutern.

Bitte beachten Sie folgende Hinweise:

- Da jeder Kandidat selbstständig eine **eigene Lösung** erarbeiten soll, ist Gruppenarbeit nur sehr eingeschränkt bei allgemeineren Problemen möglich.
So wie die Aufgaben gestellt sind, ist es äußerst unwahrscheinlich, dass es zwei oder mehr gleiche (oder verdächtig ähnliche) Lösungen gibt. Einander gleichende Lösungen werden nicht akzeptiert.

- Implementieren Sie Ihre Lösung der gewählten Endaufgabe syntaktisch korrekt mit Hilfe von *HTML*, *CSS*, *TypeScript*, *NodeJS* und *MongoDB*.

- Testen Sie die Applikation regelmäßig, ausgiebig und frühzeitig. Lassen Sie auch andere Personen testen um festzustellen, ob die Anwendung bedienbar und fehlertolerant ist. 

- Die Aufgaben lassen einigen Interpretationsspielraum. Toben Sie sich aus, machen Sie sich Gedanken, **seien Sie kreativ**, **haben Sie Spaß**.

- Die Prüfungsaufgabe ist **nicht** Teil des Praktikums und muss für das Bestehen des Praktikums nicht abgegeben werden.

- Fremder Code ist nur unter zwei Voraussetzungen akzeptabel: Zum einen (1.) muss dieser klar als Zitat gekennzeichnet sein und eine Quelle angegeben werden, zum anderen (2.) müssen Sie trotzdem erklären können, was er tut. Ist ersteres nicht der Fall liegt bei schwereren Verstößen der Verdacht eines Plagiats vor, welcher desaströse Auswirkungen auf Ihr Studium haben könnte.
	- Daraus folgt: npm Module (mit Außnahme der in der Veranstaltung genutzten @types sowie mongodb module) oder sonstige server-seitige Bibliotheken dürfen nur als Ausnahme nach Absprache mit den Dozenten verwendet werden und sind ansonsten verboten.
	- Gleiches gilt für irgendwelche client-seitigen Bibliotheken (JS wie auch CSS) wie jQuery, Bootstrap, Vue, etc.


---

## Form der Abgabe

- Verwenden Sie – wie für die Praktikumsaufgaben – ein *GitHub* Repository für den Quellcode und die damit assoziierten *GitHub Pages* um die – möglichst lauffähige und vollständige – Anwendung zugänglich zu machen.

- Laden Sie im Bereich *Prüfungsabgabe* eine Archivdatei (z.B. eine ZIP-Datei) mit folgendem Inhalt hoch
  1. alle **(!)** Dateien, die zur Ausführung der Anwendung notwendig sind: JavaScript/TypeScript-Quellcode (client- und server-seitig), HTML- und CSS-Quellcode sowie ggf. Bild- und Audiodateien
  2. eine kurze (!) Anleitung, wie man die Anwendung ausführt z.B.:
    - Welche Datei muss mit dem NodeJS-Server ausgeführt werden?
    - Welche HTML-Datei im Browser geöffnet?
    - Muss ein *LiveServer* verwendet werden?
  3. einen (*GitHub Pages*) Link auf die möglichst lauffähige und vollständige Lösung
  4. eine einfache Beschreibung/Darstellung ihrer Datenbankstruktur in JSON-ähnlicher Syntax oder als Graphen (Baumstruktur)
  5. eine (unterschriebene) *Eidesstattliche Erklärung*, welche die eigenständige Lösungserarbeitung bestätigt (z.B. als PDF nach [dieser Vorlage](https://hs-furtwangen.github.io/GIS-SoSe-2021/final/ee.pdf))

- Die Anleitung (2.), der Link (3.) und die Datenbankstruktur (4.) können gerne in ein Dokument zusammengefaßt werden (z.B. PDF, MarkDown, TXT), so dass es sich hier um 3 bis 5 Dokumente handelt.

- Achten Sie auf eine sinnvolle/übersichtliche Ordner-/Dateistruktur für ihren Quellcode sowie für das gesamte Archiv Ihrer Abgabe.

- Benennen Sie das Datenarchiv nach folgendem Schema: `<Nachname>_<Vorname>_<Matrikelnummer>.zip`

- Der Inhalt der Datenbanken ist nicht abzugeben.

---

## Empfehlungen und Tipps zur Lösung

Es wird dringend empfohlen ...

- ... nicht einfach Ihren alten Code zu kopieren. Nehmen Sie was Sie bereits haben als Grundlage, aber nicht als Kopiervorlage. Einzelne Zeilen oder Konzepte können Sie ggf. übernehmen, aber bedenken Sie die aktuellen Anforderungen (und erinnern Sie sich an die Steine, die Sie sich während dem Praktikum selbst in den Weg gelegt haben und vermeiden Sie diese).

- ... nicht einfach drauf los zu Coden. Nehmen Sie sich die Zeit, machen Sie sich einen Plan und halten Sie diesen Plan in geeigneter Form fest (siehe unten). Vermutlich fallen Ihnen an diesem Punkt schon mögliche Schwierigkeiten (und Lösungen) ein, wodurch Sie dann nicht nachdem Sie schon die Hälfte gecodet haben nochmal alles wegschmeißen müssen. Dies hilft Ihnen auch selbst dabei, Ihre Gedanken zu sortieren und zu organisieren. Dazu können z.B. folgende Überlegungen gehören:
  - Wie sollte das Frontend aussehen und funktionieren? Welche Seiten brauche ich?
  - Wie sollen meine Datenstrukturen aussehen? Was für Interfaces brauche ich?
  - Welche Komponente (Client/Server/Datenbank) übernimmt welche Funktionalität?
  - Wie kann ich diese Funktionalität so implementieren, dass ich damit möglichst wenig Arbeit habe, sowohl beim Entwickeln als auch bei potentiellen (wahrscheinlichen!) Änderungen? 
  - Wie sollte die Datenbank strukturiert sein?  
  - Wie arbeitet was miteinander zusammen?

- ... Ihre Notizen mit abzugeben, damit ersichtlich wird, was Sie sich dabei gedacht haben. Besonders für den Fall dass irgendetwas nicht so ganz funktioniert wie geplant, ist das hilfreich für die Prüfer.

Die Vorgehensweise um eine Lösung der von Ihnen gewählten Aufgabe zu erarbeiten könnte z.B. folgende Schritte enthalten:
1. Nutzerseiten strukturieren und skizzieren (z.B. mit Stift und Papier)
2. Datenstrukturen planen, Interfaces anlegen
3. Beispieldaten anlegen (werden später aus DB geladen)
4. benötigte HTML-Seiten anlegen (zunächst statisch mit Beispieldaten gefüllt)
5. erste grundsätzliche CSS-Stilvorlage anlegen
6. Media Queries und responsive Design einfügen
7. TS-Code für den dynamischen Seitenaufbau implementieren (mit Beispieldaten)
8. TS-Code für Seiteninteraktion mit Event Listenern implementieren
9. Datenbank anlegen und strukturell aufbauen
10. NodeJS Server anlegen und mit DB verbinden
11. Schnittstellen/Kommunikationsbedarf zwischen Client und Server definieren
12. Server-Client Kommunikation implementieren

**Bei Problemen/Unklarheiten:** sollten Sie zum Praktikum kommen oder per Email oder Discord Fragen stellen. Denken Sie an die "magische" Grenze von 15 Minuten.

**[TypeScript Dokumentation](https://www.typescriptlang.org/){:target="_blank"}**
