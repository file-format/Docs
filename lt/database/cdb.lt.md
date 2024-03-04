{
  "date": "2021-06-16",
  "keywords": [
"CDB",
"pratęsimas",
"cdb failą",
"cdb failo formatas",
"Duomenų bazės failo tipas",
"Duomenų bazės failo formatas",
"kas yra cdb failas"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CDB failo formatą ir API, kurios gali kurti ir atidaryti CDB failus.",
  "title": "CDB – nuolatinės duomenų bazės failas",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-ltb"
}
},
  "lastmod": "2021-06-16"
}

## Kas yra CDB failas?
CDB failai naudojami svarbiose programose, tokiose kaip el. CDB reiškia nuolatinė duomenų bazė, greitas, patikimas ir paprastas paketas, skirtas nuolatinėms duomenų bazėms kurti arba skaityti. Duomenų bazės pakeitimas yra saugus nuo sistemos gedimų. Vartotojai neturi pristabdyti perrašymo metu. CDB veikia kaip asociatyvus masyvas (diske), susieja raktus su reikšmėmis ir leidžia viename rakte saugoti kelias reikšmes.

## CDB failo formatas

CDB failo formatas saugo skaičius, poslinkius, ilgius ir maišos reikšmes mažuoju formatu kaip nepasirašytus 32 bitų sveikuosius skaičius. Manoma, kad raktai ir duomenys yra nepermatomos baitų eilutės, neturinčios specialaus apdorojimo. Duomenų bazės pradžioje fiksuoto dydžio antraštė vaizduoja 256 maišos lenteles, nurodydama jų vietą faile ir ilgį tarpais. Paprastai duomenys saugomi kaip įrašų seka, kiekviename įraše saugomas rakto ilgis, duomenų ilgis, raktas ir duomenys. Rūšiavimo ar lygiavimo taisyklių nėra. Po įrašų yra 256 įvairaus ilgio maišos lentelių rinkinys. Kadangi nulis yra tinkamas ilgis, duomenų bazėje fiziškai gali būti saugomos mažiau nei 256 maišos lentelės, tačiau nėra nieko, kas laikoma 256 lentelėmis. Maišos lentelės susideda iš eilės laiko tarpsnių, kurių kiekviename yra maišos reikšmė ir įrašo poslinkis. Tuščios vietos poslinkis yra nulis.

### CDB failo formato struktūra

CDB duomenų bazė susideda iš viso duomenų rinkinio viename kompiuterio faile. Jį sudaro trys dalys:
- Fiksuoto dydžio antraštė
- Duomenys
- Maišos lentelių rinkinys.

Galima ieškoti tik tikslių raktų. Paieškos veikia pagal šį algoritmą:

- Sumaišykite raktą.
- Nustatykite, kurioje maišos lentelėje ir lizde turėtų būti šis įrašas.
- Išbandykite nurodytą lizdą maišos lentelėje.

Ieškant raktų su daugiau nei viena verte, papildomų reikšmių galima rasti tiesiog tęsiant paiešką kitame lizde.

#### Funkcijos

CDB duomenų bazės struktūra turi keletą funkcijų:

##### Greitos paieškos
Sėkminga paieška didžiulėje duomenų bazėje paprastai užtrunka tik du kartus, o nesėkmingai – tik vieną.
##### Mažos pridėtinės išlaidos
Duomenų bazėje naudojami 2048 baitai, 24 baitai vienam įrašui ir vietos raktams bei duomenims.
##### Atsitiktinių ribų nėra
CDB gali valdyti bet kokią duomenų bazę iki 4 gigabaitų. Kadangi nėra jokių kitų apribojimų, įrašai net neturi tilpti į atmintį. Duomenų bazės saugomos nuo mašinos nepriklausomu formatu.
##### Greitas atominės duomenų bazės pakeitimas
Komanda **cdbmake** gali perrašyti visą duomenų bazę į dvi eiles greičiau nei kiti maišos paketai.
##### Greiti duomenų bazės ištrynimai
**cdbdump** gali spausdinti duomenų bazės turinį su cdbmake suderinamu formatu.


## Nuorodos Nr.

* [cdb (programinė įranga) – Vikipedija](https://en.wikipedia.org/wiki/Cdb_(software))

* [CDB specifikacija](http://cr.yp.to/cdb.html)


