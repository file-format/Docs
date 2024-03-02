{
  "date": "2019-10-11",
  "keywords": [
"comhad sln",
"conas comhad sln a rith",
"sln",
"síneadh",
"formáid",
"Cad é comhad sln",
"formáid comhaid sln",
"Réiteach Stiúideo Amharc",
"Visual Studio réiteach vs tionscadal"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SLN",
  "description": "Foghlaim faoi fhormáid comhaid SLN agus APIanna ar féidir leo comhaid SLN a chruthú agus a oscailt.",
  "linktitle": "SLN",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-sl-gan"
}
},
  "lastmod": "2019-09-10"
}

## Cad é comhad SLN?
Is ionann comhad le síneadh .SLN agus comhad **Réiteach Stiúideo Amhairc** a choinníonn faisnéis faoi eagrú tionscadal i gcomhad réitigh. Tá a bhfuil i gcomhad réitigh den sórt sin scríofa i ngnáth-théacs laistigh den chomhad agus is féidir é a fheiceáil / eagarthóireacht a dhéanamh air ach an comhad a oscailt in aon eagarthóir téacs. Fanann an fhaisnéis atá i gcomhad réitigh marthanach agus úsáidtear í chun an fhaisnéis a bhaineann leis an réiteach ar nós [projects ](/programming/csproj/)agus aon fhaisnéis riachtanach eile a lódáil. Tá faisnéis bhreise sna comhaid tionscadail dá dtagraítear sa chomhad réitigh chun an timpeallacht a chumasú chun an t-ordlathas a líonadh le míreanna an tionscadail sin. Ní stóráiltear aon sonraí sa chomhad .sln, cé gur féidir faisnéis tionscadail a scríobh chuig an gcomhad .sln más gá.

## **Stair Leaganacha SLN** ##

Tá an leagan fhormáid réitigh tar éis teacht chun cinn le gach réiteach Microsoft Visual Studio le himeacht ama. Seo a leanas na sonraí fúthu seo.


| Leagan Amharc-Stiúideo|Leagan i bhFormáid Réitigh
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **Ábhar Comhad Réitigh** ###

Tá roinnt codanna i gcomhad réitigh a léann an timpeallacht chun an tionscadal a luchtú. Tá inneachar samplach comhaid .sln mar a thaispeántar thíos.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **Dearbhú Tionscadail** ###

Is féidir le comhad réitigh níos mó ná dearbhú tionscadail amháin agus sin freisin maidir le cineálacha éagsúla tionscadal. Mar shampla, is féidir le CSharp chomh maith le tionscadal VB.NET a bheith i gcomhad réitigh aonair. Déantar na cineálacha seo a idirdhealú i dtuaslagán ag baint úsáide as an [Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). Is féidir an dearbhú tionscadail thuas a ghinearálú mar seo a leanas chun tuiscint shoiléir a fháil.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Cineál-GUID:` Tá an Tionscadal-Cineál-GUID uathúil do chineálacha éagsúla tionscadal agus tá sé in úsáid ag an léitheoir réitigh chun an cineál tionscadail a aithint. Sa chás seo, léiríonn F184B08F-C81C-45F6-A57F-5ABD9991F28F gur tionscadal VB.NET é.

`TREOIR Tionscadail:` GUID uathúil an tionscadail a dhéanann idirdhealú idir é agus tionscadail eile sa réiteach. Mar gheall ar ID uathúil tionscadail sa réiteach is féidir le tionscadail eile sa réiteach rochtain a fháil air.

Bunaithe ar an bhfaisnéis atá sa rannán tionscadail den chomhad .sln, lódálann an timpeallacht gach comhad tionscadail. Tá an tionscadal féin freagrach ansin as an ordlathas tionscadail a líonadh agus as aon tionscadail neadaithe a luchtú. Déantar aon athruithe a dhéantar ar an réiteach a shábháil ar ais sa chomhad réitigh nuair a dhéantar an tionscadal a shábháil nó a dhúnadh.

## Visual Studio réiteach vs tionscadal

**Tionscadal:** Go loighciúil, nuair a thosaíonn tú aip nó bogearraí a chruthú trí úsáid a bhaint as Visual Studio, cuireann tú tús le tionscadal nua. Tá gach comhad riachtanach i dtionscadal, mar shampla cód foinse, deilbhíní, íomhánna, comhaid sonraí, agus go leor eile, a thiomsófar in aip inrite, suíomh Gréasáin nó leabharlann.

**Réiteach:** Tá tionscadal amháin nó níos mó i réiteach. Mar sin tá an réiteach díreach cosúil le coimeádán do thionscadail Visual Studio. Go loighciúil, is féidir linn a rá go bhfuil duine ag iarraidh réiteach iomlán a fháil dá ghnó lena n-áirítear suíomh Gréasáin, aip deisce, seirbhís scíthe agus app soghluaiste.

### **Tagairtí** ###

* [Comhad Réitigh - Le MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)

* [GUIDanna Cineál Tionscadail](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)


