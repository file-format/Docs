{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"comhad",
"síneadh",
"formáid comhaid",
"Comhad Tionscadal VB",
"Treoir Ríomhchlárúcháin"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "Foghlaim faoi fhormáid comhaid VBPROJ agus APIs is féidir comhaid VBPROJ a chruthú agus a oscailt.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-gaj"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad VBPROJ ann?

Is comhad tionscadail Microsoft Visual Basic é comhad le síneadh .vbproj a úsáideann inneall MBuild Microsoft chun na tionscadail a thógáil laistigh de réiteach Visual Studio. Tá sé cosúil le comhad [CSPROJ](/programming/csproj/) do thionscadail .NET atá scríofa in [C#](/programming/cs/). Léann an t-inneall MBuild faisnéis atá i ngrúpaí éagsúla ó na comhaid VBPROJ agus gineann an comhad aschuir. Is féidir faisnéis a bhaineann le haitheantóirí domhanda, aicmí agus airíonna a shainíonn an tionscadal a bheith i gcomhad VBPROJ. Is féidir comhaid VBPROJ a oscailt agus a chur in eagar ag baint úsáide as Microsoft Visual Studio agus aon eagarthóir téacs coitianta ar nós Notepad ar Chórais Oibriúcháin Windows agus MacOS.

## Formáid Chomhaid VBPROJ - Tuilleadh Eolais

Is comhaid téacs iad comhaid VBPROJ atá scríofa i bhformáid comhaid [XML](/web/xml/) bunaithe ar [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). Tá faisnéis i gcomhad VBPROJ i bhfoirm clibeanna XML a shainíonn faisnéis a bhaineann leis an ngrúpa socruithe áirithe sin. Moltar go mór na comhaid socruithe seo a oscailt agus a chur in eagar i Microsoft Visual Studio IDE.

### Eilimintí VBPROJ

Tá na comhchodanna de chomhad Socruithe VB mar a thaispeántar san íomhá seo a leanas.

{{< figure src="../vbproj.png" alt="Formáid Comhaid VBPROJ" >}}

The following table gives a brief description of these elements.

|Eilimint|Cur Síos|
---|---|
|Tionscadal| Bunghné de gach comhad tionscadail agus is féidir tréithe a áireamh leis na pointí iontrála don phróiseas tógála a shonrú chomh maith le scéimre XML a aithint don chomhad tionscadail|
|Airíonna agus Coinníollacha| Péirí eochairluacha atá i réadmhaoin agus sainítear iad le heilimint PropertyGroup. Seasann an t-ainm maoine don eochair airí agus sainmhíníonn ábhar na heiliminte an luach maoine.|
|Míreanna agus Grúpaí Míreanna|Is éard atá i míreanna i gcomhad tionscadail ná ionchuir sa phróiseas tógála mar chomhaid chóid-chomhaid, comhaid cumraíochta, comhaid ordaithe, agus cinn eile a theastaíonn mar chuid den phróiseas tógála. Tá agus ní mór míreanna a shainiú laistigh d'eilimint ItemGroup.|
|Spriocanna agus Tascanna| Is ionann eilimint Tasc agus teagasc (nó tasc) tógála aonair. Áirítear ar MBuild an iliomad tascanna réamhshainithe mar Cóip, CSC, VBC, Feidhmeannacht. Ní mór tascanna a bheith i gcónaí in Eilimint `Sprioc` arb é atá ann ná sraith de thasc amháin nó níos mó a chuirtear i gcrích go seicheamhach, agus is féidir le spriocanna iolracha a bheith i gcomhad tionscadail.|

## Tagairtí

* [Comhad an Tionscadail a Thuiscint]( https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [Eilimintí Scéimre MSBuild]( https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


