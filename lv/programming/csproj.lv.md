{
  "date": "2019-10-11",
  "keywords": [
"csproj failu",
"csproj",
"pagarinājumu",
"formātā",
"Kas ir csproj fails",
"csproj faila formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "Uzziniet par CSPROJ faila formātu un API, kas var izveidot un atvērt CSPROJ failus.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-lvj"
}
},
  "lastmod": "2021-05-21"
}

## Kas ir CSProj fails?
Faili ar CSPROJ paplašinājumu ir C# projekta fails, kurā ir iekļauts projektā iekļauto failu saraksts, kā arī atsauces uz sistēmas komplektiem. Kad programmā Microsoft VIiual Studio tiek uzsākts jauns projekts, jūs saņemat vienu .csproj failu kopā ar galvenā risinājuma ([.sln](/programming/sln/)) failu. Ja projektā ir vairāk nekā viens komplekts, būs vienāds projekta failu skaits, kur .sln fails tos visus saista kopā kā daļu no projekta. Šī faila saturs nosaka visas prasības, kas ir nepieciešamas, lai izveidotu projektu, piemēram, iekļaujamo saturu, platformas prasības, versijas informāciju, tīmekļa servera vai datu bāzes servera iestatījumus un veicamos uzdevumus. Projekta faila saturs ir sakārtots XML faila formātā, un to var atvērt jebkurā teksta redaktorā rediģēšanai, kā arī apskatei. Tas arī sniedz loģisku skatu uz projekta failiem pareizai sakārtošanai.

## CSPROJ faila formāts Nr.

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Nākamajās sadaļās ir aprakstīti projekta faila faila formāta elementi.

### Projekta elements ###

Elements [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) ir katra projekta faila saknes elements. Tas identificē projekta faila XML shēmu un var ietvert atribūtus, lai norādītu veidošanas procesa ievades punktus.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Īpašības un nosacījumi

Rekvizīti atspoguļo nepieciešamo informāciju, kas nepieciešama, lai izveidotu projektu. Šādi rekvizīti ir definēti elementā [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Šie rekvizīti sastāv no atslēgu un vērtību pāriem, kur rekvizīta elementa nosaukums definē rekvizīta atslēgu un elementa saturs nosaka rekvizīta vērtību. Piemēram, varat definēt rekvizītus ar nosaukumu ServerName un ConnectionString, lai saglabātu statisku servera nosaukumu un savienojuma virkni.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Nosacījumi var tikt norādīti caur elementiem, lai precizētu elementa novērtēšanas kritērijus. To norāda nosacījuma vārds, definējot īpašumu, kā parādīts tālāk:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Kad MSBuild apstrādā šo rekvizītu definīciju, tā vispirms pārbauda, vai ir pieejama rekvizīta vērtība **$(OutputRoot)**. Ja rekvizīta vērtība ir tukša — citiem vārdiem sakot, lietotājs nav norādījis vērtību šim īpašumam, nosacījums tiek novērtēts kā **true** un rekvizīta vērtība ir iestatīta uz **..\Publish\Out.**

### Preces un preču grupas

Projekta fails definē veidošanas procesa ievadi, kas faktiski ir dažādi failu tipi. MSBuild nomenklatūrā šīs ievades tiek attēlotas ar vienumu elementiem un ir definētas elementā [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Tāpat kā **Property** elementiem, varat nosaukt elementu **Item**, kā vēlaties. Tomēr ir jānorāda atribūts **Include**, lai identificētu failu vai aizstājējzīmi, ko vienums pārstāv.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Mērķi un uzdevumi

Elements [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) apzīmē atsevišķu veidošanas instrukciju (vai uzdevumu). MSBuild ietver daudzus iepriekš definētus uzdevumus. Piemēram:

* Uzdevums **Kopēt** kopē failus uz jaunu vietu.

* **Csc** uzdevums izsauc Visual C# kompilatoru.

* **Vbc** uzdevums izsauc Visual Basic kompilatoru.

* **Exec** uzdevums palaiž noteiktu programmu.

* Uzdevums **Ziņojums** raksta ziņojumu reģistrētājam.


Uzdevumiem vienmēr ir jābūt ietvertiem [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) elementos. Elements **Target** ir viena vai vairāku uzdevumu kopa, kas tiek izpildīti secīgi, un projekta failā var būt vairāki mērķi.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Atsauces

* [Izpratne par projekta failu — MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- fails)


