{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WHL-tiedostomuoto - Python Wheel -pakettitiedosto",
  "description": "Opi WHL-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata WHL-tiedostoja.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-wh-fil"
}
},
  "lastmod": "2022-06-29"
}

## Mikä on WHL-tiedosto?

WHL (Wheel) -tiedosto on Pythonin pyörämuotoon tallennettu jakelupakettitiedosto. Se on Python-jakelujen vakiomuotoinen asennus ja sisältää kaikki asennukseen tarvittavat tiedostot ja metatiedot. WHL-tiedosto sisältää myös tietoja tämän pyörätiedoston tukemista Python-versioista ja -alustoista. Samoin kuin [MSI](/executable/msi/)-asennustiedosto, WHL-tiedostomuoto on asennusvalmis muoto, joka mahdollistaa asennuspaketin suorittamisen rakentamatta lähdejakelua.

## WHL tiedostomuoto

WHL-tiedostomuoto on [ZIP](/compression/zip/) (.zip) -arkisto, joka sisältää kaikki asennustiedostot ja metatiedot, joita asentajat tarvitsevat paketin asentamiseen. Nämä WHL-tiedostot voidaan purkaa käyttämällä unzip-vaihtoehtoa tai tavallisia purkuohjelmistosovelluksia, kuten WinZIP ja WinRAR.

### WHL:n tiedostonimisopimus

WHL-tiedosto on nimetty seuraavan käytännön mukaisesti.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Esimerkki WHL-tiedoston nimestä on seuraava.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * cryptography on paketin nimi.
 * 2.9.2 on kryptografian pakettiversio. Versio on PEP 440 -yhteensopiva merkkijono, kuten 2.9.2, 3.4 tai 3.9.0.a3.
 * cp35 on Python-tunniste ja ilmaisee Python-toteutuksen ja -version, jota pyörä vaatii.
 * abi3 on ABI-tunniste. ABI tarkoittaa sovellusbinaarirajapintaa.
 * `macosx_10_9_x86_64` on alustatunniste, joka sattuu olemaan melkoinen suupala.

## Viitteet

* [Mitä Python-pyörät ovat ja miksi sinun pitäisi välittää?](https://realpython.com/python-wheels/)

* [Python Wheel](https://pypi.org/project/wheel/)


