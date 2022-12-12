{
  "date" : "2021-08-17",
  "keywords" :[ "fișier udf", "format fișier udf", "ce este un fișier udf", "fișier", "exemplu udf", "extensie fișier udf", "extensie", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Aflați despre formatul de fișier UDF și despre API-urile care pot crea și deschide fișiere UDF.",
  "title" :"UDF – Fișier format universal disc",
  "linktitle" : "UDF",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-17"
}

## Ce este un fișier UDF?
Fișierul cu extensia .udf este un format de imagine de disc utilizat de obicei pentru salvarea fișierelor pe suporturi optice; poate fi folosit pentru a inscripționa DVD-uri, CD-uri și alte medii optice; stochează o colecție de fișiere folosind structura de directoare specificată în standardul UDF; permite ștergerea și modificarea fișierelor de pe discul țintă chiar și după ce au fost scrise. Optical Storage Technology Association a stabilit sistemul de fișiere UDF ca standard pentru a forma un sistem de fișiere comun pentru toate mediile optice, cum ar fi mediile optice re-inscriptibile și mediile de numai citire.

## Format de fișier UDF
Formatul de fișier UDF este un sistem de fișiere deschis, neutru de furnizor, pentru stocarea datelor de pe computer pentru o gamă largă de medii. A fost folosit în mod obișnuit pentru DVD-uri și formate mai noi de discuri optice. De obicei, software-ul stăpânește un sistem de fișiere UDF într-un proces batch și îl scrie pe suportul optic într-o singură trecere. Cu toate acestea, atunci când scrie pachete pe medii reinscriptibile, UDF permite crearea, ștergerea și modificarea fișierelor pe disc similar cu un sistem de fișiere de uz general pe medii amovibile, cum ar fi unități flash sau dischete.
### Specificații UDF
Standardul UDF definește următoarele trei variante ale sistemului de fișiere:

- **Plain Build**: Acesta este formatul original acceptat în toate versiunile UDF. A fost introdus în prima versiune a standardului, acest format poate fi folosit pe orice tip de disc care permite accesul aleatoriu de citire sau scriere, cum ar fi DVD+RW, hard disk-uri și suporturi DVD-RAM.
- **TVA build**: Folosit special pentru scrierea pe medii de scriere o singură dată. TVA-ul este o structură suplimentară pe disc care permite scrierea pachetelor; adică remaparea blocurilor fizice atunci când fișierele sau alte date de pe disc sunt modificate sau șterse. Pentru mediile de scriere o singură dată, întregul disc este virtualizat, făcând transparentă natura scrisului o dată pentru utilizator; discul poate fi tratat în același mod în care s-ar trata un disc reinscriptibil.
- **Spared (RW) build**: Folosit special pentru scrierea pe medii reinscriptibile. Se adaugă un tabel de rezervă suplimentar pentru a gestiona defecțiunile care vor apărea în cele din urmă pe părțile discului care au fost rescrise de mai multe ori. Acest tabel salvează evidența sectoarelor uzate și le remapează la cele funcționale. Managementul defectelor UDF nu se aplică sistemelor care implementează deja o altă formă de management al defectelor, cum ar fi Mount Rainier (MRW) pentru discuri optice sau un controler de disc pentru un hard disk.
 




## Referințe


* [Format Windows Imaging - de Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


