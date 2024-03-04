{
  "date": "2023-08-03",
  "keywords": [
"usr",
"usr failą",
"kas yra usr failas",
"kaip atidaryti usr failą",
"failą",
"usr failo plėtinys",
"pratęsimas"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "USR failo formatas – Lowrance GPS duomenų failas",
  "description": "Sužinokite apie USR formatą ir API, kurios gali kurti ir atidaryti USR failus.",
  "linktitle": "USR",
  "menu": {
    "docs": {
      "identifier": "gis-usr-lt",
      "parent": "gis"
}
},
  "lastmod": "2023-08-03"
}

## Kas yra USR failas?

.usr failo plėtinys taip pat susijęs su Lowrance GPS įrenginiais. Visų pirma, jis naudojamas GPS duomenims saugoti formatu, žinomu kaip Vartotojo duomenų formatas (USR formatas), kurį naudoja Lowrance GPS įrenginiai.

Naudodami Lowrance GPS įrenginį, galite išsaugoti savo kelio taškus, pėdsakus ir maršrutus kaip .usr failus. Šiuose failuose paprastai yra tokios informacijos kaip platuma, ilguma, aukštis virš jūros lygio, laiko žyma ir kiti duomenys, susiję su jūsų GPS veikla.

Štai keletas bendrų .usr failų naudojimo Lowrance GPS įrenginiuose:

– **Kelio taškai:** maršruto taškai yra konkrečios vietos, pažymėtos GPS, pvz., orientyrai, mėgstamos žvejybos vietos arba lankytinos vietos. Galite išsaugoti šias vietas kaip .usr failus ir jas importuoti, eksportuoti arba bendrinti su kitais Lowrance GPS naudotojais.

- **Prase:** pėdsakai rodo įrašytą GPS judėjimo kelią. Galite išsaugoti savo maršrutų žurnalus kaip .usr failus, leidžiančius vėliau peržiūrėti ir analizuoti maršrutus arba dalytis jais su kitais.

– **Maršrutai:** Maršrutai yra iš anksto nustatyti keliai, kuriuos galite sukurti ir išsaugoti savo GPS įrenginyje. Šiuos maršrutus taip pat galima išsaugoti kaip .usr failus, kad juos būtų galima naudoti ar dalytis ateityje.

Norėdami valdyti .usr failus savo Lowrance GPS įrenginyje, paprastai naudojate tokią programinę įrangą kaip Lowrance Insight Planner arba Lowrance GPS Utility, kad importuotumėte, eksportuotumėte ir tvarkytumėte GPS duomenis.

## USR failo formatas – daugiau informacijos

Lowrance iFinder GPS įrenginiuose .usr failai sukuriami ir išsaugomi į įrenginį įdėtoje MultiMediaCard (MMC) atminties kortelėje. Šiuose failuose yra vartotojo duomenų, pvz., kelio taškai, pėdsakai ir maršrutai.

Norėdami perkelti .usr failus iš MMC į kompiuterį, galite atlikti šiuos veiksmus:

- ** Išimkite MMC:** Atsargiai išimkite MultiMediaCard (MMC) iš Lowrance iFinder GPS įrenginio.

- **Įdėkite MMC į kompiuterį:** naudokite atitinkamą MMC kortelių skaitytuvą, kad įdėtumėte atminties kortelę į kompiuterio kortelių skaitytuvo angą.

- **Raskite .usr failus:** kai kompiuteris atpažins MMC, turėtumėte turėti prieigą prie jame saugomų failų. Ieškokite .usr failų, kuriuose yra jūsų GPS duomenys.

- **Konversija naudojant GPSBabel:** norėdami konvertuoti .usr failus į kitą GPS formatą, galite naudoti GPSBabel, kuris yra nemokamas atvirojo kodo įrankis, skirtas dirbti su įvairiais GPS failų formatais. GPSBabel palaiko platų įvesties ir išvesties formatų spektrą, leidžiantį konvertuoti .usr failus į formatus, suderinamus su kita GPS programine įranga ar įrenginiais.

Galite atsisiųsti GPSBabel iš oficialios svetainės (http://www.gpsbabel.org/) ir įdiegti ją savo kompiuteryje. Įdiegę konvertavimui galite naudoti programinės įrangos komandinės eilutės sąsają arba grafinę vartotojo sąsają (jei yra).

Pavyzdžiui, jei norite konvertuoti .usr failus į GPX formatą, galite naudoti tokią komandą:

```
gpsbabel -i lowranceusr -f input.usr -o gpx -F output.gpx
```

Aukščiau pateikta komanda nurodo GPSBabel nuskaityti įvesties failą input.usr Lowrance USR formatu ir įrašyti išvesties failą output.gpx GPX formatu.

– **Konvertuotų failų importavimas / naudojimas:** po konvertavimo turėsite naujus GPS duomenis (pvz., GPX), kuriuos galėsite naudoti su kita GPS programine įranga arba įrenginiais, palaikančiais tą formatą.

## Kaip atidaryti USR failą?

Programos, kurios atidaro arba nurodo USR failus, apima

– GPSBabel (Windows)
- GPSBabel (Mac)
- GPSBabel (Linux)

## Nuorodos
* [Lowrance Electronics](https://en.wikipedia.org/wiki/Lowrance_Electronics)


