{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Tee tiedosto - Xcode Makefile -skriptitiedosto",
  "description": "Opi XCode MakeFile Formatista ja sovellusliittymistä, jotka voivat luoda ja avata MakeFile-tiedostoja.",
  "linktitle": "MAKE",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mak-fie"
}
},
  "lastmod": "2020-09-10"
}


## Mikä on MAKE-tiedosto?

MAKE-tiedosto on XCode-skriptitiedosto, joka järjestää koodin kokoamisen. Sitä käytetään ohjelmien kääntämiseen ja linkittämiseen useista lähdekooditiedostoista. Tämä auttaa päättämään, mitkä suuren sovelluksen osat on käännettävä uudelleen, kun sovellus on päivitettävä. Aseta tiedostot suorittamaan useita ohjeita sen mukaan, mitkä tiedostot ovat muuttuneet.

## Esimerkki MAKE-tiedostomuodosta

Seuraava sisältö suoritetaan Make-apuohjelmalla ja tulosteet ovat seuraavat.

```
hello:
	echo "hello world"
```
**Tee tulos**

```
$ make
echo "hello world"
hello world
```

## Viitteet
 * [XCode and Make - Apple Forums](https://developer.apple.com/forums/thread/657458)
 * [Object-C-opas](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

