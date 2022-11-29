{
  "date" : "2019-10-11",
  "keywords" :[ "txt-fil", "txt-filformat", "vad är en txt-fil", "fil", "txt-exempel", "txt-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TXT - Textdokumentfil",
  "description":"Läs mer om TXT-filformat och API:er som kan skapa och öppna TXT-filer.",
  "linktitle" : "TXT",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## Vad är en TXT fil?

En fil med filtillägget .TXT representerar ett textdokument som innehåller ren text i form av rader. Stycken i ett textdokument känns igen av vagnreturer och används för bättre arrangemang av filinnehållet. Ett standardtextdokument kan öppnas i alla textredigerare eller ordbehandlingsprogram på olika operativsystem. All text som finns i en sådan fil är i läsbart format och representeras av teckensekvenser.

Textfiler kan lagra stora mängder data eftersom det inte finns någon begränsning på storleken på innehållet. Men textredigerare som öppnar så stora filer måste vara smarta för att ladda och visa dessa. Nästan alla operativsystem kommer med textredigerare som låter dig skapa och redigera textfiler. Till exempel kommer Windows OS med Notepad och Wordpad för detta ändamål. På liknande sätt kommer MacOS med TextEdit för att skapa och redigera textdokument. Det finns dock andra gratis textredigerare tillgängliga också över internet som ger dig möjligheten att arbeta med textdokument som Notepad++ som är mycket mer avancerad när det gäller funktionalitet.

## Filformatspecifikationer ##

Textfilformatet har inga speciella filformatspecifikationer. Textfiler har "text/vanlig" MIME-typ och har liten eller ingen formatering alls. Detta gör det möjligt för textredigerare att öppna sådana filer utan några andra krav. Standardteckenuppsättningen för textfiler är ASCII som används för att skapa och visa textfilinnehåll. Tecken kodas med hjälp av ASCII-teckenuppsättning, men detta medför begränsning av användningen av tecken som pundtecken, dollar- och eurotecken som inte kan representeras med hjälp av ASCII-teckenuppsättningen. Således kan textfiler också sparas i Unicode-format, där UTF-8 är det mest använda.

### Windows textfilformat ###

Textfiler på Windows OS består av flera rader där varje rad består av en sekvens av tecken. Varje användares implicerad rad definieras av en kombination av två tecken, dvs. vagnretur (CR) och Line Feed (LF). Windows textfiler kan vara i ANSI, OEM, Unicode eller UTF-8-kodning. UTF-16-kodningen hjälper till att spara information i en textfil som kräver två byte för representation. Sådana filer börjar vanligtvis med Byte Order Mark (BOM) som kommunicerar filinnehållets endianitet. Det bör noteras att andra applikationer på Windows OS kan lagra information i textfilformat men med olika filtillägg för att representera applikationsspecifik text. Till exempel, programmeringsspråk brukar spara kod i textfil men med sina egna tillägg.

### Unix textfilformat ###

Alla sådana system finjusterar en textfil som en fil vars tecken är organiserade i noll eller fler rader. Varje rad är en sekvens av noll eller fler tecken utan nyrad och ett avslutande nyradstecken, normalt LF.

## Referenser ##

* [TXT-filformat](https://en.wikipedia.org/wiki/Text_file)

