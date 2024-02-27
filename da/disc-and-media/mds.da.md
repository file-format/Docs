{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Lær om MDS-filformat og API'er, der kan oprette og åbne MDS-filer.",
  "title" : "MDS-filformat - Mediebeskrivelse Sidecar-fil",
  "linktitle" : "MDS",
  "menu" : {
    "docs" : {
      "identifier":"disc-and-media-mds-da",
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2023-01-23"
}

## Hvad er en MDS fil?

MDS (Media Descriptor Sidecar File) er en fil tilknyttet softwaren Alcohol 120% og Daemon Tools, som begge bruges til at skabe og administrere virtuelle cd- og dvd-drev. MDS-filen indeholder information om layoutet af dataene på disken, herunder placeringen af alle filerne og diskens struktur. Dette gør det muligt for det virtuelle drev at efterligne adfærden af en fysisk disk, så softwaren kan læse dataene på den virtuelle disk, som om det var en rigtig disk.

When you want to mount an image file to a virtual drive, the MDS file is used along with the corresponding image file in a format such as ISO, BIN or CUE. The MDS file contains a description of the layout of the data on the disc, and the virtual drive software uses this information to create a virtual disc. This allows you to use the software as if you were using a physical disc, without having to physically insert the disc into the drive.

## Relation til alkohol 120%

Alcohol 120% er en populær software til at skabe og administrere virtuelle cd- og dvd-drev, og den bruger MDS-filformatet til at gemme og få adgang til diskbilleder. MDS-filformatet er proprietært til Alcohol 120% og kan kun åbnes og bruges af Alcohol 120% softwaren eller anden software, der understøtter det.

## Hvordan åbner jeg filen MDS?

For at åbne en MDS-fil i Alcohol 120%, skal du have softwaren installeret på din computer. Når du har installeret Alcohol 120%, kan du åbne filen MDS ved at gøre følgende:

1. Launch Alkohol 120%.
2. Klik på menuen Filer og vælg Åbn.
3. Naviger til placeringen af MDS-filen på din computer, og vælg den.
4. MDS-filen vil nu blive åbnet i Alcohol 120%, og du bliver bedt om at vælge den tilsvarende billedfil (såsom ISO, BIN eller CUE).
5. Når du har valgt billedfilen, vil Alcohol 120% montere billedet til et virtuelt drev.

Alternativt kan du også åbne en MDS fil ved at dobbeltklikke på den, hvis Alcohol 120% er indstillet som standardprogrammet til at åbne MDS filer. Du kan også bruge anden software, der understøtter MDS-format som Daemon Tools, Virtual CloneDrive, Virtual Drive Manager og MagicISO.

## Referencer
* [Alkohol 120 % - software til cd- og dvd-brænding](https://www.alcohol-soft.com/)


