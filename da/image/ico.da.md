{
  "date": "2019-10-11",
  "keywords": [
"ico fil",
"ico filformat",
"hvad er en ico-fil",
"fil",
"ico eksempel",
"ico filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO - Billedfilformat",
  "description": "Lær om ICO-filformat og API'er, der kan oprette og åbne ICO-filer.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-dao"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en ICO fil?

Filer med ICO-udvidelse er billedfiltyper, der bruges som ikon til repræsentation af en applikation på [Microsoft Windows](https://www.microsoft.com/en-us/windows). Disse kommer i forskellige størrelser, farveunderstøttelse og opløsning for at passe til skærmens krav. Et andet lignende billedfilformat på Microsoft Windows er [CUR](/image/cur/) til markørrepræsentation og definerer et hotspot i billedoverskriften. På MacOS tjener ICNS-filformater det samme formål som ICO-filer. Adskillige onlinewebsteder såvel som applikationer giver mulighed for at oprette sådanne filer og konvertere andre billedformater såsom [BMP](/image/bmp/), [PNG](/image/png/) osv. til ikonfilformat. Den officielle IANA-registrerede internetmedietype for ICO-filer er image/vnd.microsoft.icon.

## Kort historie ##

Icons were introduced with the launch of Microsoft Windows 1.0. Disse var 32x32 i størrelse og var monokrome. Med ankomsten til win32 blev understøttelse af ikonbilleder i ægte farver introduceret med op til 256x256 pixels i dimension. Windows XP var den første til at understøtte 32-bit farveikonbilleder, hvilket gjorde det muligt at tilføje semi-transparente områder som skygger, anti-aliasing og glaslignende effekter til ikonet. Microsoft anbefalede kun ikonstørrelser op til 48×48 pixels til Windows XP. Windows Vista tilføjede en 256×256-pixel ikonvisning til Windows Stifinder, samt understøttelse af det komprimerede [PNG](/image/png/)-format. Med brugere, der bruger højere opløsninger og høje DPI-tilstande, anbefales større ikonformater (såsom 256×256).

## ICO-filformat ##

En enkelt ICO-fil består af et eller mere end et lille billede af flere størrelser og farvedybder. Tilstedeværelsen af billeder i flere størrelser er til passende skalering ved forskellige skærmopløsninger. Alle værdier i ICO/CUR-filer er repræsenteret i [little-endian](https://en.wikipedia.org/wiki/Little-endian) byte-rækkefølge.

ICO-filen består af en Icon-header, en Icon Directory,

|Felt|Beskrivelse
---|---|
|Icon Header|Gemmer generel information om ICO-filen.
|Directory[1..n]|Gemmer generel information om hvert billede i filen.
|Ikon #1|De faktiske data for det første billede i gammelt OG/XOR DIB-format eller nyere PNG
|...|
|Ikon #n|Data for det sidste ikonbillede

### Header ###

|Offset|Størrelse (i bytes)|Formål
---|---|---|
|0|2|Reserveret. Skal altid være 0.
|2|2|Specificerer billedtype: 1 for ikonbillede (.ICO), 2 for markørbillede (.CUR). Andre værdier er ugyldige.
|4|2|Specificerer antallet af billeder i filen.

### Directory ###

Mappen indeholdt i en ICO-fil, repræsenteret som ICONDIR-struktur, indeholder en ICONDIRECTORY-struktur for hvert billede i filen. Det samme efterfølges af en sammenhængende blok af alle billedbitmapdata. Dette er som vist nedenfor.

|Offset|Størrelse|Beskrivelse
---|---|---|
|0 (0)|1|Bredde, skal være 0 hvis 256 pixels
|1 (1)|1|Højde, skal være 0 hvis 256 pixels
|2 (2)|1|Farveantal, skal være 0 hvis mere end 256 farver
|3 (3)|1|Reserveret, skal være 0
|4 (4)|2|Farveplaner i .ICO-format skal være 0 eller 1, eller X-hotspot i .CUR-format
|6 (6)|2|Bits pr. pixel i .ICO-format, eller Y-hotspottet i .CUR-format
|8 (8)|4|Størrelse af bitmapdata i bytes.
|12 (C)|4|Offset i filen.

## Referencer ##

* [ICO - Af Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


