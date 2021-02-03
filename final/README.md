## **!** Modulprüfung

Die Modulprüfung zu GIS besteht aus einer **Prüfungsaufgabe** und einer **mündlichen Prüfung**. Zum Bestehen der Modulprüfung müssen beide Prüfungsteile erfolgreich abgeschlossen werden.

Ihnen stehen drei Aufgabenstellungen zur Wahl ([siehe unten](#prüfungsaufgaben-zur-wahl)), die Sie selbstständig bearbeiten sollen. Die Lösung der Aufgabe ist im besten Fall eine lauffähige Anwendung, die der jeweiligen Beschreibung genügt ([siehe unten](#hinweise-zur-abgabe-der-prüfungsaufgabe)).

Die Bewertung der Aufgabenlösungen folgt einem einheitlichen [Kriterienkatalog](criteria). Sie werden in der mündlichen Prüfung aufgefordert die Details der Implementierung Ihrer Lösung zu erläutern.

Der letztmögliche **Abgabetermin für die Lösung der Prüfungsabgabe** ist **Sonntag, 7. Februar 2021 um 23:59.**

Die mündliche Prüfung besteht aus einer detaillierten Auseinandersetzung mit Ihrer Lösung der gewählten Prüfungsaufgabe und allgemeinen Fragen zu den Lehrinhalten des Moduls.

Die **mündlichen Prüfungen** finden am **15., 16. und 17. Februar** über Videokonferenz statt (weitere Prüfungstermine am 18. Februar sind möglich).

Um an der Modulprüfung teilzunehmen müssen Sie sich bis spätestens 7. Februar 2021 in das [FELIX-Kursmodul *GIS Praktikumsabgaben und Modulprüfung WiSe 2020/2021 (MIB und OMB)*](https://felix.hs-furtwangen.de/auth/RepositoryEntry/3994517970) einschreiben. Sollten Sie nicht daran teilnehmen wollen, müssen Sie sich bis spätestens 6. Februar beim Prüfungsamt davon abmelden. 

Dieses Kursmodul bietet die Infrastruktur für folgende Schritte zur Moduleprüfung:
1. Abgabe der *Einwilligungserklärung zur Durchführung von Online-Prüfungen*
2. Abgabe der Lösung der Prüfungsaufgabe (siehe unten)
3. Eintragung eines Termins für die mündliche Prüfung

Die Abgabe der Einwilligungserklärung ist Vorraussetzung um zur mündlichen Prüfung zugelassen zu werden. Die Eintragung eines Prüfungstermins für die mündliche Prüfung sowie die Abgabe ihrer Lösung der Prüfungsaufgabe ist erst nach Abgabe der Einwilligungserklärung möglich.

### Allgemeine Hinweise zur Prüfungsaufgabe

- Jeder muss eine **eigene Lösung** erarbeiten! Unter diesem Gesichtspunkt ist Gruppenarbeit nur sehr eingeschränkt bei allgemeineren Problemen möglich. So wie die Aufgaben gestellt sind, ist es äußerst unwahrscheinlich, dass es zwei oder mehr gleiche (oder verdächtig ähnliche) Lösungen gibt. Einander gleichende Lösungen werden nicht akzeptiert.

- Implementieren Sie Ihre Lösung der gewählten Endaufgabe syntaktisch korrekt mit Hilfe von *HTML*, *CSS*, *Typescript*, *NodeJS* und *MongoDB*.

- Testen Sie die Applikation regelmäßig, ausgiebig und frühzeitig. Lassen Sie auch andere Personen testen um festzustellen, ob die Anwendung bedienbar und fehlertolerant ist. 

- Die Aufgaben lassen einigen Interpretationsspielraum. Toben Sie sich aus, machen Sie sich Gedanken, **seien Sie kreativ**, **haben Sie Spaß**.

- Die Prüfungsaufgabe ist **nicht** Teil des Praktikums und muss für das Bestehen des Praktikums nicht abgegeben werden.

- Fremder Code ist nur unter zwei Voraussetzungen akzeptabel: Zum einen muss dieser klar als Zitat gekennzeichnet sein und eine Quelle angegeben werden, zum anderen müssen Sie trotzdem erklären können, was er tut. Ist ersteres nicht der Fall liegt bei schwereren Verstößen der Verdacht eines Plagiats vor, welcher desaströse Auswirkungen auf Ihr Studium haben könnte.

### Hinweise zur Abgabe der Prüfungsaufgabe

- Verwenden Sie – wie für die Praktikumsaufgaben – ein *GitHub* Repository für den Quellcode und die damit assoziierten *GitHub Pages* um die – möglichst lauffähige und vollständige – Anwendung zugänglich zu machen (siehe [Einführung vom 7. Oktober](../content/L1.1)).

- Laden Sie im Bereich *Prüfungsaufgabe* des FELIX-Kursmoduls der GIS Modulprüfung (siehe oben) eine Archivdatei (z.B. eine ZIP-Datei) mit folgendem Inhalt hoch
  1. alle **(!)** Dateien, die zur Ausführung der Anwendung notwendig sind: Javascript/Typescript-Quellcode (client- und server-seitig), HTML- und CSS-Quellcode sowie ggf. Bild- und Audiodateien
  2. eine kurze (!) Anleitung, wie man die Anwendung ausführt z.B.:
    - Welche Datei muss mit dem NodeJS-Server ausgeführt werden?
    - Welche HTML-Datei im Browser geöffnet?
    - Muss ein *LiveServer* verwendet werden?
  3. einen (*GitHub Pages*) Link auf die möglichst lauffähige und vollständige Lösung
  4. eine einfache Beschreibung/Darstellung ihrer Datenbankstruktur in JSON-ähnlicher Syntax oder als Graphen (Baumstruktur)
  5. eine (unterschriebene) *Eidesstattliche Erklärung*, welche die eigenständige Lösungserarbeitung bestätigt (z.B. als PDF nach [dieser Vorlage](ee.pdf))

- Die Anleitung (2.), der Link (3.) und die Datenbankstruktur (4.) können gerne in ein Dokument zusammengefaßt werden (z.B. PDF, MarkDown, TXT), so dass es sich hier um 3 bis 5 Dokumente handelt.

- Achten Sie auf eine sinnvolle Ordner-/Dateistruktur für ihren Quellcode sowie für das gesamte Archiv Ihrer Abgabe.

- Benennen Sie das Datenarchiv nach folgendem Schema: `<Nachname>_<Vorname>_<Matrikelnummer>.zip`

- Der Inhalt der Datenbanken ist nicht abzugeben.

### Prüfungsaufgaben zur Wahl

Zur Erinnerung: _Sie müssen nur **eine** dieser drei Aufgaben bearbeiten._

#### Aufgabe A: Online-Verwaltung für den AStA-Verleih

Erstellen Sie ein vereinfachtes Websystem, das es erlaubt den Verleih verschiedener Artikel (Geräte und Gegenstände) des AStA an der Hochschule Furtwangen zu unterstützen.
Das System soll den Studierenden eine Webseite zur Reservierung von Artikeln zur Verfügung stellen sowie den Mitgliedern des AStA eine Webseite zur Verwaltung der Reservierungen.
Um die Implementierung zu vereinfachen gibt es für die Reservierung und Verwaltung keinen Kalender, sondern für jeden Artikel nur einen aktuellen Status, *frei*, *reserviert* oder *ausgeliehen*.

Erstellen Sie für die ausleihenden Studierenden eine mit CSS wohlgestaltete Webseite, die eine Liste von mindestens 9 zur Ausleihe angebotenen Artikel präsentiert.
Die Liste wird beim Aufruf der Webseite aus dem Inhalt einer Datenbank dynamisch generiert, wobei zu jedem Artikel mindestens ein Titel, eine kurze Beschreibung, ein Bild und eine Ausleihgebühr angeführt wird.
Artikel, die nicht *frei* sind, werden in der Liste entsprechend markiert (z.B. ausgegraut).
Die Nutzer können auf der Webseite einen oder mehrere freie Artikel zur Reservierung auswählen.
Die ausgewählten Artikel werden herausgehoben oder markiert und die der Auswahl entsprechene Ausleihgebühr (Summe) angezeigt.
Die Nutzer können dann auf einer zweiten Seite einen Namen angeben und die Reservierung abschicken, die damit für jeden der ausgewählten Artikel in der Datenbank registriert wird.

Erstellen Sie eine weitere mit CSS wohlgestaltete Webseite auf der die Mitglieder des AStA einsehen können, welche Artikel momentan *frei*, *reserviert* oder *ausgeliehen* sind.
Als *reserviert* registrierte Artikel können über diese Seite in den Status *ausgeliehen* versetzt werden und ausgeliehene Artikel – bei Rückgabe – wieder als *frei* registrierte werden, wobei für Artikel, die nicht frei sind, der Name des Nutzers angegeben wird, der sie reserviert oder bereits ausgeliehen hat.

#### Aufgabe B: Twitter für Anfänger

Erstellen Sie ein Twitter-ähnliches Websystem, mit dem registrierte Nutzer kurze Textbeiträge posten und einsehen können.
Das sehr vereinfachte System stellt mehrere mit CSS wohlgestaltete Webseiten zur Verfügung mit denen Nutzer interagieren können.

Auf der *Login*-Seite können Nutzer ein neues Nutzerkonto anlegen oder sich mit einem bestehenden Konto über die Datenbank einloggen (ein Nutzernahme kann natürlich nur einmal registriert werden).

Nach einem erfolgreichen Zugang über die Login-Seite kommt der Nutzer zunächst auf die *Hauptseite*, wo der Fluß der Beiträge der abonnierten Nutzer (siehe unten) angezeigt wird.
Außerdem kann der Nutzer auf dieser Seite selbst Beiträge (Posts) abschicken, die mit den Beitägen der anderen Nutzer in der Datenbank gespeichert werden.

Ein Link auf der Hauptseite führt zur *Follow*-Seite, wo eine Liste aller registrierten Nutzer angezeigt wird.
Zu jedem Nutzer in der Liste gibt es einen "Folgen/Entfolgen" Button, mit dem die Beiträge des entsprechenden Nutzers abonniert werden können. Ein zweiter Link auf der Hauptseite führt auf die *Profil*-Seite, wo das Profil des Nutzers angepasst werden kann. Zu einem Nutzerprofil gehören mindestens ein Name, ein Studiengang und eine Semesterangabe.

#### Aufgabe C: Moorhuhn Shooter

Erstellen Sie eine mit CSS wohlgestaltete Webseite mit einem Moorhun-Minigame, dessen Grafik auf dem Canvas-Element beruht.

Vor Beginn des Spiels geben die Nutzer ihren Namen ein, der ggf. in der Anzeige der Highscores benutzt wird (siehe unten).
Im Spiel kann der Nutzer in Ego-Perspektive Projektile wie z.B. Schneebälle, Torten, Gemüse oder Kugeln auf vorbeifliegende oder vorbeilaufende Ziele wie Moorhühner oder Schneemänner werfen oder schießen.

Die Ziele bewegen sich in unterschiedlichen Richtungen zufällig über den Bildschirm und sind unterschiedlich groß und unterschiedlich schnell (skalieren Sie die Parameter zufällig zwischen einem minimalen und maximalen Wert).
Die Flugzeit der Projektile beträgt mindestens 1 Sekunde.

Wird ein Ziel getroffen, verschwindet es vom Bildschirm und der Score wird entsprechend der Treffer-Schwierigkeit erhöht.
Die Treffer-Schwierigkeit varriert z.B. mit der Größe und Geschwindigkeit des Ziels.

Nach Ende des Spiels werden die Highscores (die besten 10) auf einer seperaten Seite angezeigt.
Dazu wird die erreichte Punktzahl mit in einer Datenbank gespeicheten Highscores verglichen und ggf. mit dem eingangs vom Nutzer angegebenen Namen in die Liste der Highscores in der Datenbank eingefügt.

### Empfehlungen und Tipps zur Lösung der Prüfungsaufgaben

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

**Bei Problemen/Unklarheiten:** sollten Sie zum Praktikum kommen oder per Email oder Discord Fragen stellen.

### Typescript Dokumentation

[https://www.typescriptlang.org/](https://www.typescriptlang.org/)
