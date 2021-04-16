<!-- # 1.4 Grundlagen CSS -->

## Komplexe Selektoren
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/04/01_CSS_Komplexe_Selektoren.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/04/01_CSS_Komplexe_Selektoren.mp4">Zum Video</a>
</video>

**[Flukeout Plates](https://flukeout.github.io){:target="_blank"}**

Man kann die grundlegenden CSS-Selektoren, die in der letzten Lektion vorgestellt wurden, auch verketten, um komplexere Selektionen zu machen. So kann entweder auf einzelne, spezielle Elemente konkret zugegriffen oder nur ganz bestimmte Gruppen oder Folgen von Elementen selektiert werden. Mit Pseudoklassen können auch Elemente in ganz bestimmten Zuständen manipuliert werden, wie zum Beispiel bei einem Link der Zustand des Herüberfahrens mit der Maus ("hovern").

---

## Positionierung, Flussverhalten und Layout
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/04/02_CSS_Flussverhalten_Positionierung.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/04/02_CSS_Flussverhalten_Positionierung.mp4">Zum Video</a>
</video>

**[Float](https://codepen.io/philtim/pen/KrZmdN){:target="_blank"}**
**[Positionierung](https://codepen.io/philtim/pen/GwyWBP){:target="_blank"}**

Aufgrund der vielen verschiedenen Ausgabegeräte kann das Thema der Positionierung sehr komplex werden, in diesem Video wurden aber die grundlegenden Herangehensweisen erklärt.
Die Positionierung der Elemente auf einer gerenderten Seite hat oft wenig mit der Position im DOM-Tree zu tun.

Das Flussverhalten beschreibt das Verhalten der Elemente im Textfluss, sodass ein Element beispielsweise von den nachfolgenden Elementen in einer Zeile umflossen werden kann oder einen Zeilenumbruch bewirkt. Dieser Textfluss kann über Float und die Positionierung auch individuell manipuliert werden.

Für differenziertere Seiten-Arrangements kann man Eigenschaften, wie Grid oder Flexbox, nutzen.

---

## Responsive Design
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/04/03_Responsive_Design.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/04/03_Responsive_Design.mp4">Zum Video</a>
</video>

**[Responsive Cat](http://roxik.com/cat/){:target="_blank"}**
**[Responsive Design Check](http://ami.responsivedesign.is/){:target="_blank"}**

Responsive Design heißt, alle (relevanten) Endgerätegrößen zu bedienen, wie Smartphones, Laptops, Tablets, Bildschirme...

Technisch gesehen bedeutet Responsive Design im Web-Kontext, dass die Darstellung der Benutzeroberfläche zwar an unterschiedliche Ausgabegeräte angepasst wird, die Datenbasis bleibt jedoch gleich. Konzeptionell bedeutet Responsive Design, dass eine interaktive Anwendung in möglichst vielen (relevanten) Anwendungsszenarien (am Schreibtisch, unterwegs im Bus usw...) genutzt werden kann. 

In CSS lässt sich eine **adaptive** (stufenweise) oder **responsive** (stufenlose) Darstellung beispielweise durch Breakpoints und Mediaqueries oder flexible Größen- und Positionierungsanweisungen realisieren.

---

## CSS Transition und Animation
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/04/04_CSS_Transition_und_Animation.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/04/04_CSS_Transition_und_Animation.mp4">Zum Video</a>
</video>

**[CSS Transition Beispiel](https://codepen.io/grausch/pen/XWWeZXW){:target="_blank"}**
**[CSS Animationen](https://codepen.io/ajerez/pen/EaEEOW){:target="_blank"}**
**[Eigene Bezierkurve zeichnen](http://cubic-bezier.com/){:target="_blank"}**

Mit **Übergängen** (Transitions) und **Animationen** können in Webanwendungen zeitbasierte Effekte genutzt werden, die ein Design lebendig und flüssig wirken lassen oder dem Nutzer auf narrativer Ebene den Interaktionsfluss beschreibt.
Die Animation von CSS Eigenschaften lässt sich durch viele Parameter steuern, bspw. auch durch die Definition der Beschleunigung der Animation.

---

## Take Aways
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/04/05_Take_Aways.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/04/05_Take_Aways.mp4">Zum Video</a>
</video>

- Komplex verkettete Selektoren ermöglichen es, spezifischere Auswahlpfade zu erstellen.
- Elemente haben individuelle Positionen und Flussverhalten, die manipuliert werden können.
- Über Responsive Design lassen sich viele relevante Endgeräte bedienen.
- Über Transition und Animation lassen sich Elemente, oder deren Eigenschaften, animieren.

---

## CSS Inspiration

[CSS Zen Garden](http://csszengarden.com/), eine Seite welche über 200 verschiedene CSS Styles für den gleichen HTML Inhalt gesammelt hat, zeigt sehr gut die Möglichkeiteb von CSS. Lassen Sie sich inspirieren.

