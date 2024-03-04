{
  "date": "2019-10-11",
  "keywords": [
"ico failą",
"ico failo formatas",
"kas yra ico failas",
"failą",
"ico pavyzdys",
"ico failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICO – vaizdo failo formatas",
  "description": "Sužinokite apie ICO failų formatą ir API, kurios gali kurti ir atidaryti ICO failus.",
  "linktitle": "ICO",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ic-lto"
}
},
  "lastmod": "2019-09-10"
}

## Kas yra ICO failas?

Failai su ICO plėtiniu yra vaizdo failų tipai, naudojami kaip piktograma, vaizduojanti programą [Microsoft Windows](https://www.microsoft.com/en-us/windows). Jie yra skirtingo dydžio, spalvų palaikymo ir skiriamosios gebos, kad atitiktų ekrano reikalavimus. Kitas panašus vaizdo failo formatas Microsoft Windows yra [CUR](/image/cur/), skirtas žymeklio atvaizdavimui ir vaizdo antraštėje apibrėžiamas viešosios interneto prieigos taškas. MacOS ICNS failų formatai atlieka tą patį tikslą kaip ir ICO failai. Kai kurios internetinės svetainės ir programos suteikia galimybę kurti tokius failus ir konvertuoti kitus vaizdo formatus, pvz., [BMP](/image/bmp/), [PNG](/image/png/) ir kt. į piktogramos failo formatą. Oficialus IANA registruotas interneto medijos tipas ICO failams yra image/vnd.microsoft.icon.

## Trumpa istorija ##

Icons were introduced with the launch of Microsoft Windows 1.0. Jie buvo 32x32 dydžio ir vienspalviai. Pasirodžius win32, pradėtas naudoti tikros spalvos piktogramų vaizdų palaikymas iki 256 x 256 pikselių. Windows XP buvo pirmoji, palaikanti 32 bitų spalvotų piktogramų vaizdus, todėl prie piktogramos galima pridėti pusiau permatomas sritis, tokias kaip šešėliai, slapyvardžio panaikinimas ir į stiklą panašūs efektai. Windows XP Microsoft rekomenduoja tik iki 48 × 48 pikselių piktogramų dydžius. Windows Vista į Windows Explorer įtraukė 256 × 256 pikselių piktogramų rodinį, taip pat suglaudinto [PNG](/image/png/) formato palaikymą. Jei vartotojai naudojasi didesne raiška ir dideliu DPI režimu, rekomenduojami didesni piktogramų formatai (pvz., 256 × 256).

## ICO failo formatas ##

Vieną ICO failą sudaro vienas ar daugiau nei vienas mažas kelių dydžių ir spalvų gylio vaizdas. Kelių dydžių vaizdų buvimas tinkamas mastelio keitimui esant skirtingoms ekrano skyroms. Visos reikšmės ICO/CUR failuose pateikiamos [little-endian](https://en.wikipedia.org/wiki/Little-endian) baitų tvarka.

ICO failą sudaro piktogramos antraštė, piktogramų katalogas,

|Laukas|Aprašymas
---|---|
|Icon Header|Saugo bendrąją informaciją apie ICO failą.
|Katalogas[1..n]|Saugo bendrąją informaciją apie kiekvieną failo vaizdą.
|Piktograma #1|Tikėti duomenys pirmam vaizdui senu AND/XOR DIB formatu arba naujesniu PNG formatu
|...|
|Piktograma #n|Paskutinio piktogramos vaizdo duomenys

### Antraštė ###

|Poslinkis|Dydis (baitais)|Paskirtis
---|---|---|
|0|2|Rezervuota. Visada turi būti 0.
|2|2|Nurodo vaizdo tipą: 1 piktogramos (.ICO) vaizdui, 2 žymeklio (.CUR) vaizdui. Kitos vertės neteisingos.
|4|2|Nurodo vaizdų skaičių faile.

### Katalogas ###

Kataloge, esančiame ICO faile, pavaizduotame kaip ICONDIR struktūra, yra kiekvieno failo vaizdo ICONDIRECTORY struktūra. Po to seka gretimas visų vaizdo bitmap duomenų blokas. Tai yra kaip parodyta žemiau.

|Offsetas|Dydis|Aprašymas
---|---|---|
|0 (0)|1|Plotis, turėtų būti 0, jei 256 pikseliai
|1 (1)|1|Aukštis, turėtų būti 0, jei 256 pikseliai
|2 (2)|1|Spalvų skaičius turi būti 0, jei daugiau nei 256 spalvos
|3 (3)|1|Rezervuota, turėtų būti 0
|4 (4)|2|Spalvų plokštumos, kai yra .ICO formato, turi būti 0 arba 1 arba X viešosios interneto prieigos taškas, kai yra .CUR formatu
|6 (6)|2|Bitai pikselyje, kai yra .ICO formato, arba Y viešosios interneto prieigos taškas, kai yra .CUR formatas
|8 (8)|4|Betmap duomenų dydis baitais.
|12 (C)|4|Poslinkis faile.

## Nuorodos Nr.

* [ICO – Vikipedija](https://en.wikipedia.org/wiki/ICO_(file_format))

* [IANA – vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)


