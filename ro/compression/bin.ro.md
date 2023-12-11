{
"data":"2023-07-20",
   "keywords":[
"COS",
"Fișier BIN",
"fişier",
"Extensie fișier BIN",
"extensie",
"fişier"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"Format fișier BIN - fișier codificat MacBinary",
   "description":"Aflați despre formatul BIN și despre API-urile care pot crea și deschide fișiere BIN.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## Ce este un fișier BIN?

Un fișier BIN, în contextul computerelor Macintosh, se poate referi la un fișier salvat în formatul MacBinary. MacBinary este un format de fișier special conceput pentru transferul fișierelor Macintosh pe internet, e-mail, FTP sau medii portabile. Scopul MacBinary este de a păstra structura completă a fișierelor și atributele fișierelor Macintosh, inclusiv atât fork-ul de date, cât și fork-ul de resurse, într-un singur fișier.

Formatul MacBinary realizează acest lucru prin încapsularea fork-ului de resurse Macintosh Hierarchical File System (HFS) și a fork-ului de date într-un fișier comprimat. De asemenea, include un antet de căutare care conține metadate importante despre fișier. Combinând toate aceste componente într-un singur fișier, MacBinary se asigură că fișierul își păstrează integritatea și poate fi ușor transferat și partajat pe diferite platforme.

Odată cu progresele în sistemele de fișiere Apple și protocoalele de transfer de fișiere, utilizarea fișierelor BIN și a formatului MacBinary a devenit mai puțin obișnuită. Introducerea formatelor de fișiere precum ZIP și trecerea la sisteme de fișiere mai moderne, cum ar fi HFS+ și APFS, au redus nevoia de fișiere codificate cu MacBinary. Aceste sisteme de fișiere mai noi oferă modalități mai eficiente de gestionare a atributelor fișierelor, a fork-urilor de resurse și a fork-urilor de date, făcând formatul MacBinary mai puțin necesar în peisajul informatic de astăzi.

## Format de fișier BIN - Mai multe informații

În primele zile ale computerelor Macintosh, fișierele erau stocate în două "furcuri" separate din cauza limitărilor de date. "Resource fork" conținea date structurate, în timp ce "data fork" conținea date nestructurate. În timp ce Classic Mac OS a tratat aceste furci ca pe un singur fișier, transferul fișierelor către sisteme non-Mac a dus la pierderi de date, deoarece nu recunoșteau furcile ca o singură entitate. Pentru a rezolva acest lucru, formatul MacBinary a fost creat de persoane precum Dennis Brothers, Harry Chesley și Yves Lempereur. MacBinary a comprimat și combinat fork-urile într-un singur fișier, cunoscut sub numele de fișier BIN, pentru a fi transferat pe sisteme non-Mac. La revenirea la Mac OS, furcile ar fi din nou separate. Odată cu trecerea de la HFS bazat pe furcă în anii 2000, utilizarea formatului MacBinary a scăzut semnificativ. Astăzi, întâlnirea unui fișier BIN codificat în MacBinary este rară, cu excepția cazului în care întâlniți un fișier vechi pe un sistem non-Mac sau descărcați unul de pe internet.

Formatul MacBinary a trecut prin mai multe versiuni de-a lungul timpului pentru a se adapta schimbărilor în sistemele Macintosh și gestionarea fișierelor. Iată câteva dintre diferitele versiuni ale formatului MacBinary:

- **MacBinary I:** Versiunea inițială a MacBinary, introdusă la sfârșitul anilor 1980. Acesta a combinat fork-ul de resurse și fork-ul de date într-un singur fișier binar, permițând transferul pe mai multe platforme de fișiere Macintosh.

- **MacBinary II:** Această versiune, lansată la începutul anilor 1990, a îmbunătățit formatul original MacBinary prin adăugarea de informații suplimentare, cum ar fi tipul fișierului și codurile de creator, la antetul fișierului binar. Aceste coduri au ajutat la menținerea integrității și identificării fișierelor Macintosh în timpul transferului.

- **MacBinary III:** Formatul MacBinary III, introdus la mijlocul anilor 1990, a îmbunătățit și mai mult versiunile anterioare prin includerea de metadate suplimentare, cum ar fi numele fișierului și datele de creare și modificare a fișierului, în antetul fișierului binar. Acest lucru a permis o conservare mai cuprinzătoare a atributelor fișierelor Macintosh în timpul transferului.

- **MacBinary IV:** MacBinary IV a fost dezvoltat pentru a rezolva problemele de compatibilitate cu sistemul de operare Mac OS X în curs de dezvoltare la începutul anilor 2000. A încorporat modificări pentru a se adapta la noua structură a sistemului de fișiere și la atributele introduse în Mac OS X.

## Cum se deschide un fișier BIN?

Fișierele BIN codificate MacBinary pot fi deschise folosind diverse utilitare de compresie. Pentru utilizatorii de macOS, **Apple Archive Utility** este o opțiune potrivită. Utilizatorii Windows pot utiliza software precum **Smith Micro StuffIt Deluxe** pentru a extrage conținutul unui fișier BIN codificat MacBinary. O altă opțiune pentru utilizatorii macOS este **The Unarchiver**, care este un instrument versatil capabil să gestioneze mai multe formate de fișiere, inclusiv MacBinary.

Este important de reținut că extensia de fișier .bin este utilizată de diferite formate de fișiere, nu doar de MacBinary. Prin urmare, dacă întâlniți un fișier BIN care nu poate fi deschis cu utilitarele menționate mai sus, acesta poate fi salvat într-un format diferit. În astfel de cazuri, poate fi necesar să identificați formatul de fișier specific și să utilizați software-ul sau utilitarul adecvat proiectat pentru acel format pentru a accesa conținutul fișierului.

## Alte fișiere BIN

Iată și alte tipuri de fișiere care folosesc extensia de fișier **.bin**.

- [BIN - Fișier imagine disc binar](/ro/disc-and-media/bin/)
- [BIN - Fișier executabil Unix](/ro/executable/bin/)
- [BIN - BlackBerry IT Policy File](/ro/settings/bin/)
- [BIN - Sega Genesis Game ROM](/ro/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/ro/game/bin-pcsx/)

## Referințe

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

