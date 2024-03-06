{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "LAIKA fails — kas ir .time fails? Laiks, kad fails tika izveidots operētājsistēmā Linux",
  "description" : "Uzziniet par TIME failu un uzziniet laiku, kad fails tika izveidots operētājsistēmā Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-lv",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Kas ir TIME fails?

TIME faila formātu izmantoja tīmekļa sistēma LIGHT, kas palīdzēja lietotājiem ierakstīt, organizēt un dalīties savā dzīvē. Būtībā tas saglabāja ziņu kolekciju un pārstāvēja mapi lietotāja dzīves lapā sistēmā.

## Kā uzzināt, kad fails tika izveidots operētājsistēmā Linux

Operētājsistēmā Linux varat izmantot komandu stat, lai uzzinātu, kad fails tika izveidots. Lūk, kā to izdarīt:

Atveriet termināli un ierakstiet šādu komandu:

```
stat <file_path>
```

Aizstāt `<file_path> ` ar ceļu uz jūs interesējošo failu. Piemēram:

```
stat /path/to/your/file.txt
```

Šī komanda parādīs dažādu informāciju par failu, tostarp tā izveides laiku. Meklējiet rindiņu, kas sākas ar Birth vai File:. Dzimšanas laiks norāda, kad fails tika izveidots failu sistēmā.

Šeit ir piemērs tam, kā varētu izskatīties izvade:

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

Šajā piemērā dzimšanas laiks norāda, kad fails tika izveidots.

