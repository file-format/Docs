{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PUP File Format - PlayStation 3 Update File",
  "description":"Läs mer om PUP-filformat och API:er som kan skapa och öppna PUP-filer.",
  "linktitle" : "PUP",
  "menu" : {
    "docs" : {
      "identifier":"game-pup",
      "parent" : "game"
}
},
  "lastmod" : "2022-06-23"
}

## Vad är en PUP fil?

En PUP-fil är en systemuppdateringspatchfil som används av PlayStation 4 (PS4) och PlayStation 5 (PS5) systemprogramvara. Den uppgraderar spelets firmware till en nyare version som kan innehålla programvaruförbättringar när det gäller buggfixar, nya operativsystemfunktioner och förbättringar när det gäller mjukvarans prestanda. PUP-filen kan också innehålla patchar för att fixa buggar som annars kan leda till säkerhetsproblem. PUP-filer kan laddas ner till systemet genom att ansluta det till internet eller manuellt ladda ner firmwareuppdateringen till en dator och sedan överföra till enheten med ett USB-minne eller annan lagringsenhet. Den tidigare versionen av PlayStation, dvs PS3, använde även PUP-filen för uppgradering av firmware.

## PUP-filformat - Mer information

PUP-filer sparas på skiva i binärt filformat [komprimerat](/sv/compression/). Men detaljerna om komprimering är inte tillgängliga offentligt. Innehållet i en PUP-fil kan extraheras med programmet PS3 PUP Extractor på Windows OS. För att uppgradera mjukvarusystemet för PS3 laddas PUP-filen upp och sparas i mappen /PS3/UPDATE på maskinen. Detta låter systemuppdateringsalternativet hitta uppgraderingsfilen för den fasta programvaran och köra den.

### Namnkonvention för PUP-filformat

* `PS3UPDAT.PUP` - Standardfilnamnet som används för PlayStation 3-uppdateringar
* `PS4UPDATE.PUP` - Standardfilnamnet som används för PlayStation 4-uppdateringar
* `PS5UPDATE.PUP` - Standardfilnamnet som används för PlayStation 5-uppdateringar

## Använda PUP-fil för att återställa fabriksinställningarna för PlayStation

PUP-filer kan användas för att fabriksåterställa din PlayStation-enhet. Detta kommer att skriva över all data från enheten, ta bort befintlig firmware och ställa in den som en helt ny enhet. Fabriksåterställning av din PlayStation tar också bort all sparad speldata.

## Referenser

* [PS3 System Software Update](https://www.playstation.com/en-us/support/hardware/ps3/system-software/)

