
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "ADS-tiedosto - Ada-määritystiedostomuoto",
  "description":"Opi ADS-tiedostomuodosta esimerkkien ja sovellusliittymien avulla, jotka voivat luoda ja avata ADS-tiedostoja.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads-fi",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Mikä on ADS-tiedosto?

ADS-tiedosto on Ada-ohjelmointiprojektin määritystiedosto. Se on samanlainen kuin Java-luokka tai otsikko- ja toteutuspari C++:n tapauksessa. Ada-paketin julkiset ja yksityiset tiedot tallennetaan .ads-tiedostoon. .adb-tiedosto sen sijaan sisältää toteutuksen eli Ada-kappaleet. Kuten {{HYPERLINKKI}}, Ada tarjoaa erittelyn OOP:sta riippumattomien eritelmien ja toteutusten välillä.

ADS-tiedostoja voidaan avata millä tahansa tekstieditorilla, kuten Microsoft Notepad, Notepad++ ja Atom.

## ADS-tiedostomuoto

ADS-tiedostot ovat yksinkertaisessa tekstitiedostomuodossa ja niitä voidaan avata/muokata millä tahansa tekstieditorilla. Ada-paketit voidaan järjestää hierarkioihin. Lapsiyksikkö voidaan ilmoittaa seuraavalla tavalla:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Viitteet

 * [Ada-paketit](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

