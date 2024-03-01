{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Opi KIT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata KIT-tiedostoja.",
  "title" : "KIT-tiedostomuoto - CodeKit-tiedosto",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit-fi",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## Mikä on KIT-tiedosto?

Tiedosto, jonka tunniste on .kit, on HTML-tiedosto, joka luodaan ohjelmointikielisovelluksella [CodeKit](https://codekitapp.com/). Se sisältää tuonteja ja muuttujia olemassa olevien [HTML](/web/html/)-tiedostojen lisäksi, mikä tekee siitä ihanteellisen staattisille sivustoille. CodeKit kokoaa KIT-tiedostot HTML-muotoon, jota voidaan helposti käyttää staattisina verkkosivustotiedostoina.

## KIT tiedostomuoto

KIT-tiedostot ovat HTML-tiedostoja, jotka sisältävät lisäksi tuontia ja muuttujia. Nämä tallennetaan pelkkinä tekstitiedostoina ja ne voidaan avata millä tahansa tekstieditorilla tai web-tiedostoeditorilla.

### KIT-tiedostojen tuonti

Lähes minkä tahansa tyyppisiä tiedostoja voidaan tuoda Kit-tiedostoon. Seuraavassa on tuontisyntaksi, jota käytetään tiedostojen tuomiseen .kit-tiedostoon.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Kun tuonti lisätään KIT-tiedostoon ja tallennetaan, se korvataan tuotavan tiedoston tekstillä. Voit myös käyttää @include-näppäintä @import sijaan.

### Useita tuontia KIT-tiedostossa

Voit myös tuoda useamman kuin yhden tiedoston kerralla käyttämällä pilkuilla eroteltua luetteloa:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Viitteet

* [Mikä Kit on?](https://codekitapp.com/help/kit/)


