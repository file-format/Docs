{
  "date": "2019-10-11",
  "keywords": [
"odp fails",
"odp faila formātā",
"kas ir odp fails",
"failu",
"odp piemērs",
"odp faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODP - OpenOffice prezentācijas faila formāts",
  "description": "Uzziniet par ODP failu formātu un API, kas var izveidot un atvērt ODP failus.",
  "linktitle": "ODP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-od-lvp"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ODP fails?

Faili ar paplašinājumu .odp ir prezentācijas faila formāts, ko OpenOffice.org izmanto OASISOpen standartā. Prezentācijas fails ir slaidu kolekcija, kurā katrs slaids var ietvert tekstu, attēlus, formatējumu, animācijas un citus multivides failus. Šie slaidi tiek prezentēti auditorijai slaidrādes veidā ar pielāgotiem prezentācijas iestatījumiem. ODP failus var atvērt lietojumprogrammās, kas atbilst OpenDocument formātam (piemēram, OpenOffice vai StarOffice).

## Īsa vēsture

ODP faila formāta specifikācijas ir balstītas uz standartu, kas izstrādāts kā ODF specifikācijas. Šīs specifikācijas pagātnē ir attīstījušās trīs OASIS izstrādātu un publicētu versiju veidā:

`2005` — versija 1.0 tika publicēta 2005. gada maijā
2007 — versija 1.1 tika publicēta 2007. gada februārī
`2011` — versija 1.2 tika publicēta 2011. gada septembrī

Pārejot no ODF 1.0 uz 1.1 versijām, bija diezgan nelielas izmaiņas. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ir jaunākā ODF specifikāciju versija, un izstrādātājiem ir jākonsultējas ar to, lai izstrādātu lietojumprogrammas, kas saistītas ar ODS lasīšanu/rakstīšanu.

## Faila formāta specifikācijas

OpenDocument formāts atbalsta dokumentu attēlošanu kā vienu XML dokumentu, kā arī vairāku apakšdokumentu kolekciju pakotnē kā [ZIP](/compression/zip/) arhīvu. Katrs no ZIP arhīva failiem saglabā daļu no visa dokumenta. Katrs apakšdokuments saglabā noteiktu dokumenta aspektu. Piemēram, vienā apakšdokumentā ir informācija par stilu, bet citā apakšdokumentā ir dokumenta saturs. Tipiskam ODF dokumentam ir šādas sastāvdaļas:

* `content.xml` — dokumenta saturs un saturā izmantotie automātiskie stili.

* `styles.xml` — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.

* `meta.xml` — dokumenta metainformācija, piemēram, autors vai pēdējās saglabāšanas darbības laiks.

* `settings.xml` — lietojumprogrammai specifiski iestatījumi, piemēram, loga izmērs vai printera informācija.


Papildus tiem iepakojumā var būt arī daudzi citi apakšdokumenti, piemēram, dokumenta sīktēli, attēli utt.

Izklājlapu dokumentu faili ir ODF failu apakškopa, kurā saturs (lapas) tiek glabāts apakšdokumentā content.xml.

## Atsauces

* [OpenDocument — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


