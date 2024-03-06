{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"failu",
"pagarinājumu",
"faila formātā",
"VB projekta fails",
"Programmēšanas rokasgrāmata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "Uzziniet par VBPROJ faila formātu un API, kas var izveidot un atvērt VBPROJ failus.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-lvj"
}
},
  "lastmod": "2020-09-10"
}

## Kas ir VBPROJ fails?

Fails ar paplašinājumu .vbproj ir Microsoft Visual Basic projekta fails, ko Microsoft MSBuild programma izmanto, lai izveidotu projektus Visual Studio risinājumā. Tas ir līdzīgs [CSPROJ](/programming/csproj/) failam .NET projektiem, kas rakstīti [C#](/programming/cs/). MSBuild dzinējs nolasa informāciju, kas atrodas dažādās grupās no VBPROJ failiem, un ģenerē izvades failu. VBPROJ fails var saturēt informāciju, kas saistīta ar globālajiem identifikatoriem, klasēm un rekvizītiem, kas nosaka projektu. VBPROJ failus var atvērt un rediģēt, izmantojot Microsoft Visual Studio un jebkuru izplatītu teksta redaktoru, piemēram, Notepad operētājsistēmās Windows un MacOS operētājsistēmās.

## VBPROJ faila formāts — vairāk informācijas

VBPROJ faili ir teksta faili, kas ir rakstīti [XML](/web/xml/) faila formātā, pamatojoties uz [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). VBPROJ fails satur informāciju XML tagu veidā, kas definē informāciju, kas saistīta ar konkrēto iestatījumu grupu. Ir ļoti ieteicams atvērt un rediģēt šos iestatījumu failus programmā Microsoft Visual Studio IDE.

### VBPROJ elementi

VB iestatījumu faila elementi ir tādi, kā parādīts nākamajā attēlā.

{{< figure src="../vbproj.png" alt="VBPROJ faila formāts" >}}

The following table gives a brief description of these elements.

|Elements|Apraksts|
---|---|
|Projekts| Katra projekta faila saknes elements un var ietvert atribūtus, lai norādītu veidošanas procesa ievades punktus papildus XML shēmas identificēšanai projekta failam|
|Īpašumi un nosacījumi| Rekvizīti sastāv no atslēgas vērtību pāriem un tiek definēti PropertyGroup elementā. Rekvizīta elementa nosaukums apzīmē rekvizītu atslēgu, un elementa saturs nosaka rekvizīta vērtību.|
|Items and ItemGroups|Projekta failā esošie vienumi ir veidošanas procesa ievade, piemēram, failu koda faili, konfigurācijas faili, komandu faili un citi, kas nepieciešami veidošanas procesā. Vienumi ir un tiem ir jābūt definētiem elementā ItemGroup.|
|Mērķi un uzdevumi| Uzdevuma elements ir individuāla veidošanas instrukcija (vai uzdevums). MSBuild ietver daudzus iepriekš definētus uzdevumus, piemēram, Copy, CSC, VBC, Exec. Uzdevumiem vienmēr ir jābūt ietvertiem elementā Mērķis, kas ir viena vai vairāku secīgi izpildītu uzdevumu kopa, un projekta failā var būt vairāki mērķi.|

## Atsauces

* [Izpratne par projekta failu](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild shēmas elementi](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


