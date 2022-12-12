{
  "date" : "2021-04-22",
  "keywords": [ "aps file", "visual studio aps file", "extension", "format","aps file visual studio","aps file extension","how to open aps file","APS file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APS - Visual C++ Resource File",
  "description":"Další informace o formátu souboru APS s příkladem APS a rozhraními API, která mohou vytvářet a otevírat soubory APS.",
  "linktitle" : "APS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Co je formát souboru APS?
Soubor APS je vytvořen Visual C++, aplikací pro vývoj softwaru od společnosti Microsoft. Ukládá binární reprezentaci zdroje začleněného do projektu a umožňuje aplikaci načítat zdroje rychleji. Tyto soubory můžete snadno najít s příponou .aps. Ve skutečnosti editory prostředků přímo nečtou soubory resource.h, proto je kompilátor prostředků kompiluje do souborů .aps, které jsou spotřebovávány editory prostředků.

## Formát souboru APS
Formát souboru APS je pouze krokem kompilace a ukládá pouze symbolická data. Nesymbolické informace, jako jsou komentáře, jsou během procesu kompilace zahozeny. Když například uložíte, editor prostředků přepíše soubor skriptu prostředku a soubor resource.h. Jakékoli změny samotných prostředků zůstanou začleněny do souboru skriptu prostředků, ale po přepsání souboru skriptu prostředků budou komentáře vždy ztraceny.


## Reference

* [Soubory zdrojů (C++)](https://docs.microsoft.com/en-us/cpp/windows/resource-files-visual-studio?view=msvc-160)
 


