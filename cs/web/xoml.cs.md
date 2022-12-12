{
  "date" : "2019-10-11",
  "keywords" :["xoml", "Soubor", "Rozšíření", "Formát souboru", "Přípona souboru", "Extensible Object Markup Language"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XOML - Windows Workflow File Format",
  "description":"Další informace o formátu souboru XOML a rozhraních API, která mohou vytvářet a otevírat soubory XOML.",
  "linktitle" : "XOML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor XOML?

XOML je zkratka pro Extensible Object Markup Language a je to serializační formát pro objekty pracovního postupu Windows Workflow Foundation. Na základě **[XAML](/cs/web/xaml/)** se většinou používá pro vytváření uživatelských rozhraní v prostém **[XML](/cs/web/xml/)**. Ty se používají k deklaraci pracovního postupu pro uživatelské rozhraní a jsou kompilovány spolu se samostatným souborem obsahujícím implementační logiku. Obsahuje stromovou strukturu, která definuje kořenový uzel pracovního postupu, vnořené dílčí prvky a vložené segmenty kódu. Když je vytvořen nový pracovní postup pomocí sady Visual Studio for .NET, máte možnost zvolit, zda má být ve formátu Code format nebo Code Separated. V případě, že vyberete pozdější, IDE vám vytvoří dva soubory; jeden ve formátu XOML (sestávající z rozvržení pracovního postupu a nastavení) a druhý ve formátu [.CS](/cs/programming/cs/)/[.VB](/cs/programming/vb/), kde se nachází programovací kód.

