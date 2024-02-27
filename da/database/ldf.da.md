{
  "date": "2020-11-11",
  "keywords": [
"LDF",
"udvidelse",
"fil",
"filformat",
"Database filtype",
"Database filformat",
"Database filer"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om LDF-filformat og API'er, der kan oprette og åbne LDF-filer.",
  "title": "LDF - SQL Server Master Database Filformat",
  "linktitle": "LDF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-ld-daf"
}
},
  "lastmod": "2020-08-12"
}

## Hvad er LDF fil?

En fil med filtypenavnet .ldf er en logfil, der vedligeholdes af Microsoft SQL Server, som er et relationelt databasestyringssystem (RDBMS). Alle transaktioner udført på primære databasefiler ([MDF](/database/mdf/))(såsom indsættelse, opdatering, sletning) registreres i LDF-filen. LDF-filer er kritiske komponenter i enhver database. I tilfælde af en systemfejl, bruges logfilen til at gendanne databasen til en konsistent tilstand. Transaktionslogfilen kan øges i størrelse, hvis transaktionerne ikke er fuldt forpligtede. LDF filer kan åbnes med Microsoft SQL Server-softwareapplikation.

## Operationer registreret i LDF-fil

En SQL-logfil registrerer følgende handlinger:

 * Begyndelsen og slutningen af hver transaktion.

 * Hver datadataændring (indsæt, opdater eller slet). Dette inkluderer også ændringer af systemlagrede procedurer eller DDL-sætninger (Data Definition Language) til enhver tabel, inklusive systemtabeller.

 * Hvert omfang og sidetildeling eller deallokering.

 * Oprettelse eller sletning af en tabel eller et indeks.

## LDF filformat

The LDF file consists of SQL Server transaction records that are arranged as string of log records. Each log record has a log sequence number (LSN) that is higher than the LSN of the previous record. The strings are concatenated after each other in the file. Due to the modern high speed computers, records can be inserted where the LSN2 exists in the log file before LSN1. Da operationerne er registreret i en seriel, blev ændringen beskrevet af LSN2 udført efter logposten LSN1. Posterne for en bestemt transaktion er forbundet bagud ved hjælp af pointere, der bruges og fremskynder tilbagerulningen af transaktionen.
 
## Referencer

 * [Databasefiler og filgrupper](https://learn.microsoft.com/en-us/sql/relational-databases/databases/database-files-and-filegroups?view=sql-server-ver15)
 * [Transaction Log Architecture and Management Guide](https://learn.microsoft.com/en-us/sql/relational-databases/sql-server-transaction-log-architecture-and-management-guide?view=sql-server -ver15)

