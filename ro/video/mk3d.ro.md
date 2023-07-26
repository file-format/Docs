{
  "date" : "2021-23-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format fișier MK3D",
  "keywords" :[ "mk3d", "matroska video", "mkv format", "stereoscopic 3d", "StereoMode", "video", "fișier", "format" ],
  "description":"Aflați despre formatul de fișier MK3D pentru videoclipuri 3d stereoscopice create de Matroska și API-uri care pot crea și deschide fișiere MK3D.",
  "linktitle" : "MK3D",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-23-02"
}

## Ce este un fișier MK3D? ##

Fișierele MK3D aparțin familiei de formate video Matroska. Aceste fișiere sunt de fapt videoclipuri **stereoscopice 3d** create folosind formatul Matroska 3D. Fișierul MKV Container folosește valoarea unui câmp StereoMode pentru a defini tipul de materiale video 3D stereoscopice. O valoare StereoMode este, de asemenea, disponibilă pentru a afișa vechile videoclipuri 3D stereo prin separarea culorilor cyan și roșu (AnaGlyph)

## Detalii tehnice ##
Videoclipurile 3D pot fi comprimate în următoarele două moduri:

- Pistă separată pentru fiecare ochi.
- Combinați fiecare urmărire a ochilor într-o singură pistă.

Containerul de fișiere MKV acceptă ambele.

Pentru videoclipurile cu o singură pistă, care sunt mai ușoare cu materialul 3D din interiorul lor, trebuie să setați câmpul **StereoMode** care decide fie ca avioanele să fie asamblate pe pistă combinată mono sau stânga dreapta. Puteți utiliza una dintre următoarele valori de câmp StereoMode:

|Valoare | Descriere |
|---|---|
|0| mono|
|1| unul lângă altul (ochiul stâng este primul)|
|2| sus-jos (ochiul drept este primul)|
|3| sus-jos (ochiul stâng este primul)|
|4| tablă de verificare (dreapta este primul)|
|5| tablă de verificare (stânga este primul)|
|6| rând intercalat (dreapta este primul)|
|7| rând intercalat (stânga este primul)|
|8| coloană intercalată (dreapta este prima)|
|9| coloană intercalată (stânga este prima)|
|10| anaglifă (cian/roșu)|
|11| unul lângă altul (ochiul drept este primul)|
|12| anaglifă (verde/magenta)|
|13| ambii ochi împletiti într-un singur bloc (ochiul stâng este primul) (modul secvenţial câmp)|
|14| ambii ochi împletiti într-un singur bloc (ochiul drept este primul) (modul secvenţial câmp)|

Pentru mai multe piese, containerul MKV trebuie să decidă funcționalitatea fiecărei piese separat. **TrackOperation** cu **TrackCombinePlanes** sunt folosite pentru a face treaba.


## Referințe ##

- [Note privind specificațiile Matroska](https://www.matroska.org/technical/notes.html)
- [Compatibilitate pentru containere de fișiere MKV pentru videoclipuri 3D stereo și fișiere MK3D](https://3dvision-blog.com/5520-mkv-file-container-support-for-stereo-3d-video-and-the-mk3d-files/)

