{
  "date": "2019-10-11",
  "keywords": [
"odt fails",
"odt faila formātā",
"kas ir odt fails",
"failu",
"dīvains piemērs",
"odt faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ODT — OpenDocument teksta fails",
  "description": "Uzziniet par ODT faila formātu un API, kas var izveidot un atvērt ODT failus.",
  "linktitle": "ODT",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-od-lvt"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir ODT fails?

ODT faili ir dokumentu tipi, kas izveidoti ar tekstapstrādes lietojumprogrammām, kuru pamatā ir OpenDocument teksta faila formāts. Tie ir izveidoti ar tekstapstrādes lietojumprogrammām, piemēram, bezmaksas OpenOffice Writer, un var saturēt tādu saturu kā teksts, attēli, objekti un stili. ODT fails Writer tekstapstrādes programmai ir tas pats, kas [DOCX](/word-processing/docx/) ir Microsoft Word. Vairākas lietojumprogrammas, tostarp Google dokumenti un Google tīmekļa tekstapstrādes programma, kas iekļauta Google diskā, var atvērt ODT failus rediģēšanai. Microsoft Word var arī atvērt ODT failus un saglabāt tos citos formātos, piemēram, [DOC](/word-processing/doc/) un DOCX.

## Īsa vēsture ##

ODP faila formāta specifikācijas ir balstītas uz standartu, kas izstrādāts kā ODF specifikācijas. Šīs specifikācijas pagātnē ir attīstījušās trīs OASIS izstrādātu un publicētu versiju veidā:

**2005** 1.0 versija tika publicēta 2005. gada maijā

**2007:** versija 1.1 tika publicēta 2007. gada februārī

**2011:** versija 1.2 tika publicēta 2011. gada septembrī

Pārejot no ODF 1.0 uz 1.1 versijām, bija diezgan nelielas izmaiņas. [ODF 1.2 version](https://www.oasis-open.org/standards#opendocumentv1.2) ir jaunākā ODF specifikāciju versija, un izstrādātājiem ir jākonsultējas ar to, lai izstrādātu lietojumprogrammas, kas saistītas ar ODS lasīšanu/rakstīšanu.

## Faila formāta specifikācijas ##

OpenDocument formāts atbalsta dokumentu attēlošanu kā vienu XML dokumentu, kā arī vairāku apakšdokumentu kolekciju pakotnē kā [ZIP](/compression/zip/) arhīvu. Katrs no ZIP arhīva failiem saglabā daļu no visa dokumenta. Katrs apakšdokuments saglabā noteiktu dokumenta aspektu. Piemēram, vienā apakšdokumentā ir informācija par stilu, bet citā apakšdokumentā ir dokumenta saturs. Tipiskam ODF dokumentam ir šādas sastāvdaļas:

* content.xml — dokumenta saturs un saturā izmantotie automātiskie stili.

* styles.xml — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.

* meta.xml — dokumenta metainformācija, piemēram, autors vai pēdējās saglabāšanas darbības laiks.

* settings.xml — lietojumprogrammas iestatījumi, piemēram, loga izmērs vai printera informācija.


Papildus tiem pakotnē var būt arī daudzi citi apakšdokumenti, piemēram, dokumenta sīktēli, attēli utt. Dokumentu faili ir ODF failu apakškopa, kur saturs (lapas) tiek glabāts //content.xml// apakšdokumentā.

## Atsauces Nr.

* [OpenDocument — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


