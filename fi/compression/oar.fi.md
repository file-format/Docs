{
  "date": "2021-04-08",
  "keywords": [
"airo tiedosto",
"oar tiedostomuoto",
"mikä on airotiedosto",
"tiedosto",
"airo esimerkki",
"oar tiedostopääte",
"laajennus",
"muoto"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OAR - OpenSimulator-arkistotiedostomuoto",
  "description": "Opi OAR-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata OAR-tiedostoja.",
  "linktitle": "OAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-oa-fir"
}
},
  "lastmod": "2021-04-15"
}

## Mikä on OAR-tiedosto?

Tiedosto, jonka pääte on .oar, on arkistotiedosto, jota käyttää OpenSimulator-sovellus, joka on avoimen lähdekoodin 3D-sovelluspalvelin virtuaalisen ympäristön luomiseen, johon useat käyttäjät voivat päästä verkon kautta. OAR-tiedostomuoto tarjoaa tarvittavat resurssitiedot, joita tarvitaan maaston, objektien pintakuvioiden ja varastojen lataamiseen kokonaan eri järjestelmään. OpenSimulatorissa on myös valinnainen hypergrid, jonka avulla käyttäjät voivat vierailla muissa OpenSimulator-asennuksissa verkossa. OAR-tiedostoissa on Internet-MIME-tyyppinen sovellus/oar ja ne sisältävät yhden tai useamman arkistoidun tiedoston.


## OAR-tiedostomuoto

OAR are binary files that are stored in compressed archive file format. The latest version of OAR file format is [version 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) that has major changes from its previous [version 0.8](http://opensimulator.org/wiki/OAR_Format_0.8). The latest version supports storing multiple regions in a single OAR and is not backwards compatible with versions of OpenSimulator before 0.7.5. OAR-tiedosto on gzip-pakattu tar-tiedosto (tar.gz) alkuperäisessä unix-tar-muodossa (ei USTAR).

## Esimerkki OAR-alueista
AOR-tiedostot voivat sisältää useita alueita. Arkiston rakenne on seuraava (tämä esimerkki sisältää 4 aluetta):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

Arkiston ohjaustiedosto sisältää pääversionumeron, jonka avulla voidaan määrittää yhteensopivuus tulevien muotomuutosten kanssa. OAR-muodossa olevien resurssien olemassaolo ilmaistaan boolean-elementillä<assets_included> . Tiedot sisällytetyistä alueista sisältyvät luetteloon, joka on ohjaustiedostossa. Esimerkki tiedostosta Archive.xml on seuraava.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## Viitteet

 * [OAR-muoto v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
 * [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

