{
  "date": "2019-10-11",
  "keywords": [
"vb",
"tiedosto",
"laajennus",
"tiedosto muoto",
"Visual Basic",
"Ohjelmointiopas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VB - Visual Basic Code -tiedosto",
  "description": "Opi VB-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata VB-tiedostoja.",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-v-fib"
}
},
  "lastmod": "2019-09-10"
}

## Mikä on VB-tiedosto?

VB-tiedosto on Visual Basic -kielellä luotu lähdekooditiedosto, jonka Microsoft on luonut .NET-sovellusten kehittämiseen. Toinen samanlainen kieli eri syntaksilla on C#, jonka tiedostot tallennetaan tiedostotunnisteella [.CS](/programming/cs/). Tiedostomuoto tarjoaa matalan tason ohjelmointikielen koodin kirjoittamiseen, joka on käännetty luomaan lopullinen tulostiedosto EXE- tai DLL-muodossa. Nämä voidaan luoda ja kääntää Microsoft Visual Studiolla. Microsoft Visual Studio Expressiä voidaan käyttää myös sellaisten tiedostojen luomiseen ja päivittämiseen, mikä on ilmainen IDE. VB-kielellä luotu yksinkertainen Visual Studio -projekti [solution](/programming/sln/) voi sisältää yhdestä tai useammasta tällaisesta tiedostosta. Kokoonpanoon merkityt tiedostot luetellaan [CSPROJ](/programming/csproj/)-tiedostossa, joka on osa projektia ja käskee kääntäjää käyttämään merkittyjä tiedostoja.

## VB-tiedostomuoto - lisätietoja

VB-tiedostot ovat tekstipohjaisia tiedostomuotoja, jotka voidaan avata missä tahansa tekstieditorissa muokkausta varten. Kuitenkin, kun se avataan tuetussa IDE:ssä, jossa on oikea syntaksin korostus, koodi on helppo lukea ja järjestää. Yksinkertainen VB-tiedosto sisältää:

* Nimiavaruuksien ilmoitus - Viittaa tiettyyn nimiavaruuteen määrittelemään toimintoon

* Muuttujien ilmoitus - Ilmoittaa luokkatason muuttujat tietylle toteutukselle

* Method Declaration - Ilmoittaa menetelmien ilmoitus tietylle toiminnalle


## Esimerkki VB-tiedostomuodosta

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



