{
  "date" : "2021-06-11",
  "keywords" :[ "wpl", "file wpl", "estensione", "formato", "cos'è un file wpl", "musica", "formato file wpl"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Scopri il formato di file WPL e le API che possono creare, convertire e aprire file WPL.",
  "title" :"WPL - File playlist di Windows Media Player",
  "linktitle" : "WPL",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## Che cos'è un file WPL?

Un file con estensione .wpl contiene la playlist di brani da eseguire su Microsoft Windows Media Player. Questi file vengono solitamente creati dagli utenti per le loro raccolte video e audio. Il contenuto scritto in un file WPL è solo percorsi di directory o posizioni per i file multimediali selezionati dal creatore del file .wpl, in modo che l'applicazione del lettore multimediale possa trovare e riprodurre prontamente il contenuto multimediale dalle posizioni della directory.

## Formato file WPL

WPL (Windows Media Player Playlist) è un formato di file proprietario utilizzato in Microsoft Windows Media Player versioni 9 o successive. È un formato di file per computer che memorizza playlist multimediali. Per impostazione predefinita, la playlist viene salvata con un'estensione .wpl (Playlist Windows Media Player). Puoi invece utilizzare l'estensione [.m3u](/it/audio/m3u/), se desideri riprodurre i tuoi dischi dati su un dispositivo che non supporta questa estensione. Gli elementi di un file WPL sono rappresentati in formato XML.

L'elemento di primo livello "smil" specifica che gli elementi del file seguono la struttura Synchronized Multimedia Integration Language (SMIL). Il file viene creato e salvato con estensione .wpl e il suo tipo MIME è application/vnd.ms-wpl.

### Esempio WPL

Ecco un esempio di file wpl:
```
<?wpl version="1.0"?>
<smil>
    <head>
        <meta name="Generator" content="Microsoft Windows Media Player -- 11.0.5721.5145"/>
        <meta name="AverageRating" content="33"/>
        <meta name="TotalDuration" content="1102"/>
        <meta name="ItemCount" content="3"/>
        <author/>
        <title>Bach Organ Works</title>
    </head>
    <body>
        <seq>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio01.mp3"/>
            <media src="\\server\vol\music\Classical\Bach\OrganWorks\cd03\audio02.mp3"/>
            <media src="SR15.mp3" tid="{35B39D45-94D8-40E1-8FC2-9F6714191E47}"/>
        </seq>
    </body>
</smil>
```




## Riferimenti ##

* [MPEG-1 Audio Layer II - Di Wikipedia](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

