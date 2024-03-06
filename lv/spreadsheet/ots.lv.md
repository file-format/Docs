{
  "date": "2019-12-16",
  "keywords": [
"OTS",
"failu",
"pagarinājumu",
"faila formātā",
"Excel",
"Izklājlapa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par OTS failu formātu un API, kas var izveidot un atvērt OTS failus.",
  "title": "OTS — OpenDocument izklājlapas veidnes faila formāts",
  "linktitle": "OTS",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-ot-lvs"
}
},
  "lastmod": "2021-01-19"
}

## Kas ir OTS fails?

Fails ar paplašinājumu .ots ir OpenDocument izklājlapas veidnes fails, kas tiek izveidots ar Calc lietojumprogrammatūru, kas iekļauta Apache OpenOffice. Calc lietojumprogrammatūra ir līdzīga programmai Excel, kas pieejama programmā Microsoft Office. OTS faila formātu izmanto, lai izveidotu veidnes, kurās ir iepriekš noteikti iestatījumi, kas saistīti ar stiliem, fontu, datiem, izklājlapas izkārtojumu un formatējumu. OTF failiem ir mime-type application/vnd.oasis.opendocument.spreadsheet-template”. Šos veidņu failus var izmantot kā sākumpunktu, lai ģenerētu un saglabātu faktiskos datu failus, kas tiek saglabāti [ODS file format](/spreadsheet/ods/). OTS failus var izmantot ar tādām lietojumprogrammām kā OpenOffice un LibreOffice.

## OTS faila formāts

OTS faili tiek saglabāti OASIS OpenDocument XML faila formātā, kas sastāv no vairāku apakšdokumentu kolekcijas ar pakotni kā [ZIP](/compression/zip/) arhīvu. Katrā zip arhīvā tiek glabāta daļa no visa dokumenta, un katrā apakšdokumentā tiek glabāts noteikts dokumenta aspekts. Piemēram, vienā apakšdokumentā ir informācija par stilu, bet citā apakšdokumentā ir dokumenta saturs. Tipiskam ODF dokumentam ir šādas sastāvdaļas:

### OTS Content.xml

Fails content.xml satur faktisko dokumenta saturu. Tomēr tas neietver bināros datus, piemēram, attēlus.
```
<text:h style-name="Heading_2">This is a title</text:h>
<text:p style-name="Text_body"/>
<text:p style-name="Text_body">
   This is a paragraph. The formatting information is
   in the Text_body style. The empty text:p tag above
   is a blank paragraph (an empty line).
</text:p>
```

### Styles.xml OTS faila formātā

Fails styles.xml satur stila informāciju un tiek plaši izmantots formatēšanai un izkārtojumam. Stilu veidi ietver:

 * Rindkopu stili
 * Lapu stili
 * Rakstzīmju stili
 * Rāmju stili
 * Sarakstu stili

### Meta.xml

Fails meta.xml satur informāciju par faila metadatiem, piemēram, autoru, pēdējās modifikācijas datumu utt.
```
<meta:creation-date>2003-09-10T15:31:11</meta:creation-date>
<dc:creator>Daniel Carrera</dc:creator>
<dc:date>2005-06-29T22:02:06</dc:date>
<dc:language>es-ES</dc:language>
<meta:document-statistic
      table-count="6" object-count="0"
      page-count="59" paragraph-count="676"
      image-count="2" word-count="16701"
      character-count="98757"/>
```
### Settings.xml

Failā settings.xml” ir iekļauti dokumenta līmeņa iestatījumi, piemēram, tālummaiņas koeficients un kursora pozīcija.

## Atsauces Nr.

* [OpenDocument 1.2 specifikācija](https://www.oasis-open.org/standards#opendocumentv1.2)

* [OpenDocument — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)


