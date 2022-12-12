{
  "date" : "2021-02-15",
  "keywords" :[ "fișier vp6", "format fișier vp6", "ce este un fișier vp6", "fișier", "exemplu vp6", "extensie fișier vp6", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Fișier video TrueMotion",
  "description":"Aflați despre formatul de fișier VP6 și despre API-urile care pot crea și deschide fișiere VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## Ce este un fișier VP6?

VP6 este un format video cu compresie cu pierderi care a fost introdus de tehnologiile On2 în mai 2003. Face parte dintr-o serie de codecuri video dezvoltate de TrueMotion, inclusiv V3, V4 și V5. Formatul a fost folosit în scurt timp în domeniul radiodifuziunii, cum ar fi rapoartele BBC și software-ul QuickLink. VP6 a fost succedat de VP7 Codec în ianuarie 2005, cu o compatibilitate mai bună cu compresia.

## Format de fișier VP6

Specificațiile complete pentru fișierele V6 nu sunt disponibile public. On2 a făcut publice specificațiile inițial, dar în curând acestea au fost făcute indisponibile pentru utilizatorii generali. O documentație neoficială a formatului de fișier VP6 este disponibilă la [multimedia wiki](https://wiki.multimedia.cx/index.php?title=On2_VP6) care poate fi trimisă pentru referință de către dezvoltatori.

### Macroblocuri (MB)

Similar cu MPEG-2, MPEG-4 părțile 2 și 10, fiecare cadru video al unui fișier VP6 este compus dintr-o matrice de macroblocuri de 16x16 (MB). Fiecare MB poate fi în unul dintre următoarele moduri:

* Intra MB
* Inter MB, null MV, referință cadru anterior
* Inter MB, diferenţial MV, cadru de referinţă anterior
* Inter MB, patru MV, referință de cadru anterior
* Inter MB, MV 1, referință cadru anterior
* Inter MB, MV 2, referință cadru anterior
* Inter MB, null MV, referință cadru marcat
* Inter MB, diferenţial MV, cadru de referinţă marcat
* Inter MB, MV 1, referință cadru marcat
* Inter MB, MV 2, cadru de referință marcat

### Antet cadru

Antetul cadrului unui VP6 este așa cum se arată mai jos, care urmează împachetarea biților big-endian.

|Sintaxă|Număr de biți|Tip|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 semnifică un intra cadru|
|qp |6 |Nesemnat |Interval valid al parametrului de cuantizare 0..63|
|marcator| 1| Constant| 0=VP61/62, 1=VP60|
|dacă (mod_cadru == 0) { | 0 | |egal cu INTRA_FRAME|
|versiunea |5| Constant| 6=VP60/61, 7=VP60(Arte electronice), 8=VP62|
|versiunea2 |2| Constanta |0=VP60, 3=VP61/62|
|interlace |1| Boolean |true (1) înseamnă că se va folosi interlace|
|dacă (marcator==1 sau versiunea2==0) {||||
|offset |16 |Nesemnat| offset buffer secundar (octeți relaționați la începutul bufferului)|
|}||||
|dim_y |8| Nesemnat| Înălțimea macroblocului video|
|dim_x |8| Nesemnat| Lățimea macrobloc video|
|render_y |8 |Nesemnat |Înălțimea afișajului videoclipului|
|render_x |8 |Nesemnat |Lățimea de afișare a videoclipului|
|}altfel{||||
|dacă (marcator==1 sau versiunea2==0) {||||
|offset |16 |Nesemnat |Decalaj tampon secundar (octeți relevanți la începutul tamponului)|
|}||||
|}||||

## Referințe

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

