{
  "date" : "2021-04-15",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MPG-filformat",
  "keywords" :[ "MPG", "fil", "tillägg", "format", "videoformat","vad är ett mpg-filformat", "mpg-filformat", "mpg-filspelare","mpeg-komprimering", "video ", "MPEG", "MPEG-1", "MPEG-2"],
  "description":"Läs mer om MPG-filformat och API:er som kan skapa och visa hur man öppnar MPG-filer.",
  "linktitle" : "MPG",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-07-26"
}

## Vad är ett MPG-filformat? ##

Filen med filtillägget .mpg tillhör gruppen filtillägg för MPEG-1 eller MPEG-2 ljud- och videokomprimering. MPEG-1 Part 2-video är inte lätt tillgänglig, och denna tillägg (MPG-filformat) pekar vanligtvis på en MPEG-programström som definieras i MPEG-1 och MPEG-2, eller en MPEG-transportström som definieras i MPEG-2 . Andra tillägg som .m2ts finns också som anger den korrekta behållaren, i det här fallet MPEG-2 TS, men detta har liten relevans för MPEG-1-media. [.mp3](https://docs.fileformat.com/audio/mp3/) är det vanligaste tillägget för filer som innehåller MP3-ljud. En MP3-fil är en typisk ström av råljud; det traditionella sättet att tagga MP3-filer är att skriva strömdata till "skräp"-segment av varje bildruta, som sparar medieinformationen men kasseras av **mpg-filspelaren**. Detta är en liknande teknik som används för att tagga AAC-filer, men som stöds mindre nuförtiden.

## MPEG-komprimering ##

Namnet MPEG står för Moving Pictures Experts Group. MPEG är ett verktyg för videokomprimering, vilket innebär komprimering av bilder och ljud, samt synkronisering av de två.
Det finns för närvarande flera MPEG-standarder.

- MPEG-1 föreslås för mellanliggande datahastigheter, i storleksordningen 1,5 Mbit/sek.
- MPEG-2 föreslås för höga datahastigheter på minst 10 Mbit/sek.
- MPEG-3 föreslogs för HDTV-komprimering men befanns vara redundant och slogs samman med MPEG-2.
- MPEG-4 föreslås för mycket låga datahastigheter på mindre än 64 Kbit/sek.


## Programström av MPG-filformat ##

Programströmmen är en behållare för multiplexering av digitalt ljud, video och mer. Programströmningsformatet specificeras i den första delen av MPEG-1 (ISO/IEC 11172-1) och den första delen av MPEG-2, Systems (ISO/IEC-standard 13818-1/ITU-T H.222.0). MPEG-2 Program Stream är analogbaserad och liknar ISO/IEC 11172 Systems lager och framåtkompatibel.

### Kodningsdetaljer ###

Här är kodningsdetaljerna för partiellt MPEG-2 Program Stream-pakethuvudformat:

| Namn | Antal bitar | Beskrivning |
---|---|---|
| synkronisera bytes | 32 | 0x000001BA |
| markörbitar | 2 | 01b för MPEG-2-version. Markörbitarna för MPEG-1-versionen är 4 bitar med värdet 0010b. |
| Systemklocka [32..30] | 3 | System Clock Reference (SCR) bitar 32 till 30 |
| markörbit | 1 | 1 bit alltid inställd. |
| Systemklocka [29..15] | 15 | Systemklockbitar 29 till 15 |
| markörbit | 1 | 1 bit alltid inställd. |
| Systemklocka [14..0] | 15 | Systemklockbitar 14 till 0 |
| markörbit | 1 | 1 bit alltid inställd. |
| SCR-förlängning | 9 | |
| markörbit | 1 | 1 bit alltid inställd. |
| bithastighet | 22 | I enheter om 50 byte per sekund. |
| markörbitar | 2 | 11 bitar alltid inställda. |
| reserverad | 5 | reserverad för framtida bruk |
| fyllningslängd | 3 | |
| fyllningsbytes | 8*fyllningslängd | |
| systemhuvud (valfritt) | 0 eller fler | om systemhuvudets startkod följer: 0x000001BB |

Följande tabell visar det partiella systemhuvudformatet:

| Namn | Antal byte | Beskrivning |
---|---|---|
| synkronisera bytes | 4 | 0x000001BB |
| rubriklängd | 2 | |
| hastighetsbundna och markörbitar | 3 | |
| ljud bunden och flaggor | 1 | |
| flaggor, markörbitar och videobundna | 1 | |
| Pakethastighetsbegränsning och reserverad byte | 1 | |


## Referenser ##

- [MPEG-1 - Wikipedia](https://en.wikipedia.org/wiki/MPEG-1)



