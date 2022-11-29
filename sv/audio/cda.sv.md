{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "fil", "tillägg", "format", "vad är en cda-fil", "musik", "cda-filformat", "cda filformatspecifikation"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om CDA-filformat och API:er som kan skapa, konvertera och öppna CDA-filer.",
  "title" :"CDA - CD Audio Track Shortcut File",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## Vad är en CDA fil?

En fil med filtillägget .cda är en liten stubbfil som genereras av Microsoft Windows för varje ljudspår på en ljud-CD. Dessa filer innehåller typisk information som spårtider och en Windows-genväg som gör det möjligt för användare att komma åt de specifika ljudspåren. CDA-filerna är inte musik, men de pekar på en musikfil som finns någonstans på lagringen. Vi kan säga det som en genväg till en ljudfil som finns på en CD.

## CDA filformat

CDA-filformatet används för att tala om för en dator vilken ljudfil som ska spelas upp på en CD. Så CDA-filerna blir värdelösa separerade från en CD de representerar. CDA-filerna betraktas vanligtvis som RIFF-resurser. Det finns bara en bit som heter "CDDA" och innehåller bara ett datablock som heter "FMT" i nuvarande version av .cda-filen. Detta block är 24 byte långt. Identifieraren som skapats av Windows används av den Windows 95- och Windows 98-relaterade CD-enheten och dess spelare kan inte ansluta till FreeDB eller CDDB. Så att den kan visa låttitel och artistnamn, som du måste manuellt ange denna information i filen cdplayer.ini.

### Organisering av en CDA-fil

Följande tabell visar information om typiska förskjutningar:
| offset | längd | innehåll |
---|---|---|
| 0x00 | 4 | de 4 ASCII-tecknen "RIFF" |
| 0x04 | 4 | storleken på följande bit: alltid 36 (44 - 8), på 4 byte (Intel order) |
| 0x08 | 4 | chunk-identifierare: de 4 ASCII-tecknen "CDDA" |
| 0x0C | 4 | de 3 ASCII-tecknen "fmt" följt av ett mellanslag |
| 0x10 | 4 | längden på biten: alltid 24, på 4 byte (Intel-ordning) |
| 0x14 | 2 | version av CD-formatet, på 2 byte (Intel order). I maj 2006, alltid lika med 1. |
| 0x016 | 2 | intervallets nummer, på 2 byte (Intel order). Det första spåret har nummer 1. |
| 0x18 | 4 | identifierare som beräknas av Windows för cdplayer.exe. |
| 0x1c | 4 | intervallförskjutning, i antal ramar (Intel-ordning) |
| 0x20 | 4 | spårets varaktighet, totalt antal bilder (Intel order) |
| 0x24 | 1 | räckviddsposition: ramar |
| 0x25 | 1 | räckviddsposition: sekunder |
| 0x26 | 1 | räckviddsposition: minuter |
| 0x27 | 1 | en nollbyte (binärt värde 0) |
| 0x28 | 1 | spårets längd: frames |
| 0x29 | 1 | spårets längd: sekunder |
| 0x2a | 1 | Spårets längd: minuter |
| 0x2b | 1 | en nollbyte (binärt värde 0) |

## Referenser

* [.cda-fil - av Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

