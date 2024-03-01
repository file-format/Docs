{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "AWK-tiedostomuoto - AWK-komentosarjatiedosto",
  "description":"Opi AWK-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata AWK-tiedostoja.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## Mikä on AWK-tiedosto?

AWK-tiedosto on tekstinkäsittelysovellukselle **AWK** luotu komentosarjatiedosto, joka toimitetaan Unix- ja Linux-käyttöjärjestelmien mukana. Se sisältää loogisia ohjeita tekstiin tai tiedoston sisältöön liittyvien toimien suorittamiseksi, kuten tekstin sovittaminen, korvaaminen ja tulostaminen. Tämä auttaa luomaan raportteja ja muotoiltua tekstiä syöttötiedostosta. awk-apuohjelma sijaitsee yleensä hakemistossa /usr/bin/awk useimmissa linux/unix-jakeluissa.

## Kuinka luoda AWK-skripti?

AWK-tiedosto voidaan luoda tai avata missä tahansa tekstieditorissa Linux/Unix-käyttöjärjestelmässä. Uusi AWK-skriptitiedosto voidaan luoda seuraavasti.

```
$ vi script.awk
```

Tämä avaa AWK-tiedoston tekstieditorissa. Kirjoita joitain lauseita tekstieditoriin seuraavasti.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Tämän tekstisisällön ensimmäinen rivi selitetään seuraavasti.

 * \#! – jota kutsutaan nimellä Shebang, joka määrittää tulkin komentosarjan ohjeille
 * /usr/bin/awk – on tulkki
 * -f – tulkin vaihtoehto, käytetään ohjelmatiedoston lukemiseen

## Kuinka suorittaa AWK-skripti?

Tallenna tiedosto ja tee komentosarjasta suoritettava antamalla alla oleva komento:
```
$ chmod +x script.awk
```

Skripti voidaan sitten suorittaa seuraavasti.

```
$ ./script.awk
```

josta saadaan seuraava tulos.

```
Writing my first Awk executable script!
```

## Viite ##

* [Kirjoita komentosarjoja Awk-ohjelmointikielellä](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)


