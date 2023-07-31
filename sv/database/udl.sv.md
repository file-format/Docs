{
  "date" : "2021-06-21",
  "keywords" :[ "UDL", "tillägg", "udl-fil", "udl-filformat", "Databasfiltyp", "Databasfilformat", "vad är en udl-fil" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Läs mer om UDL-filformat och API:er som kan skapa och öppna UDL-filer.",
  "title" :"UDL - Microsoft Universal Data Link File",
  "linktitle" : "UDL",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-21"
}

## Vad är UDL fil?
Filen med filändelsen .udl kallas Microsoft Universal Data Link-fil; specificering av anslutningsattribut; används av Windows-appar för att upprätta en anslutning till databasen. UDL-filen innehåller anslutningssträngen för en OLE DB-datakälla; med användarnamn och lösenord och viktiga egenskaper för anslutningssträngar. För att undvika att direkt specificera egenskaperna för hand i en anslutningssträng kan dialogrutan Data Link Properties användas för att spara anslutningsinformation i en .udl-fil som ett alternativ.

## UDL filformat
I grund och botten är en UDL-fil (Universal Data Link) en enkel textfil som består av en databasanslutningssträng med särskilda attribut eller egenskaper. När UDL-filen väl har skapats kan den testas genom att använda SQL Server Management Studio för att verifiera anslutningen.

### Anslutningssträngegenskaper
Följande egenskaper kan ställas in i en UDL för att säkerställa korrekt anslutning:

- **Servernamn**: platsen för servern där databasen du vill komma åt finns.
- **Autentiseringsalternativ**
- **Windows-autentisering**: Autentisering till SQL Server med den för närvarande inloggade användarens Windows-kontouppgifter.
- **SQL Server Authentication**: Autentisering med inloggnings-ID och lösenord.
- **Active Directory - Integrated**: Integrerad autentisering med en Azure Active Directory-identitet; kan också användas för Windows-autentisering till SQL Server.
- **Active Directory - Lösenord**: Användar-ID och lösenordsautentisering med en Azure Active Directory-identitet.
- **Active Directory - Universal med MFA-stöd**: Interaktiv autentisering med en Azure Active Directory-identitet.
- **Active Directory - Service Principal**: Autentisering med en Azure Active Directory-tjänstprincip.
- **Server SPN**: Om du använder en betrodd anslutning kan du ange ett tjänstehuvudnamn (SPN) för servern.
- **Användarnamn**: Ange det användar-ID som ska användas för autentisering när du loggar in på datakällan.
- **Lösenord**: Ange lösenordet som ska användas för autentisering när du loggar in på datakällan.
- **Tomt lösenord**: När det är markerat görs det möjligt för den angivna leverantören att använda ett tomt lösenord i anslutningssträngen.
- **Tillåt att spara lösenord**: Tillåter att lösenordet sparas med anslutningssträngen.
- **Använd stark kryptering för data**: data som skickas genom anslutningen kommer att krypteras.
- **Trust servercertifikat**: Serverns certifikat kommer att valideras.
- **Databas**: Databasnamn som du vill komma åt.
- **Bifoga en databasfil som ett databasnamn**: Anger namnet på den primära filen för en bifogad databas.

## Referenser ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)
* [Universal Data Link (UDL)-konfiguration](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)

