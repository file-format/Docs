{
  "date" : "2023-01-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Sužinokite apie GCF failo formatą ir API, kurios gali kurti ir atidaryti GCF failus.",
  "title" : "GCF failas – Nadeo Game GCF formatas",
  "linktitle" : "GCF",
  "menu" : {
    "docs" : {
      "identifier":"game-gcf-lt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-19"
}

## Kas yra GCF failas?

.gcf failas yra žaidimo talpyklos failas, kurį naudoja Steam žaidimų platforma. Jame yra žaidimo duomenų, tokių kaip tekstūros, modeliai ir kiti žaidime naudojami failai. Šie failai saugomi vartotojo kompiuteryje ir naudojami siekiant sumažinti duomenų, kuriuos reikia atsisiųsti atnaujinant ar diegiant žaidimą, kiekį. .gcf failai taip pat gali būti naudojami žaidimo diegimo atsarginėms kopijoms kurti arba žaidimui perkelti iš vieno kompiuterio į kitą.

GCF failus gali skaityti ir rašyti atvirojo kodo C++ programavimo biblioteka, **HLLib**.

## GCF failo formatas

GCF failai išsaugomi diske kaip dvejetainiai failai. Iš pradžių GCF buvo naudojamas kaip Grid Cache File santrumpa (ankstyvasis Steam kodinis pavadinimas buvo Grid, bet vėliau jis buvo paimtas kaip žaidimų talpyklos failas). GCF failas yra archyvo failas, kuriame saugomi Steam žaidimai. Visas oficialus turinys atsisiunčiamas kaip GCF failai. GCF failai taip pat gali būti bendrinami tarp žaidimų.

PASTABA: GCF yra [VPK file format](/game/vpk/) pirmtakas.
## Nuorodos

* [Valve Software](https://www.valvesoftware.com/en/)

* [GCF failo formatas](https://developer.valvesoftware.com/wiki/GCF)

* [HLLib – atvirojo kodo C++ programavimo biblioteka, skirta GCF failams skaityti](https://developer.valvesoftware.com/wiki/HLLib)


