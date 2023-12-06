{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HDR File - ESRI BIL Header File Format",
  "description":"Co je soubor HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Co je soubor HDR?

Soubor HDR je hlavičkový soubor GIS, který obsahuje informace o hlavičce pro soubor pásem prokládaný řádkem (.BIL). Popisuje obrazová data a má stejný název jako obrazový soubor. Soubor HDR se skládá ze sady položek, z nichž každá popisuje konkrétní atribut obrázku. Soubor HDR popisuje rozvržení a formátování souboru BIL pro převod na souřadnice reálného světa v kombinaci se samostatným souborem georeferencí.

## Formát souboru HDR

Soubory HDR se ukládají ve formátu textového souboru ASCII. Obsahuje sadu položek, kde každá položka popisuje konkrétní atribut obrázku. Každý soubor HDR má následující formát:

```
<keyword> <value>
```

'<keyword> ` - Označuje konkrétní atribut, který se nastavuje
'<value> ` - Je to hodnota, na kterou se atribut nastavuje

Pořadí položek v záhlaví není nijak omezeno. Každá položka však musí být na samostatném řádku řádku, aby vyhovovala metodě analýzy používané čtečkami HDR.

## Souhrn klíčových slov použitých v souboru HDR

|Klíčové slovo |Přijatelná hodnota |Výchozí|
---|---|---|
|nrows |libovolné celé číslo > 0| žádný
|ncols |libovolné celé číslo > 0| žádný
|npásma |libovolné celé číslo > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |stejné jako hostitelský stroj|
|rozvržení| bil, bip, bsq| bil|
|skipbytes| libovolné celé číslo ≥ 0| 0
|ulxmap |jakékoli reálné číslo| 0|
|ulymap |jakékoli reálné číslo |nrows - 1|
|xdim |jakékoli reálné číslo| 1
|ydim |jakékoli reálné číslo| 1
|bandrowbytes |libovolné celé číslo > 0| nejmenší celé číslo ≥ (ncols x nbits) / 8|
|totalrowbytes |libovolné celé číslo > 0| pro bil: npásma x pásmové bajty;pro bip: nejmenší celé číslo ≥ (ncols x npásma x nbity) / 8|
|bandgapbytes |libovolné celé číslo ≥ 0| 0|

## Reference

* [Formát souboru HRD – ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

