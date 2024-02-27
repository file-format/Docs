{
  "date": "2019-10-11",
  "keywords": [
"csproj fil",
"csproj",
"udvidelse",
"format",
"Hvad er en csproj fil",
"csproj filformat"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "Lær om CSPROJ filformat og API'er, der kan oprette og åbne CSPROJ filer.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-daj"
}
},
  "lastmod": "2021-05-21"
}

## Hvad er en CSProj fil?
Filer med CSPROJ-udvidelse repræsenterer en C#-projektfil, der indeholder listen over filer, der er inkluderet i et projekt, sammen med referencerne til systemsamlinger. Når et nyt projekt startes i Microsoft VIiual Studio, får du én .csproj-fil sammen med hovedløsningsfilen ([.sln](/programming/sln/)). Hvis der er mere end én samlinger i et projekt, vil der også være lige mange projektfiler, hvor .sln-filen binder dem alle sammen som en del af projektet. Indholdet af denne fil definerer alle de krav, der kræves for at bygge projektet, såsom indhold, der skal inkluderes, platformskravene, versionsinformation, webserver- eller databaseserverindstillinger og de opgaver, der skal udføres. Indholdet af en projektfil er arrangeret i XML-filformat og kan åbnes i en hvilken som helst teksteditor til redigering såvel som visning. Det giver også et logisk overblik over projektfilerne for korrekt arrangement.

## CSPROJ filformat #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

De følgende afsnit uddyber filformatelementerne for en projektfil.

### Projektelement ###

[Project](https://msdn.microsoft.com/library/bcxfsh87.aspx)-elementet er rodelementet i hver projektfil. Det identificerer XML-skemaet for projektfilen og kan inkludere attributter til at specificere indgangspunkterne for byggeprocessen.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Egenskaber og betingelser

Egenskaber repræsenterer den nødvendige information, der kræves for at bygge et projekt. Sådanne egenskaber er defineret i et [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx)-element. Disse egenskaber består af nøgle-værdi-par, hvor egenskabselementnavnet definerer egenskabsnøglen og indholdet af elementet definerer egenskabsværdien. For eksempel kan du definere egenskaber med navnet ServerName og ConnectionString for at gemme et statisk servernavn og en forbindelsesstreng.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Betingelser kan specificeres via elementer for at specificere kriterierne for evaluering af elementet. Dette er specificeret af betingelsesord, mens egenskaben defineres som vist nedenfor:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Når MSBuild behandler denne egenskabsdefinition, kontrollerer den først, om en **$(OutputRoot)** egenskabsværdi er tilgængelig. Hvis egenskabsværdien er tom – med andre ord, brugeren ikke har angivet en værdi for denne egenskab – evalueres betingelsen til **sand** og egenskabsværdien indstilles til **..\Publish\Out.**

### Varer og varegrupper

En projektfil definerer input til byggeprocessen, som faktisk er forskellige filtyper. I MSBuild-nomenklaturen er disse input repræsenteret af Item-elementer og er defineret i et [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx)-element. Ligesom **Ejendom**-elementer kan du navngive et **Vare**-element, som du vil. Du skal dog angive en **Inkluder**-attribut for at identificere filen eller jokertegn, som varen repræsenterer.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Mål og opgaver

Et [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx)-element repræsenterer en individuel byggeinstruktion (eller opgave). MSBuild inkluderer et væld af foruddefinerede opgaver. For eksempel:

* Opgaven **Kopier** kopierer filer til en ny placering.

* **Csc**-opgaven kalder Visual C#-kompileren.

* **Vbc**-opgaven kalder Visual Basic-kompileren.

* **Exec**-opgaven kører et specificeret program.

* Opgaven **Besked** skriver en besked til en logger.


Opgaver skal altid være indeholdt i [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elementer. Et **Target**-element er et sæt af en eller flere opgaver, der udføres sekventielt, og en projektfil kan indeholde flere mål.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Referencer

* [Forstå projektfilen - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fil)


