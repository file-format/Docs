{
  "date": "2023-02-02",
  "keywords": [
"lietotnes fails",
"kas ir lietotnes fails",
"failu",
"kā atvērt lietotnes failu",
"lietotnes faila paplašinājums",
"pagarinājumu"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par APP failu formātu un API, kas var izveidot un atvērt APP failus.",
  "title": "APP faila formāts — macOS lietojumprogrammu komplekts",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app-lv",
      "parent": "executable"
}
},
  "lastmod": "2023-02-02"
}

## Kas ir APP fails?

.app fails operētājsistēmā MacOS ir īpaša veida direktorijs, kurā ir visi faili, kas nepieciešami konkrētas lietojumprogrammas palaišanai, tostarp izpildāmais kods, resursi un metadati. Paplašinājums .app norāda operētājsistēmai, ka šis direktorijs ir jāuzskata par vienu vienību, nevis atsevišķu failu kopumu, un ka to var palaist tieši no Finder vai Dock.

Finder ir noklusējuma failu pārvaldnieka lietojumprogramma operētājsistēmā MacOS. Tas ļauj pārlūkot un kārtot failus un direktorijus datorā. Dock ir MacOS funkcija, kas nodrošina ātru piekļuvi bieži izmantotajām lietojumprogrammām un dokumentiem. Gan Finder, gan Dock ļauj palaist lietojumprogrammas, noklikšķinot uz to .app failiem, kas atvērs atbilstošo lietojumprogrammu komplektu. Palaižot lietojumprogrammu, tiek palaists izpildāmais kods .app komplektā, padarot lietojumprogrammu pieejamu lietošanai. .app fails ir lietojumprogrammas attēlojums failu sistēmā, un tas nodrošina veidu, kā lietotājs var piekļūt lietojumprogrammai un palaist to.

Ar peles labo pogu noklikšķinot uz .app faila Finder MacOS sistēmā un atlasot Rādīt pakotnes saturu, varēsit skatīt lietojumprogrammu komplekta iekšējo struktūru. Tas ir noderīgi, ja vēlaties piekļūt resursiem vai failiem, ko izmanto lietojumprogramma, vai ja vēlaties pārbaudīt lietojumprogrammas saturu problēmu novēršanas nolūkos. .app faila pakotnes saturs parasti ietver direktorijus tādiem resursiem kā attēli un skaņas, kā arī lietojumprogrammas izpildāmais kods. Izpētot .app faila saturu, varat gūt dziļāku ieskatu par to, kā lietojumprogramma ir izveidota un ko tā dara.

## Kā atvērt APP failu?

Lai atvērtu .app failu operētājsistēmā MacOS, vienkārši veiciet dubultklikšķi uz faila programmā Finder. Tiks palaists .app komplektā esošā lietojumprogramma. Ja lietojumprogramma ir instalēta jūsu sistēmā un ir saistīta ar .app faila tipu, veicot dubultklikšķi uz faila, programma tiek startēta automātiski. Ja lietojumprogramma nav saistīta ar .app faila tipu, iespējams, ar peles labo pogu noklikšķiniet uz faila un atlasiet Atvērt ar”, lai izvēlētos piemērotu lietojumprogrammu, ar kuru to atvērt.

Varat atvērt .app failu terminālī operētājsistēmā MacOS, izmantojot komandu open. Lai to izdarītu, dodieties uz direktoriju, kurā atrodas .app fails, izmantojot komandu cd, un pēc tam palaidiet šo komandu:

```
open <AppName>.app 
```

kur<AppName> ir tās lietojumprogrammas nosaukums, kuru vēlaties palaist. Tādējādi programma tiks startēta tā, it kā jūs būtu uz tās veicis dubultklikšķi programmā Finder. Komanda atvērt ir vispārēja utilīta, ko var izmantot, lai atvērtu dažādu veidu failus, tostarp lietojumprogrammas, dokumentus un direktorijus. Ja .app failā izmantojat komandu open, tā palaiž komplektā esošo lietojumprogrammu.

## Atsauces
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
