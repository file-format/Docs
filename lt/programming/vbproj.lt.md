{
  "date": "2019-10-11",
  "keywords": [
"vbproj",
"failą",
"pratęsimas",
"Dokumento formatas",
"VB projekto failas",
"Programavimo vadovas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VBPROJ",
  "description": "Sužinokite apie VBPROJ failo formatą ir API, kurios gali kurti ir atidaryti VBPROJ failus.",
  "linktitle": "VBPROJ",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-vbpro-ltj"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra VBPROJ failas?

Failas su plėtiniu .vbproj yra Microsoft Visual Basic projekto failas, kurį naudoja Microsoft MSBuild variklis projektams kurti Visual Studio sprendime. Jis panašus į [CSPROJ](/programming/csproj/) failą, skirtą .NET projektams, parašytiems [C#](/programming/cs/). MSBuild variklis nuskaito informaciją, esančią įvairiose grupėse iš VBPROJ failų, ir generuoja išvesties failą. VBPROJ faile gali būti informacijos, susijusios su visuotiniais identifikatoriais, klasėmis ir ypatybėmis, kurios apibrėžia projektą. VBPROJ failus galima atidaryti ir redaguoti naudojant Microsoft Visual Studio ir bet kurį įprastą teksto rengyklę, pvz., Notepad Windows ir MacOS operacinėse sistemose.

## VBPROJ failo formatas – daugiau informacijos

VBPROJ failai yra tekstiniai failai, parašyti [XML](/web/xml/) failo formatu, remiantis [MSBuild XML Schema](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019). VBPROJ faile yra informacijos XML žymų forma, kurios apibrėžia informaciją, susijusią su ta konkrečia nustatymų grupe. Labai rekomenduojama atidaryti ir redaguoti šiuos nustatymų failus Microsoft Visual Studio IDE.

### VBPROJ elementai

VB nustatymų failo sudedamosios dalys yra tokios, kaip parodyta kitame paveikslėlyje.

{{< figure src="../vbproj.png" alt="VBPROJ failo formatas" >}}

The following table gives a brief description of these elements.

|Elementas|Aprašymas|
---|---|
|Projektas| Kiekvieno projekto failo šakninis elementas ir gali apimti atributus, nurodančius kūrimo proceso įvesties taškus, be projekto failo XML schemos|
|Savybės ir sąlygos| Savybės susideda iš rakto-reikšmių porų ir yra apibrėžtos PropertyGroup elemente. Ypatybės elemento pavadinimas reiškia nuosavybės raktą, o elemento turinys apibrėžia nuosavybės vertę.|
|Elementai ir elementų grupės|Projekto failo elementai yra kūrimo proceso įvestis, pvz., failų kodo failai, konfigūracijos failai, komandų failai ir kiti reikalingi kaip kūrimo proceso dalis. Elementai yra ir turi būti apibrėžti elemente ItemGroup.|
|Tikslai ir užduotys| Užduoties elementas reiškia individualią kūrimo instrukciją (arba užduotį). MSBuild apima daugybę iš anksto nustatytų užduočių, tokių kaip Copy, CSC, VBC, Exec. Užduotys visada turi būti įtrauktos į elementą Target, kuris yra vienos ar daugiau užduočių, kurios vykdomos nuosekliai, rinkinys, o projekto faile gali būti keli tikslai.|

## Nuorodos

* [Projekto failo supratimas](https://learn.microsoft.com/en-us/aspnet/web-forms/overview/deployment/web-deployment-in-the-enterprise/understanding-the-project-file)

* [MSBuild Schema Elements](https://learn.microsoft.com/en-us/visualstudio/msbuild/msbuild-project-file-schema-reference?view=vs-2019)


