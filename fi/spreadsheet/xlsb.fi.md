{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Excelin binaarilaskentataulukkotiedosto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Tiedostomuoto-opas tietää, mikä on XLSB-tiedosto ja API:t, jotka voivat luoda ja avata niitä.",
  "title": "Mikä on XLSB-tiedosto?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-fib"
}
},
  "lastmod": "2019-12-10"
}

## Mikä on XLSB-tiedosto?

XLSB-tiedostomuoto määrittää Excelin binaaritiedostomuodon, joka on kokoelma tietueita ja rakenteita, jotka määrittävät Excel-työkirjan sisällön. Sisältö voi sisältää strukturoimattomia tai puolirakenteisia lukutaulukoita, tekstiä tai sekä lukuja että tekstiä, kaavoja, ulkoisia tietoyhteyksiä, kaavioita ja kuvia. Toisin kuin [XLSX](/spreadsheet/xlsx/) (joka perustuu Open XML-tiedostomuotoon), XLSB edustaa binaarista Excel-työkirjatiedostoa. XLSB-tiedostoja voidaan lukea ja kirjoittaa nopeammin, mikä tekee niistä hyödyllisiä suurten tiedostojen käsittelyssä. XLSB:tä käytetään harvoin työkirjojen tallentamiseen, koska XLSX (ja aiemmin [XLS](/spreadsheet/xls/)) ovat yleisimpiä käyttäjän valitsemia tiedostomuotoja työkirjojen tallentamiseen. Se voidaan avata Microsoft Office 2007:llä ja uudemmilla.

## XLSB-tiedostomuodon tekniset tiedot ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. Sittemmin spesifikaatioita on tarkistettu useita kertoja, ja uusin versio teknisistä tiedoista (v 10.0) julkaistiin huhtikuussa 2018. Microsoft on saatavilla julkisesti tekniset tiedot nimellä [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) ja kenen tahansa tulisi tutustua niihin. tiedostojen kirjoittaminen XLSB-tiedostomuodossa.

## XLSB-tiedostorakenne ##

XLSB-tiedosto on paketti, joka koostuu joukosta osia. Nämä osat sisältävät tietoa työkirjan sisällöstä, mukaan lukien työkirjan tiedot ja paketin rakenteen. Jotkut osat sisältävät tietoja, jotka on tallennettu binääritietueiden avulla, jotkut XML-muodossa, kun taas toiset sisältävät tietoja, jotka on tallennettu tavujen binäärivirtana. Jokainen binääritietue sisältää nolla tai useampia strukturoituja kenttiä, jotka sisältävät työkirjan tiedot.

#### Paketti ####

XLSB-paketti on [ZIP](/compression/zip/)-arkisto, jonka tulee sisältää täsmälleen yksi työkirjan osa. Tämän osan on oltava suhteen kohde tässä pakettisuhdeosassa. Työkirjan osa on XLSB-dokumentin aloitusosa.

#### Osa ####

Osa on tavuvirta, johon liittyy sisältötyyppi, joka määrittää osaan tallennetun sisällön luonteen ja tyypin. Jotkut osat tallentavat tiedot binäärimuodossa, kun taas toiset tallentavat tiedot XML-muodossa. Teknisten asiakirjojen [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) -osiossa luetellaan kelvolliset osat, sisältötyypit ja pakolliset/valinnaiset suhteet paketin kaikkien osien välillä.

#### Suhde ####

Lähdettä ja kohderesurssia yhdistää suhde. Suhde voi olla:

**Pakettisuhde:** jossa kohde on osa ja lähde on paketti kokonaisuutena

**Osien välinen suhde:** jossa kohde on osa ja lähde on osa paketissa

**Eksplisiittinen suhde:** jossa resurssiin viitataan lähdeosan sisällöstä viittaamalla suhdeelementin ID-attribuutin arvoon

**implisiittinen suhde** on suhde, joka ei ole eksplisiittinen

