{
  "date" : "2019-10-11",
  "keywords" :[ "soubor tga", "formát souboru tga", "co je soubor tga", "soubor", "příklad tga", "přípona souboru tga", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru TGA - grafický soubor TARGA",
  "description":"Další informace o formátu souborů TGA a rozhraních API, která mohou vytvářet a otevírat soubory TGA.",
  "linktitle" : "TGA",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor TGA?

Soubor s příponou .tga je rastrový grafický formát a byl vytvořen společností Truevision Inc. Byl navržen pro desky TARGA (Truevision Advanced Raster Adapter) a poskytoval podporu zobrazení Highcolor/truecolor pro počítače kompatibilní s IBM. Podporuje 8, 16, 24 a 32 bitů na pixel a 8bitový alfa kanál. Podporuje také bezeztrátovou kompresi RLE, kterou lze použít ke zmenšení velikosti obrázku. Digitální fotografie a textury používají obrazový formát TGA.

## Stručná historie

Formování formátu souboru TGA vstoupilo do bytí v roce 1984 společností AT&T EPICenter (později extrahovanou a vytvořenou jako nezávislý subjekt známý jako Truevision), která pracovala na marketingu nových technologií vyvinutých společností AT&T pro buffery barevných snímků. EPICenter již pracoval na svých prvních dvou kartách, VDA (Video Display Adapter) a ICB (image capture board), pro které již probíhala práce na dvou typech souborů, .vda a .icb. Tyto formáty souborů byly kodifikovány a byl zaveden méně široký specifický formát souborů TGA. TGA bylo rozšířením toho, co se již používalo, a poskytovalo informace, jako je šířka, výška, hloubka pixelů, související barevná mapa a původ obrazu.

Verze TGA 2.0, publikovaná v roce 1989, obsahovala několik vylepšených funkcí, jako jsou:

* Miniatury
* Alfa kanál
* Hodnota gama
* Textová metadata

Mezi hlavní přispěvatele do verze TGA 2.0 patří Shawn Steiner, Kevin Fiedly a David Spoelstra z Truevision.

## Specifikace formátu souboru TGA TARGA

Soubor TGA se skládá ze 2 hlavních částí:

* Záhlaví
* Informace o barevných pixelech

Všechny hodnoty v souboru TGA jsou v ittl-endian podle specifikací formátu.

### Záhlaví TGA

Záhlaví souboru TGA se skládá z následujících 5 polí.

|Číslo pole|Délka |Název pole |Popis|
---|---|---|---|
|1| 1 byte |délka ID| Délka pole ID obrázku (0-255)|
|2| 1 byte |Typ barevné mapy| Zda je zahrnuta barevná mapa (0 – znamená, že tento snímek neobsahuje žádná data barevné mapy. 1 – znamená, že tento snímek obsahuje mapu barev.)|
|3| 1 byte |Typ obrázku| Komprese a typy barev (0 – bez obrazových dat. 1 – nekomprimovaný, obrázek s barevnou mapou, 2 – nekomprimovaný, obrázek True Color, 9 – kódovaný v délce cyklu, obrázek s barevnou mapou, 11 – kódovaný s délkou běhu, černobílý obrázek )|
|4| 5 bajtů |Specifikace barevné mapy| Popisuje barevnou mapu|
|5| 10 bajtů |Specifikace obrázku| Rozměry a formát obrázku|

### Data obrázků a barevných map

|Pole č. |Délka |Pole |Popis|
---|---|---|---|
|6 |Z pole délky ID obrázku| ID obrázku| Nepovinné pole obsahující identifikační údaje|
|7 |Z pole specifikace barevné mapy| Údaje barevné mapy| Vyhledávací tabulka obsahující data barevné mapy|
|8 |Z pole specifikace obrázku| Obrazová data| Uloženo podle popisovače obrázku|

### Oblast pro vývojáře (volitelné)

TGA verze 2.0 poskytuje podporu pro další vylepšení/extra, do kterých si mnoho vývojářů přálo uložit více informací. Tyto informace jsou nepovinné, takže pokud je dekodér TGA není schopen interpretovat, budou ignorovány.

### Oblast rozšíření (volitelné)

|Pole č.| Délka| Pole |Popis|
---|---|---|---|
|10| 2 bajty |Velikost rozšíření |Velikost v bajtech oblasti rozšíření, vždy 495|
|11| 41 bajtů| Jméno autora | Jméno autora. Pokud se nepoužívá, bajty by měly být nastaveny na NULL (\0) nebo mezery|
|12| 324 bajtů| Komentář autora| Komentář uspořádaný do čtyř řádků, z nichž každý se skládá z 80 znaků plus NULL|
|13| 12 bajtů| Datum/časové razítko |Datum a čas, kdy byl obrázek vytvořen|
|14| 41 bajtů| ID práce||
|15| 6 bajtů| Pracovní doba| Hodiny, minuty a sekundy strávené vytvářením souboru (pro fakturaci atd.)|
|16| 41 bajtů| ID softwaru |Aplikace, která soubor vytvořila.|
|17| 3 bajty| Verze softwaru||
|18| 4 bajty| Barva klíče||
|19| 4 bajty| Poměr stran pixelů||
|20| 4 bajty| Hodnota gama||
|21| 4 bajty| Posun korekce barev |Počet bajtů od začátku souboru po tabulku korekcí barev, pokud je k dispozici|
|22| 4 bajty| Poštovní známka | Počet bajtů od začátku souboru po obrázek poštovní známky, pokud je přítomen|
|23| 4 bajty| Odsazení řádků skenování| Počet bajtů od začátku souboru do tabulky řádků skenování, pokud je k dispozici|
|24| 1 bajt| Atributy typ| Určuje alfa kanál|

### Zápatí souboru (volitelné)

Posledních 26 bajtů souboru představuje zápatí, což, pokud je přítomno, znamená pravděpodobně soubor TGA verze 2.

|Pole č.| Délka| Pole| Popis|
---|---|---|---|
|28| 4 bajty| Offset rozšíření| Posun v bajtech od začátku souboru|
|29| 4 bajty| Posun developerské oblasti| Posun v bajtech od začátku souboru|
|30| 16 bajtů| Podpis| Obsahuje "TRUEVISION-XFILE"|
|31| 1 bajt| | Obsahuje "."|
|32| 1 bajt| | Obsahuje NULL|


## Reference

* [Specifikace formátu souboru TGA 2.0](https://products.conholdate.app/viewer/view/rVqTeZPLAL/tga-file-format-specifications.pdf?default=view&preview = true.pdf)
* [TGA od Wikipedie](https://en.wikipedia.org/wiki/Truevision_TGA)

