{
  "date": "2021-08-04",
  "keywords": [
"mod",
"mp3",
"failą",
"pratęsimas",
"formatu",
"kas yra mod failo formatas",
"muzika",
"mod failo formatas",
"mod vs MP3",
"mod failo formato specifikacija"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie MOD failo formatą ir API, kurios gali kurti, konvertuoti ir atidaryti MOD failus.",
  "title": "MOD – muzikos modulio failas",
  "linktitle": "MOD",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-mo-ltd"
}
},
  "lastmod": "2021-08-04"
}

## Kas yra MOD failas?
Failas su plėtiniu .mod yra muzikos modulio failas, sukurtas naudojant standartinį muzikos modulio formatą, kuris yra pagrįstas **Amiga modulio formatu**, kurį sukūrė Karstenas Obarskis ir išleistas su Commodore skirta **Ultimate Soundtracker** programine įranga. Amiga sistema. Panašiai kaip [MIDI](/audio/mid/) failas, jį sudaro natų šablonai ir garso pavyzdžiai, atstovaujantys skirtingus instrumentus, kurie atkuriami pagal natas. MOD failai ypač naudojami vaizdo žaidimuose kaip foninė muzika ir **demoscene** kompiuterinio meno subkultūroje.

## MOD failo formatas

MOD yra kompiuterio failo formatas, kurio pagrindinė funkcija yra atvaizduoti muziką, ir tai buvo pirmasis modulio failo formatas. MOD failuose naudojamas .mod failo plėtinys, išskyrus **Amiga**, kuri nuskaito failo antraštę, kad nustatytų failo tipą, todėl nėra priklausomas nuo failo pavadinimo plėtinių. MOD failą sudaro įvairių instrumentų rinkinys pavyzdžių pavidalu, daugybė šablonų, nurodančių, kaip ir kada turi būti grojami mėginiai, ir sąrašas, kokius šablonus ir kokia tvarka groti.

### MOD failo formato specifikacijos

MOD failo šablonas iš tikrųjų yra sukurtas sekvencerio vartotojo sąsajoje kaip lentelė su vienu stulpeliu kiekvienam kanalui, todėl šioje lentelėje yra keturi stulpeliai (po vieną kiekvienam Amiga aparatūros kanalui. Kiekviename stulpelyje yra 64 eilutės).

Lentelės langelis gali sukelti vieną iš šių veiksmų stulpelio kanale, kai pasiekiamas jo eilutės laikas:

- Paleiskite instrumentą groti nauja nata šiame kanale tam tikru garsumu, galbūt su specialiu efektu.
- Pakeiskite esamai natai taikomą garsumą arba specialųjį efektą
- Keisti modelio srautą; pereiti į konkrečią dainos ar modelio padėtį arba kilpą modelio viduje
- Nieko nedaryk; ir toliau bus grojamos visos šiame kanale grojamos natos

Instrumentas yra vienas mėginys kartu su pasirenkama specifikacija, kurią mėginio dalį galima pakartoti, kad būtų išlaikyta vientisa nata.

### Laikas
Minimalus laiko tarpas buvo 0,02 sekundės pradiniame MOD faile arba vertikalaus išjungimo (VSync) intervalas, nes pradinė programinė įranga naudojo monitoriaus VSync laiką, veikiantį 50 Hz (PAL) arba 60 Hz (NTSC) dažniu. dėl laiko.

## Nuorodos

* [MOD (failo formatas) – pateikė Vikipedija](https://en.wikipedia.org/wiki/MOD_(file_format))


