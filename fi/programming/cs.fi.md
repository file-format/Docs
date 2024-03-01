{
  "date": "2019-10-11",
  "keywords": [
"cs",
"tiedosto",
"laajennus",
"tiedosto muoto",
"CSharp",
"Ohjelmointikieli"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CS - CSharp-kooditiedosto",
  "description": "Opi CS-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata CS-tiedostoja.",
  "linktitle": "CS",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-c-fis"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on CS-tiedosto?

Tiedostot, joiden laajennus on .cs, ovat C#-ohjelmointikielen lähdekooditiedostoja. Microsoft esitteli käytettäväksi .NET Frameworkin kanssa, ja se tarjoaa matalan tason ohjelmointikielen koodin kirjoittamiseen, joka on käännetty luomaan lopullinen tulostiedosto EXE- tai DLL-muodossa. Nämä voidaan luoda ja kääntää Microsoft Visual Studiolla. Microsoft Visual Studio Expressiä voidaan käyttää myös sellaisten tiedostojen luomiseen ja päivittämiseen, mikä on ilmainen IDE. CS-tiedostoja käytetään sovellusten kehittämiseen, jotka voivat vaihdella yksinkertaisista työpöytäsovelluksista monimutkaisempiin ohjelmiin. C#-kielellä luotu yksinkertainen Visual Studio -projekti [solution](/programming/sln/) voi sisältää yhdestä tai useammasta tällaisesta tiedostosta. Kokoonpanoon merkityt tiedostot luetellaan [CSPROJ](/programming/csproj/)-tiedostossa, joka on osa projektia ja käskee kääntäjää käyttämään merkittyjä tiedostoja.

## CS-tiedostomuoto ##

CS-tiedostot ovat tekstipohjaisia tiedostomuotoja, jotka voidaan avata missä tahansa tekstieditorissa muokkausta varten. Koodi on kuitenkin helppo lukea ja järjestää, kun se avataan tuetussa IDE:ssä, jossa on oikea syntaksin korostus. Yksinkertainen CS-tiedosto sisältää:

* Nimiavaruuksien ilmoitus - Viittaa tietyn nimiavaruuden määrittelemään tiettyyn toimintoon

* Muuttujien ilmoitus - Ilmoittaa luokkatason muuttujat tietylle toteutukselle

* Method Declaration - Ilmoittaa menetelmien ilmoitus tietylle toiminnalle


### Syntaksi ###

* Puolipisteitä käytetään osoittamaan lauseen loppua.

* Kaarevia sulkuja käytetään lausekkeiden ryhmittelyyn. Lausunnot ryhmitellään yleensä menetelmiin (funktioihin), menetelmät luokkiin ja luokat nimiavaruuksiin.

* Muuttujat määritetään yhtäläisyysmerkillä, mutta niitä verrataan kahdella peräkkäisellä yhtäsuuruusmerkillä.

* Hakasulkeja käytetään taulukoiden kanssa sekä niiden ilmoittamiseen että arvon saamiseksi tietyssä indeksissä yhdessä niistä.


### Esimerkki ###

```
using System;

class Program
{
    static void Main()
    {
        Console.WriteLine("Hello, world!");
}
}
```

## Muut CS-tiedostot

Tässä on muita tiedostotyyppejä, jotka käyttävät **.cs**-tiedostotunnistetta.

**Tiedot ja pelit**
- {{HYPERLINKKI1}}
- {{HYPERLINKKI1}}

**Ohjelmointi**
- {{HYPERLINKKI1}}

