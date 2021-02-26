## _P_ **3.1** Serveranbindung

### Teilaufgabe 1

Entwickeln Sie mit HTML Formularen eine einfache HTML Seite (z.B. ein Login, eine Addresseingabe, etc.) und lassen sie dieses Formular automatisch auf `https://gis-example.herokuapp.com` über GET verlinken.

Experimentieren Sie mit verschiedenen Input Elementen und den daraus erzeugten Werten. 

Folgen Sie außerdem der Erklärung zur Entwicklung mit NodeJS und setzen Sie sich einen online Server auf. Kopieren Sie als Server Code zunächst den **Code des Beispielservers**. Sonst (bei z.B. einer leeren js Datei) wird ihr Heroku Server ständig die Datei starten und erwarten, dass sie weiterläuft, da sie sich aber direkt beendet (weil es ja nichts auszuführen gibt, bzw nichts gibt was auf irgendetwas anderes wartet), denkt er die Anwendung würde crashen.

## Beispielserver Code:
```ts
import * as Http from "http";

export namespace P_3_1Server {
    console.log("Starting server");
    let port: number = Number(process.env.PORT);
    if (!port)
        port = 8100;

    let server: Http.Server = Http.createServer();
    server.addListener("request", handleRequest);
    server.addListener("listening", handleListen);
    server.listen(port);

    function handleListen(): void {
        console.log("Listening");
    }


    function handleRequest(_request: Http.IncomingMessage, _response: Http.ServerResponse): void {
        console.log("I hear voices!");
        _response.setHeader("content-type", "text/html; charset=utf-8");
        _response.setHeader("Access-Control-Allow-Origin", "*");
        _response.write(_request.url);
        _response.end();
    }
}
```


### Teilaufgabe 2

Schauen Sie sich den **Code des Beispielservers** an, versuchen Sie zu verstehen was passiert und übernehmen Sie ihn in Ihr Repository. Kommentieren Sie sich die einzelnen Zeilen und beschreiben Sie, was was tut. Passen Sie den Request Handler so an, dass der query/path string nicht nur auf der Webseite, sondern auch in der Konsole des Servers ausgegeben wird.

Passen Sie ihre Formularseite aus Teilaufgabe 1 so an, dass sie statt automatisch über die eingebaute GET Anfrage des Formulars den Versand und Empfang der Daten über FormData selbst abwickeln. Verwenden Sie `fetch` um die Anfrage asynchron an den Server zu schicken und dann z.B. in der Konsole die Antwort des Servers auszugeben.

Entwickeln Sie dazu zunächst auf Ihrem lokalen Node Server, und ändern Sie vor der Abgabe dann den Link auf ihre Heroku App.

> **Hinweis**: Heroku schaltet seine gratis Server nach einigen Minuten ohne Anfragen aus und startet sie neu sobald eine Anfrage rein kommt. Darum kann es manchmal einige (10-15) Sekunden dauern, bevor die erste Antwort von Heroku geliefert wird.
