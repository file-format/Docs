---
date: 2019-10-11
keywords: prc, .prc, prc file format, how to open prc files, .prc extension, prc extension
author:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: PRC-tiedostolomakeat
linktitle: PRC
description: Ltienaa PRC-tiedostomuodosta ja API-liittymistä, jotka voivat luoda ja avata PRC-tiedostons.
menu:
  docs:
    parent: "3d"
lastmod: 2021-03-04
---
## Kiinan kansantasavallan tiedostomuodot
MobiPocket käyttää .prc-laajennuksia Product Representation Compact 3D -tiedostomuodossa ja e-kirjan tiedostomuodossa.

## Mikä on Product Representation Compact (PRC) -tiedosto?

PRC (Product Representation Compact) on 3D-tiedostomuoto, joka on optimoitu tallentamaan, lataamaan ja näyttämään 3D-tietoja erityisesti CAD-järjestelmistä (Computer-Aided Design). Se on peräkkäinen binääritiedosto, joka on kirjoitettu kannettavalla tavalla. PRC:tä voidaan käyttää 3D-tietojen upottamiseen PDF-tiedostoon. PRC tukee useimpia CAD:n päärakenteita, kuten kokoonpanoja ja osia, 3D-kokonaisuuksien puita, tarkkaa geometriaesitystä, kolmioesitystä ja merkintöjä. PRC käyttää .prc-laajennusta ja käytetty Internet-mediatyyppi on *malli/prc*.

PRC on monikäyttöinen tiedostomuoto, joka sen käytön perusteella voidaan joko tallentaa tavallisella pakkauksella CAD-tietojen esittämiseksi suoraan tai tallentaa käyttämällä korkeaa pakkausta tiedoston koon pienentämiseksi. PRC-muotoon PDF-tiedostoon tallennetut 3D-tiedot ovat yhteentoimivia CAM- ja CAE-sovellusten kanssa.

### Product Representation Compact (PRC) -tiedostomuodon määrittely

PRC-tiedostossa on yksi pääotsikkoosio, jota seuraa yksi tai useampi tiedostorakenne ja yksi mallitiedosto lopussa. Tiedostorakenteessa on yksi otsikko, jota seuraa seuraavat tietoosiot:

- **Globals**: Se sisältää viitatut tiedostorakenteet ja värit, viivatyylit ja koordinaattijärjestelmät jokaiselle tiedostorakenteen puuyksikölle.
- **Tree**: It contains a description of the tree of items like product occurrences, part definitions, representation items, and markup.
- **Tessellation**: Se sisältää kaikki puun lehtien entiteettien tesselloidut (kolmiotetut) tiedot (esityskohteet ja merkinnät).
- **Geometria**: Se sisältää kaikki tarkat geometria- ja topologiatiedot puun lehtien kokonaisuuksista (esityskohteet).
- **Lisägeometria**: Se sisältää geometrian yhteenvetotiedot. Tämä mahdollistaa tiedoston osittaisen lataamisen lataamatta koko geometriaa.

Seuraava on tyypillisen PRC-tiedoston rakenne.

```console
PRC Header

File Structure #1
- Header for File Structure #1
- Globals for File Structure #1
- Tree for File Structure #1
- Tessellation for File Structure #1
- Geometry for File Structure #1
- Extra Geometry for File Structure #1

File Structure #2
...

File Structure #n
- Header for File Structure #n
- Globals for File Structure #n
- Tree for File Structure #n
- Tessellation for File Structure #n
- Geometry for File Structure #n
- Extra Geometry for File Structure #n

PRC model file data
```
## Mikä on MobiPocket-e-kirjatiedosto PRC-tunnisteella
Ranskalaisen yrityksen **Mobipocket** käyttöön ottama e-kirjan tiedostomuoto käyttää myös tunnistetta .prc. Aluksi Mobipocket julkaisi ilmaisen sovelluksen useille älylaitteille, kuten taulutietokoneille, kämmenmikroille ja älypuhelimille. .prc-laajennus on itse asiassa identtinen .mobi:n kanssa, mutta sitä käytetään erityisesti PDA-laitteisiin, jotka tukevat vain **.prc**- tai **.pdb**-laajennuksia.

### Mobipocket PRC -tiedostomuodon tekniset tiedot
MobiPocket PRC -tiedostomuoto perustuu Open eBook -standardiin XHTML:ää käyttäen ja se voi myös sisältää JavaScriptiä ja kehyksiä. Saatavilla on myös tuki sulautettujen tietokantojen kanssa käytettäville alkuperäisille SQL-kyselyille.

Mobipocket Readerilla on kotisivukirjasto. Lukijat voivat lisätä tyhjiä sivuja mihin tahansa kirjan osaan ja lisätä muuttuvia piirustuksia. Objekteja, kuten huomautuksia, kirjanmerkkejä, korjauksia, muistiinpanoja ja piirroksia, voidaan hallita yhdestä paikasta. Kuvat muunnetaan GIF-muotoon ja niiden enimmäiskoko on 64K, mikä riittää pieninäyttöisille matkapuhelimille. Mobipocket Readerissa on sähköiset kirjanmerkit ja sisäänrakennettu sanakirja.

Lukijassa on koko näytön tila lukemista varten ja se tukee monia PDA-laitteita, kommunikaattoreita ja älypuhelimia. Mobipocket-tuotteet tukevat useimpia Palm-käyttöjärjestelmiä, Windowsia, Symbiania, BlackBerryä, mutta eivät Androidia. Lukija toimii Linux- tai Mac OS X -käyttöjärjestelmässä WINEn avulla.

## Viitteet

- {{HYPERLINKKI}})
- [PRC Format Specification](https://web.archive.org/web/20081202034541/http://livedocs.adobe.com/acrobat_sdk/9/Acrobat9_HTMLHelp/API_References/PRCReference/PRC_Format_Specification/index.html)
- {{HYPERLINKKI1}}

