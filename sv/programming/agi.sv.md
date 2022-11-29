{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AGI-fil - Asterisk Gateway Interface File Format",
  "description":"Läs mer om vad AGI-filformat är med exempel och API:er som kan skapa och öppna AGI-filer.",
  "linktitle" : "AGI",
  "menu" : {
    "docs" : {
      "identifier": "programming-agi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Vad är AGI fil?

En AGI-fil är en skriptfil som används av telefonisystemet med öppen källkod, Asterisk. Den innehåller information som kan användas för att automatisera processer och Asterisk uppringningsplan. Med hjälp av AGI-skriptfiler kan anslutningar upprättas med relationsdatabaser som PostgreSQL eller MySQL. Dessutom kan AGI-skript användas för att komma åt andra externa resurser också. AGI-skript kan överföra kontrollen av uppringningsplanen till ett externt AGI-skript, vilket gör att Asterisk kan utföra komplexa uppgifter.

## AGI-filformat - Mer information

AGI-skriptfiler sparas som textfiler och kan öppnas i valfri textredigerare för att göra ändringar.

### Standardmönster för AGI-kommunikation

AGI-skriptet laddar variablerna och deras värden som skickas till det av Asterisk. Ett vanligt utseende på dessa variabler är följande.

```
agi_request: test.py
agi_channel: Zap/1-1
agi_language: en
agi_callerid:
agi_context: default
agi_extension: 123
agi_priority: 2
```

Dessa variabler följs av en tom rad som skickas av Asterisk, vilket visar att AGI-skriptet kan ta kontroll över uppringningsplanen nu.

### Programmeringsspråk för AGI-skriptfiler

AGI-skript kan vanligtvis skrivas i Perl, [PHP](/sv/programming/php/), [C](/sv/programming/c/), Pascal eller Bourne Shell.

## Referenser

* [Asterisk AGI-skript](https://www.oreilly.com/library/view/asterisk-the-future/9780596510480/ch09.html)

