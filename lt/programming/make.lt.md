{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Make File – Xcode Makefile scenarijaus failas",
  "description": "Sužinokite apie XCode MakeFile formatą ir API, kurios gali kurti ir atidaryti MakeFile failus.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-lte"
}
},
  "lastmod": "2020-09-10"
}


## Kas yra MAKE failas?

MAKE failas yra XCode scenarijaus failas, organizuojantis kodo kompiliavimą. Jis naudojamas programoms kompiliuoti ir susieti iš kelių šaltinio kodo failų. Tai padeda nuspręsti, kurias didelės programos dalis reikia perkompiliuoti, kai programą reikia atnaujinti. Leiskite failams paleisti vadovautis keliomis instrukcijomis, atsižvelgiant į tai, kokie failai pasikeitė.

## MAKE failo formato pavyzdys

Toliau pateiktas turinys vykdomas naudojant Make paslaugų programą, o išėjimai yra tokie.

```
hello:
	echo "hello world"
```
**Padaryti išvestį**

```
$ make
echo "hello world"
hello world
```

## Nuorodos
 * [XCode and Make – Apple forumai](https://developer.apple.com/forums/thread/657458)
 * [Object-C vadovas](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

