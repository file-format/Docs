{
  "date": "2022-02-16",
  "keywords": [
"obb failą",
"obb failo formatas",
"kas yra obb failas",
"failą",
"obb pavyzdys",
"obb failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "OBB failo formatas – „Android Opaque Binary Blob“ failas",
  "description": "Sužinokite apie OBB failo formatą ir API, kurios gali kurti ir atidaryti OBB failus.",
  "linktitle": "OBB",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-ob-ltb"
}
},
  "lastmod": "2022-02-16"
}

## Kas yra OBB failas?

OBB failas yra išplėtimo failas, kuriame yra papildomų duomenų, kurie yra be Android [APK](/compression/apk/) failo. Google Play parduotuvėje neleidžiama turėti Android APK failo, kurio dydis didesnis nei 100 MB. Tačiau kai kurioms programoms, be APK failų, gali prireikti didelės raiškos grafikos, medijos failų ar kitų didelių išteklių. Čia atsiranda OBB failų tipai. Google Play leidžia pridėti šiuos išplėtimo failus kaip priedą prie APK failo.

## OBB failo formatas

OBB failai išsaugomi kaip dvejetainiai failai kartu su APK failais. Kai APK pridedamas prie OBB failų, Google Play priglobia išplėtimo failus savo serveryje ir kūrėjas neapmokestina jokių papildomų mokesčių. Šie papildomi failai išsaugomi įrenginio bendroje saugykloje SD kortelėje arba USB montuojamame skaidinyje, kai programa atsisiunčiama įdiegti.

OBB failai atsisiunčiami ir įdiegiami atsisiunčiant. Tačiau kai kuriais atvejais jie atsisiunčiami įdiegti, kai programa paleidžiama pirmą kartą.

### OBB maksimalus failo dydis

Google Play parduotuvė leidžia įkelti iki 2 GB dydžio OBB išplėtimo failus. Didelio dydžio failus rekomenduojama įkelti kaip suglaudintus [ZIP](/compression/zip/) failus, kad būtų galima efektyviai įkelti internetu.

Šie išplėtimo failai gali būti priglobti kaip **pagrindinis** pirminis išplėtimo failas, skirtas papildomiems ištekliams, kurių reikia programai, arba pasirenkamas pataisos išplėtimo failas, skirtas nedideliems pagrindinio išplėtimo failo naujinimams.

## Nuorodos

* [Android kūrėjai – išplėtimo failai](https://developer.android.com/google/play/expansion-files)


