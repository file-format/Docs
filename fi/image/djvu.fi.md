{
  "date": "2019-10-11",
  "keywords": [
"djvu tiedosto",
"djvu tiedostomuoto",
"mikä on djvu-tiedosto",
"tiedosto",
"djvu esimerkki",
"djvu tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DJVU tiedostomuoto",
  "description": "Opi DJVU-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DJVU-tiedostoja.",
  "linktitle": "DJVU",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-djv-fiu"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on DJVU-tiedosto?

DjVu, joka lausutaan nimellä déjà vu, on grafiikkatiedostomuoto, joka on tarkoitettu skannatuille asiakirjoille ja kirjoille, erityisesti sellaisille, jotka sisältävät tekstin, piirustuksen, kuvien ja valokuvien yhdistelmän. Sen on kehittänyt AT&T Labs. Se käyttää useita tekniikoita, kuten tekstin ja taustakuvien kuvakerroserottelua, progressiivista latausta, aritmeettista koodausta ja bitonaalisten kuvien häviöllistä pakkausta. Koska DJVU-tiedosto voi sisältää pakattuja, mutta korkealaatuisia värikuvia, valokuvia, tekstiä ja piirroksia ja se voidaan säästää pienemmässä tilassa, sitä käytetään verkossa e-kirjoina, käsikirjoina, sanomalehtinä, muinaisina asiakirjoina jne.

DjVu voidaan luokitella ylivoimaiseksi vaihtoehdoksi {{HYPERLINKKI}}:lle. DjVu:hun liittyvät tiedostotunnisteet ovat .DJVU tai .DJV. DjVu voi saavuttaa noin 5–10 paremman pakkaussuhteen kuin nykyiset menetelmät, kuten [JPEG](/image/jpeg/) ja [GIF](/image/gif/) värillisissä asiakirjoissa ja 3–8 kertaa paremmat kuin [TIFF](/image/tiff/) mustavalkoisissa asiakirjoissa. Skannatut 300 DPI:n ja täysväriset asiakirjat jopa 25 megatavuun asti voidaan pakata 30–100 kt:iin. Samoin mustavalkoisia asiakirjoja voidaan pakata 5–30 kilotavuun asti. Keskimääräinen HTML-sivu voi olla jopa 50 kt, joten nämä asiakirjat voidaan ladata verkkoon ilman ongelmia.

## Lyhyt historia ##

The DjVu technology was developed in AT&T labs by [Yann LeCun](https://en.wikipedia.org/wiki/Yann_LeCun), [Léon Bottou](https://en.wikipedia.org/wiki/L%C3%A9on_Bottou), Patrick Haffner, and Paul G from 1996 to 2001. DjVu-tiedostomuoto on käynyt läpi useita versioita, joista viimeisin on vuodelta 2005.


|Versio|Julkaisupäivä|Huomautuksia
---|---|---|
|1–19|1996–1999|Nämä ovat kehitysversiot.
|20|huhtikuu 1999|Yksisivu muutettiin monisivuiseksi.
|23|heinäkuu 2002|CID-kappale
|24|helmikuu 2003|LTAnno pala
|21|Syyskuu 1999|Epäsuora tallennusmuoto vaihdettu. Tekstihakutaso lisättiin.
|22|huhtikuu 2001|Sivun suunta, väri JB2
|25|toukokuuta 2003|NAVM-kappale. Tuki DjVu-kirjanmerkeille lisättiin.
|26|huhtikuu 2005|Teksti-/rivimerkinnät

## DjVu-tiedostomuoto ##

DjVu documents are IFF85 files. The structure provides a hierarchy of containers which holds information in a DjVu file. These containers are also called “Chunks”. Chunk type and Chunk ID describes how the chunk is used. There is a 4byte header followed by IFF structure. The first four bytes of a DjVu file are 0x41 0x54 0x26 0x54. Tässä osiossa käsitellään erilaisia DjVu-dokumentteja ja niitä vastaavia osia, joista ne koostuvat.


|Chunk ID|Käyttö
---|---|
|FORM|Yhdistelmäpala, jossa on FORM-kappaleen neljä ensimmäistä datatavua, jotka ovat toissijaisia tunnisteita.
|FORM:DJVM|Monisivuinen DjVu-dokumentti. Komposiittikappale, joka sisältää DIRM-kappaleen.
|FORM:DJVU|Yksisivuinen DjVu-dokumentti. Yhdistelmäpala, joka sisältää palat, jotka muodostavat sivun djvu-asiakirjassa.
|FORM:DJVI|jaettu DjVu-tiedosto, joka sisältyy INCL-kappaleen kautta. Jaetut merkinnät ja muotosanakirja.
|FORM:THUM|Yhdistelmäpala, joka sisältää TH44-palat, jotka ovat upotettuja pikkukuvia.
|DIRM|Monisivuisten asiakirjojen sivunimitiedot.
|NAVM|Kirjanmerkin tiedot
|ANTa, ANTz|Merkinnät, jotka sisältävät sekä aloitusnäkymän asetukset että päällekkäiset hyperlinkit, tekstilaatikot jne.
|TXTa, TXTz|Unicode Teksti- ja asettelutiedot.
|Djbz|Jaettu muototaulukko.
|Sjbz|BZZ pakattu JB2-bitonaalinen data, jota käytetään maskin tallentamiseen.
|FG44|IW44-tiedot, joita käytetään etualan tallentamiseen
|BG44|IW44-tiedot, joita käytetään taustan tallentamiseen
|TH44|IW44-tiedot, joita käytetään upotettujen pikkukuvien tallentamiseen
|WMRM|JB2-tiedot tarvitaan vesileiman poistamiseen
|FGbz|Väri JB2-tiedot. Tarjoaa värin kullekin vastaavassa Sjbz-kappaleessa (blit tai muoto?).
|INFO|Tietoja DjVu-sivusta
|INCL|Sisältyneen FORM:DJVI-osan tunnus.
|BGjp|JPEG-koodattu tausta
|FGjp|JPEG-koodattu etualalla
|Smmr|G4-koodattu maski

### DJVU-pakkaus

Yksittäinen kuva jaetaan useisiin eri kuviin, minkä jälkeen jokainen kuva pakataan erikseen. DjVu-tiedoston luomista varten kuva erotetaan ensin kolmeen kuvaan, taustaan, etualaan ja maskikuvaan. Tyypillisesti tausta- ja etualan kuvat ovat alhaisemman resoluution värikuvia; mutta maskikuva on korkeamman resoluution kuva ja tyypillisesti teksti tallennetaan sinne. Erottamisen jälkeen etu- ja taustakuvat pakataan aallokepohjaisella pakkausalgoritmilla IW44, kun taas maskikuva pakataan toisella menetelmällä nimeltä JB2.

JB2-koodausmenetelmä eliminoi suuren osan tekstikuvan redundanssista tunnistamalla sivulla identtiset muodot, kuten useat merkin esiintymät tietyssä kirjasimessa. JB2 koodaa ensin kunkin ainutlaatuisen muodon bittikartan hyödyntämällä samanlaisten muotojen välistä redundanssia. Sitten se koodaa paikat, joissa kukin muoto näkyy sivulla. Sekä JB2 että IW44 luottavat uudentyyppiseen mukautuvaan binääriaritmeettiseen kooderiin nimeltä ZP-kooderi, joka puristaa jäljellä olevan redundanssin muutaman prosentin sisällä Shannonin rajasta. ZP-kooderi on mukautuva ja nopeampi kuin muut likimääräiset binaariaritmeettiset kooderit.

## Viitteet ##

* [DjVu - Wikipedia](https://en.wikipedia.org/wiki/DjVu)

* [DjVu File Format](https://www.cuminas.jp/docs/techinfo/DjVu3Spec.pdf)

