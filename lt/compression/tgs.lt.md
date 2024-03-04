{
  "date": "2019-10-11",
  "keywords": [
"tgs failą",
"tgs failo formatas",
"kas yra tgs failas",
"failą",
"tgs pavyzdys",
"tgs failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGS – telegramos animacinio lipduko failo formatas",
  "description": "Sužinokite apie TGS failo formatą ir API, kurios gali kurti ir atidaryti TGS failus.",
  "linktitle": "TGS",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-lts"
}
},
  "lastmod": "2021-04-02"
}

## Kas yra TGS failas?

Failas su plėtiniu .tgs yra animuotas lipduko failas, kurį pristatė kelių platformų pranešimų siuntimo paslauga [Telegram](https://core.telegram.org/stickers#animated-stickers). Animuotus lipdukus naudoja pranešimų siuntimo programų naudotojai, norėdami siųsti patobulintą ir gyvesnį pranešimų turinį, skirtingai nei statinė grafika, kuri yra nejudantys vaizdai. Iš pradžių Telegram nejudančių vaizdų lipdukams naudojo [WEBP](/image/webp/) failo formatą. TGS failo formatas gali saugoti animacijos duomenis didesne raiška ir mažesniu failo dydžiu, palyginti su statiniais WEBP lipdukais. TGS failus galima atidaryti naudojant tokias programas kaip Telegram, 7-zip, Apple Archive Utility ir Corel WinZip.

## TGS failo formatas

Telegram TGS failo formatą pristatė dar 2019 m. liepos mėn., remdamasi Lottie biblioteka. TGS failą sudaro [JSON](/web/json/) tekstas, kuris eksportuojamas iš Adobe After Effects animacijos. Eksportuotas JSON tekstas suglaudinamas naudojant gzip glaudinimą, kuris sumažina failo dydį. JSON informacija apie tekstinį failą saugoma tekstiniame faile, kuris tampa aukšto glaudinimo greičio pagrindu.

### TGS lipdukų specifikacijos

TGS failo formatas nustato tam tikrus TGS animuotų lipdukų kūrimo apribojimus. TGS animacinis failas:

 * Lipduko / drobės dydis turi būti 512 x 512 pikselių.
 * Lipdukų objektai neturi palikti drobės.
 * Animacijos trukmė neturi viršyti 3 sekundžių.
 * Visos animacijos turi būti kilpinės.
 * Lipduko dydis neturi viršyti 64 KB po atvaizdavimo Bodymovin.
 * Visos animacijos turi veikti 60 kadrų per sekundę greičiu.

### TGS JSON teksto pavyzdys

Išskleistame animuoto lipduko pavyzdyje yra šis JSON teksto turinys.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## Nuorodos Nr.

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip – Vikipedija](https://en.wikipedia.org/wiki/Gzip)


