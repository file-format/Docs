{
  "date": "2021-06-21",
  "keywords": [
"UDL",
"udvidelse",
"udl fil",
"udl filformat",
"Database filtype",
"Database filformat",
"hvad er en udl-fil"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om UDL-filformat og API'er, der kan oprette og åbne UDL-filer.",
  "title": "UDL - Microsoft Universal Data Link-fil",
  "linktitle": "UDL",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ud-dal"
}
},
  "lastmod": "2021-06-21"
}

## Hvad er UDL fil?
Filen med filtypen .udl kaldes Microsoft Universal Data Link-fil; angivelse af forbindelsesattributter; bruges af Windows-apps til at oprette forbindelse til databasen. UDL-filen indeholder forbindelsesstrengen for en OLE DB-datakilde; med brugernavn og adgangskode og væsentlige forbindelsesstrengegenskaber. For at undgå direkte specificering af egenskaberne i hånden i en forbindelsesstreng, kan en Data Link Properties-dialogboks bruges til at gemme forbindelsesoplysninger i en .udl-fil som et alternativ.

## UDL filformat
Grundlæggende er en UDL-fil (Universal Data Link) en simpel tekstfil, der består af en databaseforbindelsesstreng med bestemte attributter eller egenskaber. Når UDL-filen er oprettet, kan den testes ved at bruge SQL Server Management Studio til at verificere forbindelsen.

### Forbindelsesstrengegenskaber
Følgende egenskaber kan indstilles i en UDL for at sikre den korrekte forbindelse:

- **Servernavn**: placeringen af serveren, hvor den database, du vil have adgang til, er placeret.
- **Godkendelsesmuligheder**
- **Windows-godkendelse**: Godkendelse til SQL Server ved hjælp af den aktuelt loggede brugers Windows-kontooplysninger.
- **SQL Server Authentication**: Autentificering ved hjælp af login-id og adgangskode.
- **Active Directory - Integreret**: Integreret godkendelse med en Azure Active Directory-identitet; kan også bruges til Windows-godkendelse til SQL Server.
- **Active Directory - Adgangskode**: Bruger-id og adgangskodegodkendelse med en Azure Active Directory-identitet.
- **Active Directory - Universal med MFA-understøttelse**: Interaktiv godkendelse med en Azure Active Directory-identitet.
- **Active Directory - Service Principal**: Godkendelse med en Azure Active Directory-serviceprincipal.
- **Server SPN**: Hvis du bruger en betroet forbindelse, kan du angive et serviceprincipal name (SPN) for serveren.
- **Brugernavn**: Indtast det bruger-id, der skal bruges til godkendelse, når du logger på datakilden.
- **Adgangskode**: Indtast adgangskoden, der skal bruges til godkendelse, når du logger på datakilden.
- **Blank adgangskode**: Når det er markeret, gør det muligt for den angivne udbyder at bruge en tom adgangskode i forbindelsesstrengen.
- **Tillad lagring af adgangskode**: Tillader, at adgangskoden gemmes med forbindelsesstrengen.
- **Brug stærk kryptering til data**: data, der sendes gennem forbindelsen, bliver krypteret.
- **Trust server certificate**: The server's certificate will be validated.
- **Database**: Databasenavn, som du vil have adgang til.
- **Vedhæft en databasefil som et databasenavn**: Angiver navnet på den primære fil for en vedhæftelig database.

## Referencer ##

* [Microsoft Data Access Components](https://en.wikipedia.org/wiki/Microsoft_Data_Access_Components#Universal_data_link)

* [Universal Data Link (UDL)-konfiguration](https://learn.microsoft.com/en-us/sql/connect/oledb/help-topics/data-link-pages?view=sql-server-ver15)


