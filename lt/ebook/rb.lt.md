{
  "date": "2021-03-08",
  "keywords": [
"RB",
"Nuvo Media Rocket eBook įrenginys",
"failą",
"pratęsimas",
"formatu",
"eBook"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie „Nuvo Media“ „Rocket eBook“ įrenginio RB failo formatą ir API, kurios gali kurti ir atidaryti RB failus.",
  "title": "RB – „Rocket eBook File“.",
  "linktitle": "RB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-r-ltb"
}
},
  "lastmod": "2021-03-08"
}

## Kas yra RB failas?

The file with extension .rb holds the Rocket eBook content. The Rocket eBook is actually a device made by Nuvo Media; they released this device in 1998. Nors Rocket eBook gali rodyti vaizdus, bet tik juodai baltame ekrane. Jis turi 106 dpi arba 480 x 320 pikselių ekraną 4,5 x 3 colių jutikliniame ekrane. Rocket eBook jungiasi prie kompiuterio per nuoseklųjį prievadą, kad būtų galima atsisiųsti el. knygas RB failo formatu. RB failai gali naudoti DRM, tačiau ši technologija nenaudojama šiuolaikinėse el. knygose. RB faile paprastai yra HTML failas su vaizdais ir pseudo-OPF failas su visais metaduomenimis (.info).

## Techninė RB failo formato specifikacija Nr.

Pirmuosiuose 4 failo baituose pasirodo magiškas skaičius (šešioliktainiais): B0 0C B0 0C.

Atrodo, kad kiti du baitai yra versijos numeris, pvz., 02 00, kuris reiškia 2 pagrindinę ir 0 mažąją versiją.

Kituose keturiuose baituose yra tekstas NUVO, po kurio seka 4 baitai 00h.

The next 4-byte is the date when the book was created, encoded as an int16. Dėl to mes turime 0Eh kompensaciją. Senoji ORocketLibrary versija užkodavo visą metų vertę (ty 1999 m. buvo CF 07, 2000 m. – D0 07). Naujausioje versijoje tm_year saugomas pažodžiui, ty 100 2000 metams (64 00). Po metų ateina int8, reiškiantis 1 santykinį mėnesio skaičių, ir int8, reiškiantis mėnesio dieną.

Kiti 6 baitai yra 00 val. Laiko nustatymui jie gali būti rezervuoti.

Absoliutus Turinio poslinkis yra int32 poslinkis 18h.

Po to yra int32, kuriame yra .rb failo ilgis. Tai naudojama norint nustatyti, ar failai yra baigti, ar ne.

Atrodo, kad visa ši baitų dalis (nuo 20 iki 128 val.) reikalinga tik užšifruotam pavadinimui. Nešifruotuose pavadinimuose jų visada yra nulis.

Daugeliu atvejų toliau pateikiamas turinys (128 poslinkis). Jis prasideda puslapio įrašų (.rb failo skyrių) skaičiaus int32 skaičiumi ToC. Kiekvieną įrašą sudaro pavadinimas (32 baitų ilgio nulis), po kurio seka 3 int32: duomenų segmento ilgis, padėtis .rb faile ir šio įrašo vėliavėlė. Šiandien žinomos reikšmės yra: 1 (šifruota), 2 (informacijos puslapis) ir 8 (defliuota). Visi pavadinimai yra pritaikyti, jei reikia, siekiant užtikrinti, kad jie visi būtų unikalūs.

## Nuorodos

* [E-Reader – MobileRead](https://en.wikipedia.org/wiki/E-reader)


