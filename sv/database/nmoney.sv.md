{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om NMONEY-filformat och API:er som kan skapa och öppna NMONEY-filer.",
  "title" :"NMONEY File - Denaro Account File Format",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Vad är en NMONEY fil?

En NMONEY-fil är en databasfil för finansiell datalagring som innehåller meriter över finansiella transaktioner. Den har utvecklats av Nickvision och användes i Nickvision Denaro-mjukvaran som är en personlig ekonomisk programvara. Data som lagras i en NOMONEY-fil inkluderar information om kredit- och debettransaktioner till ett konto.

NOMONEY-filer kan öppnas med applikationen [Github](https://github.com/NickvisionApps/Denaro).

## Om Denaro Software

Denaro utvecklades ursprungligen av [Nickvision](https://nickvision.org/) som en produkt som senare konverterades till en programvaruapp med öppen källkod värd på [Github](https://github.com/NickvisionApps/Denaro) . Sedan dess har appen endast modifierats och uppdaterats på Github. Appen är utvecklad i C# i Windows UI med Windows App SDK (WinUI 3 som vid denna tidpunkt).

### Funktioner som erbjuds av Denaro

* Hantera flera konton samtidigt med dess mest populära och välbekanta flikgränssnitt
* Filtrera transaktioner efter typ, grupp eller datum
* Upprepa transaktioner som räkningar som sker varje månad
* Överför pengar från ett konto till ett annat
* Exportera data från ett konto som en CSV-fil och importera en CSV-, OFX- eller QIF-fil för att lägga till transaktioner till ett konto

## Denaro filformat - Mer information

Denaro-filer sparas på skiva i binärt filformat. Finansiell data lagras som en databasfil i filformatet **.SQLITE3**. SQLITE är en lättviktig SQL-databasfil skapad med SQLite-mjukvaran. Den tillhandahåller en fristående databasmotor som kan tillhandahålla en komplett och mycket pålitlig databas. SQLite databasfiler kan användas för att dela rikt innehåll mellan system genom att helt enkelt utbyta dessa filer över nätverket. SQLite-bindningar finns för programmeringsspråk som C, [C#](/sv/programmering/cs/), [C++](/sv/programmering/cpp/), [Java](/sv/programmering/java/), [PHP](/sv/programmering/ php/) och många andra.

## Referenser

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

