{
  "date": "2019-10-11",
  "keywords": [
"vcxproj",
"comhad",
"síneadh",
"formáid comhaid",
"Tionscadal Visual C++",
"Treoir Ríomhchlárúcháin"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCXPROJ",
  "description": "Foghlaim faoi fhormáid comhaid VCXPROJ agus APIs is féidir comhaid VCXPROJ a chruthú agus a oscailt.",
  "linktitle": "VCXPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vcxpro-gaj"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad VCXPROJ ann?

Is comhad tionscadail de chuid Microsoft Visual C++ é comhad a bhfuil iarmhír .vcxproj air a stórálann faisnéis faoin tionscadal [C++](/programming/cpp/). Tá faisnéis ann a úsáideann córas tionscadail MBuild chun an t-aschur deiridh a thiomsú agus a thógáil. Tá VCXPROJ de thionscadail Visual C++ mar an gcéanna le {{ HYPERLINK2}} do thionscadail .NET. Níl aon chód i gcomhaid VCXPROJ ach tagraíonn siad do na ranganna, na spriocanna agus na hairíonna go léir a shainítear don tionscadal chun an tionscadal a thógáil. Is féidir iad seo a oscailt in eagarthóirí gnáth-théacs nó in Microsoft Visual Studio IDE más féidir.


## Formáid Chomhaid VCXPROJ - Tuilleadh Eolais

Is comhaid téacs iad comhaid VCXPROJ a chruthaítear i bhformáid comhaid [XML](/web/xml/). Is féidir iad seo a oscailt in aon eagarthóir téacs ach moltar go mór Microsoft Visual Studio IDE a úsáid chun na comhaid seo a oscailt agus a chur in eagar. Níor dearadh iad seo le haghaidh eagarthóireacht láimhe. Is féidir le botúin a chur faoi deara an IDE tuairteála nó é féin a iompar ar bhealaí gan choinne.

Seo a leanas a bhfuil i gcomhad samplach VCXPROJ.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Eilimintí Comhad VCXPROJ

Tá roinnt gnéithe i gcomhad tipiciúil VCXPROJ mar atá le feiceáil sa sampla XML thuas. Míníonn an [VCXPROJ structure](https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) le Microsoft gach eilimint comhaid go mion agus is féidir iad a tharchur ó thaobh an fhorbróra de.

#### Eilimint an Tionscadail

Seo é bunnóid an chomhaid VCXPROJ. Úsáideann MBuild an eilimint seo chun an leagan tógála agus an sprioc réamhshocraithe le haghaidh tiomsaithe a léamh.

#### Eilimint Grúpa Míreanna Cumraíochtaí Tionscadail

Tá an fhaisnéis cumraíochta tionscadail ann a fhéadfaidh an modh tógála (Dífhabhtú nó Scaoileadh), tiomsú 32 nó 64-giotán, roghanna leas iomlán a bhaint, agus eile a áireamh. Úsáideann IDE faisnéis sa ghrúpa seo chun an tionscadal a lódáil.

#### Eilimintí Cumraíochta an Tionscadail

Tá faisnéis sna heilimintí ProjectConfiguration i gcomhad VCXPROJ maidir leis an tógáil agus an t-ardán dá bhfuil an tionscadal lódáilte. Ba cheart go leanfadh a ainm an fhormáid `$(Cumraíocht)|$(Ardán)`.

#### Eilimint Globals PropertyGroup

Tá socruithe sa rannán seo a sholáthraíonn faisnéis do leibhéal an tionscadail mar:

 * ProjectGuid
 * RootNamespace
 * Cineál Iarratais nó ApplicationTypeRevision


## Tagairtí

* [Struchtúr VCXPROJ - MSDN]( https://learn.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)

* [C++ Comhaid Tionscadail]( https://learn.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)


