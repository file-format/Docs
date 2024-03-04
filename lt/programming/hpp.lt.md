{
  "date": "2023-06-08",
  "keywords": [
"hpp failą",
"kas yra hpp failas",
"kas yra hpp faile",
"hpp failo pavyzdys",
"koks yra hpp failo formatas",
"failą",
"hpp failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "HPP failo formatas – C++ antraštės failas",
  "description": "Sužinokite apie HPP formatą ir API, kurios gali kurti ir atidaryti HPP failus.",
  "linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp-lt",
      "parent": "programming"
}
},
  "lastmod": "2023-06-08"
}

## Kas yra HPP failas?

.hpp failo formatas dažniausiai naudojamas antraštės failams C++ programavimo kalba. Antraštės failuose paprastai yra funkcijų, klasių, kintamųjų ir konstantų, naudojamų kituose šaltinio kodo failuose C++ projekte, deklaracijos ir apibrėžimai.

Antraštės failų naudojimo tikslas yra suteikti galimybę bendrinti bendrą kodą keliuose šaltinio kodo failuose nedubliuojant paties kodo. Kai C++ šaltinio failas turi pasiekti deklaracijas arba apibrėžimus iš antraštės failo, jis apima antraštės failą naudodamas išankstinio procesoriaus direktyvą #include.

Failo plėtinys .hpp dažnai naudojamas norint nurodyti, kad failas yra C++ antraštės failas. Nebūtina naudoti šio konkretaus plėtinio antraštės failams, taip pat galite susidurti su antraštės failais su .h ar kitais plėtiniais. Pratęsimo pasirinkimas daugiausia priklauso nuo susitarimo ir asmeninių pageidavimų.

Kai C++ šaltinio faile yra antraštės failas naudojant #include, kompiliatorius veiksmingai sujungia antraštės failo turinį su šaltinio failu, prieš sukompiliuodamas jį kaip vienetą. Tai leidžia šaltinio failui pasiekti deklaracijas ir apibrėžimus antraštės faile, suteikdama reikalingą informaciją, kad kompiliatorius galėtų atlikti tipo tikrinimą ir kodo generavimą.

## Kas yra HPP faile?

Štai keletas įprastų turinio, kurį galite rasti .hpp faile:

- **Funkcijų deklaracijos:** antraštės failuose dažnai pateikiamos funkcijų deklaracijos be faktinio jų įgyvendinimo. Šiose deklaracijose pateikiama informacija apie funkcijos pavadinimą, grąžinimo tipą ir parametrus, leidžiančius kitiems šaltinio kodo failams naudoti funkciją, nežinant įgyvendinimo detalių.
- **Klasių deklaracijos:** Antraštės failuose gali būti klasių deklaracijų, įskaitant klasės pavadinimą, narių kintamuosius, narių funkcijas ir prieigos specifikacijas. Įtraukus klasės deklaraciją į antraštės failą, kiti šaltinio kodo failai gali sukurti tos klasės objektus ir pasiekti jos narius.
- **Pastovios deklaracijos:** antraštės failai gali apibrėžti konstantas, pvz., visuotinius kintamuosius arba enum reikšmes, kurios turi būti bendrinamos keliuose šaltinio kodo failuose. Šias konstantas galima pasiekti įtraukus antraštės failą į kitus šaltinio failus, leidžiančius jiems naudoti apibrėžtas konstantas.
– **Tipo apibrėžimai:** antraštės failuose gali būti tipo apibrėžimų naudojant typedef raktinį žodį arba tipo slapyvardžių naudojant using raktinį žodį. Šie apibrėžimai sukuria naujus esamų tipų pavadinimus, todėl kodas tampa lengviau skaitomas ir prižiūrimas.
– **Įterptieji funkcijų apibrėžimai:** kai kuriais atvejais antraštės failuose gali būti įterptinių funkcijų apibrėžimų. Įterptosios funkcijos yra mažos funkcijos, kurios išplečiamos skambučio vietoje, o ne iškviečiamos kaip atskira funkcija. Įtraukus tiesioginį funkcijos apibrėžimą į antraštės failą, kompiliatorius gali pakeisti funkcijos iškvietimą tiesiogiai funkcijos korpusu, o tai gali pagerinti našumą.

## HPP failo pavyzdys

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Koks yra HPP failo formatas?

HPP yra paprasto teksto failas, tačiau jis atitinka bendrąsias C++ programavimo kalbos taisykles ir sintaksę. Toliau pateikiamas bendrojo formato ir .hpp failo struktūros suskirstymas:

– **Antraštės apsauga:** Paprastai .hpp failas prasideda antraštės apsaugomis, kad būtų išvengta kelių to paties failo įtraukimų. Tai pasiekiama naudojant išankstinio procesoriaus direktyvas, tokias kaip #ifndef, #define ir #endif. Antraštės apsauga užtikrina, kad failo turinys įtraukiamas tik vieną kartą kompiliavimo proceso metu.
– **Įtraukti teiginius:** po antraštės apsaugos galite įtraukti kitus reikalingus antraščių failus naudodami direktyvą #include. Tai gali apimti standartines bibliotekos antraštes arba kitas pasirinktines antraštes, kurių reikalauja jūsų kodas.
- ** Deklaracijos ir apibrėžimai:** Pagrindinis .hpp failo turinys yra deklaracijos ir, kai kuriais atvejais, klasių, funkcijų, konstantų, tipų slapyvardžių ir kitų elementų apibrėžimai. Pavyzdžiui, galite deklaruoti klases naudodami raktinį žodį class, funkcijas naudodami grąžinimo tipą, pavadinimą ir parametrų sąrašą, o konstantas – naudodami raktinį žodį const, po kurio nurodomas jų tipas ir pavadinimas.
- **Įterptosios funkcijų apibrėžimai:** tam tikrais atvejais galite įtraukti įterptųjų funkcijų apibrėžimus tiesiai į .hpp failą. Eilutinės funkcijos paprastai apibrėžiamos klasės turinyje, o tai reiškia, kad funkcijos apibrėžimas įtraukiamas kartu su jos deklaracija. Tai galima padaryti prieš funkcijos apibrėžimą įtraukus raktinį žodį inline.
– **Vardų erdvės deklaracijos:** jei kode naudojate vardų sritis, galite jas deklaruoti .hpp faile. Tai atliekama naudojant vardų erdvės raktinį žodį, po kurio nurodomas vardų erdvės pavadinimas ir atitinkamas kodas įtraukiamas į vardų erdvės bloką.

## Nuorodos
* [Antraštės failai (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)


