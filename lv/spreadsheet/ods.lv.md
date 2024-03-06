{
  "date": "2019-12-10",
  "keywords": [
"ODS",
"failu",
"pagarinājumu",
"faila formātā",
"OpenDocument izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsu faila formāta ceļvedis, lai uzzinātu, kas ir ODS fails un API, kas tos var izveidot un atvērt.",
  "title": "Kas ir ODS fails? ",
  "linktitle": "ODS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-od-lvs"
}
},
  "lastmod": "2019-12-10"
}

## Kas ir ODS fails?

Faili ar paplašinājumu .ods nozīmē OpenDocument izklājlapas dokumenta formātu, ko lietotājs var rediģēt. Dati tiek glabāti ODF failā rindās un kolonnās. Tas ir uz XML balstīts formāts un ir viens no vairākiem apakštipiem Open Document Formats (ODF) saimē. Formāts ir norādīts kā daļa no ODF 1.2 specifikācijām, ko publicē un uztur OASIS. Vairākas lietojumprogrammas operētājsistēmā Windows, kā arī citas operētājsistēmas var atvērt ODS failus rediģēšanai un manipulācijām, tostarp Microsoft Excel, NeoOffice un LibreOffice. ODS failus dažādās lietojumprogrammās var pārveidot arī citos izklājlapu formātos, kā arī [XLS](/spreadsheet/xls/), [XLSX](/spreadsheet/xlsx/) un citos.

## Īsa vēsture ##

ODS faila formāta specifikācijas ir balstītas uz standartu, kas izstrādāts kā ODF specifikācijas. Šīs specifikācijas pagātnē ir attīstījušās trīs OASIS izstrādātu un publicētu versiju veidā:

`2005` — versija 1.0 tika publicēta 2005. gada maijā

2007 — versija 1.1 tika publicēta 2007. gada februārī

`2011` — versija 1.2 tika publicēta 2011. gada septembrī

Pārejot no ODF 1.0 uz 1.1 versijām, bija diezgan nelielas izmaiņas. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ir jaunākā ODF specifikāciju versija, un izstrādātājiem ir jākonsultējas ar to, lai izstrādātu lietojumprogrammas, kas saistītas ar ODS lasīšanu/rakstīšanu.

## ODS faila formāts ##

OpenDocument formāts atbalsta dokumentu attēlošanu kā vienu XML dokumentu, kā arī vairāku apakšdokumentu kolekciju pakotnē kā [ZIP](/compression/zip/) arhīvu. Katrs no ZIP arhīva failiem saglabā daļu no visa dokumenta. Katrs apakšdokuments saglabā noteiktu dokumenta aspektu. Piemēram, vienā apakšdokumentā ir informācija par stilu, bet citā apakšdokumentā ir dokumenta saturs. Tipiskam ODF dokumentam ir šādas sastāvdaļas:

* `content.xml` — dokumenta saturs un saturā izmantotie automātiskie stili.

* `styles.xml` — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.

* `meta.xml` — dokumenta metainformācija, piemēram, autors vai pēdējās saglabāšanas darbības laiks.

* `settings.xml` — lietojumprogrammai specifiski iestatījumi, piemēram, loga izmērs vai printera informācija.


Papildus tiem iepakojumā var būt arī daudzi citi apakšdokumenti, piemēram, dokumenta sīktēli, attēli utt.

Izklājlapu dokumentu faili ir ODF failu apakškopa, kurā saturs (lapas) tiek glabāts apakšdokumentā content.xml.

## Atsauces Nr.

* [OpenDocument — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


