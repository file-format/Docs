{
  "date" : "2020-01-10",
  "keywords" :[ "fișier dib", "format fișier dib", "ce este un fișier dib", "fișier", "exemplu dib", "extensie fișier dib", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DIB",
  "description":"Aflați despre formatul de fișier DIB și despre API-urile care pot crea și deschide fișiere DIB.",
  "linktitle" : "DIB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2020-01-10"
}

## Ce este un fișier DIB?

Un bitmap independent de dispozitiv (DIB) este un fișier imagine raster care este similară ca structură cu fișierele standard Bitmap ([BMP]()/image/bmp/)). Conține un tabel de culori care descrie maparea culorilor RGB la valorile pixelilor. Acest lucru permite DIB să reprezinte imaginea pe orice dispozitiv. Poate fi deschis cu aproape toate aplicațiile care pot deschide un fișier BMP standard pe Windows, precum și pe macOS. DIB sunt fișiere binare și au un format de fișier complex similar cu BMP. Imaginile DIB sunt independente de capacitățile de ieșire ale dispozitivelor de randare în ceea ce privește adâncimea culorii și pixelul pe inch.

## Specificații format fișier DIB ##
Un DIB conține următoarele informații despre culori și dimensiuni:

* Formatul de culoare al dispozitivului pe care a fost creată imaginea dreptunghiulară.
* Rezoluția dispozitivului pe care a fost creată imaginea dreptunghiulară.
* Paleta pentru dispozitivul pe care a fost creată imaginea.
* O serie de biți care mapează tripleți roșu, verde, albastru ( RGB ) în pixeli din imaginea dreptunghiulară.
* Un identificator de comprimare a datelor care indică schema de comprimare a datelor (dacă există) utilizată pentru a reduce dimensiunea matricei de biți.

### Format bloc de date DIB ###

DIB vine în contextul blocului de memorie în comparație cu fișierele .DIB stocate pe disc. Blocul de memorie cuprinde o structură care este în conformitate cu specificațiile Windows API pentru DIB. DIB real constă din:
* Un antet
* Paleta de culori
* Date Pixel

Practic, lucrul cu paleta, antetul și datele de imagine se face ca și cum ar fi trei blocuri separate de memorie. Un mâner acestui bloc comun de memorie este atribuit folosind GlobalAlloc și este cunoscut sub numele de HDIB, care este folosit pentru a extrage și a lucra cu antetul, tabelul de culori și datele pixelilor.

### Structuri ###
Informațiile conținute într-un DIB sunt reprezentate de structuri diferite. Acestea includ:

BITMAPInfo - Definește informațiile despre dimensiune și culoare pentru un DIB
```
typedef struct tagBITMAPINFO {
  BITMAPINFOHEADER bmiHeader;
  RGBQUAD          bmiColors[1];
} BITMAPINFO, *LPBITMAPINFO, *PBITMAPINFO;
```
Este format dintr-un BITMAPINFOHEADER:

```
typedef struct tagBITMAPINFOHEADER {
  DWORD biSize;
  LONG  biWidth;
  LONG  biHeight;
  WORD  biPlanes;
  WORD  biBitCount;
  DWORD biCompression;
  DWORD biSizeImage;
  LONG  biXPelsPerMeter;
  LONG  biYPelsPerMeter;
  DWORD biClrUsed;
  DWORD biClrImportant;
} BITMAPINFOHEADER, *PBITMAPINFOHEADER;
```
urmat de două sau mai multe structuri RGBQAD.

```
typedef struct tagRGBQUAD {
  BYTE rgbBlue;
  BYTE rgbGreen;
  BYTE rgbRed;
  BYTE rgbReserved;
} RGBQUAD;
```
### Biți de date ###
|Biți|Descriere|
---|---|
|Format de 1 bit (monocrom)|Hărțile de biți monocrome constau din două culori (alb și negru). Datorită acestui număr limitat de culori, aceste bitmap-uri ocupă mai puțin spațiu pe disc. BitBitCount returnează adevărat sau fals pentru reprezentarea ambelor culori. Majoritatea aplicațiilor omit complet paleta dacă bitBitCount==1.
|Format de 4 biți (VGA sau 16 culori)|Fiecare octet de date de imagine reprezintă doi pixeli și bitBitCount==4. Acești biți reprezintă culoarea pixelului în ordine descrescătoare.
|Format de 8 biți (256 de culori)|Acest format de 8 biți poate reprezenta maximum 256 de culori. Fiecare octet din matricea de date bitmap a imaginii reprezintă un singur pixel. Valoarea acelui octet este numărul intrării din paleta de culori care va fi utilizată din cele 256 de intrări reprezentate de bmciColors.
|Format de 24 de biți (TrueColor)|Aceste hărți de biți pot avea maximum 2^24 de culori (biBitCount == 24). Fiecare secvență de trei octeți din matricea de date bitmap reprezintă intensitățile relative ale celor trei nuanțe primare ale unui pixel. Nuanțele sunt descrise ca valori cuprinse între 0 și 255 și sunt stocate în cei trei octeți în ordinea Albastru, Verde și Roșu. Aceasta este o distincție importantă, deoarece majoritatea referințelor la culori în Windows folosesc ordinea opusă: roșu/verde/albastru, așa că gândiți-vă la „BGR” când lucrați cu imagini TrueColor în loc de „RGB”. O paletă de culori poate fi specificată pentru a accelera procesul de desen pentru Windows, caz în care biClrUsed nu va fi 0. Dar după cum puteți vedea, nu este necesară, deoarece datele pixelilor în sine conțin informațiile de culoare.
|Format 32 de biți|Imaginile pe 32 de biți au maximum 2^24 de culori (biBitCount == 24).

## Referințe ##
* [Bitmaps independente de dispozitiv - de la Microsoft](https://docs.microsoft.com/en-us/windows/win32/gdi/device-independent-bitmaps)

