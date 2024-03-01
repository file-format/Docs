{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR-tiedosto",
"tiedosto",
"PAR tiedostopääte",
"laajennus",
"tiedosto"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR-tiedostomuoto - FMS-lentokoneen parametrien tiedosto",
   "description":"Opi PAR-muodosta ja API-liittymistä, jotka voivat luoda ja avata PAR-tiedostoja.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"game-par-fi",
         "parent":"game"
}
},
   "lastmod":"2023-07-18"
}

## Mikä on PAR-tiedosto?

PAR-tiedostoa, joka tunnetaan yleisesti lentokoneparametritiedostona, käyttää erityisesti FMS (Flying-Model-Simulator), Windows-käyttöjärjestelmille suunniteltu lentosimulaatiopeli. Sen tarkoitus on tallentaa tärkeitä tietoja lentokoneen geometriasta ja fyysisistä ominaisuuksista, mukaan lukien ominaisuudet, kuten massa, painopiste ja hitausmomentit. Nämä PAR-tiedostot ovat tärkeitä räätälöityjen lentokoneiden luomisessa pelin sisällä, jolloin pelaajat voivat simuloida ja lentää omia ainutlaatuisia virtuaalilentokoneita tarkalla ja realistisella fysiikalla.

## PAR-tiedostomuoto - lisätietoja

FMS on lentokoneissa käytettävä ohjelmistojärjestelmä, joka auttaa navigoinnissa, lennon suunnittelussa ja autopilottitoiminnoissa. FMS Aircraft Parameters -tiedosto, josta käytetään usein lyhennettä PAR-tiedosto, sisältää erityisiä tietoja, jotka liittyvät lentokoneen suorituskykyominaisuuksiin ja lennonhallintaan.

Tämä PAR-tiedostomuoto on erityinen lentosimulaattoriohjelmistoille, kuten sellaisille, joita käytetään suosituissa lentosimulaattoriohjelmissa, kuten Microsoft Flight Simulator tai X-Plane. Tiedosto sisältää erilaisia parametreja ja tietoja, jotka määrittelevät simulaattorissa olevan virtuaalisen lentokoneen käyttäytymisen, suorituskyvyn ja järjestelmät.

FMS Aircraft Parameters -tiedosto sisältää yleensä tietoja, kuten:

- **Ilma-aluksen tekniset tiedot:** Tämä sisältää tietoja lentokoneen fyysisistä ominaisuuksista, kuten painosta, mitoista, polttoainetilavuudesta ja moottorin teknisistä tiedoista.

- **Lennon suorituskykytiedot:** Se sisältää tietoja, jotka liittyvät lentokoneen suorituskykyyn lennon eri vaiheissa, mukaan lukien nousu, risteily, laskeutuminen ja lasku. Näitä voivat olla nousunopeudet, polttoaineenkulutus, nopeusrajoitukset ja muut suorituskykyyn liittyvät parametrit.

- **Autopilotin asetukset:** Tiedosto voi määrittää automaattiohjauksen käyttäytymisen ja rajoitukset lentokoneelle, mukaan lukien autopilottitilat, korkeus- ja suuntarajoitukset sekä ohjausherkkyydet.

- **Navigointitiedot:** Se voi sisältää navigointiin liittyviä parametreja, kuten lentokoneen navigointitietokannan, mukaan lukien reittipisteet, lentoreitit ja lentokenttätiedot.

Nämä PAR-tiedostot ovat yleensä lentokonekehittäjien tai kolmannen osapuolen harrastajien luomia ja ylläpitämiä, jotka pyrkivät tarjoamaan realistisia ja tarkkoja simulaatiokokemuksia lentosimulaattoriohjelmistossa. Tiedostot ladataan sitten simulaattoriin simuloidun lentokoneen käyttäytymisen ja suorituskykyominaisuuksien määrittämiseksi.

## PAR-tiedostojen, 3D-mallien, tekstuurien ja äänien rooli lentosimulaatiopeleissä

PAR-tiedostot ovat vain yksi osa lentokoneen kokonaistietopakettia. PAR-tiedostojen lisäksi on useita muita tiedostoja, jotka yhdessä myötävaikuttavat lentokoneen täydelliseen esittämiseen pelissä. Nämä lisätiedostot sisältävät yleensä 3D-mallitiedostoja, pintakuviobittikarttoja ja ääniä.

- **3D-mallitiedostot:**

Lentosimulaatiopelit vaativat yksityiskohtaisia 3D-malleja lentokoneen visuaaliseksi esittämiseksi virtuaaliympäristössä. Nämä 3D-mallit koostuvat erilaisista osista, kuten rungosta, siiveistä, laskutelineistä ja muista lentokoneen monimutkaisista osista. 3D-mallitiedostot tarjoavat visuaalisen rakenteen ja geometrian, joka tarvitaan kuvaamaan tarkasti lentokoneen ulkonäköä ja muotoa pelissä.

- **Tekstuuribittikartat:**

Pintakuviobittikarttoja, joita kutsutaan myös tekstuuriksi tai kuvakartoiksi, käytetään lisäämään väriä, pintayksityiskohtia ja visuaalista realismia 3D-malleihin. Nämä pintakuviotiedostot sisältävät tietoja, kuten maalikuvioita, tarroja, logoja ja pintakuvioita, kuten metallia, muovia tai kangasta. Lisäämällä pintakuviobittikarttoja 3D-malleihin, pelin lentokoneita voidaan parantaa visuaalisesti, mikä johtaa mukaansatempaavampaan ja visuaalisesti houkuttelevampaan kokemukseen.

-**Äänet:**

Äänitiedostot ovat olennainen osa lentosimulaatiopelejä, koska ne tarjoavat kuulopalautetta ja realistisuutta. Nämä tiedostot sisältävät yleensä moottorin ääniä, ohjaamon ääniä, ympäristövaikutuksia, kuten tuuli tai sade, ja muita lentokonekohtaisia äänimerkkejä. Sisällyttämällä asianmukaiset äänitiedostot, peli voi luoda tarkasti uudelleen simuloituun lentokoneeseen liittyvän ääniympäristön, mikä parantaa entisestään yleistä uppoamista.

Vaikka PAR-tiedosto sisältää erityisiä tietoja, jotka liittyvät lentokoneen suorituskykyyn ja lennonhallintaan, se on yhdistelmä PAR-tiedostoja, 3D-mallitiedostoja, tekstuuribittikarttoja ja äänitiedostoja, jotka yhdessä herättävät virtuaalisen lentokoneen henkiin lentosimulaatiopelissä. Jokaisella tiedostolla on ainutlaatuinen tarkoitus luoda kattava ja realistinen esitys lentokoneesta, mikä takaa pelaajille mukaansatempaavan kokemuksen.

## Kuinka avata PAR-tiedosto?

PAR-tiedostoja avaavia ohjelmia ovat mm

- Lentävä mallisimulaattori (FMS)
- Microsoft Flight Simulator
- X-Plane

## Viitteet
* [Flying-Model-Simulator (FMS)](https://modelsimulator.com/)

* [Microsoft Flight Simulator](https://en.wikipedia.org/wiki/Microsoft_Flight_Simulator)



