{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VPK failas – „PlayStation Vita“ programų paketo failo formatas",
  "description": "Sužinokite apie VPK failo formatą ir API, kurios gali kurti ir atidaryti VPK failus.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-ltk"
}
},
  "lastmod": "2022-03-01"
}

## Kas yra VPK failas?

Failas su plėtiniu .vpk yra suspausto archyvo paketo failas, naudojamas trečiųjų šalių programoms įdiegti Sony PlayStation Vita žaidimų konsolėje. Šiuos failus galima įdiegti tik HENkaku Jailbreak Vita PlayStation, kuris leido PS Vita ir PSTV naudoti tinkintą vartotojo sukurtą turinį. VPK archyvo faile yra visas turinys, sudarantis žaidimą, įskaitant vaizdus, pvz., [PNG](/image/png/) failus, nustatymų failus, pvz., [.bin](/disc-and-media/bin/), ir visas konfigūracijas [XML](/web/xml/) failo formatu.

## VPK failo formatas

VPK failai išsaugomi diske kaip standartiniai suspausti [ZIP](/compression/zip/) archyvai. Juose gali būti keli aplankai ir kiti susiję failai, skirti trečiųjų šalių programoms, kurios bus įdiegtos Vita Gaming Console. Norėdami peržiūrėti VPK paketo failo turinį, pervardykite jo plėtinį iš .vpu į .zip ir išskleiskite turinį naudodami standartines išskleidimo priemones, pvz., WinZip arba WinRAR.

Valvesoftware turi išsamios informacijos apie [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format), kurią galima nurodyti kūrėjo požiūriu.

## Kaip įdiegti VPK failus?

VPK failus galima įdiegti iš komandinės eilutės programos VPK.exe. Windows operacinėje sistemoje failus galima išmesti į vpk.exe failą, kuris grąžina \*.vpk, kuriame yra visi supakuoti failai. Arba komandinės eilutės įrankį galima naudoti taip.

### Sukurkite VPK ir pridėkite failus

```
vpk <dirname>
```

### Ištraukite VPK failus

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Nuorodos

* [VPK failo formatas](https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [VPK failai](https://developer.valvesoftware.com/wiki/VPK)


