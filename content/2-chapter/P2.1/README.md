## _P_ **2.1** Typescript und Javascript Einstieg

Diese Woche dient als Einstieg in die Entwicklung mit einer für Sie neuen Sprache, darum werden wir lediglich die Grundlagen behandeln. In der übernächsten Woche geht es dann an konkretere Umsetzungen für die Kapitelaufgabe.

### Aufgabe 1 - Basics

```ts
function a1(): void {
    let x: string = "Alles";
    console.log(x);
    func1();
    console.log("Logo!");
}

a1();

function func1(): void {
    console.log("Klar?");
}

```

**a)** Lesen Sie das obige Programm. Was wird wohl auf der Konsole ausgegeben? Lassen Sie das Programm laufen und experimentieren Sie mit den Namen der Variablen und Funktionen. Welche Variablennamen sind zulässig, welche nicht?  

**b)** Öffnen Sie im Browser den Debugger (neben der Konsole) und setzen Sie einen Breakpoint in Zeile 3 (alternativ können Sie im Code vor Zeile 3 das Schlüsselwort `debugger;` einfügen). Laden Sie dann die Seite neu und gehen Schritt für Schritt durch den Code durch, die Schaltflächen dafür sind normalerweise rechts am Rand:  
![](https://camo.githubusercontent.com/372a0f981e20eab3064ce57f78bf81a23c9808e2/68747470733a2f2f692e696d6775722e636f6d2f53566e4c5930702e706e67)  
Verfolgen Sie, welcher Codeabschnitt wann ausgeführt wird und in welcher Reihenfolge die Funktionen aufgerufen werden.


> ℹ Ein Debugger dient wie der Name schon vermuten lässt dem Debuggen, dem Entfernen von Bugs, dem Finden und Erkennen von Fehlern. Er erlaubt es einem, ein Programm zu pausieren und dieses dann Zeile für Zeile durchzuführen um den Ablauf und die Änderungen die während des Durchlaufs passieren, nachzuvollziehen. Diese langsame und Schritt für Schritt Vorgehensweise erlaubt es relativ einfach die internen Vorgänge nachzuvollziehen und Fehler in der Logik des Programms zu finden. Er ist also neben Konsolenausgaben das wichtigste und wertvollste Tool zur Fehlererkennung.

> > Der Name "Bug" stammt Gerüchten nach daher, dass in den ersten elektronischen Rechnern die mechanischen Kontake nicht mehr zusammengedrückt werden konnten, weil ein Käfer seinen Weg in den Zwischenraum gefunden hat, wodurch sich die Maschine verrechnet hat.

> ℹ️ Bei vielen Programmiersprachen ist der Debugger direkt in der IDE (in unserem Fall VSCode) integriert, aber um Javascript Code ausführen zu können benötigt man entweder einen Browser oder einen Server, was das Debuggen deutlich schwieriger macht. Glücklicherweise steht uns in Browsern ein Debugger zur Verfügung.

**c)** Fügen Sie weitere Funktionen ein, die wie `func1()` jeweils ein Wort ausgeben. func1 kann dafür kopiert und angepasst werden. Rufen Sie die Funktionen in `a1()` so auf, dass der Text "Alles Gute! Alles klar? Alles Logo!" auf der Konsole ausgegeben wird.

### Aufgabe 2 - Kontinuierliche Variablenmanipulation

```ts

function a2(): void {
    let i: number = 9;

    do {
        console.log(i);
        i = i - 1;
    } while( i > 0);
}

a2();

```

Schauen Sie sich den obigen Code an und versuchen Sie nur durch lesen zu verstehen was passiert. Was wird auf der Konsole ausgegeben? Wann verändert sich was?  
Lassen Sie den Code dann laufen und überprüfen Sie, ob sie richtig liegen. Schauen Sie sich den Programmablauf mit dem Debugger an. Fügen Sie außerdem im Debugger die Variable `i` zu den überwachten Variablen hinzu ("Watch" in Chrome, "Ausdruck beobachten" in Firefox), um deren Änderung einfacher zu verfolgen.


### Aufgabe 3 - Fehler erkennen und vermeiden lernen

