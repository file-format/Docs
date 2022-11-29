{
  "date" : "2019-12-12",
  "keywords" :[ "SQLite", "tillägg", "fil", "filformat", "Databasfiltyp", "Databasfilformat", "Databasfiler" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om SQLITE-filformat och API:er som kan skapa och öppna SQLITE-filer.",
  "title" :"SQLite-filformat",
  "linktitle" : "SQLITE",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2020-11-09"
}

## Vad är en SQLite-fil?

En fil med tillägget .sqlite är en lättviktig SQL-databasfil som skapats med programvaran [SQLite](https://www.sqlite.org/index.html). Det är en databas i själva filen och implementerar en fristående, fullfjädrad, mycket pålitlig [SQL](/sv/database/sql/) databasmotor. SQLite-databasfiler kan användas för att dela rikt innehåll mellan system genom att enkelt utbyta dessa filer över nätverket. Nästan alla mobiler och datorer använder SQLite för lagring och delning av data, och är valet av filformat för plattformsoberoende applikationer. På grund av dess kompakta användning och enkla användbarhet levereras den med i andra applikationer. SQLite-bindningar finns för programmeringsspråk som C, [C#](/sv/programmering/cs), [C++](/sv/programmering/cpp), [Java](/sv/programmering/java/), [PHP](/sv/programmering/php/ ), och många andra.

## SQLite filformat

SQLite är i verkligheten ett C-Language-bibliotek som implementerar SQLite RDBMS med hjälp av SQLite-filformatet. Med utvecklingen av nya enheter varje dag, har filformatet hållits bakåtkompatibelt för att rymma äldre enheter. SQLite-filformat ses som ett långsiktigt arkivformat för data.

### Databasfilen

En SQLite-databas underhålls fullt ut via två filer.
* Huvuddatabasfil - Innehåller komplett tillstånd för SQLite-databasen
* Återställ journal - Lagrar ytterligare information i en andra fil och används under utförandet av transaktioner. Om SQLite är i WAL-läge, upprätthålls en skrivhuvudsloggfil.

#### Journalfil

Den här filen är avsedd att behålla all information om den senaste transaktionen inte kunde slutföras i fall som en datorkrasch. Denna fil används för att återställa databasfilen till ett konsekvent tillstånd.

#### Sidor

Den huvudsakliga SQLite-databasfilen består av en eller flera sidor. När som helst har varje sida i huvuddatabasen en enda användning som är något av följande:

* Lås-byte-sidan
* En freelistsida
* En frilista stamsida
* En frilista bladsida
* En b-trädsida
* En tabell b-träd inredningssida
* En tabell b-träd blad sida
* En index b-tree interiörsida
* En indexb-trädbladssida
* En överflödessida för nyttolast
* En pekare kartsida

Storleken på SQLite-databasfiler kan variera från några kilobyte till några få gigabyte.

### SQLite Header

SQLite-databashuvudet finns i de första 100 byten i databasfilen. Varje giltig SQLite-databasfil börjar med 16 byte (i hexadecimal):53 51 4c 69 74 65 20 66 6f 72 6d 61 74 20 33 00. Information om rubrikfälten är som i följande tabell.

|Offset|Storlek|Beskrivning|
---|---|---|
|0|16|Rubriksträngen: "SQLite format 3\000"|
|16|2|Databasens sidstorlek i byte. Måste vara en potens av två mellan 512 och 32768 inklusive, eller värdet 1 representerar en sidstorlek på 65536.|
|18|1|Skrivversion för filformat. 1 för arv; 2 för WAL.|
|19|1|Läs version av filformat. 1 för arv; 2 för WAL.|
|20|1|Byte av oanvänt "reserverat" utrymme i slutet av varje sida. Vanligtvis 0.|
|21|1|Maximal inbäddad nyttolastandel. Måste vara 64.|
|22|1|Minsta andel av inbäddad nyttolast. Måste vara 32.|
|23|1|Lövnyttolastfraktion. Måste vara 32.|
|24|4|Räknare för filändring.|
|28|4|Storlek på databasfilen i sidor. "In-header databasstorlek".|
|32|4|Sidnummer för den första frilistans trunksida.|
|36|4|Totalt antal freelistsidor.|
|40|4|Schema-cookien.|
|44|4|Numret för schemaformatet. Schemaformat som stöds är 1, 2, 3 och 4.|
|48|4|Standardstorlek för sidcache.|
|52|4|Sidnumret för den största b-trädets rotsida i autovakuum eller inkrementellt vakuumläge, eller noll annars.|
|56|4|Databastextkodningen. Ett värde på 1 betyder UTF-8. Ett värde på 2 betyder UTF-16le. Ett värde på 3 betyder UTF-16be.|
|60|4|"Användarversionen" som lästs och ställts in av pragman för user_version.|
|64|4|True (ej noll) för inkrementellt vakuumläge. Falskt (noll) annars.|
|68|4|"Applikations-ID" satt av PRAGMA application_id.|
|72|20|Reserverad för expansion. Måste vara noll.|
|92|4|Version-giltigt-för-numret.|
|96|4|SQLITE_VERSION_NUMBER|

## Referenser ##

* [SQLite-filformat - SQLite](https://www.sqlite.org/fileformat2.html)
* [SQLite - Wikipedia](https://en.wikipedia.org/wiki/SQLite)
* [SQLite - C Language Specs](https://www.sqlite.org/c3ref/intro.html)

