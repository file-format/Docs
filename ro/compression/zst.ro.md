{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Fișier ZST - Format de fișier comprimat Zstandard",
  "description":"Aflați despre formatul de fișier ZST și despre API-urile care pot crea și deschide fișiere ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-ro",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Ce este un fișier ZST?

Un fișier ZST este un fișier comprimat care este generat cu algoritmul de compresie Zstandard (zstd). Este un fișier comprimat care este creat cu compresie fără pierderi de către algoritm. Fișierele ZST pot fi utilizate pentru a comprima diferite tipuri de fișiere, cum ar fi baze de date, sisteme de fișiere, rețele și jocuri. Standardul Z este guvernat de [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878) care descrie mecanismul general de compresie, tipul media și codificarea conținutului.

## Format de fișier ZST

Fișierele ZST sunt stocate în format de fișier comprimat pe disc. Mecanismul de compresie este așa cum este descris de RFC 8878, care depășește RFC 8478.

## Cadre ZST

Un fișier ZST este format din unul sau mai multe cadre. Fiecare cadru poate fi fie un cadru Zstandard, fie un cadru ignorabil. Un cadru Zstandard conține date comprimate, în timp ce un cadru care poate fi ignorat conține metadate personalizate ale utilizatorului.

### Z cadru standard

Un cadru Zstandard are următoarea structură.

|Câmp|Dimensiune în octeți|
---|---|
|Număr_Magic |4 octeți|
|Frame_Header |2-14 bytes|
|Data_Block |n bytes|
|[Mai multe_blocuri de date] ||
|[Suma de control_conținut] |4 octeți|

### Cadru ignorabil

Un cadru care poate fi ignorat permite inserarea metadatelor definite de utilizator într-un flux de cadre concatenate. Structura unui cadru care poate fi ignorat este următoarea.

|Număr_Magic |Dimensiune_cadru |Date_utilizator|
---|---|---|
|4 bytes |4 bytes |n bytes|

## Referințe ##

* [RFC 8878 Zstandard Compresie](https://www.rfc-editor.org/rfc/rfc8878)


