{
  "date": "2021-07-29",
  "keywords": [
"pes failą",
"pes failo formatas",
"kas yra pes failas",
"failą",
"pes pavyzdys",
"pes failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PES failo formatas – Brother PE siuvinėjimo formatas",
  "description": "Sužinokite apie PES failo formatą ir API, kurios gali kurti ir atidaryti PES failus.",
  "linktitle": "PES",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-pe-lts"
}
},
  "lastmod": "2021-07-29"
}

## Kas yra PES siuvinėjimo failas?

PES siuvinėjimo failas yra dizaino failas, kuriame yra siuvinėjimo / siuvimo mašinų instrukcijos. Jį sukūrė Brother Industries savo siuvinėjimo mašinoms, bet vėliau buvo įformintas kaip bendras failo formatas. PES failus naudoja siuvimo mašinos, kad perskaitytų instrukcijas, kaip susiūti raštus ant audinio. Šie failai skirti dviem tikslams; Pirma, pateikiama Brother Industries sukurtos PE-Design programos dizaino informacija, o antra – dizaino pavadinimas, spalvos ir siuvinėjimo mašinos kodai, tokie kaip stop, jump ir trim.

## PES failo formatas – daugiau informacijos

PES failas išsaugomas diske dvejetainiu formatu. Jame yra keli skyriai, kuriuose yra iš anksto nustatyta siuvimo informacija. PES failo formatas yra toks.

 * Versijos duomenys – pateikiama versijos informacija ir gali būti bet kokia vertė #PES0001, #PES0020, #PES0030, #PES0040, #PES0050, #PES0055, #PES0060
 * PEC paieškos vertė – 4 baitų mažo galo sveikasis skaičius, einantis iškart po versijos duomenų ir reiškia paieškos reikšmę PEC skyriui, kuriame yra išsami informacija apie dizainą.
 * PSE skyrius – yra su Brother PE-Design susijusi dizaino informacija ir gali būti pritaikyta kitoms siuvimo reikmėms
 * PCE skyrius – gali būti bet kurioje PSE failo vietoje, bet nurodyta PEC Seek Value.

## Siuvimo mašinų tipas naudojant PES failą

PES failus pirmiausia sukuria PE-Design programinė įranga, naudojama su Brother siuvimo mašinomis. Kai kurios kitos mašinos, galinčios palaikyti PES failus, yra Babylock ir Bernina namų siuvinėjimo mašinos.

## Kaip konvertuoti PSE failus?

PE-Design programinė įranga gali [convert PSE file](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/11_1088392?hl=pes+file) į kitus formatus, pvz., .pes, .dst, .exp, .pcs, .hus, .vip, .shv, .jef, .sew, .csd arba .xxx . Tai galima padaryti naudojant PE-Design programą, atidarius failą ir pasirinkus Konversijos formatą.

## Nuorodos

* [PE dizainas – instrukcijų vadovas](https://support.brother.com/g/s/hf/htmldoc/ped/im/ped11/en/PED11_EN/index.html#!/)


