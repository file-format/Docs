{
  "date": "2021-01-21",
  "keywords": [
"otp failą",
"otp failo formatas",
"kas yra otp failas",
"failą",
"otp pavyzdys",
"otp failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OTP – „OpenDocument“ pristatymo šablonas",
  "description": "Sužinokite apie OTP failo formatą ir API, kurios gali kurti ir atidaryti OTP failus.",
  "linktitle": "OTP",
  "menu": {
    "docs": {
      "parent": "presentation",
      "identifier": "presentation-ot-ltp"
}
},
  "lastmod": "2021-01-21"
}

## Kas yra OTP failas?

Failai su plėtiniu .otp yra pristatymo šablonų failai, sukurti programų OASIS OpenDocument standartiniu formatu. Tokio failo turinys apima pristatymo informaciją skaidres su tekstu, vaizdais, figūromis, daugialypės terpės turiniu, perėjimo efektais ir kitais skaidrių elementais. Šie šablonų failai naudojami greitam naujų pristatymų kūrimui, remiantis pačiame šablone saugoma stiliaus informacija. OTP failus galima sukurti ir išsaugoti naudojant kelias skirtingas programas, tokias kaip Impress, kuri pateikiama kartu su OpenOffice paketu ir Microsoft PowerPoint. OTP failo formatas panašus į Microsoft PowerPoint šablonų failus [.pot](/presentation/pot/) ir [.potx](/presentation/potx/).

## OTP failo formatas

OTP failo formatas yra pagrįstas OpenDocument standartu, kuris palaiko dokumento vaizdavimą kaip vieną XML dokumentą, taip pat kelių antrinių dokumentų rinkinį viename supakuotame pakete [ZIP](/compression/zip/) formatu. Failo turinys platinamas keliais xml failais, supakuotais kartu. Šiuose keliuose [XML](/web/xml/) failuose yra informacijos apie dokumento stilių, turinį, metainformaciją ir nustatymus, kaip nurodyta toliau.

* `content.xml` – dokumento turinys ir turinyje naudojami automatiniai stiliai.

* `styles.xml` – dokumento turinyje naudojami stiliai ir pačiuose stiliuose naudojami automatiniai stiliai.

* `meta.xml` – dokumento metainformacija, pvz., autorius arba paskutinio išsaugojimo veiksmo laikas.

* `settings.xml` – konkrečios programos nustatymai, pvz., lango dydis arba spausdintuvo informacija.


## Nuorodos

* [OpenDocument – Vikipedija](https://en.wikipedia.org/wiki/OpenDocument)


