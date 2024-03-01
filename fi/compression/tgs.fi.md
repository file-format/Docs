{
  "date": "2019-10-11",
  "keywords": [
"tgs-tiedosto",
"tgs tiedostomuoto",
"mikä on tgs-tiedosto",
"tiedosto",
"tgs esimerkki",
"tgs tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGS - Telegram-animoitu tarratiedostomuoto",
  "description": "Opi TGS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata TGS-tiedostoja.",
  "linktitle": "TGS",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-fis"
}
},
  "lastmod": "2021-04-02"
}

## Mikä on TGS-tiedosto?

Tiedosto, jonka laajennus on .tgs, on animoitu tarratiedosto, jonka esitteli monialustainen viestipalvelu [Telegram](https://core.telegram.org/stickers#animated-stickers). Viestintäsovellusten käyttäjät käyttävät animoituja tarroja lähettääkseen paranneltua ja elävämpää sisältöä viesteissä toisin kuin staattinen grafiikka, joka on still-kuvia. Telegram käytti alun perin tiedostomuotoa [WEBP](/image/webp/) still-kuvatarroille. TGS-tiedostomuoto voi tallentaa animaatiodataa korkeammalla resoluutiolla ja pienemmällä tiedostokoolla verrattuna staattisiin WEBP-tarroihin. TGS-tiedostoja voidaan avata käyttämällä sovelluksia, kuten Telegram, 7-zip, Apple Archive Utility ja Corel WinZip.

## TGS-tiedostomuoto

Telegram esitteli TGS-tiedostomuodon jo heinäkuussa 2019, joka perustuu Lottie-kirjastoon. TGS-tiedosto koostuu [JSON](/web/json/) tekstistä, joka viedään Adobe After Effectsin animaatiosta. Viety JSON-teksti pakataan gzip-pakkauksella, joka pienentää tiedoston kokoa. Tekstitiedostoa koskevat JSON-tiedot tallennetaan tekstitiedostoon, josta tulee korkeiden pakkausnopeuksien perusta.

### TGS-tarrojen tekniset tiedot

TGS-tiedostomuoto asettaa tiettyjä rajoituksia animoitujen TGS-tarrojen luomiseen. TGS-animoitu tiedosto:

 * Tarran/kankaan koon on oltava 512 x 512 pikseliä.
 * Tarraesineitä ei saa jättää kankaalle.
 * Animaation pituus ei saa ylittää 3 sekuntia.
 * Kaikki animaatiot on oltava silmukassa.
 * Tarran koko ei saa ylittää 64 kt Bodymovinissa renderöinnin jälkeen.
 * Kaikkien animaatioiden tulee olla 60 ruutua sekunnissa.

### Esimerkki TGS JSON -teksti

Animoitu esimerkkitarra sisältää seuraavan JSON-tekstisisällön purettuna.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Viitteet ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)


