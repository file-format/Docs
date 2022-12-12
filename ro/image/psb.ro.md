{
  "date" : "2019-10-11",
  "keywords" :[ "fișier psb", "format fișier psb", "ce este un fișier psb", "fișier", "exemplu psb", "extensie fișier psb", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSB - Format de fișier imagine mare Photoshop",
  "description":"Aflați despre formatul de fișier PSB și despre API-urile care pot crea și deschide fișiere PSB.",
  "linktitle" : "PSB",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier PSB?
Adobe Photoshop salvează fișierele în două formate. Fișierele cu dimensiunea de 30.000 x 30.000 pixeli sunt salvate cu extensia PSD, iar fișierele mai mari decât PSD până la 300.000 x 300.000 pixeli sunt salvate cu extensia PSB cunoscută sub numele de „Photoshop Big”. Mai precis, fișierele PSB pot fi de până la 4 EB (peste 4,2 miliarde GB) cu imagini care au o înălțime și lățime de până la 300.000 de pixeli. PSD-urile, pe de altă parte, pot avea maximum 2 GB și dimensiunile imaginii de 30.000 de pixeli.

PSB este cunoscut și ca dimensiune de format mare pentru Photoshop și acceptă toate caracteristicile Photoshop, cum ar fi straturi, efecte și filtre. Photoshop poate converti fișierul PSB în [PSD](/ro/image/psd/), [JPG](/ro/image/jpeg/) , [PNG](/ro/image/png/), [EPS](/ro/page-description-language/eps/), [GIF](/ro/image/gif/) și alte formate. Formatul de document mare Photoshop este disponibil odată ce caracteristica panoului de gestionare a fișierelor din caseta de dialog de preferințe Photoshop este activată.

## Informații despre formatul fișierului ##

Formatul de fișier Photoshop este împărțit în cinci părți majore, cu mulți marcatori de lungime pentru a vă deplasa între secțiuni.

|Format de fișier
---|
| Antet fișier
|Datele modului de culoare
| Resurse de imagine
|Informații despre strat și mască
|(((
Date de imagine
)))

### Antet fișier ###

Antetul fișierului are o lungime fixă de 26 de octeți și conține proprietățile de bază ale imaginii.

Semnătura BYTE [4] – Egal cu „8BPS”.

Versiunea WORD [2] – Numărul versiunii, PSD # 1, PSB # 2.

BYTE Rezervat [6] – Rezervat și întotdeauna zero.

Canale WORD [2] – Numărul de canale de culoare din imagine, inclusiv canalele alfa. Valoarea sa variază de la 1 la 56.

LONG Rows [4] – Înălțimea imaginii în pixeli, PSD 1-30.000, PSB 1-300.000.

LONG Columns [4] – Lățimea imaginii în pixeli, PSD 1-30.000, PSB 1-300.000.

WORD Depth [2] – Număr de biți pe canal. Valorile acceptate sunt 1,8,16 și 32.

WORD Mode [2] – Modul Color al fișierului.

#### Descrierea modului ####


|Modul|Descriere
---|---|
|0|Bitmap (monocrom)
|1|Scara de gri
|2|Indexat
|3|RGB
|4|CMYK
|7|Multicanal
|8|Duoton (semitonuri)
|9|Labor

### Date mod culoare ###

După secțiunea antet fișierului urmează secțiunea de date pentru modul de culoare. Blocul începe cu un număr LONG care dă lungimea blocului în octeți. Structura datelor modului de culoare este după cum urmează:

4 octeți – lungimea următoarelor date de culoare.

Variabilă – Date de culoare

Dacă valoarea câmpului de mod din secțiunea antet nu este Culoare indexată sau duoton, lungimea blocului va fi 0 și nu vor exista date după câmpul de lungime.

Pentru imaginile color indexate, lungimea va fi de 768 de octeți, care va conține o paletă de 256 de culori. Pentru duoton, datele vor conține parametrii ecranului și alte informații conexe.

### Resurse de imagine ###

După secțiunea de date pentru modul de culoare, al treilea bloc este secțiunea de resurse de imagine. Primii patru octeți sunt un număr LUNG care specifică lungimea blocului urmat de o serie de blocuri de resurse. Structura blocului de resurse imagine este următoarea:

Tip BYTE [4] – Semnătura „8BIM”

WORD ID [2] – ID resursă imagine. Există o listă de ID-uri de resurse care poate fi văzută din linkul de referință.

BYTE Nume [Variable] – Nume: șir Pascal cu lungime pară. ** **

LONG Size [4] – Dimensiunea reală a datelor despre resurse care urmează.

BYTE Data [Variabilă} – Date despre resurse. Este căptușită pentru a face dimensiunea uniformă.

Unele dintre formatele de resurse sunt explicate pe scurt mai jos:

**Format de resurse grilă și ghiduri:** informațiile grilă și ghiduri sunt stocate în blocul de resurse. Aceste blocuri de resurse conțin grilă de 16 octeți și antet ghid, urmate de blocuri de 5 octeți de informații ghid.

**Format resursă miniaturi:** Informațiile miniaturii sunt stocate în blocul de resurse de imagine pentru afișarea previzualizării, care constă dintr-un antet de 28 de octeți și o miniatură JFIF în RGB.

**Format de resurse pentru eșantionare de culoare:** Informațiile de eșantionare de culoare sunt stocate în blocul de resurse de imagine cu un antet de 8 octeți urmat de un bloc cu lungime variabilă de informații despre mostrele de culoare.

### Informații despre strat și mască ###

Al patrulea bloc este blocul de informații despre straturi și măști și conține informații despre straturi și măști. Informațiile layer sunt stocate mai întâi și apoi informațiile masca.

**Informații despre strat:** informațiile despre strat încep cu o valoare LONG, care arată lungimea informațiilor despre strat. După aceea, există un număr de valori WORD care arată numărul de înregistrări de strat de urmat.

[8] – lungimea straturilor

[2] – Număr de straturi

[Variabilă] – Informații despre fiecare strat.

[Variabilă] – Date imagini ale canalului.** **

**Informații despre mască:** Structura măștii are următorul format:


|Structura datelor|Numele câmpului| Descriere
---|---|---|
|CUVANT| Suprapunerea spațiului de culoare| (Nedocumentat)
|BYTE[8]| Componente de culoare| Componente de culoare de 4x2 octeți
|CUVANT| Opacitate| 0#transparent, 1#opac
|BYTE| Amabil| 0#inversat, 1#protejat, 128#utilizați valoarea stocată
|BYTE| căptușeală| setat la zero

### Date imagine ###

Ultima secțiune conține datele pixelilor imaginii. Datele imaginii sunt stocate ca o serie de secvențe în planuri, adică mai întâi toate datele roșii, apoi toate datele verzi etc. WORD la începutul fiecărei linii arată dimensiunea în octeți aferentă fiecărei linii de scanare.

[2] – Metoda de compresie:

[Variabilă] – Date de imagine în ordine plană, adică RRRR, GGGG, BBBB etc.

Metode de compresie:

0 – Raw Date de imagine

1 – RLE comprimat

2 – Zip fără predicție

3 – Zip cu pronostic

## Referință ##

* [Format de fișier PSB - de Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)
* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

