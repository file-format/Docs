{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME-fil - Vad är .time-fil? Tid då filen skapades i Linux",
  "description" : "Lär dig om TIME-filen och ta reda på tidpunkten när filen skapades i Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-sv",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Vad är en TIME fil?

TIME-filformatet användes av ett webbsystem som heter LIGHT, som hjälpte användare att spela in, organisera och dela sina liv. I huvudsak lagrade den en samling inlägg och representerade en mapp på användarens livssida i systemet.

## Hur man tar reda på när en fil skapades i Linux

I Linux kan du använda kommandot `stat` för att ta reda på när en fil skapades. Så här kan du göra det:

Öppna en terminal och skriv följande kommando:

```
stat <file_path>
```

Byt ut `<file_path> ` med sökvägen till filen du är intresserad av. Till exempel:

```
stat /path/to/your/file.txt
```

Detta kommando kommer att visa olika information om filen, inklusive dess skapelsetid. Leta efter raden som börjar med Födelse eller Arkiv:. Födelsetiden anger när filen skapades i filsystemet.

Här är ett exempel på hur utgången kan se ut:

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

I det här exemplet anger födelsetiden när filen skapades.

