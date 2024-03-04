{
  "date" : "2021-10-20",
  "keywords" : [ ".pak", "file format", "what is a pak file", "file", "pak example", "Video Game Package File","extension"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie .pak failą ir API, kurios gali kurti ir atidaryti PAK failus.",
  "title" : "PAK failo formatas - vaizdo žaidimų paketo failas",
  "linktitle" : "PAK",
  "menu" : {
    "docs" : {
      "identifier":"game-pak-lt",
      "parent" : "game"
}
},
  "lastmod" : "2021-10-27"
}

## Kas yra PAK failas?

PAK failas yra paketo failas, sukurtas įvairių vaizdo žaidimų, skirtų žaidimų duomenims archyvuoti. Iš esmės tai yra žaidimo failo formatas. Tai gali apimti kelis žaidimo elementus, tokius kaip grafika, tekstūros, garsai, objektai ir kiti žaidimo duomenys. Archyvas dažniausiai išsaugomas kaip .zip failas ir gali būti išgaunamas naudojant populiarią išskleidimo programinę įrangą, pvz., WinZip ir WinRAR. Vaizdo žaidimų, kuriuose naudojami PAK failai, pavyzdžiai: Quake, Hexen, Crysis ir Half-Life.

## PAK failo formatas – daugiau informacijos

Daugeliu atvejų PAK failai išsaugomi [ZIP file format](/compression/zip/). Tačiau skirtingos programos gali naudoti skirtingus failų formatus šiems failams saugoti.


## Kaip atidaryti PAK failus?

PAK failus galite atidaryti naudodami tokias programas kaip [PakExplorer](https://www.quaketerminus.com/tools.shtml) ir [SpriteExplorer](http://www.slackiller.com/hlprograms.htm).

**------------------------------------------------- -------------------------------------------------- -----------------------**

## PAK failo formatas – Simutrans objekto failas

Failas su plėtiniu .pak yra [Simutrans](https://www.simutrans.com/en/) transporto modeliavimo žaidimo failo formatas. Jame yra modeliavimui naudojami objektai, pvz., vartotojo sukurta grafika ir duomenų turinys. Jame gali būti keli skirtingi objektai, pvz., žaidimų transporto priemonės, pastatai, reljefas ir tt PAK failai generuojami naudojant MakeObject – priemonę, kuri kompiliuoja .dat failus ir .png paveikslėlius šiems modeliavimo objektams kurti. Simutrans leidžia žaidėjams valdyti sėkmingą transporto sistemą, kuriant ir valdant keleivių, pašto ir prekių transportavimo sausuma sistemas.

## Kaip sukurti PAK failus?

Simutrans pateikė pavyzdžius, kaip sukurti PAK failus Windows ir Linux OS.

### Windows OS

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

## Nuorodos

 * [Simutrans](https://en.wikipedia.org/wiki/Simutrans)

