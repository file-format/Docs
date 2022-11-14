{
  "date" : "2021-06-15",
  "keywords" :[ "DBF", "extensie", "dbf-bestand", "dbf-bestandsindeling", "Databasebestandstype", "Databasebestandsindeling", "wat is een dbf-bestand", "dBASE"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Meer informatie over DBF-bestandsindelingen en API's die DBF-bestanden kunnen maken en openen.",
  "title" :"DBF - dBase-databasebestand",
  "linktitle" : "DBF",
  "menu" : {
    "docs" : {
      "parent" : "database"
}
},
  "lastmod" : "2021-06-15"
}

## Wat is een DBF-bestand?
Het bestand met de extensie .dbf is een databasebestand dat wordt gebruikt door een databasebeheersysteemtoepassing met de naam **dBASE**. Aanvankelijk heette de dBASE-database Project Vulcan; gestart door **Wayne Ratliff** in 1978. Het DBF-bestandstype werd in 1983 geïntroduceerd met dBASE II. Het rangschikt meerdere gegevensrecords met velden van het array-type. De **xBase** databasesoftware die populair is vanwege zijn compatibiliteit met een breed scala aan bestandsformaten; ondersteunt ook de DBF-bestanden.

## DBF-bestandsindeling
Het DBF-bestandsformaat behoort tot het dBASE-databasebeheersysteem, maar is mogelijk compatibel met xBase of andere DBMS-software. De eerste versie van het dbf-bestand bestond uit een eenvoudige tabel waaraan gegevens konden worden toegevoegd, gewijzigd, verwijderd of afgedrukt met behulp van de ASCII-tekenset. Met het verstrijken van de tijd werd .dbf verbeterd en werden er extra bestanden toegevoegd om de functies en mogelijkheden van het databasesysteem te vergroten.

In moderne dBASE bestaat een DBF-bestand uit een koptekst, de gegevensrecords en de EOF-markering (End of File)

- De header bevat informatie over het bestand, zoals het aantal records en het aantal typen velden dat in de records wordt gebruikt.
- De records bevatten de feitelijke gegevens.
- Het einde van het bestand wordt gemarkeerd door een enkele byte, met de waarde 0x1A.

### Bestandskop
Lay-out van bestandsheader in dBase wordt gegeven in de volgende tabel:

| Byte | Inhoud | Betekenis |
---|---|---|
| 0 | 1 byte | Geldige dBASE voor DOS-bestand; bits 0-2 geven het versienummer aan, bit 3 geeft de aanwezigheid van een dBASE voor DOS-memobestand aan, bits 4-6 geven de aanwezigheid van een SQL-tabel aan, bit 7 geeft de aanwezigheid van een memobestand aan (dBASE m PLUS of dBASE voor DOS) |
| 1–3 | 3 bytes | Datum van laatste update; geformatteerd als JJMMDD |
| 4–7 | 32-bits nummer | Aantal records in het databasebestand |
| 8–9 | 16-bits nummer | Aantal bytes in de kop |
| 10–11 | 16-bits nummer | Aantal bytes in het record |
| 12–13 | 2 bytes | Gereserveerd; vul met 0 |
| 14 | 1 byte | Vlag die onvolledige transactie aangeeft[note 1] |
| 15 | 1 byte | Coderingsvlag [noot 2] |
| 16–27 | 12 bytes | Gereserveerd voor dBASE voor DOS in een omgeving met meerdere gebruikers |
| 28 | 1 byte | Productie .mdx-bestandsvlag; 1 als er een productie .mdx-bestand is, 0 zo niet |
| 29 | 1 byte | Taal bestuurder-ID |
| 30–31 | 2 bytes | Gereserveerd; vul met 0 |
| 32–n [noot 3][noot 4] | 32 bytes elk | array van velddescriptors (zie hieronder voor lay-out van descriptors) |
| n + 1 | 1 byte | 0x0D als de velddescriptor array-terminator |

- De ISMARKEDO-functie controleert deze vlag (BEGIN TRANSACTIE zet het op 1, END TRANSACTIE en ROLLBACK zet het terug op 0).
- Als deze vlag is ingesteld op 1, verschijnt het bericht Database versleuteld.
- Het maximum aantal velden is 255.
- n betekent de laatste byte in de velddescriptorarray.

### Velddescriptormatrix
Lay-out van velddescriptors in dBASE:

| Byte | Inhoud | Betekenis |
---|---|---|
| 0–10 | 11 bytes | Veldnaam in ASCII (nul gevuld) |
| 11 | 1 byte | Veld soort. Toegestane waarden: C, D, F, L, M of N (zie volgende tabel voor betekenissen) |
| 12–15 | 4 bytes | Gereserveerd |
| 16 | 1 byte | Veldlengte in binair (maximaal 254 (0xFE)). |
| 17 | 1 byte | Veld decimale telling in binair |
| 18-19 | 2 bytes | Werkgebied-ID |
| 20 | 1 byte | Voorbeeld |
| 21–30 | 10 bytes | Gereserveerd |
| 31 | 1 byte | Productie MDX-veldvlag; 1 als veld een indextag heeft in het productie-MDX-bestand, 0 indien niet |

### Databaserecords
Elk record begint met een verwijderingsvlag (1 byte). Velden zijn verpakt in records zonder veldscheidingstekens. Alle veldgegevens zijn ASCII. Afhankelijk van het type van het veld legt de toepassing verdere beperkingen op. Dit zijn veldtypen in dBase:

| Veldtype | ezelsbruggetje | Wat het accepteert |
-------|-----|----|
| C | Karakter | Elke ASCII-tekst (opgevuld met spaties tot de lengte van het veld) |
| D | Datum | Cijfers en een teken om maand, dag en jaar te scheiden (intern opgeslagen als 8 cijfers in de indeling JJJJMMDD) |
| F | Drijvende komma | -, ., 0–9 (rechts uitgelijnd, opgevuld met spaties) |
| L | Logisch | Y, y, N, n, T, t, F, f of ? (wanneer niet geïnitialiseerd) |
| M | Memo | Elke ASCII-tekst (intern opgeslagen als 10 cijfers die een .dbt-bloknummer vertegenwoordigen, rechts uitgelijnd, opgevuld met spaties) |
| N | Numeriek | -, ., 0–9 (rechts uitgelijnd, opgevuld met spaties) |









## Referenties ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)

