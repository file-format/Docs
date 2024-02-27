{
  "date": "2019-10-11",
  "keywords": [
"tar-fil",
"tar filformat",
"hvad er en tar-fil",
"fil",
"tjære eksempel",
"tar filtypenavnet",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR - Unix Archive File Format",
  "description": "Lær om, hvad en TAR-fil og API'er er, der kan oprette og åbne TAR-filer.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-dar"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er en TAR fil?

Filer med filtypenavnet .tar er arkiver oprettet med Unix-baseret hjælpeprogram til at indsamle en eller flere filer. Flere filer gemmes i et ukomprimeret format med understøttelse af tilføjelse af filer såvel som mapper til arkivet. TAR-værktøjet på Unix er kommandobaseret, men filer, der er oprettet, understøttes af de fleste filarkiveringssystemer på næsten alle operativsystemer. Det blev først oprettet i 1979 af AT&T Bell Laboratories, og efterfølgende versioner blev offentliggjort med tiden.

## TAR filformat

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Datasættene oprettet af tar bevarer information om filsystemparametre som:

* Navn

* Tidsstempler

* Ejerskab

* Filadgangstilladelser

* Directory Organisation


En TAR-fil har ikke noget magisk tal. Den indeholder en række blokke, hvor hver blok er på BLOCKSIZE bytes.

Hver arkiveret fil er repræsenteret af en overskriftsblok, der beskriver filen, efterfulgt af nul eller flere blokke, som angiver indholdet af filen. I slutningen af arkivfilen er der to 512-byte blokke fyldt med binære nuller som en ende-på-fil markør. Et rimeligt system bør skrive en sådan ende-af-fil-markør i slutningen af et arkiv, men må ikke antage, at en sådan blok eksisterer, når et arkiv læses. Især GNU tar udsender altid en advarsel, hvis den ikke støder på den.

Blokkene kan være blokeret for fysiske I/O-operationer. Hver post på n blokke (hvor n er sat af blokeringsfaktoren = 512-størrelsesindstillingen til at tjære) skrives med en enkelt write()-operation. På magnetbånd er resultatet af en sådan skrivning en enkelt post. Når du skriver et arkiv, skal den sidste post af blokke skrives i fuld størrelse, med blokke efter nulblokken indeholdende alle nuller. Når man læser et arkiv, bør et fornuftigt system håndtere et arkiv, hvis sidste post er kortere end resten, eller som indeholder skraldeposter efter en nulblokering.

### TAR-filoverskrift

Som alle andre filoverskrifter indeholder tar-filoverskriftsposten metadata om en fil og vises i følgende tabel.

|Feltforskydning|Feltstørrelse (Bytes)|Felt
---|---|---|
|0|100|Filnavn
|100|8|Filtilstand
|108|8|Ejers numeriske bruger-id
|116|8|Gruppens numeriske bruger-id
|124|12|Filstørrelse i bytes (oktal base)
|136|12|Sidste ændringstid i numerisk Unix-tidsformat (oktal)
|148|8|Tjeksum for overskriftspost
|156|1|Linkindikator (filtype)
|157|100|Navn på linket fil

Ubrugte felter er udfyldt med NUL-bytes. En header består af 257 bytes, som er polstret med NUL-bytes for at få den til at fylde til 512 byte-record.

## Sådan opretter du en TAR-fil

### Opret TAR-fil på Windows

På Windows kan du bruge Windows Subsystem til Linux (WSL) eller tredjepartsværktøjer som 7-Zip til at oprette TAR-filer. Sådan gør du det ved hjælp af WSL:

 1. Installer WSL, hvis du ikke allerede har gjort det. Du kan installere det via indstillingerne for Windows-funktioner.

 1. Åbn en WSL-terminal og brug den samme tar-kommando som på Linux- eller Unix-systemer til at oprette en TAR-fil.

### Opret TAF-fil på Linux fra kommandolinjen

For at oprette en TAR-fil ved hjælp af kommandolinjen på Linux- eller Unix-baserede systemer, skal du åbne en terminal og bruge tar-kommandoen. Du kan oprette en TAR-fil i forskellige komprimeringsformater (f.eks. .tar.gz, .tar.bz2, .tar.xz), men her opretter vi en almindelig .tar-fil:

For at oprette en TAR-fil fra en enkelt fil eller mappe skal du bruge følgende kommando:

```
tar -cvf archive.tar file_or_directory
```

## Sådan åbnes TAR-fil

### Åbn TAR-fil på Windows

Du skal ikke installere et dekompressionsværktøj på Windows OS, såsom 7-Zip. Det er et gratis arkiveringsværktøj, der kan bruges til at oprette og udpakke forskellige komprimerede filformater. Højreklik på din TAR-fil, og vælg muligheden **Udpak**.

### Åbn TAR-fil på Mac

På en Mac skal du bare dobbeltklikke på filen TAR, TGZ eller TAR.GZ for at pakke den ud.

### Åbn TAR-fil på Linux

Hvis du bruger Linux eller Mac Terminal-appen, skal du bruge tar -xvf til TAR-filer eller tar -xvzf for filer, der ender på TGZ eller TAR.GZ.

## Referencer ##

* [TAR - af Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))

* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


