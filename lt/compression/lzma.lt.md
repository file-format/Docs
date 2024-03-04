{
  "date": "2021-04-08",
  "keywords": [
"lzma failą",
"lzma failo formatas",
"kas yra lzma failas",
"failą",
"lzma pavyzdys",
"lzma failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LZMA – LZMA suspausto failo formatas",
  "description": "Kas yra LZMA failas ir API, kurie gali kurti ir atidaryti LZMA failus.",
  "linktitle": "LZMA",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-lzm-lta"
}
},
  "lastmod": "2021-04-18"
}

## Kas yra LZMA failas?

Failas su plėtiniu .lzma yra suglaudintas archyvo failas, sukurtas naudojant LZMA (Lempel-Ziv-Markov grandinės algoritmas) glaudinimo metodą. Jie daugiausia randami / naudojami Unix operacinėje sistemoje ir yra panašūs į kitus glaudinimo algoritmus, tokius kaip [ZIP](/compression/zip/), siekiant sumažinti failo dydį. LZMA yra senas failo formatas, kuris yra arba buvo pakeistas .xz formatu. .lzma formato MIME tipas yra \`application/x-lzma'. Šį failo formatą sukūrė Igoris Pavlovas, kad būtų galima naudoti LZMA SDK.

## LZMA failo formatas

LZMA failą sudaro dvi pagrindinės dalys:

 1. Antraštė
 1. Suspausti duomenys


### LZMA antraštė

LZMA failai turi 13 baitų antraštę, po kurios pateikiami LZMA suspausti duomenys. LZMA antraštę sudaro:

 * Savybės
 * Žodyno dydis
 * Nesuspaustas dydis

#### LZMA antraštės ypatybės

Savybių lauke yra trys ypatybės. Skliausteliuose pateikiama santrumpa, po kurios nurodomas ypatybės verčių diapazonas. Lauką sudaro

1) pažodinio konteksto bitų skaičius (lc, [0, 8]);
2) pažodinės padėties bitų skaičius (lp, [0, 4]); ir
3) padėties bitų skaičius (pb, [0, 4]).

#### LZMA žodyno dydis

Tai saugoma kaip beženklis 32 bitų mažasis sveikasis skaičius, kurio reikšmės svyruoja nuo 2^n ir 2^n + 2^(n-1). LZMA Utils gali išskleisti bet kokio dydžio žodyno failus.

#### Nesuspaustas dydis
Nesuspaustas dydis išsaugomas kaip nepasirašytas 64 bitų mažasis sveikasis skaičius. Speciali 0xFFFF_FFFF_FFFF_FFFF reikšmė rodo, kad nesuspaustas dydis nežinomas. Reikšmė rodoma naudingosios apkrovos pabaigos žymekliu (\*) tada ir tik tada, jei nesuspaustas dydis nežinomas.

## Nuorodos

* [LZMA failo formatas](https://svn.python.org/projects/external/xz-5.0.3/doc/lzma-file-format.txt)

* [Lempel–Ziv–Markov grandinės algoritmas](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm)


