{
  "date": "2019-10-11",
  "keywords": [
"ico-tiedosto",
"ico-tiedostomuoto",
"mikä on ico-tiedosto",
"tiedosto",
"ico esimerkki",
"ico tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO - Kuvatiedostomuoto",
  "description": "Opi ICO-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata ICO-tiedostoja.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-fio"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on ICO-tiedosto?

ICO-laajennuksella varustetut tiedostot ovat kuvatiedostotyyppejä, joita käytetään sovelluksen kuvakkeina {{HYPERLINKKI}}. Niitä on saatavana eri kokoisina, eri väreillä ja resoluutiolla näytön vaatimusten mukaan. Toinen samanlainen kuvatiedostomuoto Microsoft Windowsissa on [CUR](/image/cur/) kohdistimen esittämiseen ja määrittää hotspotin kuvan otsikossa. MacOS:ssa ICNS-tiedostomuodot palvelevat samaa tarkoitusta kuin ICO-tiedostot. Useat verkkosivustot ja sovellukset tarjoavat mahdollisuuden luoda tällaisia tiedostoja ja muuntaa muita kuvamuotoja, kuten [BMP](/image/bmp/), [PNG](/image/png/) jne. kuvaketiedostomuotoon. Virallinen IANA:ssa rekisteröity Internet-mediatyyppi ICO-tiedostoille on image/vnd.microsoft.icon.

## Lyhyt historia ##

Icons were introduced with the launch of Microsoft Windows 1.0. Nämä olivat kooltaan 32x32 ja olivat yksivärisiä. Win32:n tulon myötä otettiin käyttöön tuki todellisissa väreissä oleville ikonikuville, joiden mitat ovat jopa 256 x 256 pikseliä. Windows XP tarjosi ensimmäisenä tuen 32-bittisille värikuvakekuville, mikä mahdollistaa puoliläpinäkyvien alueiden, kuten varjojen, anti-aliasoinnin ja lasimaisten tehosteiden lisäämisen kuvakkeeseen. Microsoft suosittelee Windows XP:lle vain 48 × 48 pikselin kuvakkeiden kokoa. Windows Vista lisäsi 256 × 256 pikselin kuvakenäkymän Resurssienhallintaan sekä tuen pakatulle [PNG](/image/png/)-muodolle. Käyttäjille, jotka käyttävät korkeampaa resoluutiota ja korkeaa DPI-tiloja, suositellaan suurempia kuvakemuotoja (kuten 256 × 256).

## ICO-tiedostomuoto ##

Yksi ICO-tiedosto koostuu yhdestä tai useammasta pienestä kuvasta, joiden koko ja värisyvyys on useita. Erikokoisten kuvien läsnäolo on tarkoituksenmukaista skaalausta varten eri näytön resoluutioilla. Kaikki ICO/CUR-tiedostojen arvot esitetään tavujärjestyksessä [little-endian](https://en.wikipedia.org/wiki/Little-endian).

ICO-tiedosto koostuu kuvakkeen otsikosta, kuvakehakemistosta,

|Kenttä|Kuvaus
---|---|
|Icon Header|Tallennaa yleistä tietoa ICO-tiedostosta.
|Hakemisto[1..n]|Tallennaa yleistä tietoa jokaisesta tiedoston kuvasta.
|Icon #1|todelliset tiedot ensimmäiselle kuvalle vanhassa AND/XOR DIB-muodossa tai uudemmassa PNG-muodossa
|...|
|Kuvake #n|Viimeisen kuvakekuvan tiedot

### Otsikko ###

|Offset|Koko (tavuina)|Tarkoitus
---|---|---|
|0|2|Varattu. Täytyy aina olla 0.
|2|2|Määrittää kuvatyypin: 1 kuvakkeen (.ICO) kuvalle, 2 kohdistimen (.CUR) kuvalle. Muut arvot ovat virheellisiä.
|4|2|Määrittää tiedostossa olevien kuvien määrän.

### Hakemisto ###

ICO-tiedoston sisältämä hakemisto, joka esitetään ICONDIR-rakenteena, sisältää ICONDIRECTORY-rakenteen jokaiselle tiedoston kuvalle. Samaa seuraa peräkkäinen lohko kaikista kuvan bittikarttatiedoista. Tämä on alla olevan kuvan mukainen.

|Offset|Koko|Kuvaus
---|---|---|
|0 (0)|1|Leveys, tulee olla 0, jos 256 pikseliä
|1 (1)|1|Korkeus, tulee olla 0, jos 256 pikseliä
|2 (2)|1|Värimäärän tulee olla 0, jos enemmän kuin 256 väriä
|3 (3)|1|Varattu, pitäisi olla 0
|4 (4)|2|Väritasojen tulee olla .ICO-muodossa 0 tai 1 tai X-hotspotin .CUR-muodossa.
|6 (6)|2|Bittiä pikseliä kohden .ICO-muodossa tai Y-hotspot .CUR-muodossa
|8 (8)|4|Bittikarttatietojen koko tavuina.
|12 (C)|4|Siirtymä tiedostossa.

## Viitteet ##

* [ICO - Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


