{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "keywords": [
"SWF",
"tiedosto",
"laajennus",
"muoto",
"videomuoto",
"Mikä on SWF-tiedosto",
"swf-tiedostomuoto",
"swf-tiedostosoitin",
"kuinka avata swf-tiedosto"
],
  "title": "SWF-tiedosto - Shockwave Flash Movie -tiedostomuoto",
  "description": "Opi, mikä on SWF-tiedosto ja API:t, jotka voivat luoda ja näyttää, kuinka SWF-tiedosto avataan.",
  "linktitle": "SWF",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-sw-fif"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on SWF-tiedosto?

SWF-tiedosto on animaatiotiedosto, joka on luotu Adobe Flashilla. Se voi sisältää erilaisia elementtejä, kuten tekstiä, vektorikuvia, rasterikuvia, toimintoskriptejä, objekteja, kuten ympyröitä, viivoja, neliöitä ja suorakulmioita animaation luomiseksi. SWF-tiedostot järjestävät nämä multimediakohteet kehyksiksi, joita voidaan toistaa eri kehyksillä sekunnissa (fps). SWF tarkoittaa lyhyttä verkkotiedostoa, mutta sillä tunnetaan myös Shockwave-muoto.

Sovelluksia, jotka pystyivät *avamaan SWF-tiedostoja**, olivat Adobe Flash Player (nyt lopetettu) ja Eltima Elmedia Player.

## SWF-tiedostomuoto – lisätietoja

SWF-tiedostot tallennettiin binääritiedostoina levylle. SWF-tiedostomuotoa käytettiin kehittämään animaatioita ja pelejä, jotka voitiin upottaa verkkosivustoille ja pelata itsenäisesti. Se tuki myös videoita ja ääniä, jotka antoivat kehittäjille paljon vaihtoehtoja luoda interaktiivisia multimediasovelluksia. SWF-tiedostoja voi toistaa verkkoselaimissa, joihin on asennettu Adobe Shockwave. Adobe Flash lopetettiin joulukuussa 2020 sen puutteiden ja tietoturvaongelmien vuoksi.

## SWF-tiedostomuodon lyhyt historia

SWF-tiedostomuodon on alun perin suunnitellut FutureWave Software, jotta se näyttää animaatioita, joiden tarkoituksena on toimia soitinohjelmistolla missä tahansa järjestelmässä, jossa on hitaammat verkkoyhteydet, pitäen samalla tiedostokoon pienenä. Joulukuussa 1996 Macromedia omisti FutureWaven ja muutettiin Macromedia Flash 1.0:ksi.

In 2005, Macromedia was acquired by Adobe, who announced the SWF as a part of its open source project in 2008. Samana vuonna Adobe julkaisi koodin maailman suosituille verkkokoneille, jotta ne voivat indeksoida SWF-tiedostoja. Koska SWF-tiedostot näyttävät kuitenkin muodostuvan vakiomuodoksi Flash-sisällön julkaisemiseen Internetissä, SWF on muutettu tarkoittamaan pientä verkkomuotoa.

## SWF-tiedostorakenne

Polku on SWF:n graafinen peruselementti, joka on peruselementtien segmenttien sarja yksinkertaisista viivoista Bezier-käyriin. Nämä yksinkertaiset elementit auttavat myös tekemään muita primitiivisiä, kuten kuutioita, ellipsejä ja jopa tekstejä. SWF:n graafiset primitiivit ovat samankaltaisia muiden muotojen, kuten SVG:n ja MPEG-4 BIFS:n, graafisten elementtien kanssa.

Muoto sallii myös luetteloiden näyttämisen ja jo määritettyjen elementtien uudelleenkäytön/uudelleennimeämisen. SWF:n binaarivirtausmuotoa voidaan verrata QuickTime-atomeihin, joka on samanlainen tagin, koon ja hyötykuorman suhteen. Binäärisuoramuoto antaa vanhemmille pelaajille mahdollisuuden ohittaa ei-tuettua sisältöä. Vaikka SWF:n alkuperäiset versiot rajoittuivat tarjoamaan vektorigrafiikkaa ja kuvia, uudet versiot sallivat myös ääni- ja videosisällön.

A new, low-level 3D API of the Flash Player named “Stage3D” was introduced in version 11. Tämä API oli suunniteltu OpenGL:n tai Direct3D:n vastineeksi. Stage3D määrittää värit matalan tason kielellä nimeltä Adobe Graphics Assembly Language (AGAL). Seuraavassa on muutamia SWF-tiedostomuodon perustietotyyppejä.

### Koordinaatit

XY-koordinaatit SWF-tiedostomuodossa tallennetaan kokonaislukuina ja mitataan yksikössä, jota kutsutaan twipiksi. Twip koostuu 1/20 loogisesta pikselistä. Looginen pikseli ja näytön pikseli ovat samat, kun tiedostoa toistetaan ilman 100 %:n skaalausta.

### Kokonaislukutyypit ja tavujärjestys

SWF-tiedostomuodossa sallitaan 8-, 16-, 32- ja 64-bittiset etumerkityt ja etumerkitttömät kokonaisluvut. Little-endian tavujärjestystä käytetään kokonaislukuarvojen tallentamiseen. Vaikka bittijärjestys on tavuissa, se tallennetaan big-endianissa. Kaikkien kokonaislukuarvojen tulee olla tavuissa tasattuja. Etumerkilliset kokonaisluvut esitetään käyttämällä perinteisiä 2's -komplementtibittikuvioita.

### Kiinteän pisteen numerot

SWF-tiedostomuoto tukee kahta tyyppiä kiinteän pisteen numeroita eli 32- ja 16-bittisiä.

### Liukulukuluvut

SWF 8 ja uudemmat versiot käyttävät kolmen tyyppisiä liukulukulukuja (FLOAT, FLOAT 16, DOUBLE), jotka ovat yhteensopivia IEEE Standard 754 liukulukutyyppien kanssa.

### Koodatut kokonaisluvut

SWF 9 ja uudemmat tukevat yhden tyyppisiä koodattuja kokonaislukuja vaihtelevalla tavumäärällä.

## Viitteet

* [SWF-tiedostomuoto](https://en.wikipedia.org/wiki/Swf)


