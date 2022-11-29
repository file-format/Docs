{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "tillägg", "dbf-fil", "dbf-filformat", "Databasfiltyp", "Databasfilformat", "vad är en dbf-fil", "dBASE" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om DBF-filformat och API:er som kan skapa och öppna DBF-filer.",
  "title" :"DBF - dBase Database File",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Vad är DBF fil?
Filen med tillägget .dbf är en databasfil som används av en databashanteringssystemapplikation som heter **dBASE**. Ursprungligen namngavs dBASE-databasen som Project Vulcan; startade av **Wayne Ratliff** 1978. DBF-filtypen introducerades med dBASE II 1983. Den arrangerar flera dataposter med fält av Array-typ. Databasprogramvaran **xBase** som är pupulär på grund av dess kompatibilitet med ett brett utbud av filformat; stöder även DBF-filer.

## DBF filformat
DBF-filformatet tillhör dBASE-databashanteringssystemet men det kan vara kompatibelt med xBase eller andra DBMS-program. Den ursprungliga versionen av dbf-filen bestod av en enkel tabell som kunde ha data tillagd, modifierad, raderad eller utskriven med hjälp av ASCII-teckenuppsättningen. Med tiden förbättrades .dbf och ytterligare filer lades till för att utöka funktionerna och kapaciteten i databassystemet.

I modern dBASE består en DBF-fil av en rubrik, dataposterna och EOF-markören (End of File)

- Rubriken innehåller information om filen, såsom antalet poster och antalet typer av fält som används i posterna.
- Dokumenten innehåller de faktiska uppgifterna.
- Slutet på filen markeras med en enda byte, med värdet 0x1A.

### Filhuvud
Layouten av filhuvudet i dBase ges i följande tabell:

| Byte | Innehåll | Betydelse |
---|---|---|
| 0 | 1 byte | Giltig dBASE för DOS-fil; bitar 0–2 indikerar versionsnummer, bit 3 indikerar närvaron av en dBASE för DOS-memofil, bitar 4–6 indikerar närvaron av en SQL-tabell, bit 7 indikerar närvaron av en memofil (antingen dBASE m PLUS eller dBASE för DOS) |
| 1–3 | 3 byte | Datum för senaste uppdatering; formaterad som ÅÅMMDD |
| 4–7 | 32-bitars nummer | Antal poster i databasfilen |
| 8–9 | 16-bitars nummer | Antal byte i rubriken |
| 10–11 | 16-bitars nummer | Antal byte i posten |
| 12–13 | 2 byte | Reserverad; fyll med 0 |
| 14 | 1 byte | Flagga som indikerar ofullständig transaktion[not 1] |
| 15 | 1 byte | Krypteringsflagga[not 2] |
| 16–27 | 12 byte | Reserverad för dBASE för DOS i en fleranvändarmiljö |
| 28 | 1 byte | Produktions .mdx-filflagga; 1 om det finns en produktions-.mdx-fil, 0 om inte |
| 29 | 1 byte | Språkdrivrutin-ID |
| 30–31 | 2 byte | Reserverad; fyll med 0 |
| 32–n [not 3][not 4] | 32 byte vardera | array av fältdeskriptorer (se nedan för layout av deskriptorer) |
| n + 1 | 1 byte | 0x0D som fältdeskriptorarrayterminator |

- ISMARKEDO-funktionen kontrollerar denna flagga (BEGIN TRANSACTION sätter den till 1, END TRANSACTION och ROLLBACK återställer den till 0).
- Om denna flagga är inställd på 1 visas meddelandet Databas krypterad.
- Det maximala antalet fält är 255.
- n betyder den sista byten i fältdeskriptormatrisen.

### Fältbeskrivningsmatris
Layout av fältbeskrivningar i dBASE:

| Byte | Innehåll | Betydelse |
---|---|---|
| 0–10 | 11 byte | Fältnamn i ASCII (nollfyllt) |
| 11 | 1 byte | Fälttyp. Tillåtna värden: C, D, F, L, M eller N (se nästa tabell för betydelser) |
| 12–15 | 4 byte | Reserverad |
| 16 | 1 byte | Fältlängd i binär (max 254 (0xFE)). |
| 17 | 1 byte | Fältdecimalantal i binär |
| 18–19 | 2 byte | Arbetsområdes-ID |
| 20 | 1 byte | Exempel |
| 21–30 | 10 byte | Reserverad |
| 31 | 1 byte | Produktions MDX-fältflagga; 1 om fältet har en indextagg i produktions-MDX-filen, 0 om inte |

### Databasposter
Varje post börjar med en raderingsflagga (1-byte). Fält lindas in i poster utan fältavgränsare. All fältdata är ASCII. Beroende på fältets typ medför applikationen ytterligare begränsningar. Här är fälttyper i dBase:

| Fälttyp | Mnemonisk | Vad den accepterar |
-------|-----|----|
| C | Karaktär | Valfri ASCII-text (utfylld med mellanslag upp till fältets längd) |
| D | Datum | Siffror och ett tecken för att separera månad, dag och år (lagras internt som 8 siffror i formatet ÅÅÅÅMMDD) |
| F | Flytpunkt | -, ., 0–9 (högerjusterad, utfylld med blanksteg) |
| L | Logisk | Y, y, N, n, T, t, F, f eller ? (när oinitierad) |
| M | Memo | Valfri ASCII-text (lagrad internt som 10 siffror som representerar ett .dbt-blocknummer, högerjusterad, utfylld med blanksteg) |
| N | Numerisk | -, ., 0–9 (högerjusterad, utfylld med blanksteg) |









## Referenser ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

