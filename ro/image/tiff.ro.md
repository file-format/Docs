{
  "date" : "2019-10-11",
  "keywords" :[ "fișier tiff", "format fișier tiff", "ce este un fișier tiff", "fișier", "exemplu tiff", "extensie fișier tiff", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TIFF – Format fișier imagine",
  "description":"Aflați despre formatul de fișier TIFF și despre API-urile care pot crea și deschide fișiere TIFF.",
  "linktitle" : "TIFF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier TIFF?

TIFF sau TIF, Tagged Image File Format, reprezintă imagini raster care sunt destinate utilizării pe o varietate de dispozitive care respectă acest standard de format de fișier. Este capabil să descrie date de imagine pe două niveluri, tonuri de gri, paletă-color și full-color în mai multe spații de culoare. Acceptă scheme de compresie cu pierderi, precum și fără pierderi, pentru a alege între spațiu și timp pentru aplicațiile care utilizează formatul. Formatul nu depinde de mașină și nu are limite precum procesorul, sistemul de operare sau sistemele de fișiere.

## Scurt istoric al formatului de fișier TIFF

Formatul de fișier TIFF a fost creat inițial de Aldus Corporation în toamna anului 1986, după o serie de întâlniri cu diverși producători de scanere și dezvoltatori de software. Scopul principal al formatului de fișier TIFF a fost de a oferi un format de fișier imagine scanat comun pentru toți furnizorii de scanere desktop. Începând cu suportul doar pentru formatul de imagine binar, formatul a evoluat către suportul imaginilor în tonuri de gri și color odată cu trecerea timpului. Versiunea inițială a specificațiilor de format de fișier TIFF poate fi etichetată ca Reivision 3.0, deoarece au existat două versiuni anterioare. O revizuire majoră 5.0 a fost publicată în 1988, care a adăugat suport pentru imagini color paletă și compresie LZW. Revizia 6.0 a formatelor de fișiere TIFF a fost publicată în 1992 după aceea. În 1994, Adobe Systems a achiziționat Aldus, iar specificațiile sunt acum disponibile și întreținute de Adobe Systems.

## Specificații de format de fișier TIFF

Formatul de fișier TIFF este extensibil și a suferit mai multe revizuiri care permit includerea unei cantități nelimitate de informații private sau cu scop special. Un fișier TIFF începe cu un antet de 8 octeți, unde octeții sunt numerici de la 0 la N. Cel mai mare fișier TIFF posibil are 2**32 de octeți lungime. Fișierul începe cu un antet de fișier imagine de 8 octeți care indică direct un fișier imagine (IFD). Un IFD conține informații despre imagine, precum și indicii către datele reale ale imaginii.

### Antet fișier TIFF

Antetul fișierului TIFF de 8 octeți conține următoarele informații:

**Octeți 0-1:** Ordinea octeților utilizată în fișier. Valorile legale sunt: „II”(4949.H)“MM” (4D4D.H).

În formatul „II”, ordinea octetilor este întotdeauna de la octetul cel mai puțin semnificativ până la octetul cel mai semnificativ, atât pentru numerele întregi de 16 biți, cât și pentru cele de 32 de biți. Aceasta se numește ordinea octetilor mici-endian. În formatul „MM”, ordinea octeților este întotdeauna de la cel mai semnificativ la cel mai puțin semnificativ, atât pentru numerele întregi pe 16 biți, cât și pe 32 de biți. Aceasta se numește ordinea octetilor big-endian.

**Octeții 2-3:** Un număr arbitrar, dar ales cu grijă (42), care identifică în continuare fișierul ca fișier TIFF. Ordinea octeților depinde de valoarea octeților 0-1.

**Bytes 4-7:** Offset (în octeți) a primului IFD. Directorul poate fi în orice locație din fișier după antet, dar trebuie să înceapă de la granița unui cuvânt. În special, un Director de fișiere de imagine poate urma datele de imagine pe care le descrie. Cititorii trebuie să urmeze indicatorii oriunde ar putea duce. Termenul offset de octeți este întotdeauna folosit în acest document pentru a se referi la o locație în ceea ce privește începutul fișierului TIFF. Primul octet al fișierului are un offset de 0.

### Director de fișiere imagine

Un IFD conține informații despre imagine, precum și indicatori către datele reale ale imaginii.. Constă dintr-un număr de 2 octeți a numărului de intrări în director (adică numărul de câmpuri), urmat de o secvență de intrări de câmp de 12 octeți , urmat de un offset de 4 octeți a următorului IFD (sau 0 dacă nu există). Trebuie să existe cel puțin 1 IFD într-un fișier TIFF și fiecare IFD trebuie să aibă cel puțin o intrare.

#### Intrare IFD

Fiecare intrare IFD de 12 octeți este în următorul format.


|Bytes|Descriere
---|---|
|0-1|Eticheta care identifică câmpul
|2-3|Tipul câmpului
|4-7|Numărul tipului indicat
|8-11|Decalajul valorii, decalajul fișierului (în octeți) al valorii pentru câmp. Se așteaptă ca valoarea să înceapă la granița unui cuvânt; Valoarea corespunzătoare va fi astfel un număr par. Acest decalaj al fișierului poate indica oriunde în fișier, chiar și după datele imaginii

Un câmp TIFF este o entitate logică constând din eticheta TIFF și valoarea acesteia. Acest concept logic este implementat ca o intrare IFD, plus valoarea reală dacă nu se încadrează în partea de valoare/offset, ultimii 4 octeți ai intrării IFD. Termenii câmp TIFF și intrare IFD sunt interschimbabili în majoritatea contextelor.

### TIFF de referință ###

TIFF de bază este nucleul TIFF, elementele esențiale pe care toți dezvoltatorii TIFF mainstream ar trebui să le susțină în produsele lor. Conformitatea cu formatul TIFF este supusă respectării cerințelor de bază TIFF. Aceste cerințe sunt bine documentate în documentul cu specificații 6.0.

#### Mai multe imagini per fișier ####

Este posibil să existe mai multe IFD într-un fișier TIFF. Fiecare IFD definește un subfișier. O posibilă utilizare a subfișierelor este de a descrie imagini înrudite, cum ar fi paginile unei transmisii prin fax. Un cititor TIFF de referință nu este necesar să citească niciun IFD în afară de primul.

#### Tipuri de imagini ####

Imaginea TIFF de bază are următoarele tipuri:

**Bilevel:** O imagine pe două niveluri conține două culori — alb și negru. TIFF permite unei aplicații să scrie date pe două niveluri fie într-un format alb-este-zero, fie în format negru-este-zero. Câmpul care înregistrează aceste informații se numește **PhotometricInterpretation**.

* RGB full-color

Informațiile de interpretare fotometrică pentru imaginile la nivel dublu sunt următoarele:

Etichetă = 262 (106.H)
Tip = SCURT
**Valori**

|Valoare|Descriere|
---|---|
|0|Pentru imagini în două niveluri și în tonuri de gri: 0 este imaginea albă. Valoarea maximă este reprezentată ca negru. Aceasta este valoarea normală pentru Compression#2|
|1|BlackIsZero. Pentru imagini în două niveluri și în tonuri de gri: 0 este imaginea neagră. Valoarea maximă este reprezentată ca alb. Dacă această valoare este specificată pentru Compression#2, imaginea ar trebui să fie afișată și imprimată invers.|

**GrayScale:** Imaginile în tonuri de gri sunt o generalizare a imaginilor pe două niveluri. Imaginile pe două niveluri pot stoca numai date de imagine alb-negru, dar imaginile în tonuri de gri pot stoca și nuanțe de gri. Pentru a descrie astfel de imagini, trebuie să adăugați sau să modificați următoarele câmpuri. Celelalte câmpuri obligatorii sunt aceleași cu cele necesare pentru imaginile pe două niveluri. Pentru imagini în tonuri de gri, Compression # 1 sau 32773 (PackBits). În Baseline TIFF, imaginile în tonuri de gri pot fi fie stocate ca date necomprimate, fie comprimate cu algoritmul PackBits.

Informațiile **BitsPerSample** pentru imaginile în tonuri de gri sunt următoarele:

Etichetă = 258 (102.H)
Tip = SCURT

Numărul de biți per componentă. Valorile permise pentru imaginile în tonuri de gri TIFF de bază sunt 4 și 8, permițând fie 16, fie 256 de nuanțe distincte de gri.

**Palette-Color:** Imaginile cu paletă de culori sunt similare cu imaginile în tonuri de gri. Au încă o componentă per pixel, dar valoarea componentei este utilizată ca index într-un tabel complet de căutare RGB. Pentru a descrie astfel de imagini, trebuie să adăugați sau să modificați următoarele câmpuri. Celelalte câmpuri obligatorii sunt aceleași cu cele pentru imaginile în tonuri de gri.
Informațiile de interpretare fotometrică pentru imaginea Palette-Color sunt după cum urmează:

PhotometricInterpretation = 3 (Palette Color).
ColorMapTag = 320 (140.H)
Tip = SCURT
N = 3 * (2 biți pe probă)

Acest câmp definește o hartă de culori Roșu-Verde-Albastru (denumită adesea tabel de căutare) pentru imaginile color din paletă. Într-o imagine de culoare paletă, o valoare de pixel este utilizată pentru a indexa într-un tabel de căutare RGB. De exemplu, un pixel de culoare paletă având o valoare de 0 ar fi afișat conform celui de-al 0-lea triplet roșu, verde, albastru. Într-o hartă de culori TIFF, toate valorile roșii vin pe primul loc, urmate de valorile de verde, apoi de valorile de albastru. În ColorMap, negrul este reprezentat de 0,0,0 și albul este reprezentat de 65535, 65535, 65535.

**RGB full-color:** într-o imagine RGB, fiecare pixel este format din trei componente: roșu, verde și albastru. Nu există ColorMap. Pentru a descrie o imagine RGB, trebuie să adăugați sau să modificați următoarele câmpuri și valori. Celelalte câmpuri obligatorii sunt aceleași cu cele necesare pentru imaginile cu culori paletă.

BitsPerSample = 8,8,8. Fiecare componentă are o adâncime de 8 biți într-o imagine TIFF RGB de bază.

PhotometricInterpretation = 2 (RGB) și nu există ColorMap.

Etichetă = 277 (115.H)
Tip = SCURT
Numărul de componente pe pixel. Acest număr este 3 pentru imaginile RGB, cu excepția cazului în care sunt prezente mostre suplimentare.

## Referințe ##

* [Format de fișier TIFF - Wikipedia](https://en.wikipedia.org/wiki/TIFF)

