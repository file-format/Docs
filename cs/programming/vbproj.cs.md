{
  "date" : "2019-10-11",
  "keywords" :[ "vbproj", "soubor", "přípona", "formát souboru", "VB Project File", "Programming Guide" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VBPROJ",
  "description":"Další informace o formátu souborů VBPROJ a rozhraních API, která mohou vytvářet a otevírat soubory VBPROJ.",
  "linktitle" : "VBPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor VBPROJ?

Soubor s příponou .vbproj je soubor projektu Microsoft Visual Basic, který používá modul MSBuild společnosti Microsoft k vytváření projektů v rámci řešení sady Visual Studio. Je podobný souboru [CSPROJ](/cs/programming/csproj/) pro .NET projekty napsané v [C#](/cs/programming/cs/). Modul MSBuild čte informace obsažené v různých skupinách ze souborů VBPROJ a generuje výstupní soubor. Soubor VBPROJ může obsahovat informace související s globálními identifikátory, třídami a vlastnostmi, které definují projekt. Soubory VBPROJ lze otevírat a upravovat pomocí Microsoft Visual Studio a libovolného běžného textového editoru, jako je Poznámkový blok v operačních systémech Windows a MacOS.

## Formát souboru VBPROJ - Další informace

Soubory VBPROJ jsou textové soubory, které jsou napsány ve formátu souboru [XML](/cs/web/xml/) na základě [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). Soubor VBPROJ obsahuje informace ve formě značek XML, které definují informace související s konkrétní skupinou nastavení. Důrazně se doporučuje otevřít a upravit tyto soubory nastavení v Microsoft Visual Studio IDE.

### Prvky VBPROJ

Základní prvky souboru VB Settings jsou znázorněny na následujícím obrázku.

{{< figure src="../vbproj.png" alt="Formát souboru VBPROJ" >}}

Následující tabulka poskytuje stručný popis těchto prvků.

|Prvek|Popis|
---|---|
|Projekt| Kořenový prvek každého souboru projektu a kromě identifikace schématu XML pro soubor projektu může obsahovat atributy pro specifikaci vstupních bodů pro proces sestavení|
|Vlastnosti a podmínky| Vlastnosti se skládají z párů klíč–hodnota a jsou definovány v prvku PropertyGroup. Název prvku vlastnosti představuje klíč vlastnosti a obsah prvku definuje hodnotu vlastnosti.|
|Položky a skupiny položek|Položky v souboru projektu jsou vstupy do procesu sestavení, jako jsou soubory s kódem souborů, konfigurační soubory, soubory příkazů a další potřebné jako součást procesu sestavení. Položky jsou a musí být definovány v rámci prvku ItemGroup.|
|Cíle a úkoly| Prvek Task představuje individuální instrukci sestavení (nebo úkol). MSBuild obsahuje velké množství předdefinovaných úloh, jako je kopírování, CSC, VBC, Exec. Úkoly musí být vždy obsaženy v prvku `Target`, což je sada jednoho nebo více úkolů, které se provádějí postupně, a soubor projektu může obsahovat více cílů.|

## Reference

* [Porozumění souboru projektu](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)
* [Prvky schématu MSBuild](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)