**a)** Bauen Sie in dem Code von A1 und A2 Fehler ein (s. auch die Arten von Fehlern im [Fragen und Probleme](../../#fragen-und-probleme) Abschnitt) und studieren Sie die Fehlermeldungen in VSCode. Lässt sich aus den Fehlermeldungen schließen, was falsch ist?

**b)** Tun sie sich mit Komilitonen zusammen und versuchen Sie die Fehler der anderen zu finden un zu lösen.

1.) Durch Codeinspektion: Versuchen durch Lesen die Fehler zu finden.  
2.) Durch Fehlermeldungen: Die Fehler in VSCode anschauen und versuchen, diese zu verstehen.  
3.) Durch Auskommentieren und Debugger: Wenn das Programm sich übersetzen lässt, aber nicht das richtige Verhalten aufweist, nach und nach Codeschnipsel aus und wieder einkommentieren, bis der Auslöser gefunden ist.  
4.) Wenn das alles nicht hilft, mit dem vorgegebenen Code vergleichen und die Fehler finden.

### Aufgabe 4 - Gobal vs Lokal

```ts
let x: string = "Hallo";
console.log(x);
func1(x);
console.log(x);
func2();
func3();
console.log(x);

function func1(y: string): void{
    y = "Bla";
    console.log(y);
}

function func2(): void{
    let x: string = "Blubb";
    console.log(x);
}

function func3(): void{
    x = "Test";
}
```

**a)** Betrachten Sie den obigen Code. Was wird er auf der Konsole ausgeben und warum? Lassen Sie ihn anschließend laufen und überprüfen Sie Ihre Annahmen.

**b)** Erklären Sie einem Komilitonen den Unterschied zwischen globalen Variablen, lokalen Variablen und Übergabeparametern.  
Inwiefern unterscheiden sich "normale" Variablen wie Zahlen und strings von Funktionen? Inwiefern sind sie gleich?

### Aufgabe 5 - Schleifen, Funktionen und andere Kontrollstrukturen

**a)** Schreiben Sie eine Funktion `multiply` welche zwei Zahlen als Parameter entgegen nimmt und als Rückgabewert das Ergebnis der Multiplikation der beiden Parameter liefert. Testen Sie Ihre Funktion auf eine geeignete Weise.

**b)** Schreiben Sie eine Funktion `max` welche zwei Zahlen als Parameter entgegen nimmt und die größere der beiden zurück gibt. Nutzen Sie dafür nicht `Math.max` sondern schreiben Sie ihre eigene Implementation. Testen Sie Ihre Funktion auf eine geeignete Weise.

**c)** Zählen Sie mithilfe einer `while` Schleife alle Zahlen von 1 bis 100 zusammen und geben Sie das Ergebnis auf der Konsole aus.

**d)** Nutzen Sie eine `for` Schleife um 10 zufällige Zahlen zwischen 0 und 100 auf der Konsole auszugeben. Nutzen Sie dafür [Math.random](https://developer.mozilla.org/de/docs/Web/JavaScript/Reference/Global_Objects/Math/math.random)

**e)** Schreiben Sie eine Funktion `factorial` welche eine Zahl `n` entgegen nimmt und als Rückgabewert die [Fakultät](https://de.wikipedia.org/wiki/Fakult%C3%A4t_(Mathematik)) (`1*2*3*...*n`) dieser Zahl zurück gibt. Nutzen Sie dafür eine Schleife ihrer Wahl (`while, do while, for`). Geben Sie außerdem `1` zurück, wenn `n` kleiner ist als 1.

**f)** Schreiben Sie eine Funktion `leapyears` welche alle Schlatjahre von 1900 bis heute auf der Konsole ausgibt. Ein Jahr ist ein Schaltjahr, wenn die Jahreszahl durch 4, aber nicht durch 100 teilbar ist. Sollte die Jahreszahl durch 400 teilbar sein, handelt es sich dennoch um ein Schaltjahr.

### Aufgabe 6 - Mehr Schleifen und Funktionen

**a)** Schreiben Sie eine Schleife welche auf der Konsole folgende sieben Zeilen ausgibt: 
```
#
##
###
####
#####
######
#######
```
_Hinweis: die Länge eines strings kann über `stringname.length` abgefragt werden._

**b)** Schreiben Sie ein Programm welches auf der Konsole alle Zahlen von 1 bis 100 ausgibt. Dabei gibt es zwei Ausnahmen: Ist die Zahl durch 3 teilbar, geben Sie statt der Zahl `Fizz` aus. Ist sie durch 5 (und nicht durch 3) teilbar, geben sie `Buzz` aus.  
_Hinweis: Nutzen sie den Modulo Operator `%` um zu prüfen, ob eine Variable durch eine andere teilbar ist (Rest 0)._

