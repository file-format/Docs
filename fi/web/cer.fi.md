{
  "date": "2021-07-13",
  "keywords": [
"CER",
"laajennus",
"tiedosto",
"muoto",
"web",
"todistus",
"Kieli"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CER - Varmenteen tiedostomuoto",
  "description": "Lue lisää CER-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CER-tiedostoja.",
  "linktitle": "CER",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ce-fir"
}
},
  "lastmod": "2021-07-13"
}

## Mikä on CER-tiedosto? ##

A file with an extension .cer is responsible for storing some information about the owner certificate and the specific public key. This format of files cannot store the private keys and have the capacity to store only one certificate which is x509. Erityisesti suojatut varmenneviranomaiset kuuluvat HTTPS:ään, joka on luotettava ja suojattu selausprotokolla  
CER on palvelimesi sertifikaatti. Sen vastaanottaa yleensä verkkotunnuksen varmentaja. CER:ää pidetään enimmäkseen samana kuin {{HYPERLINKKI}}, vaikka molemmat ovat samaa SSL-varmenteen muotoa, mutta ne ovat eri tiedostopäätteitä.
Näitä voidaan käyttää käyttöjärjestelmissä avaamalla selain ja tarkistamalla käytettävän selaimen tai verkkosivuston suojaus.

## Lyhyt historia ##

Vuonna 1995 Thawtesta tuli ensimmäinen sertifiointiviranomainen, joka ratkaisi julkisten SSL-varmenteiden (secured socket link) ongelman Yhdysvalloissa. Sen jälkeen on olemassa sarja tällaisia viranomaisia, jotka perustettiin vuosina 1995–2020.

## CER-tiedostomuoto ##

Nämä tiedostot voivat olla yksinkertaisia
* PKC S#7 sisältää Base64 ASCII -koodauksen
* Sen tiedostotunnisteet ovat p7b tai p7cZ
* Binäärisisällölle varmenne olisi DER tai pkcs12/pfx.
On olemassa monen tyyppisiä varmennetiedostoja, joilla on ainutlaatuisia määrityksiä:
* .pem, kun organisaatio usThawteificate ketjuttaa tämän muodon tunnetusti luovan varmenteita
* .arm, kun sertifikaatin purkutapa auttaa allekirjoittamaan itseään, vaaditaan, tätä tarkoitusta varten määritetty muoto on .arm. Se esitetään base-64 ASCII-koodauksella.
* .der, Se koostuu binääritiedoista. Tämä tarkoittaa, että sitä voidaan käyttää vain yhteen varmenteeseen
* .pfx (PKC512), Se koostuu CA:n myöntämää varmennetta vastaavasta yksityisestä avaimesta tai itse allekirjoitetusta sertifikaatista. Tämä muoto tunnetaan hyvin SSL-toteutuksen muuntamisesta toiseksi.


