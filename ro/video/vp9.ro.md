{
  "date" : "2021-03-12",
  "keywords" :[ "VP9", "Fișier", "Extensie", "Format fișier", "Format video", "Video TrueMotion", "VPX", "Tehnologii On2"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP9 - Fișier video TrueMotion",
  "description":"Aflați despre formatul de fișier VP9 și despre API-urile care pot crea și deschide fișiere VP9.",
  "linktitle" : "VP9",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-03-27"
}

## Ce este un fișier VP9?

Google a dezvoltat codecul VP9 ca un standard de codare video cu sursă deschisă, fără drepturi de autor, ca succesor al VP8. A fost conceput inițial pentru a comprima conținutul ultra HD de pe YouTube, deoarece extinde și îmbunătățește eficiența de codare a predecesorului său. Dacă vorbim despre codecurile VPX originale, acestea au venit de la On2 Technologies, care a fost asimilată de Google în 2010. Google a oferit ulterior codecul în sursă deschisă. Ambele formate VP8 și VP9 sunt disponibile sub o licență BSD gratuită care permite operatorilor să organizeze competențe de codificare sau decodare atât în software-ul exclusiv, cât și în software-ul open-source, fără a-și dezvălui codul sursă.

## Caracteristicile tehnice ale VP9

* VP9 oferă o rezoluție maximă de 8192x4352 la până la 120 fps și spații de culoare multiple, cu Rec 601, Rec 709, Rec 2020, SMPTE-170, SMPTE-240 și sRGB
* Gama completă de cazuri de utilizare web și mobile, de la compresie cu rată scăzută de biți până la ultra-HD de înaltă calitate, cu suport suplimentar pentru codificarea pe 10/12 biți și HDR, este pe deplin acceptată de acest format
* Poate reduce ratele de biți video cu până la 50% în comparație cu altele
* Este pregătit pentru streaming adaptiv și este folosit de YouTube și de alți furnizori de video web bine-cunoscuți
* Dispozitivele Chrome, Opera, Edge, Firefox și Android, precum și milioane de televizoare inteligente, acceptă decodarea acestui codec
* Rezoluțiile video mai mari de 1080p sunt modificate prin VP9 și permit compresia fără pierderi
* Diferite spații de culoare, cum ar fi Rec. 601, Rec. 709, Rec. 2020, SMPTE-170, SMPTE-240 și sRGB sunt acceptate de VP9
* Videoclipul HDR folosind Hybrid Log-Gamma și Perceptual Quantizer poate fi acceptat și de VP9


## Scurt istoric

* Dezvoltarea codecului video VP9 a început în 2011, iar decodorul său a fost adăugat la browserul web Chromium în decembrie 2012
* Prima versiune a browserului web Google Chrome a fost lansată în februarie 2013 și a lansat decodarea la acel moment
* Google a lansat Chrome 29.0.1547 cu suport final VP9 în august 2013
* În octombrie 2013, un decodor instinctiv VP9 a fost adăugat la FFmpeg
* Mozilla a adăugat suport VP9 la Firefox în decembrie 2013 în versiunea 2 care a fost lansată apoi pe 18 martie 2014
 

## Funcționarea VP9

De obicei, videoclipul 4K crește calitatea imaginii prin micșorarea anumitor pixeli, codecul VP9 și HEVC îi fac mai mari pentru a reduce rata de biți și dimensiunea fișierului. Deși acest lucru ar putea părea contradictoriu, motorul de codificare preia pixelii mai mari și îi transformă într-o productivitate cu rezoluție mai bună. Video sursă, care implică cadre video, este codificat sau comprimat pentru a face un flux de biți video comprimat. Fiecare cadru separat este mai întâi împărțit în blocuri de pixeli. Blocurile sunt apoi analizate pentru concedieri tridimensionale și conexiunile secvențiale dintre cadre sunt evaluate pentru a profita de zonele care nu pot fi modificate. Acestea sunt codificate prin vectori de mișcare care asigură calitățile blocului dat în cadrul următor. Informațiile reziduale sunt codificate folosind o compresie binară eficientă.

## Referințe

* [VP9 Wikipedia](https://en.wikipedia.org/wiki/VP9)
* [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/Media/Formats/Video_codecs#vp9)
* [Nucă de cocos](https://www.coconut.co/)

