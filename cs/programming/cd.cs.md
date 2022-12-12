{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd","co je to soubor cd", "jak otevřít soubor cd", "přípona", "soubor", "soubor cd", "formát souboru cd", "přípona souboru cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Visual Studio Class Diagram File",
  "description":"Další informace o formátu souborů CD a rozhraních API, která mohou vytvářet a otevírat soubory CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## Co je soubor CD?

Soubor s příponou .cd je soubor diagramu tříd sady Visual Studio, který poskytuje informace o struktuře a vztahu mezi všemi třídami v aktuálním řešení. Řešení Visual Studio (reprezentované [.sln](/cs/programming/sln/)) může obsahovat jeden nebo více projektů, z nichž každý má několik různých tříd. Soubor diagramu tříd lze vygenerovat kliknutím pravým tlačítkem myši na projekt a výběrem možnosti diagramu tříd.

## Formát souboru diagramu tříd (.cd) – Další informace

Soubor diagramu tříd je uložen ve standardním formátu souboru XML, který představuje třídy v projektu jako uzly XML. Pokud Visual Studio není k dispozici, lze tyto soubory diagramů tříd otevřít v libovolném aplikačním programu, který podporuje otevírání souborů XML.

### Jak přidat diagramy tříd do projektu Visual Studio

V sadě Visual Studio otevřete řešení/projekt, pro který chcete přidat diagram tříd. Poté klikněte pravým tlačítkem na uzel projektu a zvolte Přidat > Nová položka. Nebo stiskněte Ctrl+Shift+A.

* Otevře se dialogové okno Přidat novou položku.

* Rozbalte Běžné položky > Obecné a poté vyberte Diagram třídy ze seznamu šablon. U projektů Visual C++ vyhledejte šablonu Diagramu třídy v kategorii Utility.

### Export diagramů tříd (CD) do obrázků

Visual Studio umožňuje převádět/exportovat diagramy tříd do obrázků jako [PNG](/cs/image/png/), [JPEG](/cs/image/jpeg/) a [BMP](/cs/image/bmp/). Tyto exportované soubory diagramů tříd lze použít pro účely uchovávání dokumentace a sady technických dat (TDP). Chcete-li převést diagram tříd na obrázek, lze v rámci Microsoft Visual Studio použít následující kroky.

1. Otevřete soubor diagramu tříd (.cd).
1. Z nabídky Diagram tříd nebo z místní nabídky povrchu diagramu zvolte Exportovat diagram jako obrázek.
1. Vyberte diagram.
1. Vyberte požadovaný formát.
1. Pro dokončení exportu zvolte Export.

## Reference

* [Kurzy designu ve Visual Studiu](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

