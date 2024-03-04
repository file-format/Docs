{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "Sužinokite apie SAV failo formatą ir API, kurios gali kurti ir atidaryti SAV failus.",
  "title" : "SAV – SPSS duomenų failas",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-lt",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## Kas yra SAV failas?
SAV failas yra socialinių mokslų statistinio paketo (SPSS) sukurtas duomenų failas, kurį statistinei analizei plačiai naudoja rinkos tyrinėtojai, sveikatos tyrėjai, tyrimų bendrovės, vyriausybė, švietimo tyrėjai, rinkodaros organizacijos, duomenų gavėjai. SAV, išsaugotas patentuotu dvejetainiu formatu ir susidedantis iš duomenų rinkinio bei žodyno, vaizduojančio duomenų rinkinį, išsaugo duomenis eilutėse ir stulpeliuose.

## SAV failo formatas
SAV failo formatas tapo gana stabilus, bet negalime sakyti, kad jis statiškas. Suderinamumas atgal ir pirmyn yra pasirinktinai prieinamas, kai reikia, bet netinkamai prižiūrimas. SAV failo duomenys suskirstyti į šias dalis:

### Failo antraštė
Jį sudaro 176 baitai. Pirmieji 4 baitai nurodo eilutę **$FL2** arba **$FL3** failo simbolių koduotėje. Paskutiniai trys baitai rodo, kad failo duomenys yra suglaudinti naudojant **ZLIB**. Kita 60 baitų eilutė prasideda **@(#) SPSS DATA FILE** ir taip pat nustato operacinę sistemą ir SPSS versiją, kuri sukūrė failą. Tada antraštė tęsiasi šešių skaitmenų laukais, kuriuose yra kintamųjų skaičius kiekvienam stebėjimui ir skaitmenų kodas suspaudimui, o baigiasi simbolių duomenimis, nurodant sukūrimo datą ir laiką bei failo etiketę.
### Kintamųjų deskriptorių įrašai
Įraše yra fiksuota laukų seka, klasifikuojanti kintamojo tipą ir pavadinimą kartu su SPSS naudojama formatavimo informacija. Kiekviename kintamojo įraše pasirinktinai gali būti iki 120 simbolių kintamojo etiketė ir iki trijų trūkstamų reikšmių specifikacijų.
### Vertės etiketės
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Pirmasis įrašas, kuris yra 3 žyma, turi laukų porų seką, kiekvienoje poroje yra reikšmė ir susijusi vertės etiketė. Antrasis įrašas, kuris yra 4 žyma, nurodo, kuriems kintamiesiems taikomas reikšmių / etikečių rinkinys.
### Dokumentai
Single or multiple records with integer tag 6. Neprivaloma dokumentacija. yra 80 simbolių eilučių.
### Pratęsimo įrašai
Single or multiple records with integer tag 7. Išplėtimo įrašuose pateikiama informacija, kurios galima saugiai nepaisyti, tačiau daugeliu atvejų išsaugota leidžia naujesne programine įranga įrašytiems failams išsaugoti atgalinį suderinamumą. Plėtinio įrašai turi sveikųjų skaičių potipio žymas.
### Žodyno terminatorius
Only record with integer tag 999. Jis atskiria žodyną nuo duomenų stebėjimų.
### Duomenų stebėjimai
Laikoma, kad duomenys yra stebėjimo tvarka, pvz., visos kintamųjų reikšmės pirmajam stebėjimui, po to visos antrojo stebėjimo reikšmės ir tt Duomenų įrašo formatas skiriasi priklausomai nuo suspaudimo kodo failo antraštės įraše. Sav failo duomenų dalis gali būti nesuspausta:
- **kodas 0**: suglaudintas baitų kodu
- **kodas 1**: suglaudintas naudojant ZLIB glaudinimą
 






## Nuorodos Nr.

* [SPSS sistemos duomenų failų formatų šeima (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


