{
  "date": "2022-05-09",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie PYC failo formatą ir API, kurios gali kurti ir atidaryti PYC failus.",
  "title": "PYC failo formatas - Python kompiliuotas failas",
  "linktitle": "PYC",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-py-ltc"
}
},
  "lastmod": "2022-05-09"
}

## Kas yra PYC failas?

PYC failas yra sudarytas išvesties failas, sugeneruotas iš šaltinio kodo, parašyto Python programavimo kalba. Kai PY failas paleidžiamas naudojant Python interpretatorių, jis konvertuojamas į baitinį kodą vykdyti. Tuo pačiu metu sukompiliuotas baito kodas taip pat išsaugomas kaip .pyc failas, kad vėliau būtų galima pakartotinai panaudoti talpyklą, jei reikia.

## PYC failo formato struktūra

PYC failai yra baitinio kodo ir jų failo formato specifikacijos nėra viešai prieinamos. Tačiau kai kurių šaltinių atliktas tyrimas rodo, kad [structure of a PYC file](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html) sudaro:

 * Keturių baitų magiškas skaičius – tiesiog du baitai, kurie keičiasi kiekvieną kartą pakeitus skirstymo kodą, o tada du baitai 0d0a.
 * Keturių baitų modifikavimo laiko žyma – šaltinio failo, sugeneravusio .pyc, Unix modifikavimo laiko žyma, kad ją būtų galima iš naujo sukompiliuoti, pasikeitus šaltiniui.
 * Suskirto kodo objektas – kodo objekto marshal.dump išvestis, kuri yra šaltinio failo kompiliavimo rezultatas.

## DUK

1. **Kaip generuojamas PYC failas?** PYC failas sukuriamas, kai Python šaltinio kodas kompiliuojamas naudojant Python interpretatorių. Tada sukompiliuotas kodas išsaugomas PYC faile.

1. **Ar PYC greitesnis už py?** PYC failai išsaugomi sukūrus python šaltinio kodą. Kadangi jie jau yra interpretuoti, šie failai yra greitesni nei .py failai.

1. **Kuo skiriasi py ir pyc failai?** PY failuose yra programos Python šaltinio kodo failas, o .pyc failuose yra interpretuotas programos baitinis kodas.

1. **Ar PYC yra dvejetainis failas?** Taip, PYC failas yra dvejetainis failas, kuriame yra 4 baitų magiškasis skaičius, 4 baitų modifikavimo laiko žyma ir suskirstyto kodo objektas.

1. **Ar galime konvertuoti .pyc į .py?** Taip, pyc failus galima konvertuoti į py. Dekompiliatoriai, tokie kaip Decompyle++, gali būti naudojami sukompiliuotam Python baitų kodui išversti atgal į galiojantį ir žmogui skaitomą Python šaltinio kodą.

## Nuorodos

* [.pyc failų struktūra](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html)


