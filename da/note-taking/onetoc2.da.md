{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ONETOC2 - Microsoft OneNote-filformat",
  "description": "Lær om ONETOC2-filformat og API'er, der kan oprette og åbne ONETOC2-filer.",
  "linktitle": "ONETOC2",
  "menu": {
    "docs": {
      "parent": "note-taking",
      "identifier": "note-taking-onetoc-da2"
}
},
  "lastmod": "2019-09-10"
}

## Hvad er ONETOC2? ##

Those who have worked with [Microsoft OneNote](https://products.office.com/en-us/onenote/digital-note-taking-app) application may have noticed the presence of .onetoc2 files in the notebook folder. Microsoft OneNote creates binary .onetoc2 file as Table of Contents for keeping an index about the ordering of different note-taking sections in a notebook. A notebook is a collection of section files that are stored in the same directory. The .onetoc2 file uses a collection of properties to specify settings such as order of sections within the notebook and the color of the notebook.

Når du opretter en notesbog i OneNote 2016, gemmes den automatisk i det nye 2010-2016-filformat. Du skal bruge dette format, hvis du ønsker, at alle funktionerne i OneNote 2016, såsom matematiske ligninger og sammenkædede noter, skal fungere korrekt.

## ONETOC2 filformat ##

The .onetoc2 file format is represented as OneNote Revision Store File Format and is a collection of of structures that specify a revision store organized into cross-referenced object spaces, containing objects with property sets, and containing a transaction log to ensure file integrity across asynchronous writes. Complete specifications for the .onetoc2 file format are available [online](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx) and can be referred to for development of applications.

### Filstruktur ###

En revisionslagerfil SKAL begynde med en **Header**-struktur. Resten af filen er opdelt i blokke af bytes, hvor størrelsen og strukturen af hver blok er specificeret af feltet, der refererer til den. En blok er tilgængelig, hvis den refereres af **Header**-strukturen, eller hvis den refereres af et felt i en anden tilgængelig blok. Data uden for **Header**-strukturen og alle tilgængelige blokke SKAL ignoreres.

Alle strukturer er justeret på 1-byte grænser. Alle heltal er signerede, medmindre andet er angivet. Alle felter er [little-endian](https://msdn.microsoft.com/en-us/library/dd773246(v#office.12).aspx#gt_079478cb-f4c5-4ce5-b72b-2144da5d2ce7), medmindre andet er angivet.

#### Header ####

Headeren af .ONE-filen består af bidder, der indeholder forskellige unikke id'er og felter til repræsentation af filoplysninger som følger:

`guidFileType (16 bytes):` En GUID, der specificerer typen af revisionslagerfilen. SKAL være en af værdierne fra følgende tabel.

|Filformat|Værdi
--- | --- |
|.one|{7B5C52E4-D88C-4DA7-AEB1-5378D02996D3}
|.onetoc2|{43FF2FA1-EFD9-4C76-9EE2-10EA5722765F}

`guidFile (16 bytes):` En GUID, der specificerer identiteten af denne revisionslagerfil. SKAL være globalt unikt.

`guidLegacyFileVersion (16 bytes):` SKAL være {00000000-0000-0000-0000-000000000000} og SKAL ignoreres.

`guidFileFormat (16 bytes):` En GUID, der angiver, at filen er en revisionsbutiksfil. SKAL være {109ADD3F-911B-49F5-A5D0-1791EDC8AED8}.

`ffvLastCodeThatWroteToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filtypen.

|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldest CodeThatHasWrittenToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.


|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvNewestCodeThatHasWrittenToThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.
:


|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

`ffvOldestCodeThatMayReadThisFile (4 bytes):` Et heltal uden fortegn. SKAL være en af værdierne i følgende tabel, afhængigt af filformatet for denne fil.


|Filformat|Værdi
--- | --- |
|.one|0x0000002A
|.onetoc2|0x0000001B

## Referencer ##

* [[MS-ONESTORE] - OneNote-filformat](https://msdn.microsoft.com/en-us/library/dd951288(v#office.12).aspx)

* [Microsoft OneNote - Wikipedia](https://en.wikipedia.org/wiki/Microsoft_OneNote#References)


