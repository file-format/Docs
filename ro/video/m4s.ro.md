{
  "date" : "2022-07-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fișier M4S - Ce este un fișier M4S?",
  "description":"Aflați despre formatul de fișier M4S și despre API-urile care pot crea și deschide fișiere M4S.",
  "linktitle" : "M4S",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-18"
}

## Ce este un fișier M4S?

Un fișier M4S este un segment mic al unui videoclip care este transmis în flux pe internet folosind tehnica de streaming **MPEG-DASH**. Conține un segment video sub formă de date binare. Aplicația de recepție (de obicei un browser web sau playere media) redă aceste segmente în ordinea în care sunt primite. Primul segment M4S este identificat prin datele de inițializare pe care le conține. În **rezumat**, fișierele M4S sunt mici segmente media individuale ale unui fișier complet.

## Format de fișier M4S

Fișierele M4S se bazează pe [formatul ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Aceste segmente mici ale unui fișier mare pot fi descărcate independent prin HTTP. Astfel, dacă aveți un fișier de film [MP4](/ro/video/mp4/) mare, acesta poate fi transmis în flux folosind tehnica MPEG-DASH (Dynamic Adaptive Streaming over HTTP) prin segmentarea acestuia ca fișiere cu segment M4S. Dacă acest fișier de film mare este descărcat pe disc ca M4S, sunt descărcate mai multe fișiere M4S. Dacă toate aceste segmente .m4s sunt concatenate, este produs un fișier complet redabil. Playerele media nu pot reda fișierul decât dacă primul segment de inițializare este disponibil și cu fișierul.

## Despre MPEG-DASH Streaming

MPEG-DASH folosește tehnica de streaming adaptive bitrate care face posibilă transmiterea în flux a conținutului media de înaltă calitate pe internet. Acest lucru se realizează prin împărțirea conținutului într-o secvență de segmente mici care sunt transmise în flux prin HTTP. Fișierele media mari, cum ar fi filmul, podcasturile sau transmisia în direct a unui eveniment sportiv pot fi transmise în flux în acest fel. Aceste segmente sunt codificate la rate de biți diferite. Playerele media compatibile MPEG-DASH selectează automat segmentul cu cea mai mare rată de biți folosind un algoritm de adaptare a ratei de biți. Acest lucru evită blocarea sau re-bufferizarea evenimentelor în redare.

### API Open-Source pentru fișierele M4S

Există API-uri open source disponibile care pot fi folosite pentru a citi și converti fișiere M4S.

* [libdash](https://github.com/bitmovin/libdash) - .NET API pentru fișiere M4S
* [dash.js](https://github.com/Dash-Industry-Forum/dash.js) - client Javascript pentru fișierul M4S
* [Go Library pentru a crea fișiere Dash](https://github.com/zencoder/go-dash)

### API open-source pentru a converti M4S în MP4

* [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Referințe ###

* [Format ISO Base Media File (ISOBMFF)](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)
* [Dynamic Adaptive Streaming over HTTP - MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)

