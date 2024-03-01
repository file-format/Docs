{
  "date": "2021-03-11",
  "keywords": [
"APNX",
"Amazonin sivunumeroindeksi",
"laajennus",
"tiedosto",
"muoto",
"eBook",
"Amazon Kindle"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Opi Amazon APNX -tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata APNX-tiedostoja.",
  "title": "APNX - Amazonin sivunumeroindeksi",
  "linktitle": "APNX",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-apn-fix"
}
},
  "lastmod": "2021-05-28"
}

## Mikä on APNX-tiedosto? ##

Amazonin sivunumeroindeksitiedosto, joka käyttää .apnx-tunnistetta, on eBook-tiedostotyyppi; Amazon Kindlen käyttämä. Nämä tiedostot tunnetaan itse asiassa Kindle-laitteiden käyttäminä sivutustiedostoina. Joten APNX-tiedostot luodaan yleensä merkitsemään Kindle-e-kirjojen sivuja. Sivutusominaisuus on käynnistetty Amazon Kindle -laitteissa sen 3.1-laiteohjelmiston jälkeen. Se etsii APNX-tiedostosta sivuhakemistot ja yhdistää sen sitten alkuperäisen painokirjan sivunumeroihin. Nämä tiedostot tallennetaan Kindle-laitteisiin yhdessä Amazon eBooks -tiedostojen kanssa. Et voi avata tai muokata APNX-tiedostoja.

## APNX-tiedostomuodon tekniset tiedot ##

### Asettelu

|tavua| sisältö| kommentit|
---|---|---|
|4 |00010001 | Muototunniste. Arvo 65537 little-endian.|
|4 |seuraavan alku | Poikkeama ensimmäisen otsikon päättymispaikan jälkeen. Aloittaa uuden otsikkotietojen sarjan|
|4 |pituus| Ensimmäisen otsikon pituus|
|N |ensimmäinen otsikko | Merkkijono, joka sisältää sisällön otsikon. Se aloittaa seuraavan sarjan|
|2 |tuntematon | Aina 1|
|2 |pituus | Toisen otsikon pituus|
|2 |sivumäärä | Sivuja edustavien tavujen kokonaismäärä toisen otsikon jälkeen. Tämä kokonaismäärä sisältää tavut, jotka sivukartta jättää huomiotta.|
|2 |tuntematon | Aina 32|
|N |toinen otsikko | Merkkijono, joka sisältää sivukartoitusotsikon|
|4*N |täyte | Sivukartoituksen otsikossa annettu ensimmäinen numero ilmaisee 0 tavun määrän.|
|4*N |sivuluettelo ||

### Sisällön otsikko

Sisältöotsikko koostuu {}:n sisällä olevasta merkkijonosta, joka sisältää avain- ja arvopareja:

|sisältö| kommentit|
---|---|
|contentGuid| Opas.|
|asin | Amazon-tunniste kirjan Kindle-versiolle.|
|cdeType | MOBI cdeType. Pitäisi aina olla EBOK e-kirjoille.|
|fileRevisionId | Tämän tiedoston versio.|

#### Esimerkki
```
{"contentGuid":"d8c14b0","asin":"B000JML5VM","cdeType":"EBOK","fileRevisionId":"1296874359405"}
```
### Sivukartoitusotsikko
Sivukartoitusotsikko koostuu merkkijonosta, joka on suljettu {}:n sisällä ja joka sisältää avain- ja arvopareja.

|sisältö | kommentit|
---|---|
|asin | Paperikirjan ISBN 10, jota sivut vastaavat|
|sivukartta| Kolmen arvon monikko. Näyttää tältä: (N,N,N)\
1) Tavujen määrä otsikon jälkeen, joka aloittaa sivunumerointisarjan\
2) tuntematon\
3) tuntematon\|
#### Esimerkki
```
{"asin":"1906694184","pageMap":"(4,a,1)"}
```

### Sivuluettelo

Sivuluettelo on siirtymien sarja raaka-HTML:ssä. Jokainen
arvo on uuden sivun alku. Jokainen merkintä on 4-tavuinen big endian
int.



## Viitteet

* [Amazon APNX -tiedostomuoto](https://nachtimwald.com/2011/02/09/amazon-apnx-file-format/)

* [APNX - MobileRead Wiki](https://wiki.mobileread.com/wiki/APNX)


