{
  "date" : "2019-10-11",
  "keywords" :[ "fișier exif", "format fișier exif", "ce este un fișier exif", "fișier", "exemplu exif", "extensie fișier exif", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EXIF",
  "description":"Aflați despre formatul fișierului EXIF și despre API-urile care pot crea și deschide fișiere EXIF.",
  "linktitle" : "EXIF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier EXIF?
EXIF înseamnă „Exchangeable Image File Format”, definiția dată pentru prima dată de [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) în 1985. Standardul este gestionat de Japan Electronics și Asociația Industriilor de Tehnologia Informației (JEITA) începând de astăzi. EXIF este un standard pentru specificațiile formatelor de imagine și sunet utilizate în principal de camerele digitale și scanere.

Standardul EXIF include informațiile de etichetare și metadate cu fișierul imagine. Metadatele pot conține informații precum modelul camerei, viteza obturatorului, data și ora, diafragma, producătorul, timpul de expunere, rezoluția X, rezoluția Y etc. În mod normal, datele EXIF sunt ascunse în mod implicit. Pentru a vizualiza datele EXIF, trebuie să selectați proprietățile de vizualizare din aplicația de vizualizare a imaginilor. Metadatele Exif pot include, de asemenea, miniaturi împreună cu date tehnice și de imagine primară într-un singur fișier imagine.

## Istoric și versiuni ##

* În octombrie 1995, JEIDA a stabilit Versiunea 1. În această versiune, JEIDA a definit structura, care constă din formatul datelor de imagine și informații despre atribute și etichete de bază.
* Noiembrie 1997, versiunea 1.1 a fost introdusă cu majoritatea etichetelor din versiunea 1, dar au adăugat și prevederi pentru informații opționale despre atribute și operarea formatului.
* Iunie 1998, versiunea 2 cu spațiu de culoare sRGB, miniaturi comprimate și fișiere audio.
* Decembrie 1998, versiunea 2.1 cu stocare îmbunătățită și informații despre atribute.
* Februarie 2002, versiunea 2.2, versiunea îmbunătățită 2.1 cu adăugarea finisajului de imprimare.
* Septembrie 2003, versiunea 2.21 cu spațiu de culoare opțional cunoscut sub numele de Adobe RGB.

## Format de fișier EXIF

EXIF utilizează următoarele formate de fișiere cu adăugarea de metadate specifice.

1. [JPEG](/ro/image/jpeg/) - transformare cosinus discret (DCT) pentru fișiere de imagine comprimate.
1. [TIFF](/ro/image/tiff/) Rev. 6.0 (RGB sau YCbCr) pentru fișiere de imagine necomprimate.
1. [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) pentru fișiere audio (liniar [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) sau ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Law PCM pentru date audio necomprimate și [ IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) pentru date audio comprimate).

### Marker folosit de EXIF ###

Markerul 0xFFE0~~0xFFEF este "Marcatorul aplicației", utilizat de aplicația utilizator. De exemplu, camerele digi mai vechi folosesc JFIF (JPEG File Interchange Format) pentru stocarea imaginilor. JFIF folosește APP0 (0xFFE0) Marker pentru inserarea datelor de configurare a camerei digi și a imaginii în miniatură. În plus, EXIF folosește și un marcator de aplicație pentru inserarea datelor, dar EXIF folosește marcatorul APP1 (0xFFE1) pentru a evita un conflict cu formatul JFIF. Fiecare format de fișier EXIF începe de la acest format.


|Marcator SOI|Marcator APP1|Date APP1|Alt marcator
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

Pornește de la marcatorul SOI (0xFFD8), deci este un fișier JPEG. Apoi APP1 Marker urmează imediat. Toate datele EXIF sunt stocate în această zonă de date APP1. Partea „SSSS” din tabelul de sus înseamnă dimensiunea zonei de date APP1 (zona de date EXIF). Vă rugăm să rețineți că dimensiunea „SSSS” include și dimensiunea descriptorului în sine. După „SSSS”, pornesc datele APP1. Prima parte este o dată specială pentru identificarea dacă EXIF sau nu, sunt utilizați caracterul ASCII „EXIF” și 2 octeți de 0x00. După zona Marker APP1, urmează ceilalți Markeri JPEG.

### Structura datelor Exif ###

O structură aproximativă a datelor EXIF (APP1) este prezentată mai jos. După cum sa discutat mai sus, datele EXIF pornesc de la caracterul ASCII „EXIF” și 2 octeți de 0x00, apoi urmează datele EXIF. EXIF folosește formatul TIFF pentru a stoca date.


|FFE1|Marcator APP1
---|---|
|SSSS|Date APP1|Dimensiunea datelor APP1
|45786966 0000|Antet Exif
|49492A00 08000000|Ant TIFF
|XXXX. . . .|IFD0 (imaginea principală)|Director
|LLLLLLLL|Link către IFD1
|XXXX. . . .|Zona de date a IFD0
|XXXX. . . .|Exif SubIFD|Director
|00000000|Sfârșitul linkului
|XXXX. . . .|Zona de date din Exif SubIFD
|XXXX. . . .|IFD1(imagine în miniatură)|Director
|00000000|Sfârșitul linkului
|XXXX. . . .|Zona de date a IFD1
|FFD8XXXX. . . XXXXFFD9|Imagine în miniatură

#### Antet TIFF ####

Antetul fișierului [TIFF](/ro/image/tiff/) de 8 octeți conține următoarele informații:

`Bytes 0-1:` Ordinea octetilor folosita in fisier. Valorile legale sunt: „II”(4949.H)“MM” (4D4D.H).

În formatul „II”, ordinea octetilor este întotdeauna de la octetul cel mai puțin semnificativ până la octetul cel mai semnificativ, atât pentru numerele întregi de 16 biți, cât și pentru cele de 32 de biți. Aceasta se numește ordinea octetilor little-endian. În formatul „MM”, ordinea octeților este întotdeauna de la cel mai semnificativ la cel mai puțin semnificativ, atât pentru numerele întregi pe 16 biți, cât și pe 32 de biți. Aceasta se numește ordinea octetilor big-endian.

`Bytes 2-3:` Un număr arbitrar, dar ales cu grijă (42) care identifică în continuare fișierul ca fișier TIFF. Ordinea octeților depinde de valoarea octeților 0-1.

`Bytes 4-7:` Offset (în octeți) a primului IFD. Directorul poate fi în orice locație din fișier după antet, dar trebuie să înceapă de la granița unui cuvânt. În special, un Director de fișiere de imagine poate urma datele de imagine pe care le descrie. Cititorii trebuie să urmeze indicatorii oriunde ar putea duce. Termenul offset de octeți este întotdeauna folosit în acest document pentru a se referi la o locație în ceea ce privește începutul fișierului TIFF. Primul octet al fișierului are un offset de 0.

#### Director fișier imagine ####

Un IFD conține informații despre imagine, precum și indicatori către datele reale ale imaginii.. Constă dintr-un număr de 2 octeți a numărului de intrări în director (adică numărul de câmpuri), urmat de o secvență de intrări de câmp de 12 octeți , urmat de un offset de 4 octeți a următorului IFD (sau 0 dacă nu există). Trebuie să existe cel puțin 1 IFD într-un fișier TIFF și fiecare IFD trebuie să aibă cel puțin o intrare.

##### Intrare IFD #####

Fiecare intrare IFD de 12 octeți este în următorul format.


|Bytes|Descriere
---|---|
|0-1|Eticheta care identifică câmpul
|2-3|Tipul câmpului
|4-7|Numărul tipului indicat
|8-11|Decalajul valorii, decalajul fișierului (în octeți) al valorii pentru câmp. Se așteaptă ca valoarea să înceapă la granița unui cuvânt; Valoarea corespunzătoare va fi astfel un număr par. Acest decalaj al fișierului poate indica oriunde în fișier, chiar și după datele imaginii

Un câmp TIFF este o entitate logică constând din eticheta TIFF și valoarea acesteia. Acest concept logic este implementat ca o intrare IFD, plus valoarea reală dacă nu se încadrează în partea de valoare/offset, ultimii 4 octeți ai intrării IFD. Termenii câmp TIFF și intrare IFD sunt interschimbabili în majoritatea contextelor.

#### Imagine in miniatură ####

Formatul Exif conține o miniatură a imaginii (cu excepția Ricoh RDC-300Z). De obicei este situat lângă IFD1. Există 3 formate pentru miniaturi; Format JPEG (JPEG folosește YCbCr), format RGB TIFF, format YCbCr TIFF.

##### Miniatură în format JPEG #####

Dacă valoarea etichetei Compression(0x0103) din IFD1 este „6”, formatul imaginii în miniatură este JPEG. Majoritatea imaginilor Exif utilizează formatul JPEG pentru miniatură. În acest caz, puteți obține compensarea miniaturii de JpegIFOffset(0x0201) Tag în IFD1, dimensiunea miniaturii de JpegIFByteCount(0x0202) Tag. Formatul de date este formatul JPEG obișnuit, începe de la 0xFFD8 și se termină cu 0xFFD9. Se pare că formatul JPEG și dimensiunea de 160x120 pixeli sunt format de miniatură recomandat pentru Exif2.1 sau o versiune ulterioară.

##### Miniatură în format TIFF #####

Dacă valoarea etichetei Compression(0x0103) din IFD1 este „1”, formatul imaginii în miniatură nu este compresie (numită imagine TIFF). Punctul de pornire al datelor miniaturii este StripOffset(0x0111) Tag, dimensiunea miniaturii este suma etichetei StripByteCounts(0x0117).

## Referințe ##

* [EXIF - După Wikipedia](https://en.wikipedia.org/wiki/Exif)
* [Format fișier EXIF](https://www.media.mit.edu/pia/Research/deepview/exif.html)

