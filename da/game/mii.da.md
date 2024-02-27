{
  "date" : "2023-01-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lær om Age of Empires 2 Expansion Replay MGX-filformat og API'er, der kan oprette og åbne MGX-filer.",
  "title" : "MII-fil - Wii Virtual Avatar-filformat",
  "linktitle" : "MII",
  "menu" : {
    "docs" : {
      "identifier":"game-mii-da",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-15"
}

## Hvad er MII fil?

En MII-fil er et virtuelt avatar-filformat, der bruges til at gemme virtuelle avatarer på Nintendo Wii-spillekonsollen. Disse filer indeholder information såsom avatarens udseende, bevægelser og animationer. De kan bruges i spil, sociale netværksapplikationer og anden software på Wii. En MII-fil indeholder også andre funktioner om avataren, såsom køn, hårfarve, hudfarve, ansigtstræk og øjentype.

Du kan åbne en MII-fil ved hjælp af [My Avatar Editor](https://rc24.xyz/goodies/mii/).

## MII filformat

MII-filformatet er defineret i detaljer på [Wii Brew](https://wiibrew.org/wiki/Mii_data). Strenge i en MII-fil gemmes i Unicode-format (UTF-16), big-endian.

### MI-blok

MII-fildata gemmes på Wiimote i to blokke. Hver blok er 750 bytes lang, med 2 byte CRC, hvilket gør den i alt 752 bytes. Hver blok starter med en 4-byte værdi ('RNCD'), der ser ud til at være det magiske tal for MII-filformatet.

## Hvordan opretter man MII-filer?

Der er et par forskellige måder at skabe avatarer til Nintendo Wii på:

1. `Brug af den indbyggede Mii-kanal på Wii:` Denne kanal giver dig mulighed for at oprette brugerdefinerede avatarer ved hjælp af en række værktøjer, herunder ansigtstræk, kropsform og tøj. Når du har oprettet din avatar, kan du gemme den som en Mii-fil og bruge den i spil og anden software på Wii.

1. `Brug af Mii Maker-appen på Nintendo 3DS:` Mii Maker-appen giver dig mulighed for at oprette brugerdefinerede avatarer ved hjælp af berøringsskærmen og kameraet på din Nintendo 3DS. Når du har oprettet din avatar, kan du gemme den som en Mii-fil og overføre den til din Wii via en trådløs forbindelse.

1. `Brug af tredjepartssoftware:` Nogle udviklere har lavet software, der giver dig mulighed for at oprette brugerdefinerede avatarer til Wii. Denne software er typisk designet til brug på en computer og kan kræve yderligere trin for at overføre avataren til din Wii.

1. `Brug af færdiglavede avatarer:` Nogle spil og anden software på Wii kommer muligvis med færdiglavede avatarer, som du kan bruge.

I alle tilfælde skal du have en Nintendo-konto for at oprette og gemme din avatar på Wii.

## Referencer

* [My Avatar Editor](https://rc24.xyz/goodies/mii/)

* [Wii Brew](https://wiibrew.org/wiki/Mii_data)


