{
  "date": "2022-07-18",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4S failas – kas yra M4S failas?",
  "description": "Sužinokite apie M4S failo formatą ir API, kurios gali kurti ir atidaryti M4S failus.",
  "linktitle": "M4S",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-lts"
}
},
  "lastmod": "2022-07-18"
}

## Kas yra M4S failas?

M4S failas yra nedidelis vaizdo įrašo segmentas, kuris srautu perduodamas internetu naudojant **MPEG-DASH** srautinio perdavimo techniką. Jame yra vaizdo segmentas dvejetainių duomenų pavidalu. Gaunančioji programa (dažniausiai žiniatinklio naršyklė arba medijos leistuvai) leidžia šiuos segmentus tokia tvarka, kokia jie gaunami. Pirmasis M4S segmentas identifikuojamas pagal jame esančius inicijavimo duomenis. **Santrauka**, M4S failai yra nedideli atskiri viso failo medijos segmentai.

## M4S failo formatas

M4S failai yra pagrįsti [ISO Base Media File (ISOBMFF) format](https://www.w3.org/TR/mse-byte-stream-format-isobmff/). Šiuos mažus didelio failo segmentus galima atsisiųsti atskirai per HTTP. Taigi, jei turite didelį [MP4](/video/mp4/) filmo failą, jį galima transliuoti naudojant MPEG-DASH (dinaminis adaptyvus srautas per HTTP) techniką, segmentuojant jį kaip M4S segmento failus. Jei šis didelis filmo failas atsisiunčiamas į diską kaip M4S, atsisiunčiami keli M4S failai. Jei visi šie .m4s segmentai yra sujungti, sukuriamas visas paleidžiamas failas. Medijos leistuvai negali paleisti failo, nebent pirmasis inicijavimo segmentas taip pat pasiekiamas kartu su failu.

## Apie MPEG-DASH srautinį perdavimą

MPEG-DASH naudoja adaptyvų bitų dažnio srautinio perdavimo techniką, kuri leidžia srautiniu būdu perduoti aukštos kokybės medijos turinį internetu. Tai atliekama suskaidant turinį į mažų segmentų seką, kuri perduodama per HTTP. Tokiu būdu galima transliuoti didelius medijos failus, pvz., filmus, internetines transliacijas ar tiesioginę sporto renginio transliaciją. Šie segmentai yra užkoduoti skirtingu bitų greičiu. MPEG-DASH palaikantys daugialypės terpės grotuvai automatiškai parenka segmentą su didžiausia bitų sparta, naudodami bitų perdavimo spartos pritaikymo algoritmą. Taip išvengiama atkūrimo įvykių sustabdymo ar pakartotinio buferio.

### Atvirojo kodo API, skirta M4S failams

Yra atvirojo kodo API, kurias galima naudoti M4S failams skaityti ir konvertuoti.

 * [libdash](https://github.com/bitmovin/libdash) – .NET API, skirta M4S failams
 * [dash.js](https://github.com/Dash-Industry-Forum/dash.js) – M4S failo Javascript klientas
 * [Go Library for Create Dash Files](https://github.com/zencoder/go-dash)

### Atvirojo kodo API konvertuoti M4S į MP4

 * [MFourStoMp4](https://github.com/muri11o/mfourstomp4)

## Literatūra ###

* [ISO bazinės medijos failo (ISOBMFF) formatas](https://www.w3.org/TR/mse-byte-stream-format-isobmff/)

* [Dinaminis prisitaikantis srautas per HTTP – MPEG-DASH](https://en.wikipedia.org/wiki/Dynamic_Adaptive_Streaming_over_HTTP)


