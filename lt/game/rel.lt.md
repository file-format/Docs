{
  "date": "2021-09-08",
  "keywords": [
"rel failą",
"rel failo formatas",
"kas yra rel failas",
"failą",
"rel pavyzdys",
"rel failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie REL failo formatą ir API, kurios gali kurti ir atidaryti REL failus.",
  "title": "REL – perkeliamo modulio failas",
  "linktitle": "REL",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-re-ltl"
}
},
  "lastmod": "2021-09-08"
}

## Kas yra REL failas?
Failas su plėtiniu .rel gali būti naudojamas įvairiems tikslams. Todėl, kalbant apie žaidimų klasifikaciją, jis žinomas kaip perkeliamas modulio failas, naudojamas kai kuriuose Nintendo Wii žaidimuose, tokiuose kaip Brawl, Super Smash Bros ir Mario Kart Wii. Jį sudaro žaidimo duomenys, įskaitant simbolių modelius ir etapus. REL failai veikia panašiai kaip .DLL failai, naudojami Microsoft Windows.

## REL failo formatas
REL failo formatu failas yra padalintas į kelias dalis, sugrupuotas pagal panašią prieigą, pvz., skaitomi tik duomenys viename skyriuje, visas vykdomasis kodas dedamas į kitą ir tt Failas prasideda antraštės skyriumi, po kurio seka:
- Lentelė su skyriaus informacija.
- Skyriaus duomenys.
- Informacija apie persikraustymą.

### Failo antraštė
Failas prasideda iki 0x4C baitų antrašte:
| Offset | Dydis | Lauko pavadinimas | Aprašymas |
--------------------|---------------|-------------------|---------------------------------|
| 0x00 | 4 | id | Arbitrary identification number. Must be unique amongst all RELs used by a game. Must not be 0. |
| 0x04 | 4 | kitas | Rodyklė į kitą modulį, užpildytą vykdymo metu. |
| 0x08 | 4 | ankstesnis | Rodyklė į ankstesnį modulį, užpildytą vykdymo metu. |
| 0x0c | 4 | numSections | Skilčių skaičius faile. |
| 0x10 | 4 | skyriusInformacijos poslinkis | Poslinkis į skyrių lentelės pradžią. |
| 0x14 | 4 | nameOffset | Poslinkis į ASCII eilutę, kurioje yra modulio pavadinimas. Gali būti NULL. Santykinis su REL failo pradžia. |
| 0x18 | 4 | pavadinimasDydis | Modulio pavadinimo dydis baitais. |
| 0x1c | 4 | versija | REL failo formato versijos numeris. |
| 0x20 | 4 | bssSize | Skilties .bss dydis. |
| 0x24 | 4 | relOffset | Perskirstymas į perkėlimo lentelę. |
| 0x28 | 4 | impOffsetas | Poslinkis į imp lentelę. |
| 0x2c | 4 | impSize | imp lentelės dydis baitais. |
| 0x30 | 1 | prologSection | Index into section table which prolog is relative to. Skip if this field is 0. |
| 0x31 | 1 | epilogSection | Index into section table which epilog is relative to. Skip if this field is 0. |
| 0x32 | 1 | unresolvedSection | Index into section table which unresolved is relative to. Skip if this field is 0. |
| 0x33 | 1 | bssSection | Indeksas į skyrių lentelę, su kuria bss yra santykinis. Užpildyta vykdymo metu! |
| 0x34 | 4 | prologas | Poslinkis į nurodytą funkcijos _prolog skyrių. |
| 0x38 | 4 | epilogas | Poslinkis į nurodytą funkcijos _epilog skyrių. |
| 0x3c | 4 | neišspręstas | Poslinkis į nurodytą funkcijos _unresolved skyrių. |
| 0x40 | 4 | align | Version ≥ 2 only. Alignment constraint on all sections, expressed as power of 2. |
| 0x44 | 4 | bssAlign | Version ≥ 2 only. Alignment constraint on all '.bss' section, expressed as power of 2. |
| 0x48 | 4 | fixSize | Tik versija ≥ 3. Jei REL yra susietas su OSLinkFixed (vietoj OSLink), tarpas po šio adreso gali būti naudojamas kitiems tikslams (pvz., BSS). |

### Skyriaus informacijos lentelė
Skilties informacijos lentelėje yra **numSections** įrašų, kurių kiekvienas yra 0x8 baitų ilgio:
| Offset | Dydis | Aprašymas |
-------|------------|-------------|
| 0x0 | 30 bitų | Poslinkis nuo REL pradžios iki atkarpos. Jei šis skaičius lygus nuliui, sekcija yra neinicializuota sekcija (ty .bss). |
| 0x3,6 | 1 bitas | Nežinoma. |
| 0x3,7 | 1 bitas | Vykdomoji vėliava; jei tai yra 1, skyrius yra vykdomas. |
| 0x4 | 4 | Skilties ilgis baitais. Jei tai yra nulis, šis įrašas praleidžiamas. |
| 0x8 | Kitas įrašas | Kitas įrašas |

### Perkėlimo duomenys
Perkėlimo duomenys yra vienas ar keli 0x8 baitų struktūrų sąrašai. Kiekvieno sąrašo pabaiga pažymėta specialiu tipo kodu 203:
| Offset | Vardas | Dydis | Aprašymas |
-------|------------|------------|-----|
| 0x0 | kompensuoti | 2 | Poslinkis baitais nuo ankstesnio perkėlimo į šį. Jei tai pirmasis perkėlimas skyriuje, tai susiję su sekcijos pradžia. |
| 0x2 | tipas | 1 | Perkėlimo tipas. Aprašyta žemiau. |
| 0x3 | skyrius | 1 | Simbolio skyrius, prieš kurį reikia perkelti. Naudojant specialų perkėlimo tipą 202, tai yra šio failo skyriaus, kuriam taikomi šie perkėlimo įrašai, numeris. |
| 0x4 | pridėti | 4 | Simbolio poslinkis baitais, prieš kurį reikia perkelti, palyginti su jo sekcijos pradžia. Vietoj to, tai yra absoliutus adresas perkėlimams iš main.dol. |
| 0x8 | Kitas įrašas | Kitas įrašas | Kitas įrašas |


 



## Nuorodos 

* [Relocatable Object Module Format](https://en.wikipedia.org/wiki/Relocatable_Object_Module_Format)



