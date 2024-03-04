{
  "date": "2019-10-11",
  "keywords": [
"h",
".hh",
"kas yra .hh failas",
"kaip atidaryti .hh failą",
"pratęsimas",
"failą",
".hh failą",
".hh failo formatas",
".hh failo plėtinys",
".HH failo pavyzdys"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HH – C++ antraštės failo formatas",
  "description": "Sužinokite apie HH failo formatą ir API, kurios gali sukurti ir atidaryti HH failą.",
  "linktitle": "HH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-h-lth"
}
},
  "lastmod": "2021-06-20"
}

## Kas yra HH failas?

Failas su plėtiniu .hh yra C++ antraštės failas, apimantis kintamųjų, konstantų ir funkcijų deklaraciją. Šias deklaracijas naudoja atitinkami C++ diegimo failai, paprastai išsaugomi kaip [.cpp](/programming/cpp/) failai, kuriuose yra tikrasis vartotojo logikos įgyvendinimas. .hh antraštės failai pateikiami diegimo CPP failuose naudojant direktyvą #include. Galite pridėti kuo daugiau antraštės failų į savo C++ projektą, kad įtrauktumėte projekto lygio deklaracijas.

## .HH failo formatas

.hh failas yra paprasto teksto failas, sukurtas atsižvelgiant į antraštės failo apibrėžimo taisykles. Dažniausiai .hh faile pateikiama informacija yra tokia.

**`Kintamieji`** – Objektinio programavimo (OOP) atveju klasės antraštės faile yra visų klasės lygio kintamųjų, kurie pasiekiami diegimo šaltinio kodo failuose, apibrėžimai.
**`Metodų deklaracija`** – visos metodų deklaracijos įtrauktos į .h antraštės failus, kad būtų pasiekiami keliuose diegimo failuose.
**Neįdėtos funkcijos apibrėžimai** – antraštės failuose taip pat gali būti netiesioginių metodų apibrėžimų.
**`Pranešimų žemėlapiai`** – antraštės faile taip pat gali būti pranešimų žemėlapių, jei įdiegtas MFC šaltinio kodas. Tokiu atveju pranešimų žemėlapiai yra susieti su funkcijų įgyvendinimu, kuris yra susietas su vartotojo sąsajos elementais, tokiais kaip mygtukas, žymės langelis, radijo mygtukai ir kt.

## Skirtumas tarp .H ir .HH failų

Matyt, nėra tokio skirtumo tarp .h ir .hh antraščių failų, išskyrus rekomenduojamą jų naudojimo būdą atitinkamoms kalboms, ty [C](/programming/c/) arba C++. Antraštės failų pavadinimai pagal šias kalbas padeda juos atskirti dideliame projekte, kuris gali būti C ir C++ diegimų derinys.

Be to, jei antraštės yra atskirtos plėtiniu, redaktorius gali automatiškai pritaikyti atitinkamą formatavimą.

Apskritai šių dviejų failų formatų atskyrimas nepadarys jokios žalos, bet bus naudingas, todėl rekomenduojama vadovautis C ir C++ skyrimu.

### Antraštės apsaugai

Antraštės failai gali sukelti sudėtingų klaidų, kai į tą patį failą įtraukiamos kelios deklaracijos dėl kitų antraštės failų pridėjimo. Šie pasikartojantys apibrėžimai sukelia kompiliatoriaus klaidas. Šios probleminės situacijos galima išvengti naudojant mechanizmą, vadinamą antraštės apsauga, kurios yra sąlyginės kompiliavimo direktyvos, kaip parodyta toliau.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Naudodamas šią antraštę, pirminis procesorius patikrina, ar ANY_UNIQUE_NAME_HERE_HPP jau buvo apibrėžtas. Jei antraštė pakartotinai įtraukiama į tą patį failą, antraštės turinys bus ignoruojamas.

## Nuorodos

* [Antraštės failai – „Microsoft“](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

* [Skirtumas tarp .h ir .hh failų formatų](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)


