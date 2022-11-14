{
  "date" : "2022-04-01",
  "keywords" :[ "file nkit", "formato file nkit", "cos'è un file nkit", "file", "esempio nkit", "estensione file nkit", "estensione", "formato", "piè di pagina nkit", "file formato del kit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Scopri il formato di file NKIT e le API che possono creare e aprire file NKIT.",
  "title" :"NKIT - Formato file immagine disco",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## Che cos'è un file NKIT?

Un file NKIT è un'immagine disco di dati estratti dai giochi NintendoWii e GameCube. NKIT è per il formato Nintendo Toolkit. Il risultante file di compressione [ISO](/it/compression/iso/) utilizza i dati principali di questi giochi per essere eseguiti con programmi di emulazione come Dolphin, Swiss e Nintendont. NKit è disponibile in formati di file raw (iso) e compressi (gcz), entrambi progettati tenendo in considerazione la riproducibilità e le dimensioni.

## Formato file NKIT

Il formato di file NKit è un formato senza perdita di dati e viene utilizzato per ridurre e ripristinare le immagini di Nintendo Wii e GameCube. I formati sono disponibili nei formati di file ISO e GCZ per ciascuno dei giochi GameCube e Wii.

|Sistema |Formato |Hardware supportato |Dolphin supportato |Ripristinabile 1:1 |Note|
---|---|---|---|---|---|
|Cubo di gioco| nkit.iso| Sì |Sì| Sì | Come per GameCube iso compatto|
|Cubo di gioco| nkit.gcz| No| Sì| Sì |GCZ è il formato di compressione ricercabile per blocchi di Dolphin|
|Wii| nkit.iso| No Sì| Sì| Formato RVT-H riproducibile solo in Dolphin|
|Wii| nkit.gcz| No Sì| Sì| RVT-H in GCZ giocabile solo in Dolphin|

### Intestazione NKIT

L'intestazione del formato del file NKIT è la seguente.

|Offset |Lunghezza |Nome|
---|---|---|
|0x200 |0x4 |NKit Intestazione 'NKIT'|
|0x204 |0x4 |NKit Versione 'v01'|
|0x208 |0x4 |Fonte immagine originale CRC32|
|0x20C |0x4 |NKit CRC - rende il file NKit CRC32 uguale al CRC sorgente a 0x208 (a 0x4 in GCZ)|
|0x210 |0x4 |Lunghezza immagine sorgente|
|0x214 |0x4 |ID spazzatura forzato (quando l'ID disco è diverso - raro - solo GameCube)|
|0x218 |0x4 |Wii Aggiorna la partizione CRC32 se rimossa durante la conversione|

## Riferimenti ##

* [Formato file NKIT - di gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

