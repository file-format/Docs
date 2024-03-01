{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "STR File - dBASE Structure List Object File - Mikä on .str-tiedosto ja kuinka avata se?",
  "description" : "Opi STR dBASE Structure List Object File -tiedostosta ja sen avaamisesta.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-fi",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Mikä on STR-tiedosto?

STR-tiedostomuoto yhdistetään yleisesti tietokannan hallintajärjestelmään dBASE. dBASE:ssa .str-tiedosto edustaa tyypillisesti rakenneluetteloobjektitiedostoa. Tämä tiedosto sisältää tietokantataulukon rakenteen, mukaan lukien tiedot kentistä (sarakkeista) ja niiden ominaisuuksista.

Rakenneluetteloobjektitiedosto (.str) sisältää metatietoja, kuten kenttien nimet, tietotyypit, kenttien pituudet ja kaikki muut tietokantataulukon kuhunkin kenttään liittyvät ominaisuudet. Sitä käytetään tietokantataulukon rakenteen määrittelemiseen ilman varsinaisia tietueita.

Ohjelmat, kuten dBASE tai muut tietokannan hallintatyökalut, voivat käyttää tätä tiedostoa ymmärtääkseen tietokantataulukon asettelun ja suorittaakseen toimintoja, kuten kyselyjä, päivityksiä tai uusien tietueiden luomista tämän rakenteen perusteella.

Tässä on perusesimerkki siitä, mitä STR-tiedosto saattaa sisältää:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Tässä esimerkissä kuvataan taulukko, jossa on neljä kenttää: ID, Nimi, Ikä ja DOB sekä niiden tietotyypit ja pituudet.

## Kuinka avata STR-tiedosto?

Ensisijainen tapa avata .str-tiedostoja on käyttää itse dBASE:a, erityisesti Windows-käyttöjärjestelmissä. dBASE pystyy lukemaan ja tulkitsemaan näiden tiedostojen sisältöä, jolloin käyttäjät voivat tarkastella ja käsitellä tietokantarakennetta.

Koska .str-tiedostot ovat pohjimmiltaan pelkkiä tekstitiedostoja, jotka sisältävät tietoa tietokannan rakenteesta, voit avata ne myös tekstieditorilla. Esimerkkejä tekstieditoreista ovat Microsoft Notepad Windowsissa ja Apple TextEdit Macissa. Kun avaat tiedoston tekstieditorissa, voit nähdä tiedoston sisällön, mukaan lukien kenttien nimet, tietotyypit ja muut rakenteelliset tiedot, ihmisen luettavassa muodossa.

## Viitteet
* [dBase](https://en.wikipedia.org/wiki/DBase)


