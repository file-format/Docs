{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Lav fil - Xcode Makefile Script-fil",
  "description": "Lær om XCode MakeFile Format og API'er, der kan oprette og åbne MakeFile-filer.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-dae"
}
},
  "lastmod": "2020-09-10"
}


## Hvad er en MAKE fil?

En MAKE-fil er en XCode-scriptfil, der organiserer kompilering af kode. Det bruges til at kompilere og linke programmer fra flere kildekodefiler. Denne hjælper med at bestemme, hvilke dele af en stor applikation, der skal genkompileres, når applikationen skal opdateres. Få filer til at bruge en række instruktioner til at køre, afhængigt af hvilke filer der er ændret.

## GØR Eksempel på filformat

Følgende indhold udføres ved hjælp af Make-værktøjet, og output er som fulgt.

```
hello:
	echo "hello world"
```
**Lav output**

```
$ make
echo "hello world"
hello world
```

## Referencer
 * [XCode and Make - Apple-fora](https://developer.apple.com/forums/thread/657458)
 * [Object-C Guide](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

