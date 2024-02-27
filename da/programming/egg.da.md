{
  "date": "2022-03-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EGG-filformat - Python-distributionsfil",
  "description": "Lær om EGG filformat og API'er, der kan oprette og åbne EGG filer.",
  "linktitle": "EGG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-eg-dag"
}
},
  "lastmod": "2022-03-15"
}

## Hvad er en EGG fil?

En EGG-fil, også kendt som Python-æg, er et ældre distributionsformat Python-distributioner. Det er et [ZIP](/compression/zip/) komprimeret arkiv med .egg-udvidelsen og indeholder Python-applikationens kildefiler sammen med metainformation om distributionen. EGG-filer er alternative til en Windows-eksekverbar [EXE](/executable/exe/)-fil, men er på tværs af platforme. Dette ældre format til Python-distributioner er blevet erstattet med det nyere Wheel (WHL) filformat i begyndelsen af 2010.

## EGG filformat

EGG-filer gemmes som komprimerede ZIP-arkiver. Det betyder, at hvis du erstatter .egg-udvidelsen med .zip, vil du være i stand til at åbne den med standard dekompressionsværktøjer såsom Corel WinZIP, Microsoft Explorer eller RARLAB WinRAR.

EGG-filer kan oprettes ved hjælp af pakken **distutils**, der er tilgængelig af Python. Et andet værktøj, der kan oprette og åbne EGG-filer, er **SetupTools**. EGG-filer kan installeres som en pakke ved hjælp af **easy_install**.

`BEMÆRK - EGG filformat er blevet forældet til fordel for det nye hjul WHL filformat.`

## Reference ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)


