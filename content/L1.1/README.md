## _V_ **1.1** Arbeitsumgebung und Grundlagen HTML

### Einführung in die Thematik
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/00_Einfuehrung.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/00_Einfuehrung.mp4">Zum Video</a>
</video>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/00_GIS-EIA1-Einführung.pdf){:target="_blank"}*

---

### Vorbereitung / Tools

**Bitte ignorieren Sie den Teil des Videos in dem es um die Registrierung auf der Kursseite sowie das Anlegen des Steckbriefes geht, dadurch dass wir in diesem Semester auf ein neues System der Abgaben umgestellt haben, brauchen wir das nicht!**

<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/00_Arbeitsumgebung.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/00_Arbeitsumgebung.mp4">Zum Video</a>
</video>

#### Tools / Software
- [Visual Studio Code](https://code.visualstudio.com/)
- [Git](https://git-scm.com/)
- [GitHub](https://github.com/)
- [Github Desktop](https://desktop.github.com/)
- [Gitkraken](https://www.gitkraken.com/)
- [Sourcetree](https://www.sourcetreeapp.com/)

##### Weitere Hinweise:
- GIT selbst muss nur installiert werden, wenn sie es direkt aus VSCode heraus nutzen wollen, da sowohl Github Desktop als auch Gitkraken git integriert haben.
- VSCode ist erstmal auf Englisch installiert. Es gibt das Deutsche Sprachpaket -> Das Paket kann man Links in VSCode in der Plugins Sektion hinzufügen (einfach nach German Language suchen).
- Es ist empfohlen, eine grafische Oberfläche für die Verwendung von git zu nutzen, da diese viele der etwas komplizierteren Vorgänge übernimmt. Später im Arbeitsleben wird wahrscheinlich auch niemand vorschreiben, wie man git zu nutzen hat. Die grafischen Oberflächen kommen nur bei fortgeschrittenen git Operationen an ihre Grenzen.
- Github Pages zeigt Änderungen nach dem pushen nicht sofort an, da diese zunächst von ihrem Repository verarbeitet werden müssen. Dies kann mehrere Minuten dauern.
- Gitkraken/Github Desktop zeigt u.U. Dateien an, welche Sie selbst nicht sehen (z.B. `.DS_Store`). Dabei handelt es sich um versteckte Dateien welche das Betriebssystem selbst anlegt. Diese Dateien werden nicht auf dem git gebraucht und können durch das Anlegen einer [.gitignore](https://www.atlassian.com/git/tutorials/saving-changes/gitignore) Datei ignoriert werden.
- GitHub hat seit der Aufnahme des Videos den "Master" Branch in den "Main" Branch umbenannt. Darauf müssen Sie beim Aktivieren von Github Pages achten. Außerdem muss man inzwischen auch den Ordner auswählen, da nutzen Sie einfach "root", also den Hauptordner.

--- 

### HTML Basics
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Basics.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Basics.mp4">Zum Video</a>
</video>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/01_GIS-EIA1-1-HTML-Basics.pdf){:target="_blank"}*

##### Weitere Hinweise:

- HTML Dateien können einfach lokal angezeigt werden, indem man die .html Datei im Browser der Wahl öffnet (Firefox oder Chrome sind zu empfehlen). Mit F5 bzw CTRL+F5 laden Sie die Seite neu wenn Sie Änderungen daran vorgenommen haben.
- Mit der Tastenkombination ALT + SHIFT + F kann geschriebener Code automatisch formatiert werden.

---

### HTML Syntax und erste Elemente
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Syntax.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/01_GIS-EIA1-HTML-Syntax.mp4">Zum Video</a>
</video>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/01_GIS-EIA1-2-HTML-Syntax.pdf){:target="_blank"}*

---

### HTML Bilder und Verweise

_Hier gibt es kein Video, stattdessen den ausführlichen Foliensatz zum selbst erarbeiten._
<embed src="https://scheuerle.net/lehre/gis/scripts/01_GIS-EIA1-3-HTML-Bilder-Verweise.pdf" type="application/pdf" width="100%" height = "400px"/>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/01_GIS-EIA1-3-HTML-Bilder-Verweise.pdf){:target="_blank"}*

---

## **?!** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A-Termin)

Zusammenfassung von: [&lt;TawsTm&gt;](https://github.com/TawsTm)

### Warum kann ich mich nicht auf Felix anmelden?
Der Großteil der Veranstaltung wird über GitHub laufen. Zum Ende der Veranstaltung wird es jedoch einen Felix-Kurs geben, um die mündlichen Prüfungstermine zu organisieren.

### Wo müssen die Abgaben/Aufgaben hochgeladen werden?
Hierfür gibt es pro Abgabe eine GitHub Issue-Seite: [Issues](https://github.com/hs-furtwangen/GIS-WiSe-2020-2021/issues).
Es gibt jeweils pro größerem Kapitel einen Issue-Thread (1, 2, 3).

### Muss ich zu den Terminen kommen, wenn ich keine Hilfe bei den Aufgaben brauche bzw. schon vorher fertig bin?
Nein, es besteht keine Anwesenheitspflicht.

### Wie kann ich testen ob GIT auf meinem PC vorhanden ist?
Der.git-Ordner ist meist versteckt und wird nicht angezeigt. Wenn ihr GitHub Desktop benutzt sollte GIT aber funktionieren.

### Gibt es die Möglichkeit, eine Abgabe nachzubessern?
Bei den Abgaben gibt es nur die Zustände “bestanden” oder “nicht bestanden”. Da die Aufgaben aber über mehrere Wochen aufgebaut werden, muss die Endabgabe deutlich zu schlecht sein, um durchzufallen. Wer über alle Termine hinweg konsequent mitmacht und seinen eigenen Code versteht, hat wenig zu befürchten.
