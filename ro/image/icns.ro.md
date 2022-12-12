{
  "date" : "2021-06-29",
  "keywords" :[ "ICNS", "extensie", "fișier", "format", "imagine", "Imagine pictogramă Apple", "macOS", "Apple", "pictogramă"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICNS - Imagine pictogramă Apple",
  "description":"Aflați despre formatul de fișier ICNS și despre API-urile care pot crea și deschide fișiere ICNS.",
  "linktitle" : "ICNS",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-06-29"
}

## Ce este un fișier ICNS? ##

Un format de pictogramă utilizat de programele macOS se numește fișier ICNS. Permite benzi alfa de 1 și 8 biți și salvează una sau mai multe imagini, de obicei realizate din documente [PNG](/ro/image/png). Pictograma programului din browserul și interfața macOS este afișată folosind fișiere ICNS.

În funcție de locație, aceeași pictogramă de stil poate avea mai multe setări. Formatul ICNS a suferit numeroase modificări și a evoluat până la punctul în care poate fi folosit acum ca bază pentru diferite formate compatibile. Iată câteva alte puncte importante pe care trebuie să le știți:

* IconFamily Resource, Macintosh Icon, Macintosh OS X Icon, Mac OS Icon, Apple Icon, Mac OS X Icon Resource și Mac OS icon Resource sunt câteva dintre celelalte nume.
* Pentru informații despre pictograme, se folosește o sursă din ramura de resurse.
* În cele mai multe cazuri, un fișier conține numeroase imagini. 1612 pixeli pătrați și 1024, 512, 256, 128, 48, 32 și 16 pixeli pătrați sunt dimensiunile de imagine acceptate.


## Format de fișier ICNS ##

Formatul de date ICNS este o capsulă pentru una sau mai multe imagini, care acceptă benzi de 1 bit și numeroase stări de imagine.
Sistemul de operare poate redimensiona imaginile pictogramelor pentru a se potrivi cu dimensiunea de afișare necesară. Imaginile cu pictograme mai mari sunt de obicei salvate ca fișiere [JPEG](/ro/image/jpeg/) 2000 sau [PNG](/ro/image/png). Este posibil un tip de fișiere ICNS comprimate și necomprimate.

Un antet și datele de pictogramă binare formează structura unui fișier ICNS. Antetul conține 8 octeți de date, dintre care patru sunt literalul magic și patru sunt lungimea fișierului. Tipul și dimensiunea fiecărei imagini pictograme sunt stocate în secțiunea de date pictograme, care este urmată de datele binare ale imaginii. Dimensiunea imaginii determină dimensiunea secțiunii binare.

## Specificatii tehnice ##

### Antet ###

|Offset|Mărime|Obiectiv
---|---|---|
|0|4|Literal magic, trebuie să fie „icns” (0x69, 0x63, 0x6e, 0x73)
|4|4|Lungimea fișierului, în octeți, mai întâi msb


### Date pictograme ###

|Offset|Mărime|Obiectiv
---|---|---|
|0|4|Tipul pictogramei
|4|4|Lungimea datelor, în octeți (inclusiv tip și lungime), mai întâi msb
|8|Variabilă|Datele pictogramei

### Compresie ###

Datele pixelilor sunt comprimate într-o oarecare măsură. Pixelii pe 32 de biți ("is32", "il32", "ih32", "it32") și ARGB ("ic04", "ic05") sunt adesea comprimați (pe canal) într-un mod similar cu PackBits.

|Valoare Lead|Tail Bytes|Rezultat (necomprimat)
---|---|---|
|0 - 127|1 - 128|1 - 128 octeți
|128 - 255|1 octet|3 - 130 de copii

## Referință ##

* [ICNS - Wikipedia](https://en.wikipedia.org/wiki/Apple_Icon_Image_format)

