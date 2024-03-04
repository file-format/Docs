{
  "date": "2019-10-11",
  "keywords": [
"vb",
"failą",
"pratęsimas",
"Dokumento formatas",
"Visual Basic",
"Programavimo vadovas"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VB – Visual Basic kodo failas",
  "description": "Sužinokite apie VB failo formatą ir API, kurios gali kurti ir atidaryti VB failus.",
  "linktitle": "VB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-v-ltb"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra VB failas?

VB failas yra Visual Basic kalba sukurtas šaltinio kodo failas, kurį Microsoft sukūrė .NET programoms kurti. Kita panaši kalba su skirtinga sintaksė yra C#, kurios failai išsaugomi su [.CS](/programming/cs/) failo plėtiniu. Failo formatas suteikia žemo lygio programavimo kalbą, skirtą rašyti kodą, kuris yra sudarytas, kad būtų sukurtas galutinis išvesties failas EXE arba DLL pavidalu. Juos galima sukurti ir sukompiliuoti naudojant Microsoft Visual Studio. Microsoft Visual Studio Express taip pat gali būti naudojamas kurti ir atnaujinti tokius failus, kurie yra nemokama IDE. Paprastas Visual Studio projektas [solution](/programming/sln/), sukurtas VB kalba, gali apimti vieną ar daugiau tokių failų. Failai, pažymėti įtraukti į kompiliaciją, yra išvardyti faile [CSPROJ](/programming/csproj/), kuris yra projekto dalis ir nurodo kompiliatoriui naudoti pažymėtus failus.

## VB failo formatas – daugiau informacijos

VB failai yra tekstiniai failų formatai, kuriuos galima atidaryti bet kuriame teksto rengyklėje redaguoti. Tačiau atidarius palaikomoje IDE su tinkamu sintaksės paryškinimu, kodą lengva skaityti ir tvarkyti. Paprastame VB faile yra:

* Vardų erdvių deklaracija – skirta nuorodai į tam tikrą funkciją, apibrėžtą toje konkrečioje vardų erdvėje

* Kintamųjų deklaracija – deklaruoti klasės lygio kintamuosius konkrečiam įgyvendinimui

* Metodų deklaracija – deklaruoti tam tikros funkcijos metodų deklaraciją


## VB failo formato pavyzdys

```
Imports System
Module Module1
   'This program will display Hello World
   Sub Main()
      Console.WriteLine("Hello World")
      Console.ReadKey()
   End Sub
End Module
```



