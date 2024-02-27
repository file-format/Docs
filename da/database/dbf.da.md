{
  "date": "2021-06-15",
  "keywords": [
"DBF",
"udvidelse",
"dbf fil",
"dbf filformat",
"Database filtype",
"Database filformat",
"hvad er en dbf-fil",
"dBASE"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om DBF filformat og API'er, der kan oprette og åbne DBF filer.",
  "title": "DBF - dBase Database Fil",
  "linktitle": "DBF",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-db-daf"
}
},
  "lastmod": "2021-06-15"
}

## Hvad er en DBF fil?
The file with .dbf extension is a database file used by a database management system application called **dBASE**. Inititally, the dBASE database was named as Project Vulcan; started by **Wayne Ratliff** in 1978. DBF-filtypen blev introduceret med dBASE II i 1983. Den arrangerer flere dataposter med Array-typefelter. **xBase**-databasesoftwaren, som er pupulær på grund af dens kompatibilitet med en lang række filformater; understøtter også DBF-filer.

## DBF filformat
DBF-filformatet tilhører dBASE-databasestyringssystemet, men det kan være kompatibelt med xBase eller andre DBMS-software. Den oprindelige version af dbf-filen bestod af en simpel tabel, der kunne have tilføjet, ændret, slettet eller udskrevet data ved hjælp af ASCII-tegnsættet. Med tiden blev .dbf forbedret, og yderligere filer blev tilføjet for at øge funktionerne og mulighederne i databasesystemet.

I moderne dBASE består en DBF-fil af en header, dataposterne og EOF-markøren (End of File)

- Headeren indeholder information om filen, såsom antallet af poster og antallet af typer felter, der bruges i posterne.
- Optegnelserne indeholder de faktiske data.
- Slutningen af filen er markeret med en enkelt byte, med værdien 0x1A.

### Filoverskrift
Layout af filoverskrift i dBase er angivet i følgende tabel:

| Byte | Indhold | Betydning |
---|---|---|
| 0 | 1 byte | Gyldig dBASE for DOS-fil; bit 0-2 angiver versionsnummer, bit 3 angiver tilstedeværelsen af en dBASE for DOS-memofil, bit 4-6 angiver tilstedeværelsen af en SQL-tabel, bit 7 angiver tilstedeværelsen af enhver memofil (enten dBASE m PLUS eller dBASE for DOS) |
| 1-3 | 3 bytes | Dato for sidste opdatering; formateret som ÅÅMMDD |
| 4–7 | 32-bit nummer | Antal poster i databasefilen |
| 8–9 | 16-bit nummer | Antal bytes i overskriften |
| 10–11 | 16-bit nummer | Antal bytes i posten |
| 12–13 | 2 bytes | reserveret; fyld med 0 |
| 14 | 1 byte | Flag, der angiver ufuldstændig transaktion[note 1] |
| 15 | 1 byte | Krypteringsflag[note 2] |
| 16–27 | 12 bytes | Reserveret til dBASE til DOS i et flerbrugermiljø |
| 28 | 1 byte | Produktions .mdx fil flag; 1 hvis der er en produktions-.mdx-fil, 0 hvis ikke |
| 29 | 1 byte | Sprog driver ID |
| 30–31 | 2 bytes | reserveret; fyld med 0 |
| 32–n [note 3][note 4] | 32 bytes hver | række af feltdeskriptorer (se nedenfor for layout af deskriptorer) |
| n + 1 | 1 byte | 0x0D som feltdeskriptorarrayterminator |

- ISMARKEDO-funktionen kontrollerer dette flag (BEGIN TRANSACTION sætter det til 1, END TRANSACTION og ROLLBACK nulstiller det til 0).
- Hvis dette flag er sat til 1, vises meddelelsen Database krypteret.
- Det maksimale antal felter er 255.
- n betyder den sidste byte i feltbeskrivelsesarrayet.

### Feltdeskriptorarray
Layout af feltbeskrivelser i dBASE:

| Byte | Indhold | Betydning |
---|---|---|
| 0–10 | 11 bytes | Feltnavn i ASCII (udfyldt med nul) |
| 11 | 1 byte | Felttype. Tilladte værdier: C, D, F, L, M eller N (se næste tabel for betydninger) |
| 12–15 | 4 bytes | Reserveret |
| 16 | 1 byte | Feltlængde i binær (maks. 254 (0xFE)). |
| 17 | 1 byte | Felt decimaltal i binær |
| 18–19 | 2 bytes | Arbejdsområde ID |
| 20 | 1 byte | Eksempel |
| 21-30 | 10 bytes | Reserveret |
| 31 | 1 byte | Produktion MDX feltflag; 1 hvis feltet har et indeksmærke i produktions-MDX-filen, 0 hvis ikke |

### Databaseposter
Hver post starter med et sletningsflag (1-byte). Felter pakkes ind i poster uden feltseparatorer. Alle feltdata er ASCII. Afhængigt af feltets type pålægger applikationen yderligere begrænsninger. Her er felttyper i dBase:

| Felttype | Mnemonisk | Hvad den accepterer |
-------|-----|----|
| C | Karakter | Enhver ASCII-tekst (polstret med mellemrum op til feltets længde) |
| D | Dato | Tal og et tegn til at adskille måned, dag og år (gemt internt som 8 cifre i formatet ÅÅÅÅMMDD) |
| F | Flydende komma | -, ., 0–9 (højrejusteret, polstret med mellemrum) |
| L | Logisk | Y, y, N, n, T, t, F, f eller ? (når ikke initialiseret) |
| M | Memo | Enhver ASCII-tekst (lagret internt som 10 cifre, der repræsenterer et .dbt-bloknummer, højrejusteret, udfyldt med mellemrum) |
| N | Numerisk | -, ., 0–9 (højrejusteret, polstret med mellemrum) |









## Referencer ##

* [.dbf - Wikipedia](https://en.wikipedia.org/wiki/.dbf)


