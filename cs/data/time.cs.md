{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "TIME soubor - Co je soubor .time? Čas, kdy byl soubor vytvořen v Linuxu",
  "description" : "Přečtěte si o souboru TIME a zjistěte čas, kdy byl soubor vytvořen v Linuxu",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-cs",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Co je soubor TIME?

Formát souboru TIME používal webový systém s názvem LIGHT, který uživatelům pomáhal zaznamenávat, organizovat a sdílet jejich životy. V podstatě ukládal sbírku příspěvků a představoval složku na stránce života uživatele v systému.

## Jak zjistit, kdy byl soubor vytvořen v Linuxu

V Linuxu můžete pomocí příkazu `stat` zjistit, kdy byl soubor vytvořen. Můžete to udělat takto:

Otevřete terminál a zadejte následující příkaz:

```
stat <file_path>
```

Nahradit `<file_path> ` s cestou k souboru, který vás zajímá. Například:

```
stat /path/to/your/file.txt
```

Tento příkaz zobrazí různé informace o souboru, včetně času jeho vytvoření. Vyhledejte řádek, který začíná slovy Narození nebo Soubor:. Čas Narození označuje, kdy byl soubor vytvořen na souborovém systému.

Zde je příklad toho, jak může výstup vypadat:

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

V tomto příkladu čas Narození označuje, kdy byl soubor vytvořen.

