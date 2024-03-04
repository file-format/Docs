{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OFT – „Microsoft Outlook“ el. pašto šablono failas",
  "description": "Sužinokite apie OFT failo formatą ir API, kurios gali kurti ir atidaryti OFT failus.",
  "linktitle": "OFT",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-of-ltt"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra OFT failas?

Failai su plėtiniu .oft yra šabloniniai failai, sukurti naudojant Microsoft Outlook. Iš anksto suformatuotas pranešimų šablonų išdėstymas naudojamas siunčiant el. laiškus su įprasta informacija, siekiant sutaupyti laiko. Tokius failus galima sugeneruoti sukuriant naują el. laišką, pridedant reikiamą informaciją ir naudojant Microsoft Outlook išskleidžiamąjį meniu Išsaugoti kaip Office Template (.oft). Vartotojai gali atidaryti OFT failus dukart spustelėdami juos ir jis bus atidarytas atitinkamoje konkrečioje sistemoje.

## OFT failo struktūra ##

.OFT failo formatas pagrinde naudoja [MSG](/email/msg/) failo formatą. Vienintelis skirtumas yra tas, kad Oft failai turi CLSID_TEMPLATEMESSAGE ({0006F046-0000-0000-C000-000000000046}) kaip saugyklos klasė (WriteclassStg), o MSG failai naudoja clsid_maillMessage ({00020b-000000-0000-C000-000000000000000046}).

CFB_3 formatas yra MSG failo pagrindas. Paradigma pagrįsta saugyklų ir srautų koncepcijomis, gana artimomis katalogams ir failams. Todėl pagrindinis skirtumas tarp pirmųjų yra visa hierarchija, supakuota į atskirą failą, vadinamą sudėtiniu failu. Objektai sudaro pranešimų failus ir susideda iš vienos nuosavybės arba jos rinkinių. Ši galimybė palengvina programoms sudėtingus, struktūrizuotus duomenis saugoti viename faile. Šis formatas taip pat nurodo kelias saugyklas, kiekviena saugykla žymi pranešimo objektą kaip pagrindinį komponentą. Šiose saugyklose yra daug srautų, atspindinčių to komponento savybę. Taip pat galima įdėti saugyklą.

### OFT ypatybės

Viršutiniame .msg failo lygyje saugyklose yra srautai, kuriuose saugomos ypatybės. Savybės gali būti suskirstytos į šias kategorijas:

* Fiksuoto ilgio savybės

* Kintamo ilgio savybės

* Daugiavertės savybės


Nepriklausomai nuo kategorijos, nuosavybė yra pažymėta arba pavadinta. Tačiau įvardintoms ypatybėms reikalinga tinkama atvaizdavimo informacija, kaip nurodyta jų atvaizdavimo saugykloje.

### OFT saugyklos

Saugyklos yra pagrindiniai pranešimo objekto komponentai. MSG failo formatas nurodo šias saugyklas:

### Aukščiausio lygio struktūra

Pranešimo objektas reiškia visą aukščiausią Msg failo formato lygį. Priklausomai nuo tipo, savybių, gavėjų ir priedo objektų skaičiaus, pranešimo objektas gali turėti skirtingas srauto saugyklas atitinkamame .MSG faile.

#### Ryšys su kitomis struktūromis

MSG/OFT failo formatas turi šiuos ryšius su kitomis struktūromis:

* .msg pagrindas yra sudėtinio failo dvejetainio failo formatas.

* Šiame formate naudojamos ypatybės, kurias naudoja pranešimų ir priedų objektų protokolas.


## Nuorodos

* [[MS-OXMSG]: Outlook MSG failo formatas](https://msdn.microsoft.com/en-us/library/cc463912(v#exchg.80).aspx)


