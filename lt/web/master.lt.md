{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "PAGRINDINIS failas – ASP.NET pagrindinio puslapio failo formatas",
  "description" : "Sužinokite apie MASTER failo formatą ir API, kad sukurtumėte ir atidarytumėte MASTER failus.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master-lt",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## Kas yra MASTER failas?

MASTER failas yra pagrindinis tinklalapio šablono failas, sukurtas naudojant ASP.NET. Jis naudojamas kaip atspirties taškas kuriant kelis puslapius, kurių išdėstymas ir nustatymai yra tokie patys kaip MASTER failo. Šablono MASTER faile yra antraštės, naršymo meniu, poraštės, šrifto ir stiliaus informacijos nustatymai. MASTER failo naudojimas padeda greitai sukurti kelis tinklalapius.

MASTER failą galite atidaryti naudodami Microsoft Visual Studio 2022 ir naujesnę versiją.

## MASTER failo formatas – daugiau informacijos

MASTER failas sukuriamas ir išsaugomas HTML failo formatu ir yra panašus į bet kurį kitą tinklalapio failą. Jis suskirstytas į redaguojamus ir neredaguojamus skyrius. Redaguojami skyriai yra tie, kuriuos galima modifikuoti, kad atitiktų vartotojo poreikius. Neredaguojami skyriai yra pilki, kai MASTER failas atidaromas Microsoft Visual Studio.

Pagrindiniai puslapiai susideda iš dviejų dalių, ty paties pagrindinio puslapio ir vieno ar daugiau turinio puslapių.

### PAGRINDINIS puslapis

Pagrindinis puslapis turi .master plėtinį ir yra sukurtas ASP.NET. Jis turi iš anksto nustatytą išdėstymą, kurį sudaro statinis tekstas, HTML žymos ir serverio pusės valdikliai. Įprastuose .aspx puslapiuose naudojama @ Page direktyva. .master failų atveju tai pakeičiama @ Master direktyva.

### Turinio puslapiai

Turinio puslapis atspindi pagrindinio puslapio rezervuotos vietos valdiklių turinį. Tai yra .aspx puslapiai, kurie iš tikrųjų yra pagrindinio puslapio kodas. Turinio puslapiai surišami naudojant @ Page direktyvą įtraukiant MasterPageFile atributą, nurodantį pagrindinį puslapį, kuris turi būti naudojamas, kaip parodyta toliau.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Nuorodos

* [ASP.NET pagrindinių puslapių apžvalga](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))


