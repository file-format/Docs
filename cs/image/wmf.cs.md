{
  "date" : "2019-10-11",
  "keywords" :[ "soubor wmf", "formát souboru wmf", "co je soubor wmf", "soubor", "příklad wmf", "přípona souboru wmf", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Microsoft Windows Metafile Format",
  "description":"Další informace o formátu souborů WMF a rozhraních API, která mohou vytvářet a otevírat soubory WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor WMF?

Soubory s příponou WMF představují Microsoft Windows Metafile (WMF) pro ukládání dat vektorových i bitmapových obrázků. Abychom byli přesnější, WMF patří do kategorie formátů vektorových souborů grafických formátů souborů, které jsou nezávislé na zařízení. Windows Graphical Device Interface (GDI) používá funkce uložené v souboru WMF k zobrazení obrázku na obrazovce. Později byla publikována vylepšená verze WMF, známá jako Enhanced Meta Files (EMF), díky níž je formát bohatší na funkce. Prakticky jsou WMF podobné SVG.

## Specifikace formátu souboru WMF ##

Soubor WMF označoval 16bitový formát souboru v době jeho spuštění se systémem Windows 3.0. Formát souboru se skládá ze série záznamů s proměnnou délkou, které obsahují příkazy pro kreslení grafiky, definice objektů a vlastnosti. Protože soubory WMF jsou založeny na příkazech poskytnutých GDI pro kreslení obrázku, je také známý jako digitální záznam obrázku, který lze přehrát a reprodukovat tento obrázek. Kompletní specifikace formátu souborů WMF jsou k dispozici online a měly by být uvedeny pro vývoj aplikací pro práci se soubory WMF. Soubor WMF je uspořádán do:

* Záznam záhlaví WMF
* Záznam (y) WMF
* Záznam konce souboru WMF

### Záznam záhlaví WMF ###

Záznam **META_HEADER** obsahuje informace, které definují vlastnosti metasouboru, včetně:

* Typ metasouboru
* Verze metasouboru
* Velikost metasouboru
* Počet objektů definovaných v metasouboru
* Velikost největšího jednotlivého záznamu v metasouboru

### Záznam umístitelného záhlaví WMF ###

Záznam **META_PLACEABLE** obsahuje rozšířené informace týkající se obrázku, včetně:

* Ohraničující obdélník
* Velikost logické jednotky pro škálování
* Kontrolní součet pro ověření

### Záznam WMF ###

Záznamy WMF mají obecný formát, který je specifikován v dokumentu specifikací. Každý záznam WMF obsahuje následující informace:

* Velikost záznamu
* Funkce nahrávání
* Parametry, pokud existují, pro funkci záznamu

## Reference ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile – Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

