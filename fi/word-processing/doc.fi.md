{
  "date": "2019-12-03",
  "keywords": [
"doc",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Sana",
"Asiakirja"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOC - Microsoft Word -asiakirjatiedosto",
  "description": "Opi DOC-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata DOC-tiedostoja.",
  "linktitle": "DOC",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-do-fic"
}
},
  "lastmod": "2019-12-03"
}

## Mikä on DOC-tiedosto?

Tiedostot, joiden tunniste on .doc, ovat Microsoft Wordin tai muiden tekstinkäsittelydokumenttien luomia asiakirjoja binääritiedostomuodossa. Laajennusta käytettiin alun perin tekstidokumentaatioon useissa eri käyttöjärjestelmissä. Se voi sisältää useita erityyppisiä tietoja, kuten kuvia, muotoiltuja sekä pelkkää tekstiä, kaavioita, kaavioita, upotettuja objekteja, linkkejä, sivuja, sivun muotoiluja, tulostusasetuksia ja paljon muuta. Muoto oli suosittu kaikenlaisessa dokumentaatiossa, koska se tarjoaa käyttäjille lukuisia vaihtoehtoja käsikirjojen, ehdotusten, eritelmien, ansioluetteloiden, artikkeleiden tai muiden vastaavien asiakirjojen kirjoittamiseen. DOC:n päivitetty versio on [DOCX](/word-processing/docx/), joka perustuu Office OpenXML:ään, jonka tekniset tiedot ovat avoimesti saatavilla.

## Lyhyt historia ##

