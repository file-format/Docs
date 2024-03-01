{
  "date": "2021-05-25",
  "keywords": [
"DML",
"DML-tiedosto",
"DML-tiedostomuoto",
"DML-tiedostotyyppi",
"tiedosto",
"tyyppi",
"mikä on DML-tiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DML - DynaScript HTML -tiedosto",
  "description": "Opi DML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DML-tiedostoja.",
  "linktitle": "DML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-dm-fil"
}
},
  "lastmod": "2021-05-25"
}

## Mikä on DML-tiedosto?

Tiedosto, jonka pääte on .dml, on DyanScriptillä luotu Web-skriptisivun kooditiedosto. DynaScript on dynaaminen [HTML](/web/html/)-skriptikieli, joka on yhteensopiva ECMAScriptin kanssa ja tarjoaa suurimman osan samoista ominaisuuksista kuin muutkin komentosarjakielet. Se on samanlainen kuin ColdFusion-koodi ja Microsoft Active Server Pages (ASP) -koodi. DML-tiedostoja voidaan avata ja tarkastella tavallisissa verkkoselaimissa, jotka ovat samanlaisia kuin muut HTML-sivut.

## DML-tiedostomuoto

DML-tiedostot luodaan vain tekstitiedostomuodossa, ja ne voidaan avata tekstieditorilla koodin tarkastelemiseksi. Koodin kirjoittamista DML-komentosarjakielellä voidaan käyttää HTML:n luomiseen dynaamisesti palvelinpuolen isännöidyillä DML-sivuilla. DynaScriptit on rakennettu seuraavista kielielementeistä:


 * SCRIPT-tunniste – Nämä upotetaan asiakirjoihin HTML-kommentteina. HTML-kommentti on merkitty \
 * Literaalit - Nämä ovat DynaScript-tiedostojen kiinteitä arvoja. Esimerkkejä näistä ovat kokonaisluvut, kuten s 123 , 0x3F , 0123, liukulukuluvut, kuten 456.789 , 3.2e-8, Boolen, kuten tosi tai epätosi, ja merkkijono, kuten The rain in Spain
 * Muuttujat - DynaScript-muuttujia ei tarvitse määrittää tai määrittää kiinteään tietotyyppiin. Muuttujalla on oltava arvo, ennen kuin voit käyttää sitä lausekkeessa; muussa tapauksessa luodaan ajonaikainen varoitus.
 * Lausekkeet - Nämä ovat muuttujien, kirjaimellisten arvojen, operaattoreiden ja muiden lausekkeiden yhdistelmiä. Tehtävälausekkeen oikea puoli on lauseke.
 * Operaattorit - Nämä käyttävät yhtä tai useampaa lauseketta, joita kutsutaan operandiksi. Nämä voivat olla joko ternäärisiä, binäärisiä tai unaarisia: ternääriset operaattorit toimivat kolmella lausekkeella, binäärioperaattorit kahdella lausekkeella ja unäärioperaattorit yhdellä.
 * Lausunnot - Nämä ohjaavat komentosarjavirtaa, käsittelevät objekteja ja yleistä ohjelmointia. Yleensä nämä lauseet noudattavat standardia C- ja Java-syntaksia. Esimerkkejä ovat if-else, do-while -silmukat, vaihto, tauko, jatka jne. kuten mikä tahansa muu komentosarjakieli.
* Funktiot - Funktiot, kuten kaikki muutkin skriptikielet, antavat sinun kapseloida joukon ohjeita kerran dokumenttiin funktiona ja käyttää sitä sitten useita kertoja koko asiakirjassa (kutsumalla funktiota). DynaScript tukee myös toimintoja.

* Objektit – DynaScript on oliopohjainen ja tukee "objekteja" ja perusolio-käsitteitä, kuten kapselointi, polymorfismi ja perinnöllisyys.


