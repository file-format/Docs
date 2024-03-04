{
  "date": "2019-10-11",
  "keywords": [
"M4V",
"failą",
"pratęsimas",
"formatu",
"MPEG-4",
"Skaitmeninių teisių valdymas",
"DRM",
"Apple",
"vaizdo įrašą"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M4V",
  "description": "Sužinokite apie M4V failo formatą ir API, kurios gali kurti ir atidaryti M4V failus.",
  "linktitle": "M4V",
  "menu": {
    "docs": {
      "parent": "video",
      "identifier": "video-m4-ltv"
}
},
  "lastmod": "2019-09-14"
}

## Kas yra M4V failas?

**M4V** file format, developed by Apple, is a video container optionally protected with Digital Rights Management (DRM) copy protection to protect privacy or copy. Videos and audio tracks are wrapped around by container files to indexing and organizing playback streams. In addition, containers also provide the feature of chapters similar to those on DVDs. Apple uses M4V to encode videos in its iTunes Store. It protects unauthorized reproduction through Apple’s FairPlay copy protection by allowing M4V files to be played on only authorized computers having the accounts used to purchase the video. However, if DRM-protection is removed from M4V files, these files can be played in other video players by changing the extension from .m4v to .mp4, which is why M4V files are associated with MPEG-4. M4V naudoja H.264 vaizdo įrašams ir **[AAC](/audio/aac/)** ir Dolby Digital garso kodavimui ir dekodavimui.

## M4V failo struktūra ##

M4V files have continuous chunks with 8 byte header, 4 byte chunk size and 4 byte chunk type in each chunk. First chunk is “ftype” and has a sub-type at offset 8. M4V, apibrėžtas potipiu, kuris turi būti M4V_. Kiti gabalų tipai yra iš anksto nustatyti parašai: ftyp, mdat, moov, pnot, udta, uuid, moof, free, skip, jP2, wide , load, ctab, imap, matt, kmat, clip, crgn, sync, chap, tmcd, scpt, ssrc,  PICT. Kartodami gabalus, kol neaptinkamas nežinomas tipas, sudarome M4V failą.

Here is an examination of a sample: A sample m4v file’s binary data is inspected through Hex Viewer and it can be observed that it starts with a signature **ftyp** (hex: 66 74 79 70) at offset 4, which defines QuickTime Container File Type. File sub-type is **M4V_** (hex: 4D 34 56 20) which points to M4V (MPEG-4) file type. First block size is 32 (hex: 00 00 00 20, big-endian, high byte first), size located at offset 0. 32 poslinkyje (šeš. šešiolik.: 20) yra antrasis gabalas, kurio dydis yra 30 322 (šešiolik.: 00 00 76 72, big-endian, pirmas mažesnis baitas) ir tipas **moov** (šeš. šešiolik.: 6D 6F 6F 76). Kitas gabalas yra poslinkyje 32 + 30 322 # 30 354 (šeš. šešioliktainis: 00 00 76 92), jo dydis yra 8 (šeš. šešioliktainis: 00 00 00 08) ir tipas **laisvas** (šeš. šešiolik.: 66 72 65 65).
### M4V naudojami kodekai ###

#### Vaizdo įrašų kodekas H.264 ####

H.264 yra vaizdo glaudinimo standartas, konvertuojantis skaitmeninį vaizdo įrašą į formatą, kuriam reikia mažiau vietos, kai reikia perduoti arba saugoti. M4V vaizdo glaudinimui naudoja H.264. Jo taikymas svyruoja nuo DVD, televizoriaus, vaizdo konferencijų ir vaizdo transliacijos internetu. H.264 susideda iš dviejų pagrindinių dalių: Encoder – kuris suspaudžia vaizdo įrašą, dekoderis – kuris išspaudžia suspaustą vaizdo įrašą atgal. Žemiau esančiame paveikslėlyje paryškinti kodavimo ir dekodavimo procesai, o kiti procesai įtraukti į H.264 standartą.

##### Vaizdo įrašų kodavimo ir dekodavimo procesas H.264 #####

Suspaustam H.264 bitų srautui vaizdo kodavimo įrenginys atlieka numatymą, transformavimą ir kodavimo procesą. Tuo pačiu metu dekoderis atlieka atvirkštinį dekodavimo, atvirkštinės transformacijos ir rekonstrukcijos procesą, kad atkurtų vaizdo failą. H.264 užima pusę MPEG dydžio.

#### Garso kodekas ####

Išplėstinis garso kodavimas (AAC) yra garso kodekas, skirtas prarastam skaitmeninio garso suspaudimui ir naudojamas M4V talpykloje. AAC yra [MP3](/audio/mp3/) formato įpėdinis ir pasiekia geresnę kokybę nei MP3 su tuo pačiu pralaidumu. AAC formatas glaudinimo proceso metu išmeta dalį informacijos, kuri yra mažiau svarbi. AAC yra kintamo bitų spartos (VBR) blokų pagrindu sukurtas kodekas, kuriame kiekvienas blokas dekoduoja iki 1024 laiko domeno pavyzdžių.

### Nuorodos ###

* [Wikipedia – M4V](https://en.wikipedia.org/wiki/M4V)

* [Wikipedia – MPEG-4_AVC](https://en.wikipedia.org/wiki/H.264/MPEG-4_AVC)


