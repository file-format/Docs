{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato file MK3D",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "file", "format" ],
  "description":"Scopri il formato di file MK3D per i video 3d stereoscopici creati da Matroska e le API che possono creare e aprire file MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Che cos'è un file MK3D? ##

I file MK3D appartengono alla famiglia dei formati video Matroska. Questi file sono in realtà video **stereoscopici 3d** creati utilizzando il formato Matroska 3D. Il contenitore di file MKV utilizza il valore di un campo StereoMode per definire il tipo di materiale video 3D stereoscopico. È inoltre disponibile un valore StereoMode per visualizzare i vecchi video 3D stereo separando i colori ciano e rosso (AnaGlyph)

## Dettagli tecnici ##
I video 3D possono essere compressi nei seguenti due modi:

- Traccia separata per ogni occhio.
- Combina ogni tracciamento oculare in un'unica traccia.

Il contenitore di file MKV supporta entrambi.

Per i video a traccia singola che sono più facili con il materiale 3D al loro interno, devi impostare il campo **StereoMode** che decide se gli aerei sono assemblati nella traccia mono o combinata sinistra destra. È possibile utilizzare uno dei seguenti valori di campo StereoMode:

|Valore | Descrizione |
|---|---|
|0| mono|
|1| fianco a fianco (l'occhio sinistro è il primo)|
|2| top-bottom (l'occhio destro è il primo)|
|3| top-bottom (l'occhio sinistro è il primo)|
|4| checkboard (a destra è la prima)|
|5| checkboard (a sinistra è la prima)|
|6| riga interfogliata (a destra è la prima)|
|7| riga interfogliata (a sinistra è la prima)|
|8| colonna interfogliata (a destra è la prima)|
|9| colonna interfogliata (a sinistra è la prima)|
|10| anaglifo (ciano/rosso)|
|11| fianco a fianco (l'occhio destro è il primo)|
|12| anaglifo (verde/magenta)|
|13| entrambi gli occhi allacciati in un blocco (l'occhio sinistro è il primo) (modalità campo sequenziale)|
|14| entrambi gli occhi allacciati in un blocco (l'occhio destro è il primo) (modalità campo sequenziale)|

Per le tracce multiple, il contenitore MKV deve decidere la funzionalità di ciascuna traccia separatamente. **TrackOperation** con **TrackCombinePlanes** vengono utilizzati per eseguire il lavoro.


## Riferimenti ##

- [Note sulle specifiche Matroska](https://www.matroska.org/technical/notes.html)
- [Supporto contenitore file MKV per video 3D stereo e file MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d- File/)

