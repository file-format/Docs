{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato file OSR e le API che possono creare e aprire file OSR.",
  "title" : "File OSR - osu! Formato file di riproduzione",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-it",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## Cos'è un file OSR?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**Tipo MIME del formato file OSR:** x-osu-replay

## Formato file OSR

I file OSR vengono salvati come file binari con campi dati di lunghezza fissa e variabile.

|Tipo dati| Formato|
---|---|
|Byte |Modalità di gioco del replay (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Intero |Versione del gioco al momento della creazione del replay (es. 20131216)|
|Stringa |osu! beatmap MD5 hash|
|Stringa| Nome del giocatore|
|Stringa| osu! replay MD5 hash (include alcune proprietà del replay)|
|Breve| Numero di 300|
|Breve| Numero di 100 in standard, 150 in Taiko, 100 in CTB, 100 in Mania|
|Breve| Numero di 50 in standard, piccoli frutti in CTB, 50 in mania|
|Breve| Numero di Geki in standard, massimo 300 in Mania|
|Breve| Numero di Katus nello standard, 200 in Mania|
|Breve| Numero di errori |
|Intero| Punteggio totale visualizzato sul rapporto del punteggio|
|Breve| La migliore combinazione visualizzata nel report del punteggio|
|Byte| Combo perfetto/completo (1 = nessun errore, nessun cursore rotto e nessun cursore finito in anticipo)|
|Intero| Mod utilizzate. Vedi sotto per l'elenco dei valori mod.|
|Stringa| Grafico a barre della vita: coppie separate da virgole u/v, dove u è il tempo in millisecondi trascorso nel brano e v è un valore in virgola mobile compreso tra 0 e 1 che rappresenta la quantità di vita che hai in un dato momento (0 = la barra della vita è vuoto, 1= la barra della vita è piena)|
|Lungo| Timestamp (tick di Windows)|
|Intero| Lunghezza in byte dei dati di riproduzione compressi|
|Byte |Array Dati di riproduzione compressi|
|Lungo| ID punteggio online|
|Doppio| Ulteriori informazioni sulla modalità. Presente solo se il tiro al bersaglio è abilitato.|

## Riferimenti

* [OSU! Gioco del ritmo](https://osu.ppy.sh/home)

* [Formato file OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


