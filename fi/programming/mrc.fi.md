{
  "date": "2021-09-14",
  "keywords": [
"mrc",
"tiedosto",
"laajennus",
"tiedosto muoto",
"mrc-toteutus",
"Ohjelmointiopas",
"mrc esimerkki",
"mIRC",
"mIRC-skriptikieli",
"INI-tiedostot",
"mSL-skriptikieli",
"mIRC kieli",
"mIRC-skriptit",
"skriptikieli"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "MRC - mIRC Script Language File",
  "description": "Opi MRC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MRC-tiedostoja.",
  "linktitle": "MRC",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-mr-fic"
}
},
  "lastmod": "2021-09-14"
}

## Mikä on MRC-tiedosto?

mIRC on komentosarjakieli, joka on upotettu IRC-asiakkaaksi (Internet Relay Chat) Windows-käyttöjärjestelmään. Se tarjoaa suojan roskapostilta henkilökohtaiseen ja kanavakäyttöön. Tämä mIRC-skriptikieli mahdollistaa dialogiikkunoiden luomisen, jotta käyttäjäyhteensopivuus olisi parempi. Tiedostot, jotka sisältävät komentosarjoja, useimmiten vain tekstimuodossa, tallennetaan MRC-tunnisteella tai tiedostoina {{HYPERLINKKI}}. Tämän kielen funktiot tunnetaan komentoina ja tunnisteina (kun ne palauttavat arvon).

mIRC-kieli mahdollistaa useiden komentosarjatiedostojen lataamisen kerralla. Toisaalta yksi tiedosto voi aiheuttaa sen, että toista ei enää käytetä, kun se ladataan samanaikaisesti. Komennot tallennetaan ja ne voivat olla IRC:ssä automaattisesti. Tällä kielellä käytetyt komennot ja aliakset eivät sisällä minkään merkkien etusijaa.

mIRC:tä käytetään laajalti saamaan botit hallitsemaan kanavaa automaattisesti, mutta sitä voidaan muokata myös mSL-skriptikielellä. Se voi esitellä monia uusia ominaisuuksia, kuten makroja, musiikin toistokykyä, pieniä makroja ja toimintoja, peruspelejä tai pienten sovellusten käyttöä.


## Lyhyt historia ##

Tämän skriptikielen kehitti ensimmäisen kerran Khaled Adam Bey vuonna 1995. Khalid loi myös skriptikielen suunnittelun. Tämän kielen kohteena oli tapahtumaohjattu ohjelmointi. Aluksi tämän ohjelmointikielen tiedostojen tiedostotunniste oli .mrc ja .ini. Lisäksi se on kehitetty patentoidun ohjelmiston lisenssillä.

## Tekniset tiedot ##

Jotkut toiminnot ovat mukautettuja komentosarjoja tällä mIRC-kielellä, ja ne tunnetaan aliaksina. Kun nämä aliakset palauttavat arvoja, niitä kutsutaan mukautetuiksi tunnisteiksi. Kaikki tämän mIRC-kielen sisältämät muuttujat kirjoitetaan dynaamisesti. mIRC-skriptit käyttävät sigilejä. Toinen tämän skriptikielen ominaisuus on ponnahdusikkunat. Käyttäjät voivat soittaa ponnahdusikkunoihin yksinkertaisesti valitsemalla ne. Kaukosäätimet on määritetty tiettyihin tapahtumiin. Kaukosäätimiä kutsutaan, kun suhteellinen tapahtuma tapahtuu.

Välilyönnillä eroteltuja tunnuksia käytetään tämän kielen jokaisen koodirivin katkaisemiseen. mIRC-tiedostoissa käytetään joitain muita suosittuja laajennuksia, kuten MDX (mIRC Dialog Extension) ja DCX (Dialog Control Extension). Molemmat ovat dialogilaajennuksia ja ovat suhteellisen suositumpia. Kielirakenteisiin viitataan tämän skriptikielen nimikkeistössä. mIRC-kieli sisältää erilaisia komentosarjakielen näkökohtia, kuten paikallisia ja globaaleja muuttujia, binäärimuuttujia, hash-taulukoita ja tiedostojen käsittelyä.


## MRC-tiedostomuodon esimerkki ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Viite ##

* [MIRC - Wikipedia](https://en.wikipedia.org/wiki/MIRC_scripting_language)




