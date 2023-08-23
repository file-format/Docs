{
  "date" : "2019-10-11",
  "keywords" :[ "vdw", "soubor vdw", "formát souboru vdw", "typ souboru vdw", "soubor", "typ", "co je soubor vdw" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VDW - formát souboru grafické služby Visio",
  "description":"Další informace o formátu souborů VDW a rozhraních API, která mohou vytvářet a otevírat soubory VDW.",
  "linktitle" : "VDW",
  "menu" : {
    "docs" : {
      "identifier":"visio-vdw",
      "parent" : "visio"
}
},
  "lastmod" : "2019-09-10"
}
## Co je soubor VDW?

VDW je formát souboru Visio Graphics Service, který určuje datové proudy a úložiště potřebné pro vykreslení webového výkresu. Webový výkres je sbírka stránek výkresu, tvarů, písem, obrázků, datových připojení a informací o aktualizaci diagramu, které lze vykreslit jako vektorový nebo rastrový výkres. Soubory VDW lze otevřít také v aplikaci Microsoft Visio, ale primárně se ukládají pro použití na webu. Microsoft Visio nabízí možnost převádět soubory Visio do řady různých formátů souborů včetně [PNG](/cs/image/png/), [BMP](/cs/image/bmp/), [PDF](/cs/pdf/) a dalších.

## **VDW** Formát souboru

Technické specifikace formátu souboru VDW jsou k dispozici online od [Microsoft](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx) a vývojáři na ně mohou odkazovat při vytváření aplikací. Technický dokument popisuje data obsažená ve složeném souboru, který obsahuje úložiště a streamy. Reprezentace webové kresby je možná prostřednictvím streamu s názvem VisioServerData prostřednictvím archivu ZIP. Část ShapGraphic XML v archivu popisuje grafické prvky zobrazené ve webovém výkresu a jsou vyjádřeny v jazyce XAML (Extensible Application Markup Language). Kolekce částí XML v archivu ZIP popisuje datové připojení webového výkresu, informace o jeho tvaru a logiku aktualizace diagramu. Tyto části jsou vyjádřeny jako XML. Část DataGraphic XML popisuje přepočítané vlastnosti, které mají být vyhodnoceny po aktualizaci dat ve webovém výkresu ze zdroje dat. Další položky v archivu ZIP obsahují informace o písmech a obrázcích použitých ve výkresu webu.

|![Možná implementace souboru](/cs/web/vdw.png "Možná implementace souboru")

## Reference

* [[MS-VGSFF]: Formát souboru Visio Graphics Service (.vdw)](https://msdn.microsoft.com/en-us/library/dd924076(v#office.12).aspx)

