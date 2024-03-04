{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME failas – kas yra .time failas? Laikas, kai failas buvo sukurtas Linux",
  "description" : "Sužinokite apie TIME failą ir laiką, kada failas buvo sukurtas Linux sistemoje",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-lt",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Kas yra TIME failas?

TIME failo formatą naudojo žiniatinklio sistema, pavadinta LIGHT, kuri padėjo vartotojams įrašyti, tvarkyti ir dalytis savo gyvenimu. Iš esmės jis saugojo pranešimų kolekciją ir atstojo aplanką vartotojo gyvenimo puslapyje sistemoje.

## Kaip sužinoti, kada failas buvo sukurtas Linux

Linux galite naudoti komandą stat, kad sužinotumėte, kada buvo sukurtas failas. Štai kaip tai galite padaryti:

Atidarykite terminalą ir įveskite šią komandą:

```
stat <file_path>
```

Pakeiskite `<file_path> ` su keliu į jus dominantį failą. Pavyzdžiui:

```
stat /path/to/your/file.txt
```

Ši komanda parodys įvairią informaciją apie failą, įskaitant jo sukūrimo laiką. Ieškokite eilutės, kuri prasideda Gimimas arba Failas:. Gimimo laikas nurodo, kada failas buvo sukurtas failų sistemoje.

Štai pavyzdys, kaip gali atrodyti išvestis:

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

Šiame pavyzdyje Gimimo laikas nurodo, kada failas buvo sukurtas.

