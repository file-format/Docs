{
  "date" : "2022-01-04",
  "keywords" :[ ".dst", "plik", "format", "rozszerzenie", "API", "Zestaw arkuszy AutoCAD" ],
  "author" :{
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DST - plik zestawu arkuszy programu AutoCAD",
  "description" :"Poznaj plik .dst i interfejsy API, które mogą tworzyć i otwierać pliki DST.",
  "linktitle" : "DST",
  "menu" :{
    "docs" :{
      "parent" : "cad"
}
},
  "lastmod" : "2022-01-04"
}

## Czym jest plik DST?

Plik DST to plik programu AutoCAD, który zawiera powiązania i informacje do definiowania zestawów arkuszy. Są one przechowywane w domyślnym folderze przechowywania zestawu arkuszy, Zestawy arkuszy programu AutoCAD. Pliki DST nie zawierają rzeczywistych układów rysunków, ale odnoszą się do nich z wybranych plików [DWG](/pl/cad/dwg/) i [DWT](/pl/cad/dwt/) powiązanych z tymi zestawami arkuszy. W środowisku sieciowym wszyscy członkowie zespołu powinni mieć dostęp sieciowy do tych powiązanych plików. Pliki DST są zapisywane na dysku w formacie pliku [XML](/pl/web/xml/).

## Format pliku DST — więcej informacji

Pliki DST są tworzone za pomocą narzędzia AutoDesk Sheet Set Manager (SSM). Gdy ktoś z zespołu uzyskuje dostęp do pliku, plik DST jest na krótko otwierany, a następnie zapisywany z powrotem ze zaktualizowanymi informacjami. Jednoczesny dostęp do tego samego pliku DST jest zarządzany przez narzędzie SSM, które pokazuje ikonę kłódki, gdy plik jest dostępny.

W dowolnym momencie stan arkusza może mieć dowolny z poniższych stanów.

* Arkusz jest dostępny do edycji.
* Arkusz jest zablokowany.
* Brakuje arkusza lub znajduje się on w nieoczekiwanym folderze.

## Bibliografia

* [Informacje o korzystaniu z zestawów arkuszy DST](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-577D8EA0-85F2-4829-B4F9-8CAD6F7AAACC)
* [Dowiedz się więcej o zestawach arkuszy](https://help.autodesk.com/view/ACDLT/2017/ENU/?guid=GUID-34D889BC-19AD-4CD1-ADB1-F359D9B515FB)
* [Mastering zestawów arkuszy programu AutoCAD](https://damassets.autodesk.net/content/dam/autodesk/www/cad-manager-center/articles/Mastering-AutoCAD-Sheet-Sets_Preview_EN.pdf)

