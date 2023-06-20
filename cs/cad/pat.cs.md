{
  "date" : "2020-03-16",
  "keywords" :[ "Soubor PAT", "Formát", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Další informace o formátu souboru PAT a rozhraních API, která mohou vytvářet a otevírat soubory PAT.",
  "title" :"Formát souboru PAT",
  "linktitle" : "PAT",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-10-25"
}

## Co je soubor PAT?

Soubor s příponou .pat je soubor CAD, který používá software AutoCAD. Aplikace, které mohou otevírat soubory PAT, používají šrafovací vzor uložený v těchto souborech a získávají informace o textuře/výplni oblasti. Obsažené vzory poskytují nakresleným objektům informace o vzhledu materiálu. Soubory PAT lze otevřít v aplikacích, jako je Autodesk AutoCAD, CorelDRAW Graphics Suite a Ketron Software. Soubory PAT lze převést do různých obrazových formátů, jako jsou JPG, PNG, BMP atd.

## Formát souboru PAT

Soubory PAT jsou psány ve formátu prostého textu a lze je otevřít v libovolném textovém editoru. Šrafovací vzory v těchto souborech jsou vektorové a odpovídají syntaxi uvedené v dokumentaci AutoCADu.

Všechny vzory začínají v bodě 0,0, vzor je vypočítán tak, aby pokryl hranici šrafování.

### Definice vzoru

Všechny definice vzorů se skládají z následujících polí:
* Přední '\*'
* Název – Název nesmí obsahovat mezery, interpunkční znaménka, závorky ani lomítka.
* Popis

Standardní formát pro šrafovací vzory je `<\*><name> <, popis>`. Název a popis jsou odděleny čárkou a popis nesmí přesáhnout délku řádku osmdesáti znaků. Šrafovací vzory jsou definovány po této informaci.

### Příklady šrafovacích vzorů
Následuje příklad čtvercového vzoru
```
* square, a square pattern
0,     0,0,   0,1,   1,-1
90,   0,1,   0,1,   1,-1
```
Další příklad ukazující vzor rovnoběžníku je následující.

```
*pgram, parallelogram pattern
0,     0,0,    1,1,                     1,-1
45,   0,0,    0,1.4142,   1.4142,-1.4142
45,   0,1,    0,1.4142,   1.4142,-1.4142
```
## Reference ##

* [Hash Patterns od Autodesku](https://help.autodesk.com/view/ACDLT/2018/ENU/?guid=GUID-A6F2E6FF-1717-44B6-A476-0CA817ADD77E)

