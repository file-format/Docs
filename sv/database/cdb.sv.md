{
  "date" : "2021-06-16",
  "keywords" :[ "CDB", "tillägg", "cdb-fil", "cdb-filformat", "Databasfiltyp", "Databasfilformat", "vad är en cdb-fil" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om CDB-filformat och API:er som kan skapa och öppna CDB-filer.",
  "title" :"CDB - konstant databasfil",
  "linktitle" : "CDB",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-16"
}

## Vad är en CDB fil?
CDB-filerna används i verksamhetskritiska applikationer som e-post. CDB står för "konstant databas", ett snabbt, pålitligt och enkelt paket för att skapa eller läsa konstanta databaser. Databasersättning är säker mot systemkrascher. Användare behöver inte pausa under en omskrivning. CDB fungerar som en associativ array (på disk), mappar nycklar till värden och gör att flera värden kan lagras i en enda nyckel.

## CDB filformat
CDB-filformatet lagrar tal, förskjutningar, längder och hashvärden i little endian-format som osignerade 32-bitars heltal. Nycklar och data tros vara ogenomskinliga bytesträngar utan någon speciell behandling. I början av databasen representerar rubriken med fast storlek 256 hashtabeller genom att lista deras position i filen och deras längd i luckor. Vanligtvis lagras data som en sekvens av poster, varje post lagrar nyckellängd, datalängd, nyckel och data. Det finns inga regler för sortering eller anpassning. Posterna följs av en uppsättning av 256 hashtabeller av varierande längd. Eftersom noll är en giltig längd, kan det finnas färre än 256 hashtabeller fysiskt lagrade i databasen, men det anses inte vara 256 tabeller. Hashtabeller består av en serie slots, som var och en innehåller ett hashvärde och en postoffset. "Empty slots" har en offset på noll.

### Struktur
CDB-databasen består av en hel datauppsättning i en enda datorfil. Den innehåller tre delar:
- En rubrik med fast storlek
- Data
- En uppsättning hashtabeller.

Uppslagningar är endast tillgängliga för exakta nycklar. Uppslagningar fungerar med hjälp av följande algoritm:

- Haha nyckeln.
- Bestäm vid vilket hashbord och slot denna post ska placeras.
- Testa den angivna luckan i hashtabellen.

För uppslagningar av nycklar med mer än ett värde kan ytterligare värden hittas genom att helt enkelt återuppta sökningen vid nästa lucka.

#### Funktioner

CDB databasstruktur ger flera funktioner:

##### Snabba uppslagningar
En lyckad uppslagning i en enorm databas tar normalt bara två diskåtkomster och en misslyckad uppslagning tar bara en.
##### Låg overhead
En databas använder 2048 byte, 24 byte per post och utrymme för nycklar och data.
##### Inga slumpmässiga gränser
CDB kan hantera vilken databas som helst på upp till 4 gigabyte. Eftersom det inte finns några andra begränsningar behöver posterna inte ens passa in i minnet. Databaser lagras i ett maskinoberoende format.
##### Snabb ersättning av atomdatabaser
Kommandot **cdbmake** kan skriva om en hel databas i två storleksordningar, snabbare än andra hashpaket.
##### Snabba databasdumpar
**cdbdump** kan skriva ut innehållet i en databas i cdbmake-kompatibelt format.


## Referenser ##

* [cdb (programvara) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [CDB-specifikation](http://cr.yp.to/cdb.html)

