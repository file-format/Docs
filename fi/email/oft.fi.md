{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT - Microsoft Outlookin sähköpostimallitiedosto",
  "description": "Opi OFT-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OFT-tiedostoja.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-fit"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on OFT-tiedosto?

Tiedostot, joiden tiedostotunniste on .oft, ovat mallitiedostoja, jotka on luotu Microsoft Outlookilla. Viestimalleille asetettua esimuotoiltua asettelua käytetään sitten yleisiä tietoja sisältävien sähköpostien lähettämiseen ajan säästämiseksi. Tällaisia tiedostoja voidaan luoda luomalla uusi sähköposti, lisäämällä tarvittavat tiedot ja käyttämällä Microsoft Outlookin avattavaa Tallenna toimistomallina (.oft) -valikkoa. Käyttäjät voivat avata OFT-tiedostot kaksoisnapsauttamalla sitä ja se avautuu kyseisessä järjestelmässä liittyvässä sovelluksessa.

## OFT-tiedostorakenne ##

.OFT-tiedostomuoto käyttää pohjassaan tiedostomuotoa [MSG](/email/msg/). Ainoa ero on, että usein tiedostoilla on CLSID_TEMPLATEMESSAGE ({0006F046-0000-0000-C000-00000000000046}) tallennusluokkaan (WriteclassSTG), kun taas MSG-tiedostot käyttävät CLSID_MAILMESTAGE ({00020D0B-0000-0000-000-0000000046}).

CFB_3-muoto on MSG-tiedoston perusta. Paradigma perustuu tallennus- ja virtauskonsepteihin, melko lähellä hakemistoja ja tiedostoja. Siksi suuri ero edellisessä on koko hierarkia, joka on pakattu erilliseen tiedostoon, jota kutsutaan yhdistelmätiedostoksi. Objektit muodostavat viestitiedostot ja koostuvat yhdestä ominaisuudesta tai sen kokoelmista. Tämä ominaisuus helpottaa sovellusten tallentamista monimutkaisen, jäsennellyn tiedon yhteen tiedostoon. Tämä muoto määrittää myös useita tallennusvälineitä, joista jokainen edustaa Viesti-objektia pääkomponenttina. Nämä varastot sisältävät useita virtoja, jotka edustavat kyseisen komponentin ominaisuutta. Myös varaston sisäkkäin sijoittaminen on mahdollista.

### OFT-ominaisuudet

.msg-tiedoston ylimmällä tasolla varastot sisältävät virtoja, jotka tallentavat niihin ominaisuuksia. Kiinteistöt voidaan luokitella seuraavasti:

* Kiinteä pituus ominaisuuksia

* Muuttuva pituus ominaisuuksia

* Moniarvoisia ominaisuuksia


Luokasta riippumatta ominaisuus on joko merkitty tai nimetty. Nimetyille kiinteistöille vaaditaan kuitenkin sopivia kartoitustietoja niiden kartoitusmuistin määrittämänä.

### OFT-tallennustilat

Tallennustilat ovat Viesti-objektin avainkomponentit. MSG-tiedostomuoto ilmoittaa seuraavat tallennustilat:

### Ylimmän tason rakenne

Viestiobjekti edustaa Msg-tiedostomuodon koko ylätasoa. Riippuen tyypistä, ominaisuuksista, vastaanottaja- ja liiteobjektien lukumäärästä, viestiobjektilla voi olla eri virtavarasto sen vastaavassa .MSG-tiedostossa.

#### Suhde muihin rakenteisiin

MSG/OFT-tiedostomuodolla on seuraavat suhteet muihin rakenteisiin:

* .msg-tiedoston perusta on Compound File Binary File Format.

* Tämä muoto käyttää Message and Attachment Object Protocol -protokollan käyttämiä ominaisuuksia.


## Viitteet

* [[MS-OXMSG]: Outlook MSG -tiedostomuoto](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


