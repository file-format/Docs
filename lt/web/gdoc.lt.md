{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDOC failas – „Google“ dokumentų nuoroda",
  "description": "Sužinokite, kas yra GDOC failas ir API, kurios gali kurti ir atidaryti GDOC failus.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-ltc"
}
},
  "lastmod": "2022-01-23"
}

## Kas yra GDOC failas?

GDOC failas yra sparčiųjų klavišų failas, nukreipiantis į failą, esantį Google diske, debesyje pagrįstoje dokumentų saugojimo tarnyboje. Kai Google disko klientas yra įdiegtas kompiuteryje ir jame sukuriamas dokumentas, diskas sukuria dokumentą internetinėje debesies saugykloje ir įrašo šio dokumento [URL](/web/url/) į GDOC failą vietiniame Google disko aplanke. Dukart spustelėjus šį nuorodos failą, numatytoji žiniatinklio naršyklė atidaro dokumentą iš [URL](/web/url/) vietos. Jei šis sparčiųjų klavišų failas perkeliamas iš šio aplanko, nuoroda į internetinį dokumentą sugenda.

## GDOC failo formatas – daugiau informacijos

GDOC faile yra nuoroda į internetinį dokumentą, parašytą [JSON](/web/json/) failo formatu. Naršyklė, atidaranti GDOC failus, nuskaito URL informaciją ir atidaro susietą dokumentą, kad būtų rodomas, jei vartotojas yra prisijungęs prie šios Google paskyros, kurioje saugomas dokumentas. GDOC failuose nėra dokumento turinio.

### GDOC failo pavyzdys

GDOC failą galima atidaryti teksto rengyklėje, o jo turinys atrodo taip.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Kaip matote, turinys suformatuotas JSON, turintis dokumento URL ir susijusį dokumento ID.

## Nuorodos

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

