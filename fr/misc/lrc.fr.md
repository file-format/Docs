{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fichier LRC - Qu'est-ce qu'un fichier LRC ?",
  "description":"En savoir plus sur le fichier LRC Lyric et les API qui peuvent créer et ouvrir des fichiers LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## Qu'est-ce qu'un fichier LRC ?

Un fichier LRC est un fichier de paroles basé sur du texte qui contient les paroles d'une chanson audio. Lorsque la chanson audio est lue avec un lecteur de musique ou un logiciel de lecteur audio sur un ordinateur, le fichier LRC est lu en parallèle et affiché avec l'heure. Les fichiers LRC contiennent des points de repère pour l'affichage des paroles lorsque la chanson est en cours de lecture. En général, les fichiers LRC ont le même nom que le fichier audio correspondant tel que audio.mp3 et audio.lrc. Les fichiers LRC sont similaires aux fichiers de sous-titres tels que [SRT](/fr/video/srt/).

## Format de fichier LRC - Plus d'informations

Les fichiers au format de paroles LRC sont enregistrés sous forme de fichiers texte brut et peuvent être ouverts et modifiés dans un fichier texte. Le contenu d'un fichier LRC contient des informations de couleur pour l'affichage du texte des paroles.

## Formats LRC

Il existe plusieurs formats de fichiers LRC qui ont été développés au fil du temps. Ces

### Format LRC simple

Les balises de temps de ligne sont au format [mm:ss.xx] où mm correspond aux minutes, ss aux secondes et xx aux centièmes de seconde.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### Format simple étendu

Il inclut la possibilité de changer et de spécifier le genre des paroles en utilisant M : Masculin, F : Féminin, D : Duo.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### Format LRC amélioré

Le format LRC amélioré est une version étendue du format LRC simple. Il ajoute une étiquette de temps de mot au format<mm:ss.xx> à la fin du mot précédent.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## Références

* [Format de fichier des paroles LRC - Wikipédia] (https://en.wikipedia.org/wiki/LRC_(file_format))

