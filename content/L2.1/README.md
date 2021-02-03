## _V_ **2.1** Typescript und Javascript Einstieg

### Inhaltsverzeichnis

- [Einrichtung Typescript in VSCode](#einrichtung-typescript-in-vscode)
- [Vorwort JavaScript / Typescript](#vorwort-javascript--typescript)
- [JavaScript / Typescript Einführung](#javascript--typescript-einführung)
  - [Zahlen](#zahlen)
  - [Zeichenketten](#zeichenketten)
  - [Boolsche Werte](#boolsche-werte)
  - [Vergleiche](#vergleiche)
  - [Logische Operatoren](#logische-operatoren)
  - [Leere Werte](#leere-werte)
  - [Konvertierung](#konvertierung)
- [Typescript Kontrollstrukturen](#typescript-kontrollstrukturen)
  - [Funktionen](#funktionen)
  - [Programmablauf und Kontrollstrukturen](#programmablauf-und-kontrollstrukturen)
    - [if / else](#if--else)
    - [Schleifen](#schleifen)
- [Q&A](#-fragen-und-antworten)


### Einrichtung Typescript in VSCode
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_Einrichtung_Typescript.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_Einrichtung_Typescript.mp4">Zum Video</a>
</video>

Denken Sie daran, immer wenn Sie Ihren VSCode Editor öffnen, den BuildTask zu starten. Wenn Sie es automatisieren möchten, schauen Sie eigenverantwortlich [hier](https://code.visualstudio.com/docs/editor/tasks) oder [hier](https://marketplace.visualstudio.com/search?term=Typescript%20Auto%20Compiler&target=VSCode&category=All%20categories&sortBy=Relevance).


`Strg + Shift + B` für die Build Tasks oder über `Terminal > Buildaufgabe ausführen`. Wählen Sie "watch/Überwachen" um bis Sie VSCode schließen die js Dateien immer übersetzt zu bekommen oder "make/Erstellen" um einmal das gesamte Projekt zu übersetzen.

_Laden Sie die .js.map Dateien und selbstverständlich auch die .ts Dateien mit hoch._


#### Hinweis 

- sollte Ihnen VSCode einmal einen Fehler anzeigen bei dem Sie sich sicher sind, dass alles korrekt ist, starten Sie VSCode neu. Sollte der Fehler dann immernoch angezeigt werden, liegt es zu 99.9% doch an ihrem Code. Dieses Problem einer falschen Fehlermeldung ist sehr selten, soll hier aber trotzdem erwähnt werden.


**Links im Video**

- <a href="https://nodejs.org/">NodeJS</a>  
- [TSLint Erweiterung](https://marketplace.visualstudio.com/items?itemName=ms-vscode.vscode-typescript-tslint-plugin)
- [Konfigurations Dateien (*tsconfig* und *tslint*)](https://github.com/hs-furtwangen/GIS-WiSe-2020-2021/tree/master/config_files)

**Terminal Befehle**
- `npm -v`
- `npm i -g typescript`
  - falls Sie auf Mac oder Linux sind, müssen Sie eventuell `sudo` vor diesen und den nächsten Befehl schreiben. Dies führt die Befehle mit Administratorrechten aus.
- `npm i -g tslint`
- `tsc --version`
  - falls es dabei in Powershell Probleme gibt, Powershell als Administrator ausführen, den folgenden Befehl ausführen und mit J/Y bestätigen.  
  `Set-ExecutionPolicy -ExecutionPolicy RemoteSigned -Scope LocalMachine`

### Vorwort JavaScript / Typescript
<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_JSTS_Vorwort.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_JSTS_Vorwort.mp4">Zum Video</a>
</video>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/05_JSTS_Vorwort.pdf){:target="_blank"}*

### JavaScript / Typescript Einführung

JavaScript ist die primäre Sprache wenn es darum geht, in einem Browser / auf einer Webseite Code auzuführen. 1995 eingeführt für den Netscape Browser wurde sie bald weit verbreitet eingesetzt und ist heute in den Top 10 der meistgenutzten Sprachen Weltweit. Ursprünglich auch nur als Frontend (Nutzerseite) Sprache entwickelt, kann Sie heute auch als Backend (Serverseite, Datenbanken) eingesetzt werden.

JS wird stetig weiterentwickelt. Der im Video angesprochene ECMAScript Standard (welcher in vielerlei Hinsicht Synonym zu JS ist), wird jedes Jahr erweitert und ergänzt. Dabei wird stets darauf geachtet, dass eine volle Rückwärtskompatibilität möglich ist, so dass ältere Programme auch weiterhin laufen. Dies bedeutet allerdings auch, dass die Browser immer wieder neu angepasst werden müssen, um mit dem aktuellen Standard mitzuhalten, weswegen neuere Konzepte in älteren Browsern / Browserversionen gegebenenfalls nicht funktionieren. Diese Einschränkung soll uns in dieser Veranstaltung nicht zurückhalten, da wir davon ausgehen dass aktuelle Browser verwendet werden, sollte aber im Hinterkopf behalten werden wenn kommerzielle Produkte entwickelt werden.

Es gibt Menschen, die schlimme Dinge über JavaScript sagen. Und die meisten dieser Dinge sind wahr. JS akzeptiert beinahe alles was man ihm an den Kopf wirft, interpretiert und konvertiert es dann aber in oft unerwarteten / ungewollten Arten und Weisen, was sich auf die beinahe lächerliche Freizügigkeit der Sprache zurückführen lässt. Die Idee dahinter ist es, den Enstieg für Neulinge einfacher zu machen. Leider hat dies häufig den gegenteiligen Effekt, da die Fehlerfindung in den eigenen Systemen dadurch deutlich erschwert wird. Diese Freiheiten haben aber natürlich auch Vorteile, allerdings muss man bereits eine hohe Menge an Wissen haben, um diese Freiheiten sinnvoll einsetzen zu können.

Typescript ist einer der erfolgreichsten Versuche, diese Nachteile und Hürden zu kompensieren, ohne die Vorteile der Sprache zu schmälern. Aus diesem Grund werden wir in dieser Vorlesung ausschließlich mit Typescript arbeiten.

#### Beispiel

Schauen Sie sich den folgenden Code zunächst einfach nur an. Fällt ihnen irgendetwas seltsames auf, erwarten Sie irgendwelche Fehlermeldungen? Versuchen Sie vorherzusagen, was auf der Konsole ausgegeben würde.  
Nun können sie über F12 in ihrem Browser die Konsole öffnen und (in reinem Javascript) die Befehle ausführen. Stimmen Ihre Erwartungen mit dem Ergebnis überein? Kopieren Sie den Code anschließend in eine .ts Datei.

```javascript
console.log(true + true);
console.log(5 + 1);
console.log(5 + '1');
console.log('5' + 1);
console.log('5' - 1);

//BONUS:
console.log(('b' + 'a' + + 'a' + 'a').toLowerCase());
```

Bei einigen dieser Anweisungen sollte der Typescript Compiler Ihnen Fehler anzeigen. Zum Glück, denn diese Anweisungen sind allesamt legitimer Javascript Code bei denen JS einfach wild hin und her konvertiert und sorgen für die seltsamsten Ergebnisse. Typescript schützt uns vor diesem seltsam anmutenden Verhalten. Kommentieren Sie die Fehlerhaften Zeilen aus und lassen Sie den übersetzten Code im Browser ausführen.

---

<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_JSTS_Einfuehrung.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_JSTS_Einfuehrung.mp4">Zum Video</a>
</video>

*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/05_JS_Einfuehrung.pdf){:target="_blank"}*

#### Zahlen

Zahlen, der Typ `number` in Typescript, stellen alle möglichen (nicht-imaginären) Zahlen dar. Sowohl Ganzzahlen (integer in Java) als auch Gleitkommazahlen (float / double in Java) werden darüber abgebildet. Für eine `number` wird 64bit Speicherplatz bereitgestellt. Das erste Bit wird genutzt zur Speicherung des Vorzeichens, dadurch können ganzzahlige Werte bis zu astronomischen +/- 2^63 (~9 Trillionen) gespeichert und berechnet werden, ohne dass man an Grenzen stößt und so exakte Werte berechnen kann. Bei Gleitkommazahlen sieht die Sache etwas komplizierter aus, da diese eine andere Darstellungsform nutzen müssen, was zu Genauigkeitsverlusten führen kann. Genauso wie man die Kreiszahl Pi nicht mit einer endlichen Anzahl von Zeichen exakt beschreiben kann, verlieren viele Zahlen etwas Genauigkeit wenn wir nur 64 bits zur Verfügung haben um diese abzubilden. Das ist in den meisten Fällen aber kein Problem, da die Näherungswerte immernoch genau genug sind.

Zahlen können als Ganzzahl (`10`), Kommazahl (mit einem Punkt als Trennzeichen `3.1415`) oder in wissenschaftlicher Notation (`2.98e8` = 2.98 * 10^8 = 298'000'000) geschrieben werden.

Arithmetische Operationen die auf Zahlen angewandt werden können sind Addition (`+`), Subtraktion (`-`), Multiplikation (`*`), Division (`/`) sowie Modulo (`%`). JS folgt der Punkt-Vor-Strich und Klammernregelung.

In JS gibt es drei **spezielle Zahlen**. Die ersten beiden sind `Infinity` und `-Infinity`, welche positive und negative Unendlichkeit darstellen. Die dritte und wahrscheinlich häufiger genutzte ist `NaN`, was für "not a number" (keine Zahl) steht. Dieses Ergebnis erhält man unter anderem, wenn man versucht mathematischen Schwachsinn zu berechnen (`0 / 0`), oder versucht strings, welche keine Zahlen beinhalten, in Zahlen zu konvertieren (`parseInt("hello")`).

#### Zeichenketten

Zeichenketten, `string` in Typescript, repräsentieren Text und werden angelegt indem Text innerhalb von Anführungszeichen eingeschlossen wird. Dabei gibt es drei Möglichkeiten:
1. `''` Das einzelne Anführungszeichen
2. `""` Das doppelte Anführungszeichen (in diesem Kurs bevorzugt)
3. `` ` ` `` Der "Backtick". Hat besondere Funktionen, welche die anderen beiden nicht haben:
    1. Eine neue Zeile im Code wird darin als neue Zeile übernommen
    2. Kann mit Werten befüllt werden, ist dann ein sogenannter "Template String/Literal": ``` `Die Hälfte von 10 ist ${10 / 2}` ```. Diese Werte werden berechnet, in einen string konvertiert und schließlich eingefügt

Strings können nicht Multipliziert, Dividiert oder Subtrahiert werden, aber Addieren funkioniert. `"G" + "I" + "S" -> "GIS"`

#### Boolsche Werte
Wahrheitswete, `boolean` in Typescript, sind entweder `true` oder `false`, 1 oder 0, an oder aus. Diese an sich können schon sinnvoll sein, werden aber oft bei Vergleichen gebraucht.

#### Vergleiche

```js 
console.log(3 > 2); // -> true
console.log(3 < 2); // -> false
```

Die größer-als und kleiner-als Operatoren resultieren in einem Boolschen Wert, welcher Angibt ob die Aussage korrekt ist.

Ähnlich wie Zahlen, können auch Strings verglichen werden:
```js
console.log("Aal" < "Zebra") // -> true
```
Aber vorsicht, obwohl der Vergleich auf den ersten Blick dem Alphabet entspricht, werden Großbuchstaben immer als kleiner angesehen als Kleinbuchstaben. Zeichen die keine Buchstaben (!, -, etc) sind, werden dabei auch mit einbezogen. Der Grund für diese Sortierung ist, dass strings in JS Zeichen für Zeichen nach der [Unicode Tabelle](https://unicode-table.com/de/) abgearbeitet werden.

Andere Vergleichende Operatoren sind `>=`, `<=`, `==` und `!=`.

Der einzige Wert der nicht gleich zu sich selbst ist, ist `NaN`, da dieser per Definition das Ergbnis einer unsinnigen Berechnung ist, und somit nicht gleich zu jeder anderen unsinnigen Berechnung sein kann.

#### Logische Operatoren

Verschiedene Operatoren können auch auf Wahrheitswerte direkt angewandt werden. JS/TS stellt dafür drei verschiedene Operatoren zur Verfügung.

1. UND `a && b` ist nur dann `true`, wenn beide Werte `true` sind.
```js
console.log(true && true) // -> true
console.log(false && true) // -> false
console.log(false && false) // -> false
``` 
2. ODER `a || b` ist dann `true`, wenn mindestens einer der beiden Werte `true` ist.
```js
console.log(true || true) // -> true
console.log(false || true) // -> true
console.log(false || false) // -> false
``` 
3. NICHT `!a` invertiert den nachfolgenden Wahrheitswert. 
```js
console.log(!true) // -> false
console.log(!false) // -> true
``` 

#### Leere Werte
In JS/TS gibt es zwei spezielle Werte, welche die Abwesenheit von Daten ausdrücken sollen: `null` und `undefined`. Viele Operationen, welche keine bedeutungsvollen Werte zurückliefern (können), liefern `undefined`, einfach weil sie ein Wert liefern _müssen_.

`null` und `undefined` sind dadurch wie sie in JS definiert sind, in den meisten Fällen, besonders in dieser Veranstaltung, austauschbar.

```js
console.log(null == undefined) // -> true
```

Das ist praktisch, denn so kann man testen, ob eine Variable mit einem Wert befüllt ist oder nicht.

#### Konvertierung
Wie in [Beispiel](#beispiel) bereits angesprochen, konvertiert JS gerne alles in alles. Das gilt auch für alle Operatoren, auch Vergleiche. Dadurch kommt es zu solchen Ergebnissen: 

```js
console.log(0 == false) // -> true 
console.log("" == false) // -> true 
console.log(false == false) // -> true 
```
Die 0 sowie der leere string werden implizit zu einem boolschen wert konvertiert, welcher `false` ist. Wenn man eine solche Konvertierung vermeiden möchte, kann man statt `==` den `===` (oder `!==`) Operator verwenden. Dieser testet ob ein wert _ohne_ Konvertierungen exakt gleich (oder eben ungleich) ist.
```js
console.log(0 === false) // -> false
console.log("" === false) // -> false 
console.log(false === false) // -> true 
```

**Typescript sorgt auch hier dafür, dass wir uns um diesen Fall keine Sorgen machen müssen indem es uns vor solchen Konvertierungen warnt, es soll aber der Vollständigkeit und dem Verständnis halber erwähnt werden.**

---

### Typescript Kontrollstrukturen

<video controls width="100%"> 
    <source src="https://scheuerle.net/lehre/gis/videos/05_TS_Kontrollstrukturen.mp4" type="video/mp4"> 
    <a href="https://scheuerle.net/lehre/gis/videos/05_TS_Kontrollstrukturen.mp4">Zum Video</a>
</video>
*[Folien zum Herunterladen](https://scheuerle.net/lehre/gis/scripts/05_TS_Kontrollstrukturen.pdf){:target="_blank"}*

**Das Lesen und Schreiben von Code sind unverzichtbar wenn es darum geht, Programmieren zu lernen!** Versuchen Sie darum, nicht über Beispiele schnell hinweg zu lesen, sondern lesen Sie diese Aufmerksam und versuchen Sie, sie zu verstehen, probieren Sie sie ggf. selbst aus. Ähnliches gilt für Übungen im Text sowie Wochen- und Kapitelaufgaben: Gehen Sie nicht davon aus, dass Sie sie verstanden haben, bis sie tatsächlich selbst eine funktionierende Lösung gefunden und getestet haben. Dies ist eventuell zunächst langsam und verwirrend, aber mit etwas Übung haben Sie schnell den Dreh raus.

Machen Sie alle Übungen und lassen Sie diese auch tatsächlich im Browser (oder einem anderen Interpreter) ausführen. So bekommen Sie direktes Feedback über den Code den Sie geschreiben haben und ob es funktioniert. Vielleicht, so hoffe ich, verspüren Sie dann auch die Versuchung, etwas anderes auszuprobieren und mit dem Code herumzuexperimentieren.

> **Denken Sie daran, dass sie, um den Code ausführen zu können, ihn in eine HTML Datei über ein `<script>` tag einbinden und diese dann im Browser aufrufen müssen.** Der so eingebundene Code wird in dem Moment ausgeführt, wo der Browser diesen im HTML findet (oder mit `defer` nachdem der Rest der Seite geladen wurde).

### Ein paar Beispiele

Schauen Sie sich diese einfachen Beispiele an und versuchen Sie diese zu verstehen, nachzuvollziehen und die ausgegebenen Werte vorauszusagen. Überprüfen Sie dann Ihre Vorhersagen.

```ts
let five: number = 5;
console.log(five * five);
```

```ts
let weather: string = "sunny";
console.log(weather);
weather = "dark";
console.log(weather);
``` 

```ts
let lukasDebt: number = 1000;
lukasDebt = lukasDebt - 50;
console.log(lukasDebt);
```

```ts
let one: number = 1, two: number = 2;
console.log(one + two);
```

```ts
let name: string = "Lukas";
const greeting: string = "Hello ";
console.log(greeting + name);
```

### Funktionen
Funktionen dienen dazu, einen Teilablauf des Gesamtprogrammes auszuführen. In einem Browser stehen viele Funktionen vom Browser selbst implementiert zur Verfügung, z.B. `prompt()` ist eine Funktion, welche eine kleine Dialogbox öffnet und den Nutzer um eine Eingabe bittet.

```ts
prompt("Passwort eingeben");
```

Eine Funktion ist wie alle anderen Variablen in TS/JS auch unter einem Namen gespeichert und hat einen Typen, in diesem Fall `function`. 

Funktionen erlauben es unter anderem, Teile des Codes wiederzuverwenden und so Codedopplungen zu vermeiden.

#### Parameter

Eine Funktion wird aufgerufen, indem man ihrem Namen eine öffnende und schließende Klammer anhängt. Die Werte zwischen den Klammern nennt man **(Übergabe)Parameter**. Unterschiedliche Funktionen brauchen unterschiedlich viele Parameter. Die `prompt` Funktion aus dem Beispiel von oben nutzt die übergebene Zeichenkette als Text der Dialogbox.

> Prompt wird in moderner Webprogrammierung nicht mehr häufig genutzt da man keine Möglichkeiten hat, das Aussehen der Box zu beeinflussen. Es ist aber für kleine Webseiten und Experimente immernoch sehr hilfreich.

Ein weiteres Beispiel was schon oft in dieser Woche genutzt wurde ist `console.log()`, welches auf einer vorhandenen Konsole die übergebenen Werte ausgibt. Obwohl Funktionennamen kein `.` enthalten dürfen, hat diese Funktion einen. Das liegt daran, dass es nicht eine einfache globale Funktion (wie prompt) ist, sondern dass es auf einem globalen `console` Objekt die Methode `log` aufruft. Dazu in einem späteren Kapitel mehr.

#### Rückgabe

Funktionen können Werte zurück an die aufrufende Stelle geben, welche daraufhin weiterverwendet werden können. Ggf. passieren dazwischen solche Nebeneffekte wie eine Dialogbox, um dem Nutzer eine Eingabe abzufragen. Andere Funktionen produzieren Werte und brauchen darum keine Nebeneffekte um Sinnvoll zu sein. Zum Beispiel `Math.max` nimmt eine beliebige Anzahl an Argumenten entgegen und gibt den größten davon zurück.

```ts
let x: number = Math.max(2, 4);
console.log(x);
```

Ein so zurückgegebener Wert kann auch direkt wie ein normaler Wert verwendet werden.

```ts
console.log(Math.min(2, 4) + 10);
```

```ts
let userInput: string = prompt("Pick a number");
let userNumber: number = Number(userInput);
console.log("The square of your number is " + userNumber * userNumber);
```

Um einen Wert von innerhalb der Funktion zurück zu geben, wird das Schlüsselwort `return` verwendet.

```ts
function add(_a: number, _b: number): number {
  let result: number = _a + _b;
  return result;
}
```

In dem Moment wo `return` ausgeführt wird, wird die Funktion beendet.

```ts
function example(): void {
  console.log("This will be print to the console");
  return;
  console.log("This won't, because the code will never reach here.");
}
```

An diesem Beispiel sieht man auch eine weitere Besonderheit von Funktionen: Diese können als Rückgabetyp `void` (engl.: das Nichts) besitzen, das bedeutet dass sie nichts (bzw `undefined`) zurückgeben. `return` funktionert aber auch weiterhin um die Funktion zu beenden, nimmt aber keinen Parameter an.

> Normale Variablen können theoretisch auch den Typ `void` besitzen, dann kann man in Ihnen aber nichts speichern und sie wird damit sinnlos. 


#### Definition

Um eigene Funktionen zu definieren, wird `let` durch `function` ersetzt. Außerdem werden innerhalb der Klammern die erwarteten Übergabeparameter definiert. Der Rückgabewert wird wie bei "normalen" Variablen dahinter geschrieben. Aber statt einem `=` folgen nun geschweifte Klammern in welchen die Funktionalität beschrieben wird.

```ts
function myFunction(_stringParam: string, _numberParam: number): number {
  // function implementation
}
```
_(Der Unterstrich vor den Parametern folgt den [Codingstyle Guidelines](../../codingstyle) dieses Kurses.)_

> Diese Form beschreibt exakt was als Übergabeparameter erwartet wird sowie als Rückgabewert zu erwarten ist. VSCode zeigt diese Form an, wenn man mit der Maus über einen Funktionsnamen hovert. So kann man Informationen über unbekannte Funktionen einholen und diese dann korrekt benutzen.

Da Funktionen in JS/TS auch ein Typ sind, können diese auch in Variablenschreibweise definiert werden und wie Variablen genutzt werden. Diese Definitionsform steht aber im Kontrast zu anderen Sprachen, darum ist sie in diesem Kurs nicht empfohlen. Außerdem können Funktionen, welche auf diese Weise definiert wurden, erst nach ihrer Definition aufgerufen werden, während die erste Variante immer aufgerufen werden kann.

```ts
let myFunction = function(_stringParam: string, _numberParam: number): number {...}
```

> ⚠️ Dies bedeutet auch, dass Funktionen wie Variablen neue Werte zugewiesen bekommen können und so komplett überschrieben werden können. Dies ist nicht nur ein Sicherheitsproblem für Webseiten, sondern kann auch sehr unübersichtlich werden. Wir raten in diesem Kurs daher davon ab, dies zu nutzen.

```ts
let launchMissles = function(): void {
  missileSystem.launch();
}
if(safeMode) {
  launchMissles = function(): void {/* tue nichts */};
}
```

### Programmablauf und Kontrollstrukturen
JS/TS Programme laufen in einer klar definierten Reihenfolge ab. Immer eine Zeile bzw. eine Anweisung nach der anderen. Wird eine Funktion aufgerufen, so wird der Hauptlauf des Programmes pausiert, bis die Funktion beendet wurde. 

#### If / Else

Über `if` Abfragen kann der Fluss des Programmes gesteuert werden und Teile des Codes nur ausgeführt werden, wenn eine Bedingung erfüllt ist.

```ts
if (true) {
  console.log("This will be in the console");
}
if (false) {
  console.log("This won't");
}
```

Oft will man etwas tun wenn eine Bedingung erfüllt ist, aber auch auch, wenn die Bedingung nicht erfüllt ist. Dafür kann man `else` verwenden. Im nachfolgenden Beispiel wird `isNaN` genutzt, um zu überprüfen ob eine Zahl NaN ist.

```ts
let input: string = prompt("Number please");
let inputNumber: number = Number(input);
if (!isNaN(inputNumber)){
  console.log("You have given me the number" + inputNumber);
} else {
  console.log("Hey! I wanted a number!")
}
```

`if` and `else` can be chained together.

```ts
let input: number = Number(prompt("Number please"));
if (inputNumber < 10){
  console.log("Small");
} else if (inputNumber < 100) {
  console.log("Medium");
} else {
  console.log("Big");
}
```

In manchen Fällen will man die gleiche Variable auf mehrere Werte abfragen, dann bietet sich `switch case` statt einer langen elseif Schlange an. Switches haben noch einige weitere Funktionalitäten, auf welche an dieser Stelle aber nicht eingegeangen wird.

```ts
let input: string = prompt("Command please");
if(input == "test") console.log("This is a test.");
else if (input == "laugh") console.log("Hahahahaa. Ha.");
else if (input == "foo") console.log("bar");
else console.log("I don't know that command.");

switch (input) {
  case "test": {
    console.log("This is a test.");
    break;
  }
  case "laugh": {
    console.log("Hahahahaa. Ha.");
    break;
  }
  ...
  default: {
    console.log("I don't know that command.");
  }
}

```

#### Schleifen

Es gibt verschiedene Schleifenarten aus denen man sich eine aussuchen kann um seinen Code wiederholt ausführen zu lassen. Sie können alle ineinander überführt werden, haben also funktional die gleichen Fähigkeiten. Sie sind aber trotzdem unterschiedlich in ihren Anwendungsfällen durch ihren eingebauten Aufbau.

> ⚠️ Vorsicht vor Schleifen die sich nie beenden. Das kann schon mal den Browser abstürzen lassen.

**While**

Whileschleifen wiederholen einen Codeabschnitt so lange, bis die gegebene Bedingung nicht mehr erfüllt ist.

```ts
let x: number = 1;
while (x < 100){
  x *= 2;
}
console.log(x);
```

Sie eignen sich besonders für Schleifen, in denen man nicht direkt im Voraus weiß, wie oft der Code wiederholt werden muss.

**Do While**

Ähnlich wie die `while` Schleife führt eine do while schleife die Anweisungen so lange aus, bis die Wiederholungsbedingung nicht mehr gegeben ist. Der Unterschied ist jedoch, dass es auf jeden Fall einmal durchgeführt wird.

```ts
let yourAge: number;
do {
  yourAge = Number(prompt("Tell me your age please"));
} while (isNaN(yourAge));
console.log(yourAge)
```

Diese eignen sich besonders für Schleifen, welche so lange etwas wiederholen müssen bis es den Vorgaben genügt, dies aber mindestens einmal tun müssen.

**For**

Die Forschleife unterscheidet sich in ihrem Aufbau, da sie in ihrem Schleifenkopf statt nur der Laufbedingung auch die Initialbedingung als auch die Änderungsanweisung beinhaltet, getrennt durch `;`. 

```ts
for (let i: number = 0; i < 10; i++) {
  console.log(i);
}
```

Forschleifen eigenen sich besonders für Schleifen in denen es eine (im Voraus gegebene) bestimmte Menge and Operationen zu erledigen gibt, z.B. alle Einträge eines Arrays durchzugehen. 

**Spezielle Sprunganweisungen**

- `break`: Beendet die gesamte Schleife
- `continue`: Beendet nur den aktuellen Schleifendurchlauf und macht mit dem nächsten weiter (sofern die Laufbedingung noch erfüllt ist)

Die While Schleife aus dem obigen Beispiel könnte umgeschrieben werden, um break zu demonstrieren.

```ts
let x: number = 1;
while (true){
  if(!(x < 100)) {
    break;
  }
  x *= 2;
}
console.log(x);
```

### Scopes / Geltungsbereiche

Jede Variable (und damit auch Funktion) hat einen Geltungsbereich, in dem auf sie zugegriffen werden kann. Variablen welche außerhalb von Funktionen oder Blöcken (so ziemlich alles, was von `{}` umgeben ist) definiert sind, sind sogenannte globale Variablen und können von überall im Programm aufgerufen und genutzt werden.

Variablen welche jedoch innerhalb von Funktionen oder anderen Blöcken definiert werden (dazu zählen auch Parameter), sind nur innerhalb dieser Funktion nutzbar.

```ts
let x: number = 10;
if(true) {
  let y = 20;
  console.log(x + y) // -> 30
}
console.log(x + y) // -> ReferenceError, da y nicht definiert ist
```

Blöcke können zwar nicht nach innen aber dafür nach außen schauen, und alle Variablen, die weiter "außerhalb" definiert wurden nutzen.  
Die Ausnahme zu dieser Regel ist, wenn in einem inneren Block eine Variable mit dem gleichen Namen definiert wurde. Innerhalb der `square` Funktion wird die Variable `n` als Übergabeparameter definiert und blendet damit das globale `n` aus.

```ts
let n: number = 10;

function square(n: number): number {
  n = n * n;
  return n;
}
console.log(square(n)); //-> 100
console.log(n); //-> 10
```

An diesem Beispiel kann man auch sehen, dass Parameter (vom Typ `number`, `string`, oder `boolean`, dazu mehr in der nächsten Woche) unabhängig von den übergebenen Variablen sind. Der Inhalt von dem globalen `n`, welches an die `square` Funktion übergeben wurde, wird in das lokale `n` kopiert, und die Änderungen daran werden nicht auf das globale zurückgeführt.

> _**Weiterführende Informationen**_  
> Funktionen legen bei jedem Aufruf ihren eigenen kleinen lokalen Variablenbereich an, welcher _den Kontext speichert_.
Dadurch, dass diese Verschachtelung beliebig oft wiederholt werden kann, ist es so möglich mehrere Funktionen so zu verschachteln, dass diese den Kontext speichern, was sehr praktisch sein und viel Arbeit ersparen kann, aber auch schwieriger zu verstehen und anzuwenden ist. ⚠️  
> 
> In folgendem Beispiel wird deutlich, dass die `ingredient()` Funktion auf den Parameter `factor` der umliegenden Funktion zugreifen kann, ohne diesen übergeben bekommen zu müssen. 

```ts
function chiliRecipe(factor: number): void {
  ingredient(1, "can", "beans");
  ingredient(1, "piece", "garlic");
  ingredient(2, "tea spoon", "chili");
  ingredient(2, "can", "tomatoes");
  ingredient(100, "gram", "minced meat / tofu");
  
  function ingredient(amount: number, unit: string, name: string){
    let totalAmount: number = amount * factor;
    if (totalAmount > 1){
      unit += "s";
    }
    console.log(`${totalAmount} ${unit} ${name}`);
  }
}

chiliRecipe(3);
```

> Dieses letzte Beispiel nutzt viele Ihnen noch unbekannte Konzepte, illustriert aber die Macht dieser Kontextspeicherung. Kommen Sie darum in den nächsten Wochen hierher zurück wenn Sie diese Konzepte in dem späteren Kapiteln gelernt haben. Bis dahin müssen Sie nur wissen, dass mit diesem Code dafür gesorgt wird, dass jeder Button auf der Webseite eine weiter aufsteigende Zahl auf der Konsole ausgibt.

```ts
// speichert alle Buttons im gesamten HTML Dokument in eine Array ähnliche Struktur
let buttons: HTMLCollectionOf<HTMLButtonElement> = document.getElementsByTagName("button");
// die For schleife geht alle buttons einzeln durch
for (let i: number = 0; i < buttons.length; i++) {
  // fügt jedem Button einen Eventlistener hinzu, welcher bei einem Klick auf den Button die "sayNumber" Funktion ausführt
  buttons[i].addEventListener("click", sayNumber);

  // Die sayNumber Funktion ist innerhalb der for Schleife definiert und speichert diesen Kontext.
  // Dadurch kann sie auf den aktuellen Index i zugreifen, auch lange nachdem der Code durchgelaufen ist.
  // So gibt jeder Button bei einem Klick seine Position im Array aus
  function sayNumber(): void {
    console.log(i);
  }
}
```

### Typescript Dokumentation

[https://www.typescriptlang.org/](https://www.typescriptlang.org/)

---



## **?!** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A-Termin)

Zusammenfassung von: [&lt;username&gt;](https://github.com/)
