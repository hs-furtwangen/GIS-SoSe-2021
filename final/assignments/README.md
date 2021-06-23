<!-- # Aufgaben zur Wahl -->

Zur Erinnerung: _Sie müssen nur **eine** dieser zwei Aufgaben bearbeiten._

---

## Aufgabe A: Online Memory Spiel

Erstellen Sie ein [Memory Spiel](https://de.wikipedia.org/wiki/Memory_(Spiel)){:target="_blank"} für Einzelspieler:innen, das man über Maus-Interaktionen spielen kann. Das System soll den Benutzer:innen drei verschiedene Webseiten zur Verfügung stellen:
- eine *Spielseite* zum Spielen,
- eine *Score-Seite* um sich die Highscores der schnellsten Spieler:innen anzusehen
- eine *Admin-Seite*, auf der die Bilder des Spiels verwaltet werden können

Diese drei Webseiten sollen über eine (vierte) Übersichtsseite erreicht werden können. Jede dieser Webseiten soll mit CSS möglichst ansprechend grafisch gestaltet werden.

Wenn auf der Spielseite ein neues Spiel gestartet wird, wird zunächst eine zufällige Reihe von Bild-Links (d.h. Verweise auf öffentlich zugängliche Bilddateien in Form einer URL) aus der Datenbank geladen. Ein Memory Spiel sollte aus mindestens 8 Pärchen (2 Karten mit dem gleichen Bild) bestehen. Die Karten werden am Spielanfang in zufälliger Reihenfolge verdeckt auf dem Bildschirm angeordnet, so dass die Bilder nicht sichbar sind. Beim Klicken auf eine Karte wird das dazugehörige Bild aufgedeckt. Nachdem jeweils zwei Karten angeklickt wurden, wird geprüft, ob es sich um ein Pärchen handelt. Ist dies der Fall, werden die Karten aus dem Spiel genommen. Andernfalls werden beide Karten wieder verdeckt. Die Positionen der Karten dürfen sich im Laufe des Spiels nicht ändern.

Sobald das letzte Pärchen aufgedeckt wurde, werden die Spieler:innen auf eine weitere Webseite weitergeleitet (die Score-Seite oder eine fünfte Seite), auf der die Dauer des Spiels angezeigt wird und sie ihren Namen eingeben müssen. Nach Eingabe des Namens, wird der Punktestand in der Datenbank gespeichert und die Spieler:innen auf die Highscore Liste weitergeleitet, auf der mindestens die 10 schnellsten Zeiten mit Namen der Benutzer angezeigt werden. Von hier kann ein neues Spiel gestartet werden.

Auf der Admin-Webseite werden die Bilder aller in der Datenbank gespeicherten Bild-Links angezeigt. Einzelne Bilder (d.h. ihre Links) können hier aus der Datenbank entfernt werden (z.B. durch die Interaktion mit dem Bild oder einem Button) und Links auf neue Bilder hinzugefügt werden (z.B. über ein Eingabefeld, in das eine URL eingegeben werden kann).

## Aufgabe B: Online Rezepte Sammlung

Erstellen Sie ein Websystem, das es registrierten Nutzer:innen erlaubt Rezepte zu teilen, zu ändern, einzusehen und in eine Sammlung von Favoriten aufzunehmen. Das System stellt mehrere mit CSS wohlgestaltete Webseiten zur Verfügung, mit denen die Nutzer:innen interagieren. Mit Ausnahme der Login-Seite gibt es auf allen Webseiten des Systems ein einheitliches Menü zur Navigation, über das die Seiten des Systems erreichbar sind.

Auf der Login-Seite können Nutzer:innen ein neues Konto mit einem Nutzernamen und einem Passwort anlegen oder sich mit einem bestehenden Konto über die Datenbank verbinden. Ein Name kann hier selbstverständlich nur einmal registriert werden und der Versuch einen bereits registrierten Namen erneut zu registrieren führt zu einer Fehlermeldung auf der Login-Seite.

Nach einem erfolgreichen Zugang über die Login-Seite, kommen die Nutzer:innen zunächst auf die Seite *Alle Rezepte*, auf der alle Rezepte angezeigt werden, die sich aktuell in der Datenbank befinden. Hier können die Nutzer:innen über den Button *Favorisieren* ein Rezept zur ihrer persönlichen Sammlung favorisierter Rezepte hinzufügen.

Auf der Seite *Meine Favoriten* können eingeloggte (!) Nutzer:innen ihre Sammlung favorisierter Rezepte einsehen und auch wieder aus der Sammlung entfernen.

Auf der Seite *Meine Rezepte* können neue eigene Rezepte erstellt und geteilt (d.h. in die Datenbank eingefügt) werden sowie die eigenen bereits geteilten Rezepte bearbeitet und gelöscht werden. Ein Rezept besteht mindestens aus einer Zutatenliste sowie einer Zubereitungsanweisung. Die Zutatenliste wird entweder über eine variable Anzahl von Eingabefeldern (z.B. mit einem "+" Button) oder über mindestens 10 statische Eingabefelder erstellt.