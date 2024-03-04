{
  "date": "2019-10-11",
  "keywords": [
"csproj failą",
"csproj",
"pratęsimas",
"formatu",
"Kas yra csproj failas",
"csproj failo formatas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "Sužinokite apie CSPROJ failo formatą ir API, kurios gali kurti ir atidaryti CSPROJ failus.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-ltj"
}
},
  "lastmod": "2021-05-21"
}

## Kas yra CSProj failas?
Failai su CSPROJ plėtiniu yra C# projekto failas, kuriame yra į projektą įtrauktų failų sąrašas kartu su nuorodomis į sistemos mazgus. Kai Microsoft VIiual Studio inicijuojamas naujas projektas, kartu su pagrindinio sprendimo ([.sln](/programming/sln/)) failu gaunate vieną .csproj failą. Jei projekte yra daugiau nei vienas rinkinys, bus vienodas projekto failų skaičius, kai .sln failas juos visus susieja kaip projekto dalį. Šio failo turinys apibrėžia visus reikalavimus, kurių reikia norint sukurti projektą, pvz., įtrauktiną turinį, platformos reikalavimus, versijų kūrimo informaciją, žiniatinklio serverio arba duomenų bazės serverio nustatymus ir užduotis, kurias reikia atlikti. Projekto failo turinys yra išdėstytas XML failo formatu ir gali būti atidarytas bet kuriame teksto rengyklėje, kad būtų galima redaguoti ir peržiūrėti. Tai taip pat suteikia logišką projekto failų vaizdą, kad būtų galima tinkamai sutvarkyti.

## CSPROJ failo formatas Nr.

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Tolesniuose skyriuose aprašomi projekto failo failo formato elementai.

### Projekto elementas ###

Elementas [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) yra pagrindinis kiekvieno projekto failo elementas. Ji identifikuoja projekto failo XML schemą ir gali apimti atributus, nurodančius kūrimo proceso įvesties taškus.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Savybės ir sąlygos

Savybės – tai reikalinga informacija, reikalinga projektui sukurti. Tokios savybės yra apibrėžtos [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx) elemente. Šias ypatybes sudaro rakto ir reikšmių poros, kuriose ypatybės elemento pavadinimas apibrėžia nuosavybės raktą, o elemento turinys – ypatybės reikšmę. Pavyzdžiui, galite apibrėžti ypatybes pavadinimu ServerName ir ConnectionString, kad išsaugotumėte statinį serverio pavadinimą ir ryšio eilutę.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Sąlygos gali būti nurodytos per elementus, kad būtų nurodyti elemento vertinimo kriterijai. Tai nurodoma sąlyga, apibrėžiant ypatybę, kaip parodyta toliau:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Kai MSBuild apdoroja šią nuosavybės apibrėžimą, ji pirmiausia patikrina, ar yra **$(OutputRoot)** ypatybės reikšmė. Jei nuosavybės vertė yra tuščia (kitaip tariant, vartotojas nepateikė šios nuosavybės vertės), sąlyga įvertinama kaip **true**, o ypatybės vertė nustatoma į **..\Publish\Out.**

### Prekės ir prekių grupės

Projekto failas apibrėžia kūrimo proceso įvestis, kurios iš tikrųjų yra skirtingų tipų failai. MSBuild nomenklatūroje šios įvesties pateikiamos elementų elementais ir yra apibrėžtos elemente [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Kaip ir **Nuosavybės** elementus, **Prekės** elementą galite pavadinti taip, kaip norite. Tačiau turite nurodyti atributą **Include**, kad identifikuotumėte failą arba pakaitos simbolį, kurį reiškia elementas.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Tikslai ir užduotys

Elementas [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) reiškia individualią kūrimo instrukciją (arba užduotį). MSBuild apima daugybę iš anksto nustatytų užduočių. Pavyzdžiui:

* Užduotis **Kopijuoti** nukopijuoja failus į naują vietą.

* **Csc** užduotis iškviečia Visual C# kompiliatorių.

* **Vbc** užduotis iškviečia „Visual Basic“ kompiliatorių.

* **Exec** užduotis vykdo nurodytą programą.

* Užduotis **Pranešimas** rašo pranešimą registruotojui.


Užduotys visada turi būti įtrauktos į [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elementus. Elementas **Target** yra vienos ar daugiau užduočių, kurios vykdomos nuosekliai, rinkinys, o projekto faile gali būti keli tikslai.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Nuorodos

* [Projekto failo supratimas – MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- failas)