**Sisäinen suhde:** jossa kohde on osa pakettia

**Ulkoinen suhde:** jossa kohde on ulkoinen resurssi, joka ei ole paketissa

#### Ennätys ####

Tietue on perusrakennuspalikka, jota käytetään tallentamaan tietoja työkirjan ominaisuuksista. Jokainen binääritietue on muuttuvapituinen tavusarja. Binääritietue koostuu kolmesta osasta:

* tietuetyyppi

* ennätyskoko ja

* tietuetiedot, jotka liittyvät kyseiselle tietuetyypille.


**Tietueen tyyppi:** Tietueen tyyppi näyttää tietueen määrittämän tietueen tyypin. Se määrittää myös tälle tietueelle ominaisen tietuetietojen rakenteen. Kelvolliset tietuetyypit on lueteltu määritysasiakirjan [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) -osiossa. Tietueen tyypin on oltava yksi tai kaksi tavua, ja sen on oltava suurempi tai yhtä suuri kuin 128 ja pienempi kuin 16 384.

**Tietueen koko:** Tietueen koko määrittää tavumäärän, joka määrittää tietuetietojen kokonaiskoon. Tämän arvon TÄYTYY olla yhdestä neljään tavua. Tämän arvon PITÄÄ olla yksi tavu, jos matalan tavun yläbitti on yhtä suuri kuin 0; muuten tämän arvon TÄYTYY olla suurempi kuin yksi tavu. Jos tavujen määrä on suurempi kuin yksi tavu, kunkin peräkkäisen tavun korkea bitti määrittää, käytetäänkö lisätavua. Jos toisen tavun yläbitti on yhtä suuri kuin 1, tämän arvon TÄYTYY käyttää ylimääräistä kolmatta tavua. Jos kolmannen tavun yläbitti on yhtä suuri kuin 1, tämän arvon TÄYTYY käyttää neljättä lisätavua. Neljännen tavun korkea bitti TÄYTYY jättää huomiotta. Arvo koostuu kunkin tavun seitsemästä matalasta bitistä yhdistettynä. Pienet, vähiten merkitsevät bitit sisältyvät ensimmäiseen tavuun, ja jokainen peräkkäinen tavu sisältää korkeamman kertaluvun bittejä kuin edellinen tavu.

**Tietuetiedot:** Tietueen tietokomponentti sisältää kenttiä, jotka vastaavat tiettyä tietuetyyppiä ja muodostavat tietueen loppuosan. Tietueluettelossa lueteltujen tietyn tietuetyypin kenttien järjestys ja rakenne on määritetty tietuetyypin vastaavassa osiossa Tietueissa. Tietueen datakomponentin kokonaiskoon TÄYTYY olla yhtä suuri kuin tietueen koko. Tietueen tietokomponentin kentät voivat sisältää yksinkertaisia arvoja, arvotaulukoita, useiden kenttien rakenteita, kenttätaulukoita ja rakenneryhmiä.

#### XLSB-tietueesimerkki ####

Seuraava tietuetyyppi ja tietuekoko määrittävät **BrtCommentText**-tietueen, jonka koko on 200 tavua:

11111101 00000100 11001000 00000001 [tietuekentät]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, joka on 512. Tietuetyypin arvo on 125 + 512 tai 637, mikä vastaa **BrtCommentText**-tietuetyyppiä. Seuraava tavu on 11001000, joka määrittää pienen arvon 72 ja että tietueen koko vaatii toisen tavun. Toinen tavu on 00000001, joka määrittää suuremman arvon 1 * 128 ja että tietueen koko ei vaadi ylimääräistä tavua. Tietueen koko on 72 + 128 tai 200, mikä määrittää tietuetietokomponentin kokonaiskoon tavuina. Tietueen tietokomponentin kentät määrittää **BrtCommentText**.

## Viitteet ##

* [[MS-XLSB] - Excel (.xlsb) binaaritiedostomuoto](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


