{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"failą",
"pratęsimas",
"Dokumento formatas",
"Microsoft Excel makrokomandos failas",
"Skaičiuoklė"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Jūsų failo formato vadovas, kad sužinotumėte, kas yra XLM makrokomandų failas ir API, kurios gali kurti ir atidaryti XLM failus.",
  "title": "Kas yra XLM failas?",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-ltm"
}
},
  "lastmod": "2019-12-10"
}

## Kas yra XLM failas?

XLM, skirta Excel makrokomandai, yra skaičiuoklės failų tipas, naudojamas makrokomandoms saugoti. Taikymo požiūriu makrokomanda yra instrukcijų rinkinys, naudojamas procesams automatizuoti. Makrokomandos naudojama įrašyti veiksmus, kurie pakartotinai atliekami naudojant [XLS](/spreadsheet/xls/) failo formatą, ir palengvina veiksmų atlikimą dar kartą paleidžiant makrokomandą. Makrokomandos programuojamos naudojant Microsoft Visual Basic for Applications (VBA) iš Excel darbaknygės, naudojant Visual Basic rengyklę, ir jas galima paleisti / derinti tiesiai iš ten.

## Trumpa istorija ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 pagal numatytuosius nustatymus įrašė makrokomandas VBA, tačiau naudojant 5.0 versiją XLM įrašymas vis tiek buvo leidžiamas kaip parinktis. Po 5.0 versijos ši parinktis buvo nutraukta. Visose Excel versijose, įskaitant Excel 2010, galima paleisti XLM makrokomandą, tačiau Microsoft nerekomenduoja jų naudoti.

## Makrokomandos įrašymas XLM formatu ##

Excel pateikia paprastus makrokomandos įrašymo veiksmus. Kad galėtumėte dirbti su makrokomandomis, turite įdiegti kūrėjo įrankius. Kai makrokomandos įrašymas yra vykdomas, jis įrašo kiekvieną vartotojo veiksmą, kuris bus paleistas vėliau. Makrokomandos įrašymas iš tikrųjų apima visus veiksmus, kuriuos vartotojas atlieka po įrašymo pradžios. Taigi, jei paryškinsite langelio turinį, paryškinsite kursyvą ir nustatysite jo teksto pagrindimą po to, kai pradėsite makrokomandos įrašymą, visos šios komandos bus įrašytos. Kiekvienai įrašytai makrokomandai taip pat galima priskirti nuorodą, kad vėliau būtų galima greitai atkurti. Makrokomandos įrašymas generuoja VBA kodą makrokomandos pavidalu, kurį galima redaguoti naudojant Visual Basic Editor (VBE).

## „Excel“ objekto modelis Nr.

Makrokomandoms naudojamos VBA rutinos ir šiuo tikslu vadovaukitės [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model). Šis modelis identifikuoja skaičiuoklės objektus, skirtus sąveikai su skaičiuokle per vartotojo nustatytas komandų įrankių juostas, komandų juostas arba pranešimų laukelius. Pavyzdžiui, prieiga prie darbaknygės ypatybių suteikiama naudojant darbaknygės objektą. Taip pat modelyje yra darbalapio objektas, skirtas dirbti su darbaknygės darbalapiais programiškai.

## Makrokomandos ir sauga ##

VBA suteikia prieigą prie visų taikymo sričių, taip pat failų sistemos ir gali būti pavojinga. Tai kelia susirūpinimą bendrinant darbaknygę su žmogumi, kuris gali paleisti failą jam pačiam. Tai yra Microsoft Excel įspėja apie tokio failo atidarymą. Makrokomandos gali būti sertifikuotos skaitmeniniu parašu, kad kiti vartotojai galėtų patikrinti, ar jos yra patikimos. Taigi makrokomandas galima įjungti patikrinus jų šaltinį.

## Nuorodos Nr.

* [[MS-XLS] – „Excel“ dvejetainio failo formato struktūra](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [Makrokomandų programavimas](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)


