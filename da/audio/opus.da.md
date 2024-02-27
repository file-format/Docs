{
  "date": "2021-02-26",
  "keywords": [
"OPUS",
"fil",
"udvidelse",
"format",
"Lydkodning"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om OPUS filformat og API'er, der kan oprette og åbne OPUS filer.",
  "title": "OPUS",
  "linktitle": "OPUS",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-opu-das"
}
},
  "lastmod": "2021-02-26"
}

## Hvad er OPUS fil?

Opus er et lydfilformat skabt af Xiph.Org Foundation og senere standardiseret af IETF (Internet Engineering Task Force). Det er hovedsageligt udviklet til internetstreaming, Voice over IP (VOIP), videokonferencer og chat i spillet, og det er derfor, det er designet til at bevare lav latens og samtidig opretholde en interaktiv realtidskommunikation. Ved at bevare lydkvaliteten af en Opus-fil har mange blindlyttetests markeret Opus som lydformat af høj kvalitet end noget andet lydformat ved en given bitrate.

## OPUS filformatspecifikationer

Opus format bruger både SILK (brugt af Skype) og Xiph.Org codecs og understøtter variable bithastigheder fra 6 kb/s til 510 kb/s. Opus-udvidelsen bruger den taleorienterede LPC-baserede SILK-algoritme og den lavere latens-MDCT-baserede CELT-algoritme, nogle gange skifter mellem begge eller nogle gange ved at kombinere begge algoritmer for at give maksimal effektivitet. Filer i Opus-format har filtypenavnet .opus. I modsætning til Vorbis filformat kræves store kodebøger ikke af Opus for hver enkelt fil, det er grunden til, at dette format er forholdsvis effektivt.

## Referencer ##

* [OPUS - Af Wikipedia](https://en.wikipedia.org/wiki/Opus_(audio_format))


