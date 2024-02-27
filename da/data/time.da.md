{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME-fil - Hvad er .time-fil? Tiden, hvor filen blev oprettet i Linux",
  "description" : "Lær om TIME-filen og find ud af, hvornår filen blev oprettet i Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-da",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Hvad er en TIME fil?

TIME filformat blev brugt af et websystem kaldet LIGHT, som hjalp brugere med at optage, organisere og dele deres liv. I det væsentlige gemte den en samling af indlæg og repræsenterede en mappe på brugerens livsside i systemet.

## Sådan finder du ud af, hvornår en fil blev oprettet i Linux

I Linux kan du bruge kommandoen `stat` til at finde ud af, hvornår en fil blev oprettet. Sådan kan du gøre det:

Åbn en terminal og skriv følgende kommando:

```
stat <file_path>
```

Udskift `<file_path> ` med stien til den fil, du er interesseret i. For eksempel:

```
stat /path/to/your/file.txt
```

Denne kommando viser forskellige oplysninger om filen, inklusive dens oprettelsestid. Se efter linjen, der starter med Fødsel eller Fil:. Fødselstidspunktet angiver, hvornår filen blev oprettet på filsystemet.

Her er et eksempel på, hvordan output kan se ud:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

I dette eksempel angiver fødselstidspunktet, hvornår filen blev oprettet.

