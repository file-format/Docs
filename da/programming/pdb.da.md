{
  "date": "2019-10-11",
  "keywords": [
"pdb-fil",
"pdb",
"udvidelse",
"format",
"Hvad er en pdb-fil",
"pdb filformat",
"PDB metadata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDB-filformat - En programdatabasefil",
  "description": "Lær om PDB-filformat og API'er, der kan oprette og åbne PDB-filer.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-dab"
}
},
  "lastmod": "2020-09-10"
}

## Hvad er en PDB fil?

En fil med filtypenavnet .pdb er en programdatabasefil, der indeholder fejlfindingsoplysninger for en kompileret eksekverbar (EXE/DLL). PDB-filer genereres af Microsoft Compilers, når et applikationsprogram kompileres i fejlretningstilstand. Tilstedeværelsen af PDB-fil kan hjælpe med reverse engineering af en eksekverbar, da den indeholder væsentlig information om alle symboler på modulerne. Det er af denne grund, at disse filer holdes adskilt fra den endelige eksekverbare. Microsofts [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) kan åbne en PDB-fil for at indhente information såsom publics og eksport, globale symboler, lokale symboler, typedata, kildefiler og linjenumre.

## PDB filformat

PDB er Microsofts proprietære filformat og er endnu ikke blevet officielt dokumenteret nogen steder. En startdokumentation er dog tilgængelig [here](https://github.com/Microsoft/microsoft-pdb) og kan refereres til.

### PDB-strømme

PDB-filer består af flere streams, hvor hver stream fungerer som en virtuel individuel fil og indeholder information. PDB-filskrivere kan skrive til disse filer, og filen færdiggøres først, efter at der er udstedt en eksplicit commit. En compiler kan blive ved med at skrive til en PDB-fil, men kun commit, hvis al brugerkode kompileres med succes. En PDB-fil består af følgende strømme:

|Strøm nr. |Indhold |Kort beskrivelse|
---|---|---|
|1| Pdb (header) |Versionsinformation og information til at forbinde denne PDB til EXE|
|2| Tpi (Type manager) |Alle de typer, der bruges i den eksekverbare.|
|3| Dbi (Debug information) |Indeholder sektionsbidrag og liste over 'Mods'|
|4| Navnekort| Indeholder et hash-strengbord|
|4-(n+4)| n Mod'er (moduloplysninger)| Hver Mod-stream indeholder symboler og linjenumre for én compiland|
|n+4| Global symbol hash| Et indeks, der tillader søgning i globale symboler efter navn|
|n+5| Offentlig symbol hash| Et indeks, der tillader søgning i offentlige symboler efter adresser|
|n+6| Symboloptegnelser| Faktiske symbolregistreringer af globale og offentlige symboler|
|n+7| Skriv hash| Hash brugt af TPI-strømmen.|

Hver strøm i en PDB-fil består af flere sider, som ikke nødvendigvis er fortløbende nummererede.

### PDB header

En PDB-fil har en Header, der består af en signatur til at identificere og validere det specifikke format. Længden af signaturen afhænger af PDB-formatet. Overskriften kan være længere end en enkelt side.

### FBF-metadata
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Der er også en uordnet rodstrøm, som indeholder nogle af metadataene.

## Referencer
 * [PDB - Wikipedia](https://en.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

