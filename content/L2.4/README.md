## _V_ **2.4** JSON und Local Storage

### Inhaltsverzeichnis
- [JSON](#json)
- [Lokaler Speicher](#lokaler-speicher)
  - [Cookies](#cookies)
  - [Local Storage](#local-storage)
  - [Session Storage](#session-storage)
- [Q&A](#-fragen-und-antworten)


### JSON

JSON (Java Script Object Notation) ist eine Syntax um Daten speichern und austauschen zu können und wurde ursprünglich für JavaScript entwickelt, aber wird von vielen anderen Sprachen ebenfalls benutzt. JSON ist ein mit JavaScript-Objektnotation geschrieber Text. JSON ist ein Datenformat in dem Daten für Menschen les- und veränderbar abgespeichert weden.

- JSON steht für JavaScript-Objektnotation
- JSON ist leicht zu lesen/verstehen
- JSON ist sprachübergreifend

#### Daten austauschen
Die Daten in JSON liegen in Textform vor, und es kann jedes TS/JavaScript-Objekt in JSON konvertiert und aus JSON geladen werden. JSON kann auch an und von einem Server gesendet werden. Es kann jedes beliebige vom Server empfangene JSON in TS/JavaScript-Objekte umgewandelt werden.

Auf diese Weise kann komfotabel mit den Daten als TS/JavaScript-Objekte gearbeitet werden.


#### Daten speichern
Wenn Sie Daten in einem TS/JS-Objekt gespeichert haben, können Sie das Objekt in einen JSON string konvertieren:

```ts
let myObj: Person = {name: "John", age: 31, city: "New York"};
let myJSON: string = JSON.stringify(myObj);
console.log(myJSON); // '{"name":"John", "age": 31, "city": "New York"}'
```

#### Einlesen von Daten
Wenn Sie Daten im JSON-Format erhalten, können Sie diese in ein TS/JS-Objekt konvertieren:

```ts
let myJSON: string = '{"name": "John", "age": 31, "city": "New York"}';
let myObj: Person = JSON.parse(myJSON);
document.getElementById("demo").innerHTML = myObj.name;
```

> JSON ist ein reines Datenformat, das heißt, dass Methoden / Funktionen darin nicht gespeichert werden können!  
> Sollen also Klassen in JSON gespeichert / geladen werden, so müssen einige Extraschritte unternommen werden, indem man die konvertieren Daten z.B. an einen Konstruktor übergibt.

```ts
interface PersonInterface {...}
class Person {...}

let myJSON: string = '{"name": "John", "age": 31, "city": "New York"}';
let myObj: PersonInterface = JSON.parse(myJSON);
let myPerson: Person = new Person(myObj.name, myObj.age, myObj.city);
```

### Lokaler Speicher

Oftmals ist es sinnvoll, kleine Datenschnipsel lokal auf dem Gerät des Anwenders zu speichern. Dazu stehen uns drei verschiedene Optionen zur Verfügung.

#### Cookies
Cookies sind spätestens seit der DSGVO in aller Munde. Sie werden in Key-Value (Schlüssel-Werte) Paaren im Browser gespeichert Und "gehören" zu einer bestimmten Adresse. Wenn ein Browser dann eine Seite anfragt, werden die Cookies automatisch mitgeschickt, so kann der server die nötigen Daten entgegen nehmen um sich an den Nutzer zu "erinnern".

```ts
document.cookie = "username=Max Mustermann";
```

Standardmäßig werden Cookies wieder gelöscht, sobald der Browser geschlossen wird. Um dies zu ändern, kann dem Cookie ein "Ablaufdatum" gegeben werden, nach welchem es automatisch gelöscht wird (in UTC Zeit).

```ts
document.cookie = "username=Max Mustermann; expires=Fri, 18 Dec 2020 12:00:00 UTC"; 
```

Außerdem ist ein Cookie stets der aktuellen (Unter-) Seite zugeordnet. Auch das kann durch ein Attribut angepasst werden. Ein Cookie funktioniert ähnlich wie eine lokale Variable: Von weiter außen kann darauf nicht zugegriffen werden, aber tiefer innerhalb der Seitenstruktur schon.

Ein cookie, welcher in `example.com/subpage` gespeichert wurde, kann von `example.com/subpage/subsubpage` ausgelesen werden, aber nicht von `example.com/` und nicht von `example.com/differntpage`.

```ts
document.cookie = "username=Max Mustermann; expires=Fri, 18 Dec 2020 12:00:00 UTC; path=/";
```

Über `document.cookie` können alle von der aktuellen Seite erreichbaren Cookies wieder ausgelesen werden. Dabei werden alle gesetzen Cookies in einem langen String, getrennt durch `;` zurück gegeben.

```ts
let c: string = document.cookie;
```

Da Cookies immer mit der Anfrage an einen Server mitgeschickt werden, haben alle Cookies einer Seite eine gemeinsame Maximalgröße von **4000 bytes**. Außerdem können nicht mehr als 20 Cookies pro Seite gespeichert werden.

Diese ganzen Konzepte machen Cookies zwar praktisch wegen der automatischen Löschung, aber sehr umständlich zu setzen und auszulesen. Auch darum wurden in den letzten Jahren weitere Lösungen entwickelt.

[Weitere Informationen und Beispielimplementationen von benötigten Funktionen nur Nutzung von Cookies](https://www.w3schools.com/js/js_cookies.asp).

#### Local Storage

Local Storage ermöglicht es, Key-Value Paare lokal im Cache (Zwischenspeicher) des Browsers zu speichern (ist also effektiv ein Art assoziatives Array). So können Daten über meherere Seiten einer Website hinweg einfach zwischengespeichert und wieder eingeladen werden. Die Verwendung von Local Storage ist einfacher als die Verwendung von Cookies, hat aber keine automatische Löschung.

Auch hier können nur strings gespeichert werden. Sollen komplexere Daten gespeichert werden, so müssen diese zunächst in einen String konvertiert werden. Glücklicherweise steht uns dazu JSON zur Verfügung.

> **Hinweis**: Wenn Sie localStorage nutzen wollen, muss beim Testen die HTML Datei über einen Liveserver ([VSCode Liveserver Plugin](https://marketplace.visualstudio.com/items?itemName=ritwickdey.LiveServer)) ausgeführt werden, da der LocalStorage sonst beim Seitenwechsel von einer lokalen Datei zu einer anderen sich selbst wieder löscht.

##### Beispiel

```ts
// Wert Speichern
localStorage.setItem("lastname", "Smith");
// Wert Laden
console.log(localStorage.getItem("lastname"));
```

##### Daten wieder aus den LocalStorage löschen

```ts
localStorage.removeItem("lastname");
```

##### Noch ein Beispiel

HTML Teil:

```html
<p><button onclick="clickCounter()" type="button">Klick mich!</button></p>
<div id="result"></div>
<p>Klick auf den Button und der Zähler wird erhöht.</p>
<p>Wenn du die Seite schließt und wieder öffnest ist der Counter nicht zurückgesetzt</p>
```

TypeScript Teil:

```ts
function clickCounter() {
  if (localStorage.clickcount) {
    localStorage.clickcount = Number(localStorage.clickcount)+1;
  } else {
    localStorage.clickcount = 1;
  }
  (<HTMLElement>document.getElementById("result")).innerHTML = "Du hast den Button " + localStorage.clickcount + " mal geklickt.";
}
```

_(localStorage ist eigentlich überall verwendbar, s. [CanIUse](https://caniuse.com/#feat=mdn-api_window_localstorage), aber auch hier sollte man eine Fallbacklösung haben wenn man eine "richtige" Webseite entwickelt, und wenn es nur ein "Sorry, Ihr Browser ist zu alt" Nachricht ist.)_

#### Session Storage

Funktioniert bis auf einen Unterschied genau wie der LocalStorage:  
In `localStorage` gespeicherte Daten besitzen kein Verfallsdatum, während sie im `sessionStorage` mit Ablauf der Sitzung gelöscht werden. Eine Sitzung endet erst mit dem Schließen des Browsers, sie übersteht das Neuladen und Wiederherstellen einer Webseite. Das Öffnen einer Webseite in einem neuen Tab oder Browserfenster erzeugt jedoch eine neue Sitzung.

## **?!** Fragen und Antworten

(die Publikation der Zusammenfassung erfolgt nach dem Q&A-Termin)

Zusammenfassung von: [&lt;username&gt;](https://github.com/)
