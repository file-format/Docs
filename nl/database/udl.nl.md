{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "extensie", "udl-bestand", "udl-bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "wat is een udl-bestand"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over de UDL-bestandsindeling en API's die UDL-bestanden kunnen maken en openen.",
  "title" :"UDL - Microsoft Universal Data Link-bestand",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Wat is een UDL-bestand?
Het bestand met de extensie .udl heet Microsoft Universal Data Link-bestand; specificeren van verbindingskenmerken; gebruikt door Windows-apps om een verbinding met de database tot stand te brengen. Het UDL-bestand bevat de verbindingsreeks voor een OLE DB-gegevensbron; met gebruikersnaam en wachtwoord en essentiële verbindingsreekseigenschappen. Om te voorkomen dat de eigenschappen met de hand worden gespecificeerd in een verbindingsreeks, kan als alternatief een dialoogvenster Gegevenskoppelingseigenschappen worden gebruikt om verbindingsinformatie op te slaan in een .udl-bestand.

## UDL-bestandsindeling
Kortom, een UDL-bestand (Universal Data Link) is een eenvoudig tekstbestand dat bestaat uit een databaseverbindingsreeks met bepaalde attributen of eigenschappen. Nadat het UDL-bestand is gemaakt, kan het worden getest met behulp van SQL Server Management Studio om de connectiviteit te verifiëren.

### Eigenschappen verbindingsreeks
De volgende eigenschappen kunnen in een UDL worden ingesteld om de juiste connectiviteit te garanderen:

- **Servernaam**: locatie van de server waar de database die u wilt benaderen zich bevindt.
- **Verificatie-opties**
- **Windows-authenticatie**: authenticatie bij SQL Server met behulp van de Windows-accountreferenties van de momenteel aangemelde gebruiker.
- **SQL Server-authenticatie**: authenticatie met inlog-ID en wachtwoord.
- **Active Directory - Geïntegreerd**: geïntegreerde verificatie met een Azure Active Directory-identiteit; kan ook worden gebruikt voor Windows-authenticatie naar SQL Server.
- **Active Directory - Wachtwoord**: gebruikers-ID en wachtwoordverificatie met een Azure Active Directory-identiteit.
- **Active Directory - Universeel met MFA-ondersteuning**: Interactieve verificatie met een Azure Active Directory-identiteit.
- **Active Directory - Service-principal**: verificatie met een Azure Active Directory-service-principal.
- **Server-SPN**: als u een vertrouwde verbinding gebruikt, kunt u een service-principalnaam (SPN) voor de server opgeven.
- **Gebruikersnaam**: typ de gebruikers-ID die u wilt gebruiken voor verificatie wanneer u zich aanmeldt bij de gegevensbron.
- **Wachtwoord**: typ het wachtwoord dat u wilt gebruiken voor verificatie wanneer u zich aanmeldt bij de gegevensbron.
- **Leeg wachtwoord**: indien aangevinkt, stelt de opgegeven provider in staat om een leeg wachtwoord in de verbindingsreeks te gebruiken.
- **Opslaan van wachtwoord toestaan**: hiermee kan het wachtwoord worden opgeslagen met de verbindingsreeks.
- **Gebruik sterke codering voor gegevens**: gegevens die via de verbinding worden doorgegeven, worden gecodeerd.
- **Vertrouw op servercertificaat**: het servercertificaat wordt gevalideerd.
- **Database**: databasenaam waartoe u toegang wilt.
- **Een databasebestand bijvoegen als databasenaam**: Specificeert de naam van het primaire bestand voor een koppelbare database.

## Referenties ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Universal Data Link (UDL)-configuratie](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