**c)** Nehmen Sie das Programm aus b) und modifizieren Sie es so, dass das Programm `FizzBuzz` ausgibt, wenn die Zahl durch sowohl 3 als auch durch 5 teilbar ist.  
_Hinweis: Dieser Teil der Aufgabe hat eine offensichtlichere und eine cleverere Lösung. Finden Sie beide?_

> Diese Frage ist eine beliebte Frage in Vorstellungsgesprächen. Wenn Sie diese also gelöst bekommen, ist Ihr Marktwert gerade gestiegen.

**d)** Schreiben Sie eine Funktion, welche einen String zurückgibt, der ein 8x8 Schachbrett repräsentiert, mit neuen Zeilen (`"\n"`) um die Zeilen zu trennen. An jeder Position im Brett ist entweder ein `#` oder ein Leerzeichen.

Wenn der String über console.log ausgegeben wird, sollte er etwa so aussehen:

```
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
 # # # #
# # # # 
```

_Hinweis: Beginnen Sie mit einem leeren string (`""`) und fügen Sie dann immer mehr Zeichen hinzu. Für zwei Dimensionen brauchen Sie zwei Schleifen ineinander, eine für die Zeilen und eine für die Character innerhalb der Zeile._

**e)** Nehmen Sie die Funktion aus d) und fügen Sie ihr einen Übergabeparameter hinzu, welcher die Höhe und Breite des Brettes bestimmt. Schreiben Sie ihre Funktion so um, dass es mit jeder Größe Funktioniert.  
_Hinweis: Machen Sie sich Gedanken wie sie sich merken/berechnen können, welcher Character als erstes/nächstes in einer Zeile ausgegeben werden muss._

<!-- Überarbeiten Sie Ihren Shop aus Aufgabe 4 dahingehend, dass Sie die Artikel auf der Seite über TypeScript generieren.
Es sollten keine Artikel mehr im HTML direkt stehen, sondern durch TypeScript, nachdem die Seite geladen wurde, generiert werden.
Entwickeln sie dafür eine passende Datenstruktur über `interface`s, so dass alle artikelrelevanten Informationen (s. A4) in einem Array abgelegt, abgefragt und verwendet werden können. Legen Sie dann alle benötigten Informationen in Ihrem Code ab und generieren Sie über geeignete Schleife(n) nachdem die Seite geladen ist die Artikel dynamisch hinzu.
Wenn Sie können, trennen sie die Daten und die Funktionalität in unterschiedliche TS Dateien (ein gemeinsamer `namespace` ist  hier empfohlen). Beachten Sie die [Coding Style Guidelines](https://hs-furtwangen.github.io/GIS-SoSe-2020/codingstyle/).

**Klarstellung**: Das interface sollte einen Artikel abbilden, und sämtliche relevanten Artikelinformationen zu einem Artikel sollte in diesem Interface sinnvoll abgelegt werden können. Die Sammlung aller Artikel soll dann in sinnvoller Weise abgebildet werden, z.B. in _einem_ Array in dem alle Artikel liegen. Bedenken Sie dabei die Skalierbarkeit und Anpassbarkeit (wie schwierig ist es, einen Artikel hinzuzufügen/entfernen/ändern?)! Bei einer kleinen Änderung sollten Sie nicht mehr Änderungen an ihrem Code vornehmen müssen als die reine Information zu verändern. 

### Recherchehinweise:
[Auf DOM Elemente über JS zugreifen](https://www.w3schools.com/js/js_htmldom_elements.asp)  
[das HTML von DOM Elementen verändern](https://developer.mozilla.org/en-US/docs/Web/API/Element/innerHTML)  
[Template Strings](https://www.typescriptlang.org/docs/handbook/release-notes/typescript-1-4.html#template-strings)  

### Freiwillige Übungsaufgaben
[Übungsaufgaben mit Fokus auf Konsolenausgaben zum Selbststudium](https://github.com/Plagiatus/EIA/blob/master/Aufgaben.md) mit Lösungen. (Diese Aufgaben wurden ursprünglich für das Ende von EIA1 konzipiert um sich auf EIA2 vorzubereiten, stellen aber allgemein eine gute Ressource zum Selbststudium dar, inklusive einfacher Aufgaben zur Wiederholung als auch sehr komplizierte Aufgaben. _Keine offizielle Aufgabe, lediglich als Bonusmaterial wenn Sie Zeit und Lust haben noch etwas mehr zu üben!_) -->
