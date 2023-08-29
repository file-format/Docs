{
  "date" : "2019-10-11",
  "keywords" :[ "fișier ico", "format fișier ico", "ce este un fișier ico", "fișier", "exemplu ico", "extensie fișier ico", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICO – Format fișier imagine",
  "description":"Aflați despre formatul de fișier ICO și despre API-urile care pot crea și deschide fișiere ICO.",
  "linktitle" : "ICO",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier ICO?

Fișierele cu extensia ICO sunt tipuri de fișiere imagine utilizate ca pictogramă pentru reprezentarea unei aplicații pe [Microsoft Windows](https://www.microsoft.com/en-us/windows). Acestea vin în diferite dimensiuni, suport de culoare și rezoluție pentru a se potrivi cerințelor afișajului. Un alt format de fișier imagine similar pe Microsoft Windows este [CUR](/ro/image/cur/) pentru reprezentarea cursorului și definește un hotspot în antetul imaginii. Pe MacOS, formatele de fișiere ICNS au același scop ca fișierele ICO. Mai multe site-uri web online, precum și aplicații oferă caracteristica de a crea astfel de fișiere și de a converti alte formate de imagine, cum ar fi [BMP](/ro/image/bmp/), [PNG](/ro/image/png/), etc. în format de fișier pictogramă. Tipul media de internet oficial înregistrat de IANA pentru fișierele ICO este image/vnd.microsoft.icon.

## Scurt istoric ##

Pictogramele au fost introduse odată cu lansarea Microsoft Windows 1.0. Acestea aveau dimensiunea 32x32 și erau monocrome. Odată cu sosirea pentru win32, a fost introdus suportul pentru imagini cu pictograme în culori adevărate, cu dimensiuni de până la 256x256 pixeli. Windows XP a fost primul care a oferit suport pentru imaginile cu pictograme color pe 32 de biți, permițând să fie adăugate pictogramei zone semi-transparente precum umbre, anti-aliasing și efecte asemănătoare sticlei. Microsoft a recomandat doar dimensiuni de pictogramă de până la 48×48 pixeli pentru Windows XP. Windows Vista a adăugat o vizualizare a pictogramei de 256×256 pixeli în Windows Explorer, precum și suport pentru formatul comprimat [PNG](/ro/image/png/). Cu utilizatorii care folosesc rezoluții mai mari și moduri DPI ridicate, sunt recomandate formate de pictograme mai mari (cum ar fi 256×256).

## Format de fișier ICO ##

Un singur fișier ICO constă dintr-una sau mai multe imagini mici de mai multe dimensiuni și adâncimi de culoare. Prezența imaginilor de mai multe dimensiuni este pentru scalarea corespunzătoare la diferite rezoluții ale ecranului. Toate valorile din fișierele ICO/CUR sunt reprezentate în ordinea octeților [little-endian](https://en.wikipedia.org/wiki/Little-endian).

Fișierul ICO constă dintr-un antet de pictograme, un director de pictograme,

|Câmp|Descriere
---|---|
|Icon Header|Stochează informații generale despre fișierul ICO.
|Director[1..n]|Stochează informații generale despre fiecare imagine din fișier.
|pictogramă #1|„date” reale pentru prima imagine în format vechi AND/XOR DIB sau PNG mai nou
|...|
|Picoa #n|Date pentru ultima imagine pictogramă

### Antet ###

|Offset|Dimensiune (în octeți)|Scop
---|---|---|
|0|2|Rezervat. Trebuie să fie întotdeauna 0.
|2|2|Specifică tipul de imagine: 1 pentru imaginea pictogramei (.ICO), 2 pentru imaginea cursorului (.CUR). Alte valori sunt nevalide.
|4|2|Specifică numărul de imagini din fișier.

### Director ###

Directorul conținut într-un fișier ICO, reprezentat ca structură ICONDIR, conține o structură ICONDIRECTORY pentru fiecare imagine din fișier. Același lucru este urmat de un bloc contiguu al tuturor datelor bitmap a imaginii. Acesta este așa cum se arată mai jos.

|Offset|Dimensiune|Descriere
---|---|---|
|0 (0)|1|Lățimea, ar trebui să fie 0 dacă 256 pixeli
|1 (1)|1|Înălțime, ar trebui să fie 0 dacă 256 pixeli
|2 (2)|1|Număr de culori, ar trebui să fie 0 dacă mai mult de 256 de culori
|3 (3)|1|Rezervat, ar trebui să fie 0
|4 (4)|2|Planurile de culoare atunci când sunt în format .ICO, ar trebui să fie 0 sau 1, sau hotspot-ul X când sunt în format .CUR
|6 (6)|2|biți pe pixel când este în format .ICO sau hotspot-ul Y când este în format .CUR
|8 (8)|4|Mărimea datelor bitmap în octeți.
|12 (C)|4|Offset în dosar.

## Referințe ##

* [ICO - După Wikipedia](https://en.wikipedia.org/wiki/ICO_(file_format))
* [IANA - vnd.microsoft.icon](http://www.iana.org/assignments/media-types/image/vnd.microsoft.icon)

