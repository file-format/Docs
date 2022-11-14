{
  "date" : "2021-09-06",
  "keywords" :[ "btr", "extensie", "bestand", "bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "Btrieve Database"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over BTR-bestandsindeling en API's die BTR-bestanden kunnen maken en openen.",
  "title" :"BTR - Btrieve-databasebestand",
  "linktitle" : "BTR",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-09-06"
}

## Wat is een BTR-bestand?

Een bestand met de extensie .btr is een databasebestand gemaakt door [Btrieve](https://www.actian.com/) transactionele databasetoepassing. In tegenstelling tot relationele databasebeheersystemen (RBMS), is Btrieve gebaseerd op de Indexed Sequential Access Method (ISAM), een manier om gegevens op te slaan zodat ze snel kunnen worden opgehaald. Het BTR-bestand slaat een verzameling records op en wordt gebruikt om rapporten te genereren volgens de vereisten. BTR-bestanden kunnen worden geopend met Pervasive Btrieve Database Manager, Pervasive PSQL Maintenance Utility en Legend Software BTRIEVE Viewer.

## BTR-bestandsstructuur - Meer informatie

De interne gegevensstructuur en uitlijning van elke byte in de structuur van een BTR-bestand is niet openbaar beschikbaar. Echter, Btrieve
biedt de [Btrieve API](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm) die kan worden gebruikt om de informatie uit BTR-bestanden te lezen. Het is compatibel met de volgende programmeertalen en ontwikkelomgevingen.

* Embarcadero C/C++
* Embarcadero Delphi
* GNU C/C++
* Microfocus COBOL
*Microsoft Visual Basic
* Microsoft Visual C++
* Watcom C/C++

Het ophalen van gegevens uit een BTR-bestand is afhankelijk van het bijbehorende DDF-bestand. Zonder de DDF is het niet eenvoudig om de informatie uit zo'n bestand te halen.

## Referenties

* [Btrieve - Wikipedia](https://en.wikipedia.org/wiki/Btrieve)
* [Inleiding tot Btreive API's](https://docs.actian.com/psql/PSQLv13/index.html#page/btrieveapi%2Fbtrintro.htm)

