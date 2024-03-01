{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EML - Sähköpostiviesti",
  "description": "Opi EML-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata EML-tiedostoja.",
  "linktitle": "EML",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-em-fil"
}
},
  "lastmod": "2019-09-16"
}

## Mikä on EML-tiedosto?

EML-tiedostomuoto edustaa Outlookilla ja muilla asiaankuuluvilla sovelluksilla tallennettuja sähköpostiviestejä. Lähes kaikki sähköpostiohjelmat tukevat tätä tiedostomuotoa, koska se on RFC-822 Internet Message Format -standardin mukainen. Microsoft Outlook on oletusohjelmisto EML-viestityyppien avaamiseen. EML-tiedostoja voidaan käyttää sekä levylle tallentamiseen että lähettämiseen viestintäprotokollia käyttäville vastaanottajille.

## EML:n lyhyt historia

EML-tiedostomuotomääritykset ovat saatavilla [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)-standardimuodossa. Ennen RFC-822:ta RFC-733 hallitsi verkkosanomien vaihdon sääntöjä vuoteen 1982 asti, entinen luotiin parannuksena lateraaliseen luomalla ARPA-standardit. Samaan aikaan Microsoft loi omat COM-moduulit oman sähköpostiohjelmansa eli Outlook Expressin kehittämiseen. RFC-822:n polku syntyi omaksi muodoksi, kun Microsoft poikkesi avoimesta standardista ja loi [PST](/email/pst/)-tiedostomuodon, jossa sähköpostit tallennetaan erittäin jäsenneltyyn tietokantamuotoon. Tämä aiheutti ongelmia muiden kuin Microsoftin sähköpostiohjelmien käyttäjille, kun sähköpostit välitettiin edelleen Microsoft Outlookista.

Se tapahtui vuonna 2001, kun 822-standardi parannettiin 2822:ksi - Internet Message Format -muotoon, jota käytetään tällä hetkellä EML-viestien luomiseen, lukemiseen ja lähettämiseen MIME RFC-822 -muodossa.

## EML-tiedostomuodon tekniset tiedot

EML-tiedostot koostuvat kahdesta erillisestä osasta:

* **Headers** - Sisältää tietoa viestin otsikosta

* **Viestiteksti** - Sisältää sarjan tietoja, jotka voivat sisältää viestin sisältöä, upotettuja kuvia ja liitteitä


### Otsikkotiedot ###

EML-tiedosto koostuu otsikkotiedoista ja valinnaisesti viestin rungosta. Jokaisella EML:n otsikkorivillä on kaksi osaa, jotka on erotettu kaksoispisteellä :. Ensimmäinen on otsikon nimi ja kaksoispisteen jälkeinen otsikkoteksti. Tällaisia otsikoita ovat esimerkiksi:

* Lähettäjän sähköpostiosoite

* Vastaanottajan sähköpostiosoite

* Sähköpostin aihe

* Viestin aika- ja päivämääräleima


**Esimerkkiotsikko**

```
From: <John@bmw.eml.light.com>

To: <Andy@fileformat.com>

Date: Thu, 8 Mar 2018 10:43:37 +0100

Subject: bmw eml light
```

### Viestiteksti ###

EML-viestin runko sisältää sähköpostin ensisijaiset tiedot tekstin, hyperlinkkien ja liitteiden muodossa. Sähköpostin runko voi sisältää pelkkää luettavaa tekstiä, mutta se ei ole välttämätöntä. Tässä tapauksessa viestin runko voi olla tyhjä tai sisältää koodattuja liitetietoja.

Viestin rungon sisältö kuvataan sen sisältötyypillä, jonka avulla lukusovellukset voivat lukea tiedot vastaavissa muodoissa. Se edustaa itse asiassa asiakirjan luonnetta ja muotoa. MIME-tyypin tai sisältötyypin rakenne on hyvin yksinkertainen; se koostuu tyypistä ja alatyypistä, kahdesta merkkijonosta, jotka erotetaan merkillä '/'. Tilaa ei sallita. Tyyppi edustaa luokkaa ja voi olla erillinen tai moniosainen tyyppi. Alatyyppi on kullekin tyypille. Luettelo tyypeistä, jotka kuuluvat luokkaan Content-Type, on pitkä, mutta joitain tärkeitä sisältötyyppejä ovat seuraavat:


|**Tyyppi**|**Kuvaus**|**Esimerkki alatyypeistä**
---|---|---|
|teksti|Esittää muotoa, joka on ihmisen luettavissa|teksti/plain, text/html, text/css, text/javascript
|image|Estää minkä tahansa tyyppistä kuvaa paitsi videot|image/bmp, image/png, image/jpg, image/gif
|audio|Estää mitä tahansa äänitiedostomuotoa|audio/mdi, audio/wav
|sovellus|Esittää kaikenlaista binaaridataa|sovellus/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### Kiinnittymisen esitys EML-rungossa

EML-runko sisältää rajat jokaiselle sen sisältämälle sisältötyypille. Viestin rungossa oleva liite tunnistetaan sen sisältötyypin ja sisällön sijoittelun perusteella seuraavan esimerkin mukaisesti:

Sisältötyyppi: teksti/plain; merkkisarja#windows-1252; nimi#apple app store.txt
Sisältö-asetelma: kiinnitys; tiedostonimi#apple app store.txt
Sisällönsiirto-koodaus: base64
X-Attachment-Id: f_jkhztmd02

Kuten voidaan nähdä, liitteeseen asetettu Content-Disposition mahdollistaa lukusovellusten liitetietojen, kuten liitetiedoston nimen ja siirtokoodauksen, saamisen. Liitteen otsikkotietoja seuraa koodattu liitteen sisältö, joka on luettava.

#### Esimerkki laskentataulukosta liitteenä

Sisältötyyppi: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; nimi#english_spodr.xlsx
Sisältö-asetelma: kiinnitys; tiedostonimi#english_spodr.xlsx
Sisällönsiirto-koodaus: base64
X-Attachment-Id: f_jkhztmd43

## Kuinka avata EML-tiedosto

Voit avata EML-tiedostoja käyttämällä erilaisia sähköpostiohjelmia, kuten:

 * **Apple Mail macOS:ssä**
 * **Mozilla Thunderbird**
 * **Microsoft Outlook**

EML-tiedostot tallennetaan vain tekstimuodossa, ja voit myös avata nämä EML-tiedostot suosituilla tekstieditoreilla, kuten **TextEdit** macOS:ssä ja **Microsoft Notepad** Windows-käyttöjärjestelmässä.

## Kuinka muuntaa EML-tiedosto

Voit muuntaa EML-tiedostoja useisiin muihin muotoihin sovelluksilla, kuten Apple Mail ja Microsoft Outlook.

Esimerkiksi Microsoft Outlook voi muuntaa EML-tiedoston seuraaviin muotoihin:

**[.MSG](/eml/msg/)** - Microsoft Outlook -viestimuoto
**[.PDF](/pdf/)** - Protable Document Format

## Viitteet

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)


