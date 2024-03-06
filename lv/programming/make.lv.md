{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Make File — Xcode Makefile skripta fails",
  "description": "Uzziniet par XCode MakeFile formātu un API, kas var izveidot un atvērt MakeFile failus.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-lve"
}
},
  "lastmod": "2020-09-10"
}


## Kas ir MAKE fails?

MAKE fails ir XCode skripta fails, kas organizē koda apkopošanu. To izmanto, lai apkopotu un saistītu programmas no vairākiem pirmkoda failiem. Tas palīdz izlemt, kuras lielas lietojumprogrammas daļas ir jāpārkompilē, kad lietojumprogramma ir jāatjaunina. Lieciet failiem izmantot virkni norādījumu, lai tie tiktu palaisti atkarībā no tā, kādi faili ir mainīti.

## MAKE faila formāta piemērs

Tālāk norādītais saturs tiek izpildīts, izmantojot utilītu Make, un izvadi ir šādi.

```
hello:
	echo "hello world"
```
**Izveidot izvadi**

```
$ make
echo "hello world"
hello world
```

## Atsauces
 * [XCode un Make — Apple Forums](https://developer.apple.com/forums/thread/657458)
 * [Object-C rokasgrāmata](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

