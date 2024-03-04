{
  "date": "2021-08-30",
  "keywords": [
"ipa failą",
"ipa failo formatas",
"kas yra ipa failas",
"failą",
"ipa pavyzdys",
"ipa failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie IPA failo formatą ir API, kurios gali kurti ir atidaryti IPA failus.",
  "title": "IPA – iOS taikomųjų programų paketo failas",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-lta"
}
},
  "lastmod": "2021-08-30"
}

## Kas yra IPA failas?
Failas su plėtiniu .ipa priklauso iOS ir žinomas kaip programos paketo failas. Tai archyvo failas (suglaudintas naudojant [ZIP](/compression/zip/) glaudinimą), kuriame saugoma iOS programa, tačiau tą programą galima įdiegti tik iOS arba ARM pagrindu veikiančiuose MacOS įrenginiuose, pvz., iPad, iPhone ar iPod Touch. IPA failams įdiegti daugiausia galima naudoti iTunes, Apple Configurator 2 arba bet kokią trečiosios šalies programinę įrangą.

## IPA failo formatas
IOS kūrėjai, kuriantys programas naudodami Apple Xcode, yra gerai susipažinę su IPA failais, nes jie turi supakuoti savo sukurtas programas kaip IPA failus, kad galėtų išbandyti programų parduotuvės diegimą. Nors žinoma, kad IPA failai yra įdiegti kaip iOS programos, taip pat galite juos išskleisti, kad peržiūrėtumėte programos duomenis. Kadangi IPA faile yra tik vienas mobiliųjų telefonų ARM architektūros dvejetainis failas, o x86 architektūrai dvejetainio failo nėra, daugelio .ipa failų negalima įdiegti iPhone Simulator.
### .ipa failo struktūra
Toliau pateiktame pavyzdyje parodyta IPA struktūra:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Aukščiau pateikta struktūra yra integruota iTunes ir App Store atpažinti. Pagal šią struktūrą:
- Naudingos apkrovos kataloge yra visi programos duomenys.
– iTunes Artwork failas yra 512 × 512 pikselių PNG vaizdas, kuriame yra programos piktograma, skirta rodyti iTunes ir App Store programoje iPad.
- iTunesMetadata.plist yra įvairios informacijos, pradedant kūrėjo vardu ir ID, informacija apie autorių teises, paketo identifikatorių, programos pavadinimą, žanrą, išleidimo datą, pirkimo datą ir kt.
- Aplanke META-INF yra tik metaduomenys apie tai, kokia programa buvo naudojama kuriant IPA.


## Nuorodos 

* [.ipa – Vikipedija](https://en.wikipedia.org/wiki/.ipa)



