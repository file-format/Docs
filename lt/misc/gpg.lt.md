{
  "date": "2022-02-17",
  "keywords": [
"gpg failą",
"gpg failo formatas",
"kas yra gpg failas",
"failą",
"gpg pavyzdys",
"gpg failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GPG failas – GNU Privacy Guard viešasis raktų pakabuko failas",
  "description": "Sužinokite apie GPG failą ir API, kurios gali kurti ir atidaryti GPG failus.",
  "linktitle": "GPG",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-gp-ltg"
}
},
  "lastmod": "2022-02-17"
}

## Kas yra GPG failas?

GPG failas yra šifravimo / iššifravimo rakto failas, kurį naudoja GNU Privacy Guard (GnuPG) šifravimo programa. Pati GnuPC programa yra pagrįsta OpenPGP standartu, kaip apibrėžta RFC4880 ir taip pat žinoma kaip PGP. Raktas į sėkmingą GPG naudojimą šiuolaikinėje operacinėje sistemoje yra jos universali raktų valdymo sistema. GPG komandinės eilutės įrankis leidžia lengvai integruoti jį su kitomis programomis.

## GPG failo formatas

GPG failai išsaugomi kaip užšifruoti dvejetainiai failai ir, žinoma, jie nėra įskaitomi žmonėms. Norėdami iššifruoti užšifruotą GPG failą, turite naudoti tą patį saugų raktą. Štai kodėl šių failų vidinis failo formatas nėra žinomas.

## Šifruokite ir iššifruokite failus naudodami GPG sistemoje „Linux“.

GPG komandų eilutės įrankis gali būti naudojamas failams užšifruoti ir iššifruoti Linux sistemoje.

### Failo šifravimas

Failas gali būti užšifruotas naudojant gpg komandą su parinktimi -c (create), kaip parodyta toliau.

```
gpg -c file1.txt
```
Vykdant šią komandą prašoma raktinės frazės, kuria būtų galima užšifruoti pradinio failo file1.txt turinį. Taip sukuriamas užšifruotas failas file1.txt.gpg.

### Failo iššifravimas ir ištraukimas

Norint iššifruoti ir išskleisti užšifruotą failą, galima naudoti šią komandą.

```
gpg cfile.txt.gpg
```

## Nuorodos

* [GNUPG](https://gnupg.org/)

* [HDF – Vikipedija](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)


