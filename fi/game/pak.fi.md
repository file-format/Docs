{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lisätietoja .pak-tiedostoista ja sovellusliittymistä, jotka voivat luoda ja avata PAK-tiedostoja.",
  "title" : "PAK-tiedostomuoto - videopelipakettitiedosto",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-fi",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Mikä on PAK-tiedosto?

PAK-tiedosto on eri videopelien luoma pakettitiedosto pelitietojen arkistointia varten. Pohjimmiltaan se on pelin tiedostomuoto. Tämä voi sisältää useita pelielementtejä, kuten grafiikkaa, tekstuureja, ääniä, esineitä ja muuta pelidataa. Arkisto tallennetaan useimmiten .zip-tiedostona, ja se voidaan purkaa suosituilla purkuohjelmilla, kuten WinZip ja WinRAR. Esimerkkejä PAK-tiedostoja käyttävistä videopeleistä ovat Quake, Hexen, Crysis ja Half-Life.

## PAK-tiedostomuoto - lisätietoja

Useimmissa tapauksissa PAK-tiedostot tallennetaan kansioon {{HYPERLINKKI}}. Mutta eri sovellukset voivat käyttää eri tiedostomuotoja näiden tiedostojen tallentamiseen.


## Kuinka avata PAK-tiedostoja?

Voit avata PAK-tiedostoja sovelluksilla, kuten [PakExplorer](https://www.quaketerminus.com/tools.shtml) ja [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------- --------------------------------------------------- -----------------------**

## PAK-tiedostomuoto - Simutrans-objektitiedosto

Tiedosto, jonka laajennus on .pak, on [Simutrans](https://www.simutrans.com/en/) kuljetussimulaatiopelitiedostomuoto. Se sisältää simulaatiossa käytettyjä objekteja, kuten käyttäjän tekemää grafiikkaa ja datasisältöjä. Siinä voi olla useita erilaisia esineitä, kuten peliajoneuvoja, rakennuksia, maastoa jne. PAK-tiedostot luodaan käyttämällä MakeObject-apuohjelmaa, joka kokoaa .dat-tiedostoja ja .png-kuvia näiden simulaatioobjektien luomiseksi. Simutrans antaa pelaajille mahdollisuuden ylläpitää menestyvää kuljetusjärjestelmää rakentamalla ja hallinnoimalla kuljetusjärjestelmiä matkustajille, postille ja tavaroille maateitse

## Kuinka luoda PAK-tiedostoja?

Simutrans on listannut esimerkkejä PAK-tiedostojen luomisesta Windows- ja Linux-käyttöjärjestelmissä.

### Windows-käyttöjärjestelmä

```
simutrans_src
   makeobj.exe
   haus_01
        haus_01.dat
        haus_01.png
        pak.bat
   auto_03
        auto_03.dat
        auto_03.png
        pak.bat
   triebzug_01
        triebzug_vorn.dat
        triebzug_mitte.dat
        triebzug_hinten.dat
        triebzug_01.png
        pak.bat
```
### Linux BE/OS

```
simutrans_src
   makeobj
   haus_01
        haus_01.dat
        haus_01.png
        pak
   auto_03
        auto_03.dat
        auto_03.png
        pak
   triebzug_01
        triebzug_v.dat
        triebzug_m.dat
        triebzug_h.dat
        triebzug_01.png
        pak
```

## Viitteet

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

