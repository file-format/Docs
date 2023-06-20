{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "soubor", "formát", "rozšíření", "API", "Sada listů AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - soubor sady listů AutoCAD",
  "description" :"Další informace o souboru .dst a rozhraních API, která mohou vytvářet a otevírat soubory DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Co je soubor DST?

Soubor DST je soubor aplikace AutoCAD, který obsahuje přidružení a informace pro definování sad listů. Ty jsou uloženy ve výchozí složce úložiště sady listů, Sady listů aplikace AutoCAD. Soubory DST neobsahují skutečná výkresová rozvržení, ale odkazují na ně z vybraných souborů [DWG](/cs/cad/dwg/) a [DWT](/cs/cad/dwt/) spojených s těmito sadami listů. V síťovém prostředí by všichni členové týmu měli mít síťový přístup k těmto přidruženým souborům. Soubory DST se ukládají na disk ve formátu souboru [XML](/cs/web/xml/).

## Formát souboru DST – Další informace

Soubory DST se vytvářejí pomocí nástroje AutoDesk Sheet Set Manager (SSM). Když k souboru přistupuje někdo z týmu, soubor DST se krátce otevře a poté se uloží zpět s aktualizovanými informacemi. Současný přístup ke stejnému souboru DST je řízen nástrojem SSM, který zobrazuje ikonu zámku, když je soubor v přístupu.

V každém konkrétním okamžiku může být stav listu v kterémkoli z následujících stavů.

* List je k dispozici pro úpravy.
* List je uzamčen.
* List chybí nebo byl nalezen v neočekávaném umístění složky.

## Reference

* [O používání sad listů DST](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Další informace o sadách listů](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Zvládnutí sad listů AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

