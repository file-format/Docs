{
  "date" : "2021-06-09",
  "keywords" :[ "cue", "fișier", "extensie", "format", "ce este un fișier cue", "muzică", "format fișier cue", "specificație format fișier cue", "foaia cue", "CDRWIN" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aflați despre formatul fișierului CUE și despre API-urile care pot crea, converti și deschide fișiere CUE.",
  "title" :"CUE - Fișier cue Sheet",
  "linktitle" : "CUE",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-07-01"
}

## Ce este un fișier CUE?

Un fișier cu extensia .cue, cunoscut și ca fișier cue sheet, este un fișier de metadate care conține informații despre aspectul pieselor de pe un CD sau DVD. Acestea sunt acceptate de playere media și aplicații de creație a discurilor optice. Datele audio principale stocate pe CD sunt referite de fișierul cue, împreună cu specificațiile lungimii pistelor, titlurilor discurilor și interpreților. Astfel, dacă un singur fișier audio conține mai multe piese, fișierul cue poate fi folosit pentru a împărți audio în mai multe fișiere sau pentru a face referire la diferite piese.

## Format de fișier CUE

Fișierele CUE sau cue sheet sunt stocate în format text simplu, care poate fi citit de om. Informațiile dintr-un fișier cue sunt comenzi cu unul sau mai mulți parametri. Aceste comenzi fie se aplică întregului fișier, fie unei piese individuale, în funcție de comanda particulară și de context. Ghidul utilizatorului CDRWIN descrie specificațiile pentru sintaxa și semantica cue sheet.

## Comenzi esențiale din foaia CUE

|Comandă|Descriere|
---|---|
|FIȘIER| Se referă la fișierul care conține datele și formatul acestuia, cum ar fi [MP3](/ro/audio/mp3/), [WAV](/ro/audio/wav/) sau imagine de disc binară simplă)|
|TRACK| Definește informațiile contextului pistei, cum ar fi numărul și tipul sau modul acesteia.|
|INDEX| Reprezintă poziția ca index în cadrul FIȘIERULUI. Formatul este mm:ss:ff (minut-secundă-cadru).|
|PREGAP și POSTGAP|Acest lucru indică pregătirea sau post-gap-ul unei piese, care nu este stocată în niciun fișier de date. Lungimea este specificată în același format de cadru minut-secundă ca și pentru INDEX.|

### Exemplu de fișă CUE

```
REM GENRE Electronica
REM DATE 1998
PERFORMER "Faithless"
TITLE "Live in Berlin"
FILE "Faithless - Live in Berlin.mp3" MP3
  TRACK 01 AUDIO
    TITLE "Reverence"
    PERFORMER "Faithless"
    INDEX 01 00:00:00
  TRACK 02 AUDIO
    TITLE "She's My Baby"
    PERFORMER "Faithless"
    INDEX 01 06:42:00
  TRACK 03 AUDIO
    TITLE "Take the Long Way Home"
    PERFORMER "Faithless"
    INDEX 01 10:54:00
  TRACK 04 AUDIO
    TITLE "Insomnia"
    PERFORMER "Faithless"
    INDEX 01 17:04:00
  TRACK 05 AUDIO
    TITLE "Bring the Family Back"
    PERFORMER "Faithless"
    INDEX 01 25:44:00
  TRACK 06 AUDIO
    TITLE "Salva Mea"
    PERFORMER "Faithless"
    INDEX 01 30:50:00
  TRACK 07 AUDIO
    TITLE "Dirty Old Man"
    PERFORMER "Faithless"
    INDEX 01 38:24:00
  TRACK 08 AUDIO
    TITLE "God Is a DJ"
    PERFORMER "Faithless"
    INDEX 01 42:35:00
```
## Referințe

* [Fișier .cda - După Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

