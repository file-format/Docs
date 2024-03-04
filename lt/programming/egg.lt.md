{
  "date": "2022-03-15",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EGG failo formatas – Python platinimo failas",
  "description": "Sužinokite apie EGG failo formatą ir API, kurios gali kurti ir atidaryti EGG failus.",
  "linktitle": "EGG",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-eg-ltg"
}
},
  "lastmod": "2022-03-15"
}

## Kas yra EGG failas?

EGG failas, taip pat žinomas kaip Python eggs, yra senesnis Python platinimo formatas. Tai [ZIP](/compression/zip/) suglaudintas archyvas su plėtiniu .egg, kuriame yra Python programos šaltinio failai kartu su platinimo metainformacija. EGG failai yra alternatyva Windows vykdomajam [EXE](/executable/exe/) failui, bet yra kelios platformos. Šis senesnis Python platinimų formatas 2010 m. pradžioje buvo pakeistas naujesniu Wheel (WHL) failo formatu.

## EGG failo formatas

EGG failai išsaugomi kaip suspausti ZIP archyvai. Tai reiškia, kad jei .egg plėtinį pakeisite .zip, galėsite jį atidaryti naudodami standartines dekompresijos priemones, tokias kaip Corel WinZIP, Microsoft Explorer arba RARLAB WinRAR.

EGG failus galima sukurti naudojant **distutils** paketą, kurį siūlo Python. Kitas įrankis, kuriuo galima kurti ir atidaryti EGG failus, yra **SetupTools**. EGG failus galima įdiegti kaip paketą naudojant **easy_install**.

PASTABA – EGG failo formatas paseno ir tapo naujuoju rato WHL failo formatu.

## Nuoroda ##

* [Python EGGs](https://python101.pythonlibrary.org/chapter38_eggs.html)


