{
  "date" : "2021-09-08",
  "keywords" :[ "mgx fil", "mgx filformat", "vad är en mgx fil", "fil", "mgx exempel", "mgx filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Lär dig om Age of Empires 2 Expansion Replay MGX-filformat och API:er som kan skapa och öppna MGX-filer.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Vad är MGX fil?

En fil med filtillägget .mgx är en inspelad fil för spelet Age of Empires II: The Conquerors som kan spelas om i programmet Age of Empires II. Den innehåller fullständig inspelning av kampanjen som spelas av användaren. Det kan laddas och spelas upp inom programmet Age of Empires II. När spelet har spelats om visar alla händelser och scenarier som användaren planerade för kampanjen och spelade.

## MGX-filformat - Mer information

Det interna filformatet för MGX-filen har utarbetats och tillgängligt som delvis validerad information om [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx- formatera). Specifikationerna beskriver detaljerna i följande avsnitt.

### Strukturdefinitioner

Strukturdefinitionerna för GPX-filformatet tros vara baserade på [BinData Ruby Gem-deklarationer](https://github.com/dmendel/bindata/wiki) som ger ett sätt att läsa och skriva strukturerad binär data. Detta låter programmeraren specificera formatet för den binära data som sedan läses och skrivs av BinData.

### MGX Messaging

MGX-meddelanden baseras på två typer av meddelanden.

* GAMESTART - anger spelstartkommandon och är inte validerad till dags dato
* CHAT - beskriver chattmeddelanden i spelet. Både spelare och själva spelet (Gaia) kan sända meddelanden i spelet.

### SPELHANDLINGAR

Det finns flera [GAMEPLAY Actions](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) som har hämtats och vars detaljer är tillgängliga.

## Referenser

* [Age of Empires 2: The Conquerors — Savegame File Format Specification](https://github.com/stefan-kolb/aoc-mgx-format)

