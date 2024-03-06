{
  "date": "2019-10-11",
  "keywords": [
"fodg fails",
"fodg faila formātā",
"kas ir fodg fails",
"failu",
"fodg piemērs",
"fodg faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "FODG — OpenDocument zīmēšanas faila formāts",
  "description": "Uzziniet par FODG faila formātu un API, kas var izveidot un atvērt FODG failus.",
  "linktitle": "FODG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-fod-lvg"
}
},
  "lastmod": "2019-09-10"
}

## Kas ir FODG fails?

Fails ar paplašinājumu .fodg ir Apache OpenOffice Drawing faila formāts zīmēšanas elementu glabāšanai. Tā ir balstīta uz faila formāta specifikācijām, kas izklāstītas Strukturālās informācijas standartu uzlabošanai (OASIS). Vēl viens līdzīgs OpenOffice grafikas faila formāts ir [ODG](/image/odg/), kas saglabā zīmēšanas elementus kā vektora attēlu. FODG failus var atvērt, izmantojot OpenOffice, kā arī LibreOffice. Citi OpenOffice atbalstītie failu formāti, piemēram, ietver [ODT](/word-processing/odt/), ODF, [ODP](/presentation/odp/) un [ODS](/spreadsheet/ods/).

## FODG faila formāts

FODG is based on the OpenDocument's XML file format that conforms to OASIS OpenDocument Format ISO/IEC 26300. Tam ir interneta multivides tipa lietojumprogramma/vnd.oasis.opendocument.graphics, kā arī tas atbilst org.oasis-open.opendocument public.composite-content. XML struktūra ir kopīga visiem dokumentu veidiem, piemēram, izklājlapām, zīmējumu failiem un teksta dokumentiem. OpenOffice dokumenti izmanto problēmu nošķiršanas priekšrocības, atdalot saturu, stilus, metadatus un lietojumprogrammu iestatījumus četros atsevišķos XML failos.

`<office:document-content> ` - dokumenta saturs un saturā izmantotie automātiskie stili.
`<office:document-styles> ` — dokumenta saturā izmantotie stili un pašos stilos izmantotie automātiskie stili.
`<office:document-meta>` - Document meta information, such as the author or the time of the last save action.
`<office:document-settings> ` — lietojumprogrammai specifiski iestatījumi, piemēram, loga izmērs vai informācija par printeri.

## Atsauces Nr.
 * [Future Specifications for v 1.3 Standardization ](https://docs.oasis-open.org/office/OpenDocument/v1.3/cs01/OpenDocument-v1.3-cs01.zip)
 * [OASIS Open Document Format for Office Applications](https://www.oasis-open.org/committees/tc_home.php?wg_abbrev=office)
 * [OpenDocument formāts — Wikipedia](https://en.wikipedia.org/wiki/OpenDocument)

