{
  "date": "2019-10-11",
  "keywords": [
"comhad csproj",
"csproj",
"síneadh",
"formáid",
"Cad is comhad csproj ann",
"formáid comhaid csproj"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CSPROJ",
  "description": "Foghlaim faoi fhormáid comhaid CSPROJ agus APIanna ar féidir leo comhaid CSPROJ a chruthú agus a oscailt.",
  "linktitle": "CSPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-cspro-gaj"
}
},
  "lastmod": "2021-05-21"
}

## Cad is comhad CSProj ann?
Is ionann comhaid le síneadh CSPROJ agus comhad tionscadail C# ina bhfuil liosta na gcomhad atá san áireamh i dtionscadal mar aon leis na tagairtí do chomhthionóil chórais. Nuair a thionscnaítear tionscadal nua i Microsoft VIiual Studio, faigheann tú comhad .csproj amháin mar aon leis an bpríomhchomhad réitigh ([.sln](/programming/sln/)). Má bhíonn níos mó ná tionóil amháin i dtionscadal, beidh an líon céanna comhad tionscadail ann freisin nuair a nascann an comhad .sln iad go léir le chéile mar chuid den tionscadal. Sainmhíníonn ábhar an chomhaid seo na ceanglais go léir a theastaíonn chun an tionscadal a thógáil ar nós an t-ábhar atá le cur san áireamh, na riachtanais ardán, faisnéis maidir le leagan, socruithe freastalaí gréasáin nó freastalaí bunachar sonraí, agus na tascanna nach mór a dhéanamh. Socraítear a bhfuil i gcomhad tionscadail i bhformáid comhaid XML agus is féidir é a oscailt in aon eagarthóir téacs le haghaidh eagarthóireacht agus féachaint air. Tugann sé léargas loighciúil freisin ar chomhaid an tionscadail chun socrú ceart a dhéanamh.

## Formáid Chomhaid CSPROJ #

Developers can create project files by themselves as well honouring the [MSBuild XML Schema](https://msdn.microsoft.com/library/5dy88c2e.aspx). The open and transparent structure of project files lets application developers impose sophisticated and fine-grained control over how the projects are built and deployed. The contents of such a project file have a very clear relationship among themselves. The following figure shows key elements and the relationship between these for such a project file.

![](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file/_static/image2.png)

Déanann na hailt seo a leanas na heilimintí formáid comhaid do chomhad tionscadail a mhionsaothrú.

### Eilimint an Tionscadail ###

Is í an eilimint [Project](https://msdn.microsoft.com/library/bcxfsh87.aspx) buneilimint gach comhad tionscadail. Sainaithníonn sé scéimre XML don chomhad tionscadail agus féadann sé tréithe a áireamh chun na pointí iontrála don phróiseas tógála a shonrú.

```
<Project ToolsVersion#"4.0" DefaultTargets#"FullPublish"
        xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
</Project>
```

### Airíonna agus Coinníollacha

Léiríonn airíonna an fhaisnéis riachtanach a theastaíonn chun tionscadal a thógáil. Sainmhínítear airíonna den sórt sin laistigh d'eilimint [PropertyGroup](https://msdn.microsoft.com/library/t4w159bs.aspx). Is éard atá sna hairíonna seo ná péirí eochairluacha ina sainmhíníonn ainm na heiliminte maoine an eochair airí agus sainmhíníonn ábhar na heiliminte an luach maoine. Mar shampla, d'fhéadfá airíonna darb ainm ServerName agus ConnectionString a shainiú chun ainm freastalaí statach agus teaghrán ceangail a stóráil.

```
<PropertyGroup>    
 <ServerName>FABRIKAM\TEST1</ServerName>
 <ConnectionString>
     Data Source#FABRIKAM\TESTDB;InitialCatalog#ContactManager,...
 </ConnectionString>
</PropertyGroup>
```

Is féidir coinníollacha a shonrú trí eilimintí chun na critéir chun an eilimint a mheas a shonrú. Sonraítear é seo le focal Coinníoll agus an t-airí á sainmhíniú mar a thaispeántar thíos:

```
<PropertyGroup>
<OutputRoot Condition#" '$(OutputRoot)'##'' ">..\Publish\Out\</OutputRoot>
   ...
</PropertyGroup>
```

Nuair a phróiseálann MBuild an sainmhíniú maoine seo, seiceálann sé ar dtús féachaint an bhfuil luach maoine **$(OutputRoot)** ar fáil. Má tá luach na réadmhaoine bán—i bhfocail eile, níor chuir an t-úsáideoir luach ar fáil don mhaoin seo—measann an riocht go **fíor** agus socraítear luach na maoine mar **..\Foilsigh\Amach.**

### Míreanna agus Grúpaí Míreanna

Sainmhíníonn comhad tionscadail ionchuir sa phróiseas tógála ar cineálacha éagsúla comhaid iad i ndáiríre. In ainmníocht MBuild, déantar na hionchuir seo a léiriú ag eilimintí Mír agus sainítear iad laistigh d'eilimint [ItemGroup](https://msdn.microsoft.com/library/646dk05y.aspx). Díreach cosúil le heilimintí **Maoine**, is féidir leat eilimint **Mír** a ainmniú, cibé rud is mian leat. Mar sin féin, ní mór duit aitreabúid **Cuir san áireamh** a shonrú chun an comhad nó an cárta saoróg a léiríonn an mhír a shainaithint.

```
<ItemGroup>
<ProjectsToBuild Include#"$(SourceRoot)ContactManager-WCF.sln"/>
</ItemGroup>
```

### Spriocanna agus Tascanna

Léiríonn eilimint [Task](https://msdn.microsoft.com/library/77f2hx1s.aspx) teagasc (nó tasc) tógála aonair. Áirítear ar MBuild an iliomad tascanna réamhshainithe. Mar shampla:

* Déanann an tasc **Cóipeáil** comhaid a chóipeáil go dtí suíomh nua.

* Déanann tasc **Csc** an tiomsaitheoir Visual C# a agairt.

* Déanann tasc **Vbc** an tiomsaitheoir Visual Basic a agairt.

* Ritheann tasc **Exec** clár sonraithe.

* Scríobhann an tasc **Teachtaireacht** teachtaireacht chuig logálaí.


Ní mór tascanna a bheith laistigh de mhíreanna [Target](https://msdn.microsoft.com/library/t50z2hka.aspx) i gcónaí. Is éard is eilimint **Sprioc** ann ná sraith de thasc amháin nó níos mó a dhéantar go seicheamhach, agus is féidir le spriocanna iolracha a bheith i gcomhad tionscadail.

```
<Project xmlns#"http://schemas.microsoft.com/developer/msbuild/2003">
<Target Name#"LogMessage">
 <Message Text#"Hello world!" />
</Target>
</Project>
```

## Tagairtí

* [Comhad an Tionscadail a Thuiscint - MSDN](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project- comhad)


