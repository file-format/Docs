{
  "date": "2021-09-06",
  "keywords": [
"btr",
"pagarinājumu",
"failu",
"faila formātā",
"Datu bāzes faila tips",
"Datu bāzes faila formāts",
"Btrieve datu bāze"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par BTR faila formātu un API, kas var izveidot un atvērt BTR failus.",
  "title": "BTR — Btrieve datu bāzes fails",
  "linktitle": "BTR",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-bt-lvr"
}
},
  "lastmod": "2021-09-06"
}

## Kas ir BTR fails?

Fails ar paplašinājumu .btr ir datu bāzes fails, ko izveidojis [Btrieve](https://www.actian.com/) darījumu datu bāzes lietojumprogramma. Atšķirībā no relāciju datu bāzes pārvaldības sistēmām (RBMS), Btrieve pamatā ir indeksētās secīgās piekļuves metode (ISAM), kas ir datu glabāšanas veids ātrai izguvei. BTR fails saglabā ierakstu kolekciju un tiek izmantots, lai ģenerētu pārskatus atbilstoši prasībām. BTR failus var atvērt, izmantojot Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility un Legend Software BTRIEVE Viewer.

## BTR faila struktūra — vairāk informācijas

Iekšējā datu struktūra un katra baita līdzinājums BTR faila struktūrā nav publiski pieejams. Tomēr Btrieve
provides the [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) that can be used to read the information from BTR files.  It is compatible with the following programming languages and development environments.

 * Embarcadero C/C++
 * Embarcadero Delphi
 * GNU C/C++
 * Mikrofokuss COBOL
 * Microsoft Visual Basic
 * Microsoft Visual C++
 * Watcom C/C++

Datu izgūšana no BTR faila ir atkarīga no ar to saistītā DDF faila. Bez DDF nebūs viegli izgūt informāciju no šāda faila.

## Atsauces

* [Btrieve — Wikipedia](https://en.wikipedia.org/wiki/Btrieve)

* [Introduction to Btreive APIs](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

