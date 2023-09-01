{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - E-postmeddelande",
  "description":"Läs mer om EML-filformat och API:er som kan skapa och öppna EML-filer.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## Vad är en EML fil?

EML-filformat representerar e-postmeddelanden som sparats med Outlook och andra relevanta applikationer. Nästan alla e-postklienter stöder detta filformat för dess överensstämmelse med RFC-822 Internet Message Format Standard. Microsoft Outlook är standardprogramvaran för att öppna EML-meddelandetyper. EML-filer kan användas för att spara på skiva samt skicka ut till mottagare med hjälp av kommunikationsprotokoll.

## Kort historia av EML

EML-filformatsspecifikationer finns tillgängliga enligt [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Standardformat. Före RFC-822 styrde RFC-733 reglerna för utbyte av nätverksmeddelanden tills 1982, den förra skapades som en förbättring av laterala genom att etablera ARPA-standarder. Samtidigt skapade Microsoft sina egna COM-moduler för utvecklingen av sin egen e-postklient, dvs Outlook Express. RFC-822 tog vägen att etableras som ett proprietärt format när Microsoft avvek från den öppna standarden och skapade [PST](/sv/email/pst/) filformat där e-postmeddelanden sparas i ett mycket strukturerat databasformat. Detta resulterade i problem för användare av icke-Microsofts e-postklienter när e-postmeddelanden vidarebefordrades från Microsoft Outlook.

Det var 2001 när 822-standarden förbättrades till 2822 - Internet Message Format som för närvarande används för att skapa, läsa och skicka EML-meddelanden i MIME RFC-822-format.

## EML-filformatspecifikationer

EML-filer består av två distingerade sektioner:

* Rubriker - Innehåller information om meddelandehuvud
* Meddelandetext - Innehåller en rad information som kan inkludera meddelandeinnehåll, inbäddade bilder och bilagor

### Information om rubriker ###

En EML-fil består av rubrikinformation och eventuellt meddelandetext. Varje rubrikrad i EML har två delar åtskilda av ett kolon ":". Den första heter Header Name och den efter kolon är header body. Sådana rubriker inkluderar till exempel:

* Avsändarens e-postadress
* Mottagarens e-postadress
* Ämnet för e-post
* Tid och datum stämpel för meddelande

**Exempelhuvud**

```
Från:<John@bmw.eml.light.com>

Till:<Andy@fileformat.com>

Datum: tors 8 mars 2018 10:43:37 +0100

Ämne: bmw eml light
```

### Meddelandetext ###

EML meddelandetext innehåller den primära informationen för e-post i form av text, hyperlänkar och bilagor. E-posttexten kan innehålla vanlig läsbar text men det är inte nödvändigt. I det här fallet kan meddelandetexten vara tom eller innehålla kodade bilagor.

Innehållet i meddelandekroppen beskrivs av dess innehållstyp som gör att läsapplikationerna kan läsa informationen i respektive format. Det representerar faktiskt ett dokuments karaktär och format. Strukturen för en MIME-typ eller innehållstyp är mycket enkel; den består av en typ och en undertyp, två strängar, åtskilda av ett '/'. Inget utrymme tillåts. "Typen" representerar kategorin och kan vara en diskret eller en flerdelad typ. "Undertypen" är specifik för varje typ. Listan över typer som faller inom kategorin Content-Type är lång men några viktiga innehållstyper är följande:


|**Typ**|**Beskrivning**|**Exempel på undertyper**
---|---|---|
|text|Representerar format som är läsbart för människor|text/oformaterad, text/html, text/css, text/javascript
|image|Representerar bild av alla typer utom videor|image/bmp, image/png, image/jpg, image/gif
|audio|Representerar alla ljudfilformat|audio/mdi, audio/wav
|application|Representerar alla typer av binär data|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Representation av attachment i EML Body ###

EML-kropp innehåller gränser för varje innehållstyp som den innehåller. Bilaga i meddelandetexten identifieras av dess innehållstyp och innehållsfördelning som visas i följande exempel:

Content-Type: text/plain; teckenuppsättning#"windows-1252"; namn#"apple app store.txt"
Innehåll-Disposition: bilaga; filnamn#"apple app store.txt"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd02

Som kan ses gör Content-Disposition inställd på attachment läsapplikationerna för att få bilagainformation såsom bilagans filnamn och överföringskodningen. Information om bifogad rubrik följs av kodat bilagainnehåll som ska läsas.

#### Exempel på kalkylblad som bilaga ####

Content-Type: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; namn#"english_spodr.xlsx"
Innehåll-Disposition: bilaga; filnamn#"english_spodr.xlsx"
Content-Transfer-Encoding: base64
X-Attachment-Id: f_jkhztmd43

## Referenser

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

