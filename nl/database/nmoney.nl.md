{
  "date" : "2023-05-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Leer meer over het NMONEY-bestandsformaat en API's die NMONEY-bestanden kunnen maken en openen.",
  "title" :"NMONEY Bestand - Bestandsformaat Denaro-account",
  "linktitle" : "NMONEY",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2023-05-17"
}

## Wat is een NMONEY-bestand?

Een NMONEY-bestand is een databasebestand voor de opslag van financiële gegevens dat een trackrecord van financiële transacties bevat. Het is ontwikkeld door Nickvision en werd gebruikt in de Nickvision Denaro-software, een persoonlijke financiële softwareapplicatie. Gegevens die zijn opgeslagen in een NOMONEY-bestand bevatten informatie over krediet- en debettransacties naar een account.

NOMONEY-bestanden kunnen worden geopend met de toepassing [Github](https://github.com/NickvisionApps/Denaro).

## Over Denaro-software

Denaro werd aanvankelijk ontwikkeld door [Nickvision](https://nickvision.org/) als een product dat later werd omgezet naar een open-source software-app die werd gehost op [Github](https://github.com/NickvisionApps/Denaro) . Sindsdien is de app alleen op Github aangepast en bijgewerkt. De app is ontwikkeld in C# in Windows UI met Windows App SDK (momenteel WinUI 3).

### Functies aangeboden door Denaro

* Beheer meerdere accounts tegelijkertijd met de meest populaire en vertrouwde tabbladinterface
* Filter transacties op type, groep of datum
* Herhaaltransacties zoals facturen die elke maand plaatsvinden
* Geld overmaken van de ene rekening naar de andere
* Exporteer de gegevens van een account als CSV-bestand en importeer een CSV-, OFX- of QIF-bestand om transacties aan een account toe te voegen

## Denaro-bestandsindeling - Meer informatie

Denaro-bestanden worden op schijf opgeslagen in binair bestandsformaat. Financiële gegevens worden opgeslagen als databasebestand in het bestandsformaat **.SQLITE3**. SQLITE is een lichtgewicht SQL-databasebestand gemaakt met de SQLite-software. Het biedt een op zichzelf staande database-engine die een volledig functionele en zeer betrouwbare database kan bieden. SQLite-databasebestanden kunnen worden gebruikt om rijke inhoud tussen systemen te delen door deze bestanden eenvoudigweg via het netwerk uit te wisselen. Er bestaan SQLite-bindingen voor programmeertalen zoals C, [C#](/nl/programming/cs/), [C++](/nl/programming/cpp/), [Java](/nl/programming/java/), [PHP](/nl/programming/php/), en vele anderen.

## Referenties

* [Nickvision](https://nickvision.org/)
* [NIckVision - Github](https://github.com/NickvisionApps/Denaro)

