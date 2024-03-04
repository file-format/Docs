{
  "date": "2022-06-29",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WHL failo formatas – Python Wheel paketo failas",
  "description": "Sužinokite apie WHL failo formatą ir API, kurios gali kurti ir atidaryti WHL failus.",
  "linktitle": "WHL",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-wh-ltl"
}
},
  "lastmod": "2022-06-29"
}

## Kas yra WHL failas?

WHL (rato) failas yra platinimo paketo failas, išsaugotas Python rato formatu. Tai standartinio formato Python platinimų diegimas, kuriame yra visi diegimui reikalingi failai ir metaduomenys. WHL faile taip pat yra informacijos apie Python versijas ir platformas, kurias palaiko šis rato failas. Panašiai kaip [MSI](/executable/msi/) sąrankos failas, WHL failo formatas yra paruoštas diegti formatas, leidžiantis paleisti diegimo paketą nekuriant šaltinio paskirstymo.

## WHL failo formatas

WHL failo formatas yra [ZIP](/compression/zip/) (.zip) archyvas, kuriame yra visi diegimo failai ir metaduomenys, kurių reikia diegėjams norint įdiegti paketą. Šiuos WHL failus galima išskleisti naudojant išpakavimo parinktį arba standartines išskleidimo programinės įrangos programas, tokias kaip WinZIP ir WinRAR.

### WHL failų pavadinimų konvencija

WHL failas pavadintas pagal toliau pateiktą susitarimą.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

WHL failo pavadinimo pavyzdys yra toks.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

 * kriptografija yra paketo pavadinimas.
 * 2.9.2 yra kriptografijos paketo versija. Versija yra su PEP 440 suderinama eilutė, pvz., 2.9.2, 3.4 arba 3.9.0.a3.
 * cp35 yra Python žyma ir žymi Python diegimą ir versiją, kurios reikalauja ratukas.
 * abi3 yra ABI žyma. ABI reiškia dvejetainę programos sąsają.
 * macosx_10_9_x86_64 yra platformos žyma, kuri yra gana gausi.

## Nuorodos

* [Kas yra Python Wheels ir kodėl jums tai turėtų rūpėti?](https://realpython.com/python-wheels/)

* [Python Wheel](https://pypi.org/project/wheel/)


