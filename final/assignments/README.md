<!-- # Aufgaben zur Wahl -->

Zur Erinnerung: _Sie müssen nur **eine** dieser drei Aufgaben bearbeiten._

---

## Aufgabe A: Online-Verwaltung für den AStA-Verleih

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

---

## Aufgabe B: Twitter für Anfänger

Erstellen Sie ein Twitter-ähnliches Websystem, mit dem registrierte Nutzer kurze Textbeiträge posten und einsehen können.
Das sehr vereinfachte System stellt mehrere mit CSS wohlgestaltete Webseiten zur Verfügung mit denen Nutzer interagieren können.

Auf der *Login*-Seite können Nutzer ein neues Nutzerkonto anlegen oder sich mit einem bestehenden Konto über die Datenbank einloggen (ein Nutzernahme kann natürlich nur einmal registriert werden).

Nach einem erfolgreichen Zugang über die Login-Seite kommt der Nutzer zunächst auf die *Hauptseite*, wo der Fluß der Beiträge der abonnierten Nutzer (siehe unten) angezeigt wird.
Außerdem kann der Nutzer auf dieser Seite selbst Beiträge (Posts) abschicken, die mit den Beitägen der anderen Nutzer in der Datenbank gespeichert werden.

Ein Link auf der Hauptseite führt zur *Follow*-Seite, wo eine Liste aller registrierten Nutzer angezeigt wird.
Zu jedem Nutzer in der Liste gibt es einen "Folgen/Entfolgen" Button, mit dem die Beiträge des entsprechenden Nutzers abonniert werden können. Ein zweiter Link auf der Hauptseite führt auf die *Profil*-Seite, wo das Profil des Nutzers angepasst werden kann. Zu einem Nutzerprofil gehören mindestens ein Name, ein Studiengang und eine Semesterangabe.

---

## Aufgabe C: Moorhuhn Shooter

Erstellen Sie eine mit CSS wohlgestaltete Webseite mit einem Moorhun-Minigame, dessen Grafik auf dem Canvas-Element beruht.

Vor Beginn des Spiels geben die Nutzer ihren Namen ein, der ggf. in der Anzeige der Highscores benutzt wird (siehe unten).
Im Spiel kann der Nutzer in Ego-Perspektive Projektile wie z.B. Schneebälle, Torten, Gemüse oder Kugeln auf vorbeifliegende oder vorbeilaufende Ziele wie Moorhühner oder Schneemänner werfen oder schießen.

Die Ziele bewegen sich in unterschiedlichen Richtungen zufällig über den Bildschirm und sind unterschiedlich groß und unterschiedlich schnell (skalieren Sie die Parameter zufällig zwischen einem minimalen und maximalen Wert).
Die Flugzeit der Projektile beträgt mindestens 1 Sekunde.

Wird ein Ziel getroffen, verschwindet es vom Bildschirm und der Score wird entsprechend der Treffer-Schwierigkeit erhöht.
Die Treffer-Schwierigkeit varriert z.B. mit der Größe und Geschwindigkeit des Ziels.

Nach Ende des Spiels werden die Highscores (die besten 10) auf einer seperaten Seite angezeigt.
Dazu wird die erreichte Punktzahl mit in einer Datenbank gespeicheten Highscores verglichen und ggf. mit dem eingangs vom Nutzer angegebenen Namen in die Liste der Highscores in der Datenbank eingefügt.
