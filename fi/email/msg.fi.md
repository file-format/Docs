{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSG - Microsoft Outlookin sähköpostimuoto",
  "description": "Opi MSG-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata MSG-tiedostoja.",
  "linktitle": "MSG",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ms-fig"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on MSG-tiedosto?

MSG is a file format used by [Microsoft Outlook](https://products.office.com/en-us/outlook/email-and-calendar-software-microsoft-outlook?rtc#1) and Exchange to store email messages, contact, appointment, or other tasks. Such messages may contain one or more email fields, with the sender, recipient, subject, date, and message body, or contact information, appointment particulars, and one or more task specifications. The properties that constitute the Message object, including are also a part of the MSG file.  MSG file has headers, main message body, and hyperlinks as plain ASCII text. MSG files are also suitable with the programs that need Microsoft's Messaging Applications Programming Interface (MAPI).

## MSG tiedostorakenne

CFB_3-muoto on MSG-tiedoston perusta. Paradigma perustuu tallennus- ja virtauskonsepteihin, melko lähellä hakemistoja ja tiedostoja. Siksi suuri ero edellisessä on koko hierarkia, joka on pakattu erilliseen tiedostoon, jota kutsutaan yhdistelmätiedostoksi. Objektit muodostavat viestitiedostot ja koostuvat yhdestä ominaisuudesta tai sen kokoelmista. Tämä ominaisuus helpottaa sovellusten tallentamista monimutkaisen, jäsennellyn tiedon yhteen tiedostoon. Tämä muoto määrittää myös useita tallennusvälineitä, joista jokainen edustaa Viesti-objektia pääkomponenttina. Nämä varastot sisältävät useita virtoja, jotka edustavat kyseisen komponentin ominaisuutta. Myös varaston sisäkkäin sijoittaminen on mahdollista.

## Mapi-ominaisuudet

.msg-tiedoston ylimmällä tasolla varastot sisältävät virtoja, jotka tallentavat niihin ominaisuuksia. Kiinteistöt voidaan luokitella seuraavasti:

* Kiinteä pituus ominaisuuksia

* Muuttuva pituus ominaisuuksia

* Moniarvoisia ominaisuuksia


Luokasta riippumatta ominaisuus on joko merkitty tai nimetty. Nimetyille kiinteistöille vaaditaan kuitenkin sopivia kartoitustietoja niiden kartoitusmuistin määrittämänä.

## Varastot

Tallennustilat ovat Viesti-objektin avainkomponentit. MSG-tiedostomuoto ilmoittaa seuraavat tallennustilat:

## Huipputason rakenne

Viestiobjekti edustaa MSG-tiedostomuodon koko ylätasoa. Riippuen tyypistä, ominaisuuksista, vastaanottaja- ja liiteobjektien lukumäärästä, viestiobjektilla voi olla eri virtavarasto sen vastaavassa .MSG-tiedostossa.

### Suhde muihin rakenteisiin

Msg-tiedostomuodolla on seuraavat suhteet muihin rakenteisiin:

* .msg-tiedoston perusta on Compound File Binary File Format.

* Tämä muoto käyttää Message and Attachment Object Protocol -protokollan käyttämiä ominaisuuksia.


## Skenaariot MSG-muotojen välttämiseksi

Viestiobjekti voidaan jakaa asiakkaiden tai viestivarastojen välillä, jotka käyttävät .msg-tiedostojärjestelmää. On harvoja tilanteita, joissa Viesti-objektin tallentaminen .msg-tiedostomuodossa ei olisi tarkoituksenmukaista. Esimerkiksi:

* Jos ylläpidetään suurta itsenäistä arkistoa, on parempi käyttää täydellistä muotoa, jossa näkymät voidaan hahmontaa tarkemmin.

* Jos vastaanotin on tuntematon, on mahdollista, että vastaanotin ei tue muotoa ja se saattaa toimittaa yksityisen tai epäolennaisen.


## Esimerkki MSG-tiedostosta

To get an idea of how a MSG file looks like, you can download a [sample MSG file](https://products.conholdate.app/viewer/view/mL7cmq6qYbcNG329P/sample-msg-file.msg) and open on your computer to view its contents.

## Viitteet

* [[MS-OXMSG]: Outlook MSG -tiedostomuoto](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


