{
  "date": "2022-01-23",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GDOC-fil - Google Docs-genvej",
  "description": "Lær om, hvad en GDOC-fil og API'er er, der kan oprette og åbne GDOC-filer.",
  "linktitle": "GDOC",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-gdo-dac"
}
},
  "lastmod": "2022-01-23"
}

## Hvad er en GDOC fil?

En GDOC-fil er en genvejsfil, der peger på en fil, der er placeret på Google Drev, en sky-baseret dokumentlagringstjeneste. Når Google Drev-klienten er installeret på en computer, og der oprettes et dokument inde i den, opretter drevet et dokument i onlineskylageret og skriver [URL](/web/url/) af dette dokument i GDOC-filen i den lokale Google Drev-mappe. Når der dobbeltklikkes på denne genvejsfil, åbner standardwebbrowseren dokumentet fra [URL](/web/url/)-placeringen. Hvis denne genvejsfil flyttes ud af denne mappe, er linket til onlinedokument brudt.

## GDOC-filformat - flere oplysninger

GDOC-filen indeholder genvej til onlinedokumentet skrevet i filformatet [JSON](/web/json/). Browseren, der åbner GDOC-filer, læser URL-oplysningerne og åbner det linkede dokument til visning, forudsat at brugeren er logget ind på denne Google-konto, hvor dokumentet er gemt. GDOC-filer indeholder ikke indholdet af dokumentet.

### Eksempel på GDOC-fil

GDOC-filen kan åbnes i en teksteditor, og dens indhold ser ud som følgende.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Som det kan ses, er indholdet formateret i JSON med et dokuments URL og det tilhørende dokument-id.

## Referencer

* [Google Docs not opening either gdoc or docx files](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en)

