{
  "date": "2019-10-11",
  "keywords": [
"sh tiedosto",
".sh-tiedosto",
"laajennus",
"muoto",
"sh-tiedosto esimerkki",
"sh tiedostomuoto",
"kuinka ajaa sh-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH - Bash Shell Script -tiedosto",
  "description": "Opi SH-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata SH-tiedostoja.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-fih"
}
},
  "lastmod": "2021-05-21"
}

## Mikä on SH-tiedosto?

Tiedosto, jonka tarkenne on .sh, on komentosarjakielen komentotiedosto, joka sisältää Unix-kuoren suorittaman tietokoneohjelman. Se voi sisältää joukon komentoja, jotka suoritetaan peräkkäin suorittamaan toimintoja, kuten tiedostojen käsittelyä, ohjelmien suorittamista ja muita vastaavia tehtäviä. Käyttäjä suorittaa nämä komentoriviliittymästä tai erässä useiden toimintojen suorittamiseksi samanaikaisesti. Skriptitiedostoja voidaan avata tekstieditoreilla, kuten Notepad, Notepad++, Vim, Apple Terminal ja muilla vastaavilla Windows-, MacOS- ja Linux-käyttöjärjestelmillä.

## SH-tiedostomuoto

SH-tiedostot kirjoitetaan pelkällä tekstillä määritettyä syntaksia noudattaen. Nämä komentosarjatiedostot tukevat:

 * `Kommentit` - Kommentit alkavat #-merkillä, ja komentotulkki ohittaa ne.
 * Pikanäppäimet - Näitä voidaan käyttää komennon nimeämiseen uudelleen lyhyen ja helpon suorittamisen vuoksi.
 * Erätyöt - Useita komentoja voidaan suorittaa automaattisesti, jotka muutoin olisi syötettävä manuaalisesti. Tämä poistaa tarpeen odottaa, että käyttäjä käynnistää sarjan jokaisen vaiheen.
 * Yleistäminen - Yksinkertaisia silmukoita käyttämällä saadaan aikaan paljon enemmän yleistämistä sellaisille toiminnoille kuin kuvien muuntaminen yhdestä paikasta toiseen.

## Esimerkki SH-tiedostosta

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Kuinka ajaa SH-tiedostoa?
SH-tiedostot toimivat yleensä Linuxissa, jopa Windowsissa sinun on muodostettava yhteys Linux-päätteeseen käyttämällä ohjelmistoja, kuten Putty, ajaaksesi sh-tiedostoja. Seuraavassa on vaiheet SH-tiedoston suorittamiseksi Linux-päätteessä.

1. Avaa Linux-pääte ja siirry hakemistoon, jossa SH-tiedosto sijaitsee.
2. Aseta komentosarjallesi suoritusoikeus käyttämällä chmod-komentoa (jos sitä ei ole jo asetettu).
3. Suorita komentosarja jollakin seuraavista tavoista
	1. `./tiedostonimi.sh`
	2.  `sh tiedostonimi.sh`
	3.  `bash script-name-here.sh`

## Viitteet

* [Bashscripting for Beginners](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


