{
  "date": "2021-09-08",
  "keywords": [
"pcc fil",
"pcc filformat",
"hvad er en pcc-fil",
"fil",
"pcc eksempel",
"pcc filtypenavn",
"udvidelse",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "Lær om Mass Effect PCC-filformat og API'er, der kan oprette og åbne PCC-filer.",
  "title": "PCC - Mass Effect Package File",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-dac"
}
},
  "lastmod": "2021-09-08"
}

## Hvad er PCC fil?

En fil med .pcc er en [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) fil, der indeholder spildata til at ændre spilindhold såsom modeller, teksturer og rum. Mass Effect 2 og 3 er de første skydespil baseret på Unreal Engine 3-spilmotoren. Spillet blev oprindeligt udviklet af [Bioware](https://www.bioware.com/about/), som beholdt størstedelen af spilressourcerne i deres proprietære PCC-filformat. Bioware blev opkøbt af Electronic Arts, en førende global interaktiv underholdningsudgiver.

## PCC-filformat - flere oplysninger

PCC-filer indeholder komprimerede og/eller ukomprimerede strukturer, der bidrager til den overordnede filorganisation.

### Komprimeret PCC-struktur

En komprimeret PCC-fil består af tabeller og data, der er segmenteret i bidder. Hver chunk indeholder et variabelt antal komprimerede blokke.

 * `Chunks Header` - En fælles header på 16 bytes, der indeholder information om chunks.
 * Chunk Header - En 16 byte header, der indeholder information om de rå komprimerede data indeholdt i blokformularen.

### Ukomprimeret PCC-struktur

Ukomprimerede PCC-filer er opdelt i følgende fem dele.

 * `Header` - indeholder grundlæggende information om strukturen af PCC-filen.
 * `Navnetabel` - indeholder navn fundet inde i pakken inklusive importklasser, eksporter og eksportegenskaber.
 * `Import Table` - indeholder alle klasser og objekter importeret af PCC.
 * `Eksporter tabel` - indeholder alle objekter gemt i pakken. Hver eksport kan variere i størrelse.

## Referencer

 * [Me3Explorer - PCC-filformat](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)

