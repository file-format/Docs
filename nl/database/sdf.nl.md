{
  "date" : "2021-05-03",
  "keywords" :[ "SDF", "sdf-bestand", "wat is een sdf-bestand", "hoe een sdf-bestand te openen", "extensie", "bestand", "sdf-bestandsformaat", "Databasebestandstype", "Databasebestandsformaat ", "Databasebestanden" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over SDF-bestandsindelingen en API's die SDF-bestanden kunnen maken en openen.",
  "title" :"SDF - SQL Server compact databasebestand",
  "linktitle" : "SDF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-05-03"
}

## Wat is een SDF-bestand?
Een bestand met de extensie .sdf bevat de Microsoft SQL Server Compact (SQL CE) database die ook bekend staat als een compacte relationele database; geproduceerd door Microsoft voor de applicaties gemaakt voor mobiele apparaten en desktops. Het ondersteunt zowel 32- als 64-bits besturingssystemen en de volledige inhoud van de database is opgenomen in een enkel SDF-bestand en kan meer dan 4 GB schijfruimte in beslag nemen. Om veiligheidsredenen kan een .sdf-bestand worden gecodeerd met 128-bits codering. De SQL CE-runtime regelt parallelle toegang voor meerdere gebruikers tot het .sdf-bestand. Het SDF-bestand kan worden gekopieerd via **QuickOnce** of het kan eenvoudig naar de bestemming worden gekopieerd voor systeemimplementatie.

## SDF-bestandsindeling
Een SDF-bestand bevat een database die gewoonlijk compacte relationele database wordt genoemd. Een SDF-bestand bevat alle databasegerelateerde informatie en de SQL Server Compact is een lichtgewicht en gratis database-engine die wordt gebruikt om de .sdf-bestanden te beheren. De .sdf-bestandsgrootte mag de limiet van 4 GB niet overschrijden. De SDF-bestanden slaan de informatie over opgeslagen procedures, triggers of views niet op. Toepassingen die een SQL CE-database gebruiken, hoeven het pad naar een SDF-bestand niet op te geven in de ADO.NET-verbindingsreeks, maar kan worden vermeld als |DataDirectory|\database_name.sdf, waarmee de gegevensmap wordt gedefinieerd die wordt gedefinieerd in het assembly-manifest voor de toepassing
De .sdf-naamgevingsconventie is optioneel en elke extensie kan worden gebruikt om het bestand op te slaan. Het instellen van een wachtwoord voor het databasebestand is een optionele stap. Om de database te comprimeren of te repareren, moet het bestand worden opgeslagen met de optie **gecompacteerde/gerepareerde database**.

## Referenties

* [SQL Server Compact - Wikipedia](https://en.wikipedia.org/wiki/SQL_Server_Compact)
* [SQL Server Compact gebruiken voor ASP.NET-webtoepassingen](https://docs.microsoft.com/en-us/previous-versions/aspnet/ms247257(v=vs.110))


