{
  "date" : "2019-10-11",
  "keywords": [ "csproj file", "csproj", "extension", "format", "What is a csproj file", "csproj file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CSPROJ",
  "description":"Další informace o formátu souboru CSPROJ a rozhraních API, která mohou vytvářet a otevírat soubory CSPROJ.",
  "linktitle" : "CSPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## Co je soubor CSProj?
Soubory s příponou CSPROJ představují soubor projektu C#, který obsahuje seznam souborů zahrnutých v projektu spolu s odkazy na systémová sestavení. Když je v Microsoft VIiual Studio zahájen nový projekt, získáte jeden soubor .csproj spolu s hlavním souborem řešení ([.sln](/cs/programming/sln/)). Pokud je v projektu více než jedno sestavení, bude stejný počet souborů projektu i tam, kde je soubor .sln spojí všechny dohromady jako součást projektu. Obsah tohoto souboru definuje všechny požadavky, které jsou vyžadovány k sestavení projektu, jako je obsah, který má být zahrnut, požadavky platfrom, informace o verzích, nastavení webového serveru nebo databázového serveru a úlohy, které je třeba provést. Obsah souboru projektu je uspořádán ve formátu souboru XML a lze jej otevřít v libovolném textovém editoru pro úpravy i prohlížení. Poskytuje také logický pohled na soubory projektu pro správné uspořádání.

## Formát souboru CSPROJ č.

Vývojáři mohou sami vytvářet soubory projektu a respektovat [Schéma XML MSBuild] (https://msdn.microsoft.com/library/5dy88c2e.aspx). Otevřená a transparentní struktura projektových souborů umožňuje vývojářům aplikací zavést sofistikovanou a jemnou kontrolu nad tím, jak jsou projekty sestavovány a nasazovány. Obsah takového souboru projektu má mezi sebou velmi jasný vztah. Následující obrázek ukazuje klíčové prvky a vztah mezi nimi pro takový soubor projektu.

![](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Následující části vysvětlují prvky formátu souboru pro soubor projektu.

### Prvek projektu ###

Element [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) je kořenovým prvkem každého souboru projektu. Identifikuje schéma XML pro soubor projektu a může obsahovat atributy pro určení vstupních bodů pro proces sestavení.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Vlastnosti a podmínky

Vlastnosti představují nezbytné informace potřebné k sestavení projektu. Takové vlastnosti jsou definovány v prvku [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Tyto vlastnosti se skládají z párů klíč-hodnota, kde název prvku vlastnosti definuje klíč vlastnosti a obsah prvku definuje hodnotu vlastnosti. Můžete například definovat vlastnosti s názvem ServerName a ConnectionString pro uložení statického názvu serveru a připojovacího řetězce.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Podmínky mohou být specifikovány prostřednictvím prvků, aby bylo možné specifikovat kritéria pro vyhodnocení prvku. Toto je určeno slovem podmínky při definování vlastnosti, jak je uvedeno níže:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Když MSBuild zpracuje tuto definici vlastnosti, nejprve zkontroluje, zda je k dispozici hodnota vlastnosti **$(OutputRoot)**. Pokud je hodnota vlastnosti prázdná – jinými slovy, uživatel nezadal hodnotu pro tuto vlastnost – podmínka se vyhodnotí jako **true** a hodnota vlastnosti je nastavena na **..\Publish\Out.**

### Položky a skupiny položek

Soubor projektu definuje vstupy do procesu sestavení, což jsou ve skutečnosti různé typy souborů. V nomenklatuře MSBuild jsou tyto vstupy reprezentovány prvky Item a jsou definovány v prvku [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Stejně jako prvky **Property** můžete prvek **Item** pojmenovat, jak chcete. Musíte však zadat atribut **Zahrnout** k identifikaci souboru nebo zástupného znaku, který položka představuje.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Cíle a úkoly

Prvek [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) představuje individuální instrukci sestavení (nebo úlohu). MSBuild obsahuje velké množství předdefinovaných úloh. Například:

* Úloha **Kopírovat** zkopíruje soubory do nového umístění.
* Úloha **Csc** vyvolá kompilátor Visual C#.
* Úloha **Vbc** vyvolá kompilátor jazyka Visual Basic.
* Úloha **Exec** spouští určený program.
* Úloha **Zpráva** zapíše zprávu do loggeru.

Úkoly musí být vždy obsaženy v prvcích [Target](https://msdn.microsoft.com/library/t50z2hka.aspx). Element **Target** je sada jedné nebo více úloh, které se provádějí postupně, a soubor projektu může obsahovat více cílů.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Reference

* [Porozumění souboru projektu – MSDN](https://docs.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- soubor)

