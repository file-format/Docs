{
  "date": "2019-10-11",
  "keywords": [
"mpx tiedosto",
"mpx tiedostomuoto",
"mikä on mpx-tiedosto",
"tiedosto",
"mpx esimerkki",
"mpx tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX - Microsoft Project Exchange -tiedostomuoto",
  "description": "Opi MPX-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MPX-tiedostoja.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-fix"
}
},
  "lastmod": "2021-05-07"
}

## Mikä on MPX-tiedosto? ##

Tiedosto, jonka tunniste on .mpx, on Microsoft Exchange -tiedostomuoto. Microsoft Project (MSP) on kehittänyt MPX-tiedostomuodon helpottamaan projektitietojen vaihtoa MSP:n ja muiden MPX-tiedostomuotoa tukevien sovellusten välillä, mukaan lukien Primavera Project Planner, Sciforma ja Timerline Precision Estimating. MPX-tiedostojen avulla voit siirtää kaikenlaista tietoa projektista toiseen järjestelmään, kuten yksityiskohtaisia resurssien määritystietoja, kalenteritietoja tai tietoja Project Info -valintaikkunasta.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. MPX-tiedostojen luomisen tuki on kuitenkin lopettanut Microsoft Project 2000:n julkaisun, ja versiot Microsoft Project 2010:een asti tukevat vain MPX-lukua. MPX-tiedostomuotoa ei tueta MSP 2010:tä uudemmissa versioissa.

## MPX-tiedostomuoto ##

Tässä osiossa on yleiskuvaus MPX-tiedostojen teknisistä tiedoista. Täydelliset tekniset tiedot löytyvät tästä [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)-artikkelista, ja niihin voi tutustua tarkemmin.

### Records ###

MPX-tiedoston tietue sisältää projektin tiedot. On olemassa erilaisia tietueita, joissa jokaisella tietueella on oma järjestys. Jokainen tietuetyyppi tunnistetaan sen tietuenumerosta. MPX-tiedostossa on oltava File Creation -tietuetyyppi. Muun tyyppiset tietueet eivät ole pakollisia. Seuraavassa taulukossa näkyvät kaikki tietuetyypit, niiden tietuenumerot ja kunkin tyypin tietueiden määrä MPX-tiedostossa. Tietueen sisällyttämisen MPX-tiedostoon on noudatettava taulukon järjestystä, ja kommentit on lisättävä mihin tahansa.

|Tietueen nimi|Tietueen numero|Tietueiden enimmäismäärä
---|---|---|
|Tiedoston luonti (pakollinen)|ei mitään|1
|Valuutta-asetukset|10|1
|Oletusasetukset|11|1
|Päivämäärä- ja aika-asetukset|12|1
|Peruskalenterin määritelmä|20|250
|Peruskalenterin aukioloajat|25| 7 per Base Calendar Definition -tietue
|Peruskalenterin poikkeus|26| 250 per Base Calendar Definition tietue
|Projektin otsikko|30|1
|Tekstiresurssitaulukon määritelmä|140|1- (Tai voit käyttää Numeerisen resurssitaulukon määritelmätietuetta)
|Numeerinen resurssitaulukon määritelmä|41|1
|Resurssi|50|9 999
|Resurssihuomautukset|51| 1 per resurssitietue
|Resurssikalenterin määritelmä|55| 1 per resurssitietue
|Resurssikalenterin aukioloajat|56| 7 per resurssikalenteri
|Resurssikalenterin poikkeus| 57|250 per resurssikalenteri
|Teksti Tehtävätaulukon määritelmä|60|1 (Tai voit käyttää numeerista tehtävätaulukon määritelmätietuetta)
|Numeerinen tehtävätaulukon määritelmä|61|1
|Tehtävä|70|9
|Tehtävämuistiinpanot|71| 1 per tehtävätietue
|Toistuva tehtävä|72| 1 per tehtävätietue
|Resurssimääräys|75| 100 per tehtävätietue
|Osautustyöryhmäkentät|76| 1 per tehtävätietue
|Projektien nimet|80|500
|DDE- ja OLE-asiakaslinkit|81|500
|Kommentit|0|rajaton

### Tiedostorakenne ###

MPX-tiedosto koostuu edellä mainituista tietueista, jotka on järjestetty ennalta määrätyllä tavalla tiedoston sisään. Näistä tietuetyypeistä keskustellaan seuraavasti:

**File Creation Record (FCR):** Tämä on pakollinen tietue, jonka tarkoituksena on tunnistaa:

* Tiedostomuoto (MPX)

* Listaa tiedostossa käytetty erotinmerkki

* Tiedoston luomiseen käytetty ohjelma ja versionumero

