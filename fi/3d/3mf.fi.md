{
  "date": "2019-12-09",
  "keywords": [
"3mf tiedosto",
"3mf tiedostomuoto",
"mikä on 3mf-tiedosto",
"tiedosto",
"3mf esimerkki",
"3mf tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "3MF",
  "description": "Opi 3MF-tiedostomuodosta ja sovellusliittymistä, jotka voivat avata ja luoda 3MF-tiedostoja.",
  "linktitle": "3MF",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-3m-fif"
}
},
  "lastmod": "2019-12-09"
}

## Mikä on 3MF-tiedosto?

3MF, 3D Manufacturing Format, jota sovellukset käyttävät 3D-objektimallien renderöimiseen useille muille sovelluksille, alustoille, palveluille ja tulostimille. Se luotiin välttämään rajoitukset ja ongelmat muissa 3D-tiedostomuodoissa, kuten [STL](/cad/stl/), työskennellessä 3D-tulostimien uusimpien versioiden kanssa. 3MF on suhteellisen uusi tiedostomuoto, jonka 3MF-konsortio on kehittänyt ja julkaissut. Se on tarpeeksi rikas kuvaamaan mallin täydellisesti, säilyttäen sisäiset tiedot, värit ja muut ominaisuudet, mikä tekee siitä laajennettavissa tukemaan uusia 3D-tulostuksen innovaatioita. Muoto on laajennettavissa, se voidaan ottaa laajalti käyttöön, eikä siinä ole ongelmia, jotka haittaavat muita yleisesti käytettyjä tiedostomuotoja.

## 3MF-tiedostomuodon lyhyt historia

Mallia kuvaavien tiedostomuotojen, kuten STL ja muiden, olemassa olevat rajoitukset saavat johtavat tuotemerkit kokoontumaan yhteen ja muotoilemaan laajennettavissa olevan tiedostomuodon 3D-tulostusta varten. Tärkeä näkökohta oli, kuinka sovellusten tulisi välittää mallitietoja 3D-tulostimille. 3MF-konsortio syntyi siis tukemaan uutta 3MF-nimistä 3D-tiedostomuotoa tavoitteenaan tehdä siitä tarpeeksi laajennettavissa 3D-tulostuksen tarpeisiin. Konsortioon kuului useita yrityksiä, mukaan lukien Microsoft, Autodesk, Dassault Systems, Netfabb, SLM, HP ja muut. Microsoft lahjoitti 3D-tiedostomuotonsa keskeneräisen työn lähtökohtana 3MF Consortiumin yhteistyölle spesifikaation jatkokehityksessä.

## 3MF-tiedostomuoto - lisätietoja

3MF on XML-pohjainen tietomuoto – ihmisen luettavissa oleva pakattu XML –, joka sisältää määritelmät 3D-valmistukseen liittyville tiedoille, mukaan lukien kolmannen osapuolen laajennettavissa olevat mukautetut tiedot. 3MF-tiedostomuoto on suunniteltu pitäen mielessä muiden 3D-tiedostomuotojen kohtaamat rajoitukset ja ongelmat. Tämä johti 3MF-tiedostomuodon muotoiluun, joka on:

* **Täydellinen:** Sisältää kaikki tarvittavat malli-, materiaali- ja ominaisuustiedot yhdessä arkistossa

* **Ihmisen luettavissa:** yleisten rakenteiden, kuten OPC, [ZIP](/compression/zip/) ja XML käyttö helpottaakseen kehitystä

* **Yksinkertainen:** Lyhyt, selkeä spesifikaatio, joka tekee kehityksestä helppoa ja validoinnin nopeaa

* **Laajennettavissa:** XML-nimiavaruuksien hyödyntäminen mahdollistaa sekä julkiset että yksityiset laajennukset säilyttäen samalla yhteensopivuuden

* **Epäselvä:** Selkeät kieli- ja vaatimustenmukaisuustestit varmistavat, että tiedosto on aina johdonmukainen digitaalisesta fyysiseen

* **Ilmainen:** Pääsy 3MF-spesifikaatioon ja sen käyttöönotto on ja tulee aina olemaan rojaltivapaa, patentteja ja lisenssejä


The specifications for 3MF file format are hosted over [Github](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md) for public access and continuous updates. The current published version is 1.2.3 that describes the set of conventions for the use of XML and other widely available technologies to describe the content and appearance of one or more 3D models. Developers, who want to build systems for processing 3MF file formats, can refer to these specifications for implementation purpose.

## 3MF-tiedostomuodon tekniset tiedot

3MF-tiedostomuoto käyttää Open Packaging -määrityksiä ZIP-arkiston muodossa fyysisessä mallissaan. Se sisältää hyvin määritellyn joukon osia ja suhteita, jotka täyttävät asiakirjan tietyn tarkoituksen. Tämä saa myös muodon noudattamaan paketin ominaisuuksia, mukaan lukien digitaaliset allekirjoitukset ja pikkukuvat.

### 3MF-dokumentti – yleiskatsaus

Tyypillinen 3MF-asiakirja näyttää seuraavalta:

!{{HYPERLINKKI1}}

The payload includes the full set of parts required for processing the 3D Model part. All content to be used to manufacture an object described in the 3D payload MUST be contained in the 3MF Document. The description of each document part along with its status as required or option is as given in the following table.


|**Nimi**|**Kuvaus**|**Suhteen lähde**|**Pakollinen/valinnainen**
--- | --- | --- | ---
|3D Model|Contains the description of one or more 3D objects for manufacturing.|Package|REQUIRED
|Ydinominaisuudet|OPC-osa, joka sisältää useita asiakirjan ominaisuuksia.|Paketti|VALINNAINEN
|Digital Signature Origin|OPC-osa, joka on paketin digitaalisten allekirjoitusten juuri.|Paketti|VALINNAINEN
|Digitaalinen allekirjoitus|OPC-osat, joista jokainen sisältää digitaalisen allekirjoituksen.|Digital Signature Origin | VALINNAINEN
|Digitaalinen allekirjoitussertifikaatti|OPC-osat, jotka sisältävät digitaalisen allekirjoituksen varmenteen.|Digitaalinen allekirjoitus|VALINNAINEN
|PrintTicket|Tarjoaa asetukset, joita käytetään tulostettaessa 3D-objekti(t) 3D-malliosassa.|3D-malli|VALINNAINEN
|Pikkukuva|Sisältää pienen JPEG- tai PNG-kuvan, joka edustaa pakkauksen 3D-objekteja tai pakettia kokonaisuutena.|Paketti|VALINNAINEN
|3D-tekstuuri|Sisältää pintakuvion, jota käytetään värin lisäämiseen 3D-objektiin 3D-malliosassa (saatavilla laajennuksille)|3D-malli|VALINNAINEN
|Muokatut osat|OPC-osat, jotka liittyvät metatietoihin|Paketti|VALINNAINEN

Teknisten asiakirjojen osissa [Parts and Relationships](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-2-parts-and-relationships), [3D Models](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-3-3d-models), [Object Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-4-object-resources), [Material Resources](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-5-material-resources) ja [Package Features](https://github.com/3MFConsortium/spec_core/blob/master/3MF%20Core%20Specification.md#chapter-6-3mf-document-package-features) on yksityiskohtaisia tietoja 3MF-asiakirjasta.

## Viitteet ##

* [3MF-tiedostomuodon tekniset tiedot](https://github.com/3MFConsortium/spec_core)

* [3MF - Wikipedia](https://en.wikipedia.org/wiki/3D_Manufacturing_Format)


