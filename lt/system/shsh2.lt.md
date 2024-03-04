{
  "date" : "2023-02-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SHSH2 failas – iOS SHSH Blob failo formatas",
  "description":"Sužinokite, kas yra SHSH2 failas.",
  "linktitle" : "SHSH2",
  "menu" : {
    "docs" : {
      "identifier":"system-shsh2-lt",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-16"
}

## Kas yra SHSH2 failas?

SHSH2 failas, taip pat žinomas kaip SHSH blob arba ECID SHSH, yra skaitmeninis parašas, naudojamas Apple autentifikuoti ir patikrinti programinės įrangos naujinius iOS įrenginiuose, pvz., iPhone, iPad ir iPod. Jame yra unikalus įrenginio identifikatorius, žinomas kaip ECID (išskirtinis lusto ID). Jame taip pat pateikiama informacija apie įrenginyje įdiegtą programinės įrangos versiją.

## SHSH2 failo formatas – daugiau informacijos

SHSH2 failai išsaugomi diske dvejetainiu formatu, o šio failo formato vidinės failų struktūros informacija nėra viešai prieinama.

Kai Apple įrenginyje, pvz., iPhone, iPad ar Mac, įdiegiama nauja iOS versija, sugeneruojamas SHSH2 failas. Šis SHSH2 failas siunčiamas į Apple serverius, kurie nuskaito ir patikrina šį skaitmeninio parašo failą. Remdamasis šia informacija, serveris leidžia arba neleidžia įdiegti.

Tas pats atsitinka, kai prašoma atnaujinti. Kai vartotojas prašo atnaujinti arba atkurti savo įrenginį per iTunes ar kitą programinę įrangą, prieš leisdami tęsti naujinimą, Apple serveriai patikrins, ar SHSH2 failas atitinka įrenginio ECID ir programinės įrangos versiją.

## Nuorodos

* [SHSH Blob – Vikipedija](https://en.wikipedia.org/wiki/SHSH_blob)

* [TSS Saver](https://tsssaver.1conan.com/v2/)


