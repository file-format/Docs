{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GDOC-fil – genväg till Google Dokument",
  "description":"Läs mer om vad en GDOC-fil och API:er är som kan skapa och öppna GDOC-filer.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## Vad är en GDOC fil?

En GDOC-fil är en genvägsfil som pekar på en fil som finns på Google Drive, en molnbaserad dokumentlagringstjänst. När Google Drive-klienten är installerad på en dator och ett dokument skapas inuti den, skapar enheten ett dokument i online-molnlagringen och skriver [URL](/sv/web/url/) för detta dokument i GDOC-filen i lokala Google Drive-mappen. När den här genvägsfilen dubbelklickas öppnar standardwebbläsaren dokumentet från [URL](/sv/web/url/)-platsen. Om den här genvägsfilen flyttas ut från den här mappen bryts länken till onlinedokumentet.

## GDOC-filformat - Mer information

GDOC-filen innehåller genväg till onlinedokumentet skrivet i filformatet [JSON](/sv/web/json/). Webbläsaren som öppnar GDOC-filer läser URL-informationen och öppnar det länkade dokumentet för visning förutsatt att användaren är inloggad på detta Google-konto där dokumentet lagras. GDOC-filer innehåller inte innehållet i dokumentet.

### Exempel på GDOC-fil

GDOC-filen kan öppnas i en textredigerare och dess innehåll ser ut som följande.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Som kan ses är innehållet formaterat i JSON med ett dokuments URL och tillhörande dokument-ID.

## Referenser

* [Google Dokument öppnar inte vare sig gdoc- eller docx-filer](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=sv )