* Tiedostossa käytetyn MPX-tiedostomuodon versionumero

* Tiedoston luomiseen käytetty koodisivu


Tämän on oltava tiedoston ensimmäinen tietue. Kun viedään Microsoft Projectista, luettelon erotinmerkki määritetään Windowsin Ohjauspaneelin Alueasetukset-kohdassa. FCR-tietue sisältää seuraavat kentät:

* MPX, jota seuraa välittömästi luettelon erotinmerkki

* Ohjelman nimi/tunniste

* Tiedoston versionumero

* Koodisivu (850, 437, MAC, ANSI)


Tietue voi sisältää esimerkiksi tietoja **MPX, Microsoft Project, 3.0**, joka määrittää, että tässä MPX-tiedostossa käytetään pilkkua luettelon erotinmerkkinä. Tiedostossa käytetyn MPX-muodon versio on viety Microsoft Projectin versiosta 3.0.

**Valuuttaasetukset** Tämä tietue, jonka tietuenumero on 10, määrittää Asetukset-valintaikkunan valuuttavaihtoehtojen asetukset. Jos tämä tietue ei sisälly, käytetään Asetukset-valintaikkunan nykyisiä asetuksia. Tuhansien ja desimaalien erottimet määritetään Windowsin Ohjauspaneelin Alueasetukset-kohdassa.
Tähän tietueeseen sisältyvät kentät ovat:

* Valuutan symboli

