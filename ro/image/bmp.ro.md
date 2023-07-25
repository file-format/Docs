{
  "date" : "2019-10-11",
  "keywords" :[ "fișier bmp", "format fișier bmp", "ce este un fișier bmp", "fișier", "exemplu bmp", "extensie fișier bmp", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"BMP - Format fișier imagine",
  "description":"Aflați despre formatul de fișier BMP și despre API-urile care pot crea și deschide fișiere BMP.",
  "linktitle" : "BMP",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

# Ce este un fișier BMP? #

Fișierele cu extensia .BMP reprezintă fișiere Bitmap Image care sunt utilizate pentru a stoca imagini digitale bitmap. Aceste imagini sunt independente de adaptorul grafic și sunt numite și format de fișier bitmap independent de dispozitiv (DIB). Această independență are scopul de a deschide fișierul pe mai multe platforme, cum ar fi Microsoft Windows și Mac. Formatul de fișier BMP poate stoca date ca imagini digitale bidimensionale atât în format monocrom, cât și în format color, cu diferite adâncimi de culoare.

## Specificații pentru formatul fișierului BMP ##

Bitmapurile independente de dispozitiv acționează ca un ajutor pentru schimbul de bitmaps între dispozitive și aplicații. Datorită evoluției continue a acestui format de fișier, informațiile conținute în anteturi pot fi diferite în funcție de versiunea Bitmap. Un singur fișier bitmap constă din structuri fixe și de dimensiuni variabile într-o anumită secvență.

Structurile dintr-un fișier Bitmap sunt aranjate în următoarea ordine:


|Structură|Opțional|Dimensiune|Scop
---|---|---|---|
|Antul fișierului|Nr|14|Pentru a stoca informații generale despre fișierul imagine bitmap
|DIB Header|No|Fixed-Size|Pentru a stoca informații detaliate despre imaginea bitmap și a defini formatul pixelilor
|Măști de biți suplimentari|Da|12 sau 16 octeți|Pentru a defini formatul pixelilor
|Paletă de culori|Semi-opțional|Dimensiune variabilă|Pentru a defini culorile utilizate de datele imaginii bitmap
|Gap1|Da|Variable-size|Alinierea structurii
|Matrice de pixeli|Nu|Dimensiune variabilă|Formatul pixelului este definit de antetul DIB sau de măștile de biți suplimentari.
|Gap2|Da|Variable-size|Alinierea structurii
|Profil de culoare ICC|Da|Dimensiune variabilă|Pentru a defini profilul de culoare pentru gestionarea culorilor

Când o imagine bitmap este încărcată în memorie, aceasta devine o structură DIB, utilizată de Windows prin intermediul API-ului său GDI. Antetul fișierului nu face parte din această structură de date. Culoarea poate consta, de asemenea, din intrări de 16 biți care constituie indecși pentru paleta la care se face referire în prezent, în loc de definiții explicite de culoare RGB. Să aruncăm o privire la unele dintre acestea în detaliu, în special la antete.

### Antet fișier bitmap ###

Un antet de fișier bitmap este similar cu alte anteturi de fișiere utilizate pentru a identifica fișierul. Deoarece există diferite variante ale formatului de fișier BMP, primii 2 octeți ai formatului de fișier BMP sunt caracterul „B” și apoi caracterul „M” în codificare ASCII. Toate valorile întregi sunt stocate în format little-endian.

|Offset hex|Offset dec|Dimensiune|Scop
---|---|---|---|
|00|0|2 octeți|Câmpul antet utilizat pentru a identifica fișierul BMP și DIB este 0x42 0x4D în hexazecimal, la fel ca BM în ASCII. Poate urmări valorile posibile.* **BM** – Windows 3.1x, 95, NT, ... etc. * **BA** – matrice de bitmap OS/2 * **CI** – OS/2 struct pictogramă culoare * **CP** – indicator de culoare OS/2 const * **IC** – pictogramă OS/2 struct * **PT** – indicator OS/2
|02|2|4 octeți|Mărimea fișierului BMP în octeți
|06|6|2 octeți|Rezervat; valoarea reală depinde de aplicația care creează imaginea
|08|8|2 octeți|Rezervat; valoarea reală depinde de aplicația care creează imaginea
|0A|10|4 octeți|Decalajul, adică adresa de pornire, a octetului în care pot fi găsite datele imaginii bitmap (matrice de pixeli).

#### Antet DIB (antet informații bitmap) ####

Informațiile detaliate despre imagine sunt reprezentate de acest antet. Pe baza acestor informații, se va determina aplicația care va fi utilizată pentru afișarea imaginii pe ecran. Toate astfel de anteturi conțin un câmp DWORD (32 de biți), care specifică dimensiunea lor, astfel încât o aplicație să poată determina cu ușurință antetul folosit în imagine. Acest lucru se datorează în principiu faptului că formatul DIB a suferit mai multe extensii. Urmează antetul DIB cu câmpurile enumerate.

#### Paleta de culori ####

O paletă de culori BMP este o serie de structuri care specifică valorile intensității RGB ale fiecărei culori din paleta de culori a unui dispozitiv de afișare. Fiecare pixel din datele bitmap stochează o singură valoare folosită ca index în paleta de culori. Informațiile de culoare stocate în elementul la acel index specifică culoarea acelui pixel. Disponibilitatea culorii într-un fișier bitmap variază după cum urmează:

* Unul, 4 și 8 biți - se așteaptă să conțină întotdeauna o paletă de culori
* Șaisprezece, 24 și 32 de biți - nu conține niciodată palete de culori
* Fișiere BMP de șaisprezece și 32 de biți - conțin valori de masca pentru câmpuri de biți în locul paletei de culori

#### Stocare pixeli ####

Pixelii bitmap sunt stocați ca biți împachetați în rânduri în care dimensiunea fiecărui rând este rotunjită la un multiplu de 4 octeți (un DWORD pe 32 de biți) prin completare. Cantitatea totală de octeți necesari pentru a stoca pixelii unei imagini nu poate fi calculată direct prin doar numărarea biților. Deoarece este implicată umplutura, este necesar efectul de rotunjire a dimensiunii fiecărui rând la un multiplu de 4 octeți. Octeții de completare (nu neapărat 0) trebuie atașați la sfârșitul rândurilor pentru a crește lungimea rândurilor la un multiplu de patru octeți. Când matricea de pixeli este încărcată în memorie, fiecare rând trebuie să înceapă de la o adresă de memorie care este un multiplu de 4.

Imaginea este de fapt descrisă de reprezentarea DWORD pe 32 de biți a matricei de pixeli. De obicei, pixelii sunt stocați „de jos în sus”, începând din colțul din stânga jos, mergând de la stânga la dreapta și apoi rând cu rând de jos în sus al imaginii. Formatele pixelilor și implicațiile lor sunt enumerate mai jos:

* Formatul de 1 bit per pixel (1bpp) acceptă 2 culori distincte, (de exemplu: alb-negru).
* Formatul de 2 biți per pixel (2bpp) acceptă 4 culori distincte și stochează 4 pixeli pe 1 octet, pixelul din stânga fiind în cei doi biți cei mai semnificativi. Fiecare valoare de pixel este un index de 2 biți într-un tabel de până la 4 culori.
* Formatul de 4 biți per pixel (4bpp) acceptă 16 culori distincte și stochează 2 pixeli pe 1 octet, pixelul cel mai din stânga aflându-se în nibble-ul mai semnificativ. Fiecare valoare de pixel este un index de 4 biți într-un tabel de până la 16 culori.
* Formatul de 8 biți per pixel (8bpp) acceptă 256 de culori distincte și stochează 1 pixel pe 1 octet. Fiecare octet este un index într-un tabel de până la 256 de culori.
* Formatul de 16 biți per pixel (16 bpp) acceptă 65536 de culori distincte și stochează 1 pixel pe 2 octeți WORD. Fiecare CUVENT poate defini mostrele alfa, rosu, verde si albastru ale pixelului.
* Formatul de pixeli de 24 de biți (24 bpp) acceptă 16.777.216 de culori distincte și stochează valoarea de 1 pixel pe 3 octeți. Fiecare valoare a pixelului definește mostrele roșii, verzi și albastre ale pixelului (8.8.8.0.0 în notația RGBAX). Mai exact, în ordinea: albastru, verde și roșu (8 biți pentru fiecare probă).
* Formatul pe 32 de biți per pixel (32 bpp) acceptă 4.294.967.296 de culori distincte și stochează 1 pixel pe 4 octeți DWORD. Fiecare DWORD poate defini mostrele alfa, roșu, verde și albastru ale pixelului.

## Referințe ##

* [Windows MetaFile Format](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-wmf/4813e7fd-52d0-4f42-965f-228c8b7488d2)
* [Format de fișier BMP](https://en.wikipedia.org/wiki/BMP_file_format)