WordPerfect, a product of [Corel](https://www.corel.com/en/), used DOC as the extension of their proprietary format. In 1980s, WordPerfect remained the choice of usage on most of the computers due to its easy availability, conformance with most computer machines and Operating systems. However, WordPerfect saw its downfall on Windows OS when Microsoft introduced Microsoft Word as its product for documents file format and chose DOC extension for their proprietary format. As Microsoft Word became more and more popular, the DOC file format underwent several revisions from Microsoft Word 97 - 2003. Vuonna 2007 DOC-oletustiedostomuoto korvattiin Office Open XML -muodolla (tunnetaan nimellä DOCX), ja Microsoft Wordin uudet versiot käyttävät nyt tätä uutta laajennusta oletustiedostomuotona.

## DOC-tiedostomuodon tekniset tiedot – lisätietoja

Microsoft didn't release the DOC file format specifications for a long time until 2008. In Feb 2008, format specifications were released for .doc file format under the Microsoft Open Specification Promise. Though the specification does not describe all of the features used by the DOC format, it gives ample information about the knowledge required to work with this file format. Still, reverse engineering is required to make use of the available information. The specifications have been updated several times and the latest [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 which was updated as of August 2018.

### Joitakin peruskäsitteitä ###

Ennen kuin käsittelemme DOC:n tiedostomuotomäärityksiä, on tarpeen ymmärtää joitakin peruskäsitteitä, jotta voit työskennellä tämän tiedostomuodon kanssa.

**Tiedostotietokanta (Fib):** Fib-rakenne sisältää tietoja asiakirjasta ja määrittää tiedostoosoittimet eri osiin, jotka muodostavat asiakirjan.
Fib on muuttuvapituinen rakenne. Lukuun ottamatta perusosaa, jonka koko on kiinteä, jokaisen osan eteen on laskettu kenttä, joka määrittää seuraavan osan koon.

**Merkin sijainti:** CP tai merkin sijainti edustaa etumerkitöntä 32-bittistä kokonaislukua, joka toimii merkin nollapohjaisena indeksinä asiakirjatekstissä. Tiedoston jokaisen merkin sijaintia ja kokoa ei voi hakea suoraan, ja ne on laskettava ennalta määritetyn algoritmin avulla. Hahmoja ovat:

* Asiakirjan teksti

* Objektien, kuten alaviitteiden tai tekstilaatikoiden, ankkurit

* Ohjausmerkit, kuten kappalemerkit ja taulukon solumerkit


**PLC:** PLC-rakenne on joukko CP:itä, joita seuraa joukko tietoelementtejä. Minkä tahansa PLC:n tietoelementtien on oltava samankokoisia, nolla tai enemmän tavua, ja tästä syystä CP:iden määrän on oltava yksi enemmän kuin tietoelementtien lukumäärä. PLC-rakenteet ovat erityyppisiä, ja jokainen tyyppi määrittelee, sallitaanko CP:iden päällekkäisyys kyseiselle tyypille vai ei. PLC-rakenne koostuu:

* **aCP (muuttuva pituus):** CP-elementtien joukko. Jokainen **PLC**-rakennetyyppi määrittelee CP-elementtien merkityksen ja sallitun alueen.

* **aData (muuttuva pituus):** Jokainen **PLC**-rakennetyyppi määrittelee tietoelementtien rakenteen ja merkityksen, tietoelementtien lukumäärää koskevat rajoitukset ja niiden sisältämiä tietoja koskevat rajoitukset. Se määrittää myös dataelementtien ja vastaavien CP:iden välisen suhteen.


**Kelvollinen valinta:** .DOC-tiedostorakenteet kuvataan pääasiassa useilla CP:illä. Microsoft on määrittänyt useita [rules](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) -koodeja, joita on noudatettava tällaisessa tapauksessa.

**STTB:** STTB on merkkijonotaulukko, joka koostuu otsikosta, jota seuraa joukko elementtejä. **cData**-arvo määrittää taulukon sisältämien elementtien määrän.

**Ominaisuuden tallennus:** Word-tiedostossa voi olla erilaisia elementtejä, kuten tekstiä, kappaleita, taulukoita, kuvia ja osioita, joissa jokaisella voi olla omat ominaisuutensa. Näiden ominaisuudet tallennetaan Word-tiedostoon eroina oletusarvosta. Tällaiset erot määritellään PRl:llä, joka koostuu Single Property Modifierista (Sprm) ja sen operandista. Sovellus voi määrittää lopullisen ominaisuuksien joukon käyttämällä **Prl**-luetteloita.

**Salasanasuojaus:** Word-tiedostot voidaan myös suojata salasanalla, johon voidaan käyttää jotakin seuraavista mekanismeista.

* XOR-hämärtäminen

* Officen binääriasiakirjan RC4-salaus

* Office binääriasiakirja RC4 CryptoAPI salaus


Jos FibBase.fEncrypted ja FibBase.fObfuscation ovat molemmat 1, tiedosto obfusoidaan käyttämällä XOR-obfuskaatiota.

Jos FibBase.fEncrypted on 1 ja FibBase.fObfuscation on 0, tiedosto salataan käyttämällä joko Office Binary Document RC4 -salausta tai Office Binary Document RC4 CryptoAPI Encryption -salausta, jolloin EncryptionHeader on tallennettu ensimmäiseen FibBase.lKey-tavuun Tablet-virtaan. EncryptionHeader.EncryptionVersionInfo määrittää, mitä salausmekanismia käytettiin tiedoston salaamiseen.

### Tiedostorakenne ###

Binääri Word-tiedosto on alkuperäisessä muodossaan OLE-yhdistelmätiedosto, joka koostuu useista tallennusvälineistä ja virroista. Näillä tallennustiloilla ja virroilla on oma rakenne ja kokonsa, jotka määrittelevät kirjoittamisen ja lukemisen parametrit. Nämä ovat:

#### WordDocument Stream ####

This stream contains the document text and other information referenced from other parts of the file. The stream has no predefined structure other than the FIB at the beginning which is mandatory and should be at offset 0. Tämä stream ei saa olla suurempi kuin 2147 Mt.

#### 1TableStream tai 0TableStream ####

Binääri Word-tiedosto voi sisältää taulukkovirtoja, jotka tunnetaan nimellä 1Table stream tai 0Table stream. Asiakirjassa tulee olla ainakin yksi näistä. Jos asiakirja kuitenkin sisältää sekä 1Table- että 0Table-virtoja, käytetään vain tietovirtaa, johon base.fWhichTblStm viittaa. Viittaukseton stream TÄYTYY jättää huomiotta.
Taulukkovirta EI SAA olla suurempi kuin 2147 Mt.

#### Datavirta ####

Tietovirralla ei ole ennalta määritettyä rakennetta. Se sisältää tietoja, joihin viitataan FIB:stä tai muista tiedoston osista. Tämän virran ei tarvitse olla läsnä, jos siihen ei ole viittauksia. Tietovirta EI SAA olla suurempi kuin 2147 Mt.

#### Objektivarasto ####

Object Pool -tallennus sisältää tallennustilat upotetuille OLE-objekteille. Tämän tallennustilan ei tarvitse olla olemassa, jos asiakirjassa ei ole upotettuja OLE-objekteja.

#### Mukautettu XML-tietojen tallennus ####

Mukautettu XML-tietojen tallennustila on valinnainen tallennustila, jonka nimen TÄYTYY olla MsoDataStore.

#### Yhteenvetotietovirta ####

Yhteenvetotietovirta on valinnainen tietovirta, jonka nimen TÄYTYY olla \005SummaryInformation, jossa \005 on merkki, jonka arvo on 0x0005, eikä merkkijono \005.

#### Asiakirjan yhteenvetotietovirta ####

Asiakirjan yhteenvetotietovirta on valinnainen tietovirta, jonka nimen TÄYTYY olla \005DocumentSummaryInformation, jossa \005 on merkki, jonka arvo on 0x0005, ei merkkijono \005.

#### Salausvirta

Salausvirta on valinnainen tietovirta, jonka nimen TÄYTYY olla salaus. Tämä stream EI SAA olla läsnä, elleivät molemmat seuraavista ehdoista täyty:

* Asiakirja on salattu Office Binary Document RC4 CryptoAPI Encryption -salauksella.

* fDocProps-arvo asetetaan EncryptionHeader.Flagsissa.


#### Makrojen tallennustila

Makrojen tallennustila on valinnainen tallennustila, joka sisältää tiedoston makrot. Jos sellainen on, sen TÄYTYY olla projektin juuritallennustila.

#### XML-allekirjoitusten tallennus

XML-allekirjoitusten tallennustila on valinnainen tallennustila, jonka nimen TÄYTYY olla \_xmlsignatures.

#### Signatures Stream

Allekirjoitusvirta on valinnainen tietovirta, jonka nimen TÄYTYY olla \_signatures. Tämä stream sisältää digitaalisia allekirjoituksia.

#### Tietooikeuksien hallinta Tietotilan tallennus

Tietooikeuksien hallinnan tietotilan tallennustila on valinnainen tallennustila, jonka nimen TÄYTYY olla \006DataSpaces, jossa \006 on merkki, jonka arvo on 0x0006, eikä merkkijono \006. Jos tämä tallennustila on olemassa, myös suojatun sisältövirran TÄYTYY olla läsnä.
Jos tämä tallennustila on olemassa, kaikki määritetyt virrat ja tallennustilat, lukuun ottamatta tätä tallennustilaa ja suojattua sisältövirtaa PITÄISI lukea suojatusta sisältövirrasta [MS-OFFCRYPTO]:ssa määritetyllä tavalla ja jos jokin näistä virroista ja tallennuspaikoista on suojatun sisällön ulkopuolella. Stream, ne PITÄÄ jättää huomiotta.

#### Suojattu sisältövirta

Suojattu sisältövirta on valinnainen tietovirta, jonka nimen TÄYTYY olla \009DRMContent, jossa \009 on merkki, jonka arvo on 0x0009, eikä merkkijono \009.
Jos tämä tietovirta on läsnä, myös tietooikeuksien hallinnan tietotilan tallennustilan TÄYTYY olla läsnä.

## Viitteet ##

* [MS-DOC-tiedostonmuodostustiedot](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)

* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))


