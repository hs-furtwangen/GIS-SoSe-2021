## _V_ **1.4** CSS Vertiefung

### Komplexe Selektoren
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/01_CSS_Komplexe_Selektoren.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/01_CSS_Komplexe_Selektoren.mp4">Zum Video</a>
</video>

Man kann die grundlegenden CSS-Selektoren, die in der letzten Lektion vorgestellt wurden, auch verketten, um komplexere Selektionen zu machen. So kann entweder auf einzelne, spezielle Elemente konkret zugegriffen oder nur ganz bestimmte Gruppen oder Folgen von Elementen selektiert werden. Mit Pseudoklassen können auch Elemente in ganz bestimmten Zuständen manipuliert werden, wie zum Beispiel bei einem Link der Zustand des Herüberfahrens mit der Maus ("hovern").

**Links im Video**

<a href="https://flukeout.github.io">https://flukeout.github.io</a>

### Positionierung, Flussverhalten und Layout
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/02_CSS_Flussverhalten_Positionierung.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/02_CSS_Flussverhalten_Positionierung.mp4">Zum Video</a>
</video>

Aufgrund der vielen verschiedenen Ausgabegeräte kann das Thema der Positionierung sehr komplex werden, in diesem Video wurden aber die grundlegenden Herangehensweisen erklärt.
Die Positionierung der Elemente auf einer gerenderten Seite hat oft wenig mit der Position im DOM-Tree zu tun.

Das Flussverhalten beschreibt das Verhalten der Elemente im Textfluss, sodass ein Element beispielsweise von den nachfolgenden Elementen in einer Zeile umflossen werden kann oder einen Zeilenumbruch bewirkt. Dieser Textfluss kann über Float und die Positionierung auch individuell manipuliert werden.

Für differenziertere Seiten-Arrangements kann man Eigenschaften, wie Grid oder Flexbox, nutzen.

**Links im Video**

Float:
<a href="https://codepen.io/philtim/pen/KrZmdN">https://codepen.io/philtim/pen/KrZmdN</a>

Positionierung:
<a href="https://codepen.io/philtim/pen/GwyWBP">https://codepen.io/philtim/pen/GwyWBP</a>

### Responsive Design
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/03_Responsive_Design.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/03_Responsive_Design.mp4">Zum Video</a>
</video>

Responsive Design heißt, alle (relevanten) Endgerätegrößen zu bedienen, wie Smartphones, Laptops, Tablets, Bildschirme...

Technisch gesehen bedeutet Responsive Design im Web-Kontext, dass die Darstellung der Benutzeroberfläche zwar an unterschiedliche Ausgabegeräte angepasst wird, die Datenbasis bleibt jedoch gleich. Konzeptionell bedeutet Responsive Design, dass eine interaktive Anwendung in möglichst vielen (relevanten) Anwendungsszenarien (am Schreibtisch, unterwegs im Bus usw...) genutzt werden kann. 

In CSS lässt sich eine **adaptive** (stufenweise) oder **responsive** (stufenlose) Darstellung beispielweise durch Breakpoints und Mediaqueries oder flexible Größen- und Positionierungsanweisungen realisieren.

**Links im Video**

Responsive Cat:
<a href="http://roxik.com/cat/">http://roxik.com/cat/</a>

Responsive Design Check:
<a href="http://ami.responsivedesign.is/">http://ami.responsivedesign.is/</a>

### CSS Transition und Animation
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/04_CSS_Transition_und_Animation.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/04_CSS_Transition_und_Animation.mp4">Zum Video</a>
</video>

Mit **Übergängen** (Transitions) und **Animationen** können in Webanwendungen zeitbasierte Effekte genutzt werden, die ein Design lebendig und flüssig wirken lassen oder dem Nutzer auf narrativer Ebene den Interaktionsfluss beschreibt.
Die Animation von CSS Eigenschaften lässt sich durch viele Parameter steuern, bspw. auch durch die Definition der Beschleunigung der Animation.

**Links im Video**

CSS Transition Beispiel:
<a href="https://codepen.io/grausch/pen/XWWeZXW">https://codepen.io/grausch/pen/XWWeZXW</a>

CSS Animationen:
<a href="https://codepen.io/ajerez/pen/EaEEOW">https://codepen.io/ajerez/pen/EaEEOW</a>

Eigene Bezierkurve zeichnen:
<a href="http://cubic-bezier.com/">http://cubic-bezier.com/</a>

### Take Aways
<video controls width="100%"> 
    <source src="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/05_Take_Aways.mp4" type="video/mp4"> 
    <a href="https://lehre.gabriel-rausch.de/HFU/EIA1_static/L04/05_Take_Aways.mp4">Zum Video</a>
</video>

- Komplex verkettete Selektoren ermöglichen es, spezifischere Auswahlpfade zu erstellen.
- Elemente haben individuelle Positionen und Flussverhalten, die manipuliert werden können.
- Über Responsive Design lassen sich viele relevante Endgeräte bedienen.
- Über Transition und Animation lassen sich Elemente, oder deren Eigenschaften, animieren.

---

#### CSS Inspiration

[CSS Zen Garden](http://csszengarden.com/), eine Seite welche über 200 verschiedene CSS Styles für den gleichen HTML Inhalt gesammelt hat, zeigt sehr gut die Möglichkeiteb von CSS. Lassen Sie sich inspirieren.

---

## **?!** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A-Termin)

Zusammenfassung von: [&lt;TawsTm&gt;](https://github.com/TawsTm)

### Ist die Abgabe immernoch über FELIX?
Antwort: Abgaben können aus Datenschutz-rechtlichen Gründen nicht über Github, sondern müssen über FELIX getätigt werden. Der Link dazu: <a href="https://felix.hs-furtwangen.de/auth/RepositoryEntry/3994517970">Felix</a>

### Sollen wir alle unsere Aufgaben hochladen?
Nein! Ihr sollt nur die letzte Aufgabe, dieses mal also Aufgabe 1.4 abgeben. Diese muss aber alle Anforderungen der vorherigen Aufgaben enthalten. Mit hochladen ist hiermit das bereitstellen der Links in Felix gemeint.

### Soll ich die Dateien abgeben oder einen Link bereitstellen?
Sie können im Felix Text-Editor die zwei Links einfügen und abspeichern. Der erste Link sollte zur HTML-Seite führen und der zweite zu dem Ordner in ihrem Repository, in dem ihr Code liegt.

### Meine h1-Inhalte sind zu klein, was kann ich tun?
Um Größen in Schriften zu verändern, werden hauptsächlich rem, em und pt verwendet.

### Sind Anforderungen mit Sternchen Anforderungen die in der Aufgabe vorhanden sein müssen?
Alle Lösungen aus den Aufgaben 1.1. - 1.4. sollen in Aufgabe 1.4. zusammen kommen. Das heißt nicht, dass Sie alle Aufgaben einzeln hochladen sollen. Alle Punkte sollten sich in Aufgabe 1.4. wiederfinden.
