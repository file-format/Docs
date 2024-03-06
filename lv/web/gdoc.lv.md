{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDOC fails — Google dokumentu saīsne",
  "description": "Uzziniet, kas ir GDOC fails un API, kas var izveidot un atvērt GDOC failus.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-lvc"
}
},
  "lastmod": "2022-01-23"
}

## Kas ir GDOC fails?

GDOC fails ir saīsnes fails, kas norāda uz failu, kas atrodas Google diskā — mākoņa dokumentu krātuves pakalpojumā. Kad Google diska klients ir instalēts datorā un tajā tiek izveidots dokuments, disks izveido dokumentu tiešsaistes mākoņkrātuvē un ieraksta šī dokumenta [URL](/web/url/) GDOC failā vietējā Google diska mapē. Veicot dubultklikšķi uz šī saīsnes faila, noklusējuma tīmekļa pārlūkprogramma atver dokumentu no [URL](/web/url/) atrašanās vietas. Ja šis saīsnes fails tiek pārvietots no šīs mapes, saite uz tiešsaistes dokumentu ir bojāta.

## GDOC faila formāts — vairāk informācijas

GDOC failā ir saīsne uz tiešsaistes dokumentu, kas rakstīts faila formātā [JSON](/web/json/). Pārlūkprogramma, kas atver GDOC failus, nolasa URL informāciju un atver saistīto dokumentu parādīšanai, ja lietotājs ir pieteicies šajā Google kontā, kurā tiek glabāts dokuments. GDOC faili nesatur dokumenta saturu.

### GDOC faila piemērs

GDOC failu var atvērt teksta redaktorā, un tā saturs izskatās šādi.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Kā redzams, saturs ir formatēts JSON formātā ar dokumenta URL un saistītā dokumenta ID.

## Atsauces

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