* Symbolin sijainti (0 # jälkeen, 1 # ennen, 2 # jälkeen välilyönnillä, 3 # ennen välilyöntiä)

* Valuutan numerot (0,1,2)

* Tuhansien erotin

* Desimaalierotin


**Esimerkki:** 10,$,1,2,,.
Tämä esimerkki määrittää, että valuuttaarvot sisältävät dollarin merkin ($) ennen niitä, että kaksi numeroa lisätään desimaalipilkun jälkeen, että pilkkua käytetään erottelemaan tuhansia ja että pistettä käytetään desimaalipilkuna. Koska luettelon erotinmerkki sisältyy Tuhansien erotin -kenttään, kenttä on lainausmerkeillä.

**Oletusasetukset:** Tämä tietue, jonka tietuenumero on 11, määrittää oletusasetukset Asetukset-valintaikkunassa. Jos kestoa ei ole määritetty, oletuskestoyksikkö on asetettava oikeita kestoyksiköiden laskelmia varten. Jos tämä tietue ei sisälly, käytetään Asetukset-valintaikkunan nykyisiä asetuksia.
Tähän tietueeseen sisältyvät kentät ovat:

* Oletuskeston yksiköt (0 # minuuttia, 1 # tuntia, 2 # päivää, 3 # viikkoa)

* Oletuskestotyyppi (0 # ei kiinteä, 1 # kiinteä)

* Oletustyöyksiköt (0 # minuuttia, 1 # tuntia, 2 # päivää, 3 # viikkoa)

* Oletustunnit/päivä

* Oletustunnit/viikko

* Oletusvakiohinta

* Oletusylityökorko

* Tehtävän tilan päivittäminen Resurssin tilan päivitykset (0 # ei, 1 # kyllä)

* Jaetut keskeneräiset tehtävät (0 # ei, 1 # kyllä)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Tähän tietueeseen sisältyvät kentät ovat:

* Päivämäärätilaus (0 # kuukausi/päivä/vuosi, 1 # päivä/kuukausi/vuosi, 2 # vuosi/kuukausi/päivä)

* Aikamuoto (0 # 12 tuntia, 1 # 24 tuntia)

* Oletusaika (minuuttien määrä puolenyön jälkeen)

* Päivämäärän erotin

* Aikaerotin

* 0:00 - 11:59 Teksti

* 12:00-23:59 Tekstiviesti

* Päivämäärän muoto (0 -14)*

* Pylvästekstin päivämäärämuoto (0 -194)*


**Peruskalenterin määritelmä:** Nämä tietueet, joiden tietuenumero on 20, määrittelevät peruskalenterit ja niiden viikon työ- ja vapaapäivät. Oletusasetuksia käytetään, jos päivälle ei ole merkintää. Oletusasetukset ovat maanantaista perjantaihin työpäivinä ja lauantaina ja sunnuntaina vapaapäivinä. Tässä tietueessa Nimi-kenttä on pakollinen. Jokaiselle päivälle merkintä 0 osoittaa, että päivä on vapaapäivä, ja merkintä 1 osoittaa, että päivä on työpäivä.
Tähän tietueeseen sisältyvät kentät ovat:

* Nimi

* Sunnuntai

* Maanantai

* Tiistai

* Keskiviikkona

* Torstai

* Perjantai

* Lauantai


**Kalenterin perustunnit:** Nämä tietueet, joiden tietuenumero on 25, määrittävät viikonpäivien työajat, jos ne poikkeavat oletusasetuksista. Oletustyötunnit ovat 8.00–12.00 ja 13.00–17.00 Jokainen peruskalenterin tuntitietue viittaa edelliseen Base Calendar Definition -tietueeseen. Jopa seitsemän näistä tietueista voi seurata jokaista Base Calendar Definition -tietuetta.

* Viikonpäivä (1-7, missä 1 # sunnuntai ja 7 # lauantai)

* Ajasta 1

* Aika 1

* Ajasta 2

* Aika 2

* Ajasta 3

* Aika 3


**Peruskalenterin poikkeus:** Nämä tietueet, joiden tietuenumero on 26, määrittelevät poikkeukset kahdessa edellisessä tietuetyypissä määritellyille päiville ja tunteille. Jopa 250 näistä tietueista voi seurata jokaista Base Calendar Definition -tietuetta. Nämä tietueet on lueteltava kronologisessa järjestyksessä. Jos poikkeus on yksi päivä, voit jättää Päivämäärä-kentän tyhjäksi. Jos aikoja ei ole ilmoitettu, käytetään oletusaikoja 8:00-12:00 ja 13:00-17:00.
Tähän tietueeseen sisältyvät kentät ovat:

* Päivämäärästä

* Tähän mennessä

* Epätyö/työ (0 # ei-työssä, 1 # työssä)

* Ajasta 1

* Aika 1

* Ajasta 2

* Aika 2

* Ajasta 3

* Aika 3


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Tähän tietueeseen sisältyvät kentät ja välilehdet ovat:

* Projekti-välilehti

* Yhtiö

* Johtaja

* Kalenteri (standardi käytössä, jos merkintää ei ole)

* Aloituspäivämäärä (joko tämä kenttä tai seuraava kenttä lasketaan tuodulle tiedostolle aikataulun alkamisasetuksen mukaan)

* Päättymispäivämäärä

* Aikataulu alkaen (0 # aloitus, 1 # maali)

* Nykyinen päivämäärä*

* Kommentit

* Kustannus

* Peruskustannukset

* Todellinen kustannus

* Tehdä työtä

* Perustyö

* Varsinainen työ

* Tehdä työtä

* Kesto*

* Perustason kesto*

* Todellinen kesto

* Valmistusprosentti

* Perustason aloitus

* Perustason viimeistely

* Todellinen aloitus

* Todellinen viimeistely

* Aloita varianssi

* Valmis varianssi

* Aihe

* Tekijä

* Avainsanat


**Tekstiresurssitaulukon määritelmä**: Tässä tietueessa luetellaan resurssikentät järjestyksessä, joita tuodaan tai viedään. Tuotujen tiedostojen nimien on vastattava Microsoft Projectissa käytettyjä kenttien nimiä. Viedyille tiedostoille tämä tietue tulee resurssien vientitaulukosta. Joko tätä tietuetta tai numeerisen resurssitaulukon määritelmätietuetta on käytettävä. Kun viedään Microsoft Projectista, molemmat tietueet sisältyvät.

**Numeerisen resurssitaulukon määritelmä:** Tässä tietueessa luetellaan resurssikentät järjestyksessä, joita tuodaan tai viedään, käyttämällä numeroita nimien sijaan. Tämä on vaihtoehtoinen menetelmä kuhunkin resurssitietueeseen sisältyvien resurssikenttien tunnistamiseen, ja se on hyödyllinen määritettäessä vieraan kielen tuotteella luotua MPX-tiedostoa.

**Resurssi:** Nämä tietueet sisältävät tiedot jokaisesta tuodavasta tai vietävästä resurssista. Jokainen resurssitietue kuvaa yhtä resurssia. Kun tuot tietoja, tekstiresurssitaulukon määritystietueessa tai numeerisen resurssitaulukon määritystietueessa määritetään sisällytettävät kentät. Kun viet tietoja, mukana olevat kentät ovat ne, jotka on lueteltu resurssien vientitaulukossa.

**Resurssitietueet:** Nämä tietueet sisältävät huomautuksia välittömästi edeltävästä resurssitietueesta. Uudella rivillä muistiinpanossa käytetään ASCII-merkkiä 127. Jos huomautuksessa on luettelon erotinmerkki, kirjoita huomautus lainausmerkkeihin.

**Resurssikalenterin määritelmä:** Nämä tietueet määrittävät työpäivät välittömästi edeltävässä resurssitietueessa määritetylle resurssille. Jos tuoduille tiedostoille ei ole merkintää Peruskalenterin nimi -kentässä, käytetään Standardia. Tietyn päivän merkinnän puuttuminen tarkoittaa, että päivä on asetettu oletusarvoon (2). Jos resurssikalenterin määrittelytietueita ei ole, resurssin peruskalenterina käytetään vakiokalenteria, oletuksena päivinä. Jokaiselle päivälle merkintä 0 osoittaa, että päivä on vapaapäivä, 1 tarkoittaa, että päivä on työpäivä, ja 2 määrittää, että oletusarvoa käytetään.

**Resurssikalenterin tunnit:** Nämä tietueet määrittävät resurssin työajat, jotka eroavat resurssin käyttämästä peruskalenterista. Nämä tietueet koskevat tätä tietuetta välittömästi edeltävää Resource Calendar Definition -tietuetta. Jopa seitsemän näistä tietueista voi seurata kutakin Resource Calendar Definition -tietuetta.

**Resurssikalenterin poikkeus:** Nämä tietueet määrittävät poikkeukset kahdessa edellisessä tietuetyypissä määritettyihin päiviin ja tunteihin. Jopa 250 näistä tietueista voi seurata kutakin Resource Calendar Definition -tietuetta. Nämä tietueet on lueteltava kronologisessa järjestyksessä. Jos poikkeus on vain yksi päivä, voit jättää Päivämäärä-kentän tyhjäksi. Jos aikoja ei ole ilmoitettu, käytetään oletusaikoja 8:00-12:00 ja 13:00-17:00.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Numeerinen tehtävätaulukon määritelmä:** Tämä tietue luettelee tuodut tai viedään tehtäväkentät järjestyksessä numeroiden sijaan. Tämä on vaihtoehtoinen menetelmä jokaiseen tehtävätietueeseen sisältyvien tehtäväkenttien tunnistamiseen, ja se on hyödyllinen määriteltäessä vieraalla kielellä luotua MPX-tiedostoa.

**Tehtävä:** Nämä tietueet sisältävät tiedot jokaisesta tuotavasta tai vietävästä tehtävästä. Jokainen tehtävätietue kuvaa yhden tehtävän. Kun tuot tietoja, tekstitehtävätaulukon määritystietueessa tai numeerisen tehtävätaulukon määritystietueessa määritetään sisällytettävät kentät. Kun viet tietoja, mukana tulevat kentät ovat ne, jotka on lueteltu tehtävän Vienti-taulukossa.

**Tehtävän huomautukset:** Nämä tietueet sisältävät huomautuksia välittömästi edeltävästä tehtävätietueesta. Käytä ASCII-merkkiä 127 ilmaisemaan nuotin uusi rivi. Jos huomautuksessa on luettelon erotinmerkki, kirjoita huomautus lainausmerkkeihin.

**Resurssien määritys**: Nämä tietueet sisältävät tietoja edellisessä tehtävätietueessa määritellylle tehtävälle osoitetuista resursseista. Jos yhdistät tiedostoja ja haluat säilyttää resurssien määritystiedot, sinun on sisällytettävä tiedot MPX-tiedostoon. Jos yhdistät, kaikki yhdistettyjen tehtävien nykyiset tehtävät poistetaan. Jos yhdistät tiedostoja yksilöllisten tunnuksien perusteella, resurssit määritetään käyttämällä yksilöllisiä resurssitunnuksia tunnuksien sijaan.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Jos käytät Workgroup-ominaisuuksia, sinun on sisällytettävä tämä tietue varmistaaksesi, että mitään tietoja ei menetetä.

**Projektien nimet:** Näissä tietueissa luetellaan kaikki projektiin tallennetut DDE-linkkien nimet.

**DDE- ja OLE-asiakaslinkit:** Näissä tietueissa luetellaan projektiin johtavat DDE-linkit.

**Kommentit:** Näitä tietueita voidaan käyttää kommenttien lisäämiseen tiedostoon, ja ne voivat näkyä missä tahansa kohdassa tiedostossa. Jokaisen kommentit-tietueen on alettava 0.

## Ongelmia MPX-tiedoston avaamisessa ##

Tässä on luettelo yleisistä ongelmista, joita saattaa ilmetä ja jotka voivat aiheuttaa MPX-muodon toimintahäiriöitä:

 *   Tukiohjelmiston puuttuminen
 *   Vioittunut tiedosto
 *   Viruksen saastuttama tiedosto
 *   Järjestelmässä ei ole pääsyoikeutta tiedostojen avaamiseen
 *   Vanhentunut asema järjestelmässäsi
 *   Tiedoston laajennus nimetään uudelleen

## Viitteet ##

* [MPX – Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


