{
  "date": "2021-08-16",
  "keywords": [
"nrg failą",
"nrg failo formatas",
"kas yra nrg failas",
"failą",
"nrg pavyzdys",
"nrg failo plėtinys",
"pratęsimas",
"formatu",
"nrg poraštė",
"nrg failo formatas",
"Nero Burning Rom",
"Nero AG"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie NRG failo formatą ir API, kurios gali kurti ir atidaryti NRG failus.",
  "title": "NRG – disko vaizdo failo formatas",
  "linktitle": "NRG",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-nr-ltg"
}
},
  "lastmod": "2021-08-16"
}

## Kas yra NRG failas?

Vaizdo failo formatas, sukurtas naudojant optinį diską, laikomas NRG failo formatu. Šį formatą Nero sukūrė specialiai Nero Burning Rom programai. Laikoma, kad šis formatas yra naudojamas disko vaizdams saugoti, nes jis tinkamas šiems konkretiems failams. Šie failai gali būti tikslios CD arba DVD kopijos pavidalu arba gali turėti keletą failų, kuriuos galima įdėti kaip diską. Kiti populiaresni failų formatai, pvz., [ISO](/compression/iso/), yra tie, į kuriuos šiuos failus galima konvertuoti į kai kurias pagrindines programas. Dažniausiai NRG failai naudojami kai kurių svarbių duomenų ar diskų atsarginėms arba kopijoms kurti.

## NRG failo formatas ##

Šį failo formatą sukūrė Nero AG kaip disko vaizdo formatą. Jis turėjo specifinę Nero Burning Rom naudingumo savybę, nes buvo sukurtas diskų vaizdams saugoti. Pirmoji jo versija buvo nurodyta saugoti reikšmes kaip 32 bitų sveikuosius skaičius. Tačiau buvo paleista antroji jo versija, kurioje buvo palaikomi 64 bitų sveikieji skaičiai.

## Techninė specifikacija Nr.

Failo pradžioje šis formatas nesaugo jo duomenų kaip antraštės. Kaip poraštė, ji pridedama failo pabaigoje. Vaizdo informacija išsaugoma IFF gabalėlių pavidalu. Pirmojo gabalo poslinkį galima gauti nuskaitant NRG poraštę nuo paskutinių 8 iki 12 failo baitų. Visose NRG failo formato versijose yra gabalai, DAOI, kompaktinio disko tekstas, seanso informacijos laikmenos tipas, disko informacija, Relo ir grandinės pabaiga. Baitų tvarka yra didelė, o visos sveikųjų skaičių reikšmės saugojimo metu yra nepažymėtos.

### Pagrindiniai gabalai ###

#### Lakštas ####

Šis informacinis lapas yra lengvai prieinamas visose NRG failų formato versijose. **CUEX** gabalas reiškia fiksuoto dydžio sujungimo blokus ir kiekvienas iš jų reiškia orientacinį tašką.

#### DAO informacija ####

Ši informacija taip pat yra visose NRG formato versijose. **DAOI** dalys saugo atitinkamą specifinę informaciją iš 2 dalių. Pirmąją jo dalį sudaro tik seansui būdingi duomenys. Antroji jo dalis tiesiog pakartoja pilką informaciją, susijusią su sekimu, ir tai yra tik vieną kartą kiekvienam takeliui.

#### CD tekstas ####

Tai galima rasti antrojoje NRG versijoje. **CDTX** dalis susideda iš neapdoroto CD teksto paketo sujungimo, kurio kiekvienam yra 18 baitų.

#### Išplėstinė takelio informacija ####

Tai galima visose NRG failo formato versijose. Šie gabalai naudojami sekimo informacijai saugoti vienu metu vykstančių seansų takeliui. Šie duomenys kiekvieno takelio atveju kartojami tik vieną kartą.

#### Sesijos informacija ####

Tai taip pat galima visose NRG failo formato versijose. Informacija apie seanso dalis turi būti naudojama norint greitai nuskaityti seanso vaizdą ir tada sekti skaičių.

#### Grandinės pabaiga ####

Pabaigos dalis reiškia signalus, kad dabar nebėra dalių, kurias reikia skaityti, ir tai taip pat yra visose NRG versijose.


## Nuorodos Nr.

* [NRG – pateikė Vikipedija](https://en.wikipedia.org/wiki/NRG_(file_format))



