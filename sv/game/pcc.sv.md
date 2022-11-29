{
  "date" : "2021-09-08",
  "keywords" :[ "pcc-fil", "pcc-filformat", "vad är en pcc-fil", "fil", "pcc-exempel", "pcc-filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Läs mer om Mass Effect PCC-filformat och API:er som kan skapa och öppna PCC-filer.",
  "title" :"PCC - Mass Effect Package File",
  "linktitle" : "PCC",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är en PCC fil?

En fil med .pcc är en [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) fil som innehåller speldata för att modifiera spelinnehåll som modeller, texturer och rum. Mass Effect 2 och 3 är första skjutspel baserade på spelmotorn Unreal Engine 3. Spelet utvecklades ursprungligen av [Bioware](https://www.bioware.com/about/) som behöll majoriteten av spelresurserna i sitt proprietära PCC-filformat. Bioware förvärvades av Electronic Arts, ett ledande globalt förlag för interaktiv underhållning.

## PCC-filformat - Mer information

PCC-filer innehåller komprimerade och/eller okomprimerade strukturer som bidrar till den övergripande filorganisationen.

### Komprimerad PCC-struktur

En komprimerad PCC-fil består av tabeller och data som är uppdelade i bitar. Varje bit innehåller ett variabelt antal komprimerade block.

* `Chunks Header` - En 16 bytes gemensam rubrik som innehåller information om bitarna.
* `Chunk Header` - En 16 byte header som innehåller information om den råa komprimerade data som finns i blockformen.

### Okomprimerad PCC-struktur

Okomprimerade PCC-filer är indelade i följande fem delar.

* `Header` - innehåller grundläggande information om PCC-filens struktur.
* `Namntabell` - innehåller namn som finns i paketet inklusive importklasser, exporter och exportegenskaper.
* `Import Table` - innehåller alla klasser och objekt som importeras av PCC.
* `Export Table` - innehåller alla objekt lagrade i paketet. Varje export kan variera i storlek.

## Referenser

* [Me3Explorer - PCC-filformat](https://me3explorer.fandom.com/wiki/PCC_File_Format)
* [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
* [Bioware](https://www.bioware.com/about/)

