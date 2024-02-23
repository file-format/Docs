{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Scopri il formato file OSU e le API che possono creare e aprire file OSU.",
  "title" : "File OSU - Osu! Formato file di script",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-it",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## Cos'è un file OSU?

Un file OSU è uno script di gioco scritto per osu! gioco di ritmo. Contiene informazioni su una beatmap utilizzata nel gioco come il livello di difficoltà, la canzone da riprodurre e i tempi degli oggetti colpiti con cui il giocatore deve sincronizzarsi con la musica. Consente ai giocatori di giochi ritmici di sviluppare sfide personalizzate e condividerle con la comunità del gioco.

**Tipo MIME del formato file OSR:** x-osu-beatmap

## Formato file OSU

I file OSU vengono salvati come file di testo semplice su disco e la loro struttura è definita molto chiaramente in [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) da osu!.

### Sezioni nel file OSU

Un tipico file OSU ha le seguenti sezioni.

|Sezione |Descrizione |Tipo di contenuto|
---|---|---|
|[Generale]| Informazioni generali sulla beatmap| chiave: coppie di valori|
|[Editore]| Impostazioni salvate per l'editor della beatmap| chiave: coppie di valori|
|[Metadati] |Informazioni utilizzate per identificare la beatmap| coppie chiave:valore|
|[Difficoltà] |Impostazioni difficoltà| coppie chiave:valore|
|[Eventi]| Eventi grafici beatmap e storyboard| Elenchi separati da virgole|
|[Punti di temporizzazione]| Cronometraggio e punti di controllo| Elenchi separati da virgole|
|[Colori]| Combo e colori della pelle| chiave: coppie di valori|
|[HitObjects]| Colpisci oggetti| Elenchi separati da virgole|

## Riferimenti

* [OSU! Gioco del ritmo](https://osu.ppy.sh/home)

* [Formato file OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


