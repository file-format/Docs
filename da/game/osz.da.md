{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om OSZ-filformat og API'er, der kan oprette og åbne OSZ-filer.",
  "title" : "OSZ-fil - osu! Beatmap filformat",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz-da",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Hvad er en OSZ fil?

En OSZ-fil er et komprimeret filformat, der bruges af rytmespillet osu! at gemme beatmap-data. Beatmaps er i bund og grund niveauer for spillet, og de inkluderer information såsom sangen, taktimingen og placeringen af hitobjekter på spilskærmen. OSZ-filer giver mulighed for nem distribution af beatmaps og downloades typisk fra internettet og importeres til spillet. OSU! har også filformatet [OSR](/game/osr/), der er en genafspilningsfil og kan afspilles igen af spillere.

**MIME-type af OSR-filformat:** x-osu-replay

## OSZ filformat

De interne filformatdetaljer for OSZ-filtyper er ikke offentligt tilgængelige. Den indeholder [ZIP](/compression/zip/)-komprimerede data, der har information til at afspille musikken, vise grafik og vise spillere om begivenhederne, når de skal interagere med spillet.

## Hvordan opretter man OSZ-fil?

OSU! har detaljerede instruktioner til [creating OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files)- og OSK-filer. Følgende trin kan bruges til at oprette en OSZ-fil ved hjælp af OSU!.

1. Åbn et beatmap via editoren.
1. Fra topmenuen, vælg Filer > Eksporter pakke....
1. .osz-arkivet vil blive placeret i mappen Eksporter inde i osu! folder.

## Referencer

* [OSU! Rhythm Game](https://osu.ppy.sh/home)


