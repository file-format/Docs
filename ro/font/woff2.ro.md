{
  "date": "2023-01-10",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Fișier WOFF2 - Fișier Web Open Font Format 2.0",
  "description": "Aflați despre ce este un fișier WOFF2 și API-urile care pot crea și deschide fișierul WOFF2.",
  "linktitle": "WOFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-woff-ro2"
}
},
  "lastmod": "2023-01-10"
}

## Ce este un fișier WOFF2?

WOFF2 este un format de fișier de font care este o versiune mai comprimată a Web Open Font Format (WOFF). A fost dezvoltat ca o modalitate de a reduce dimensiunea fișierelor fonturilor web, permițându-le să se încarce mai rapid și să utilizeze mai puțină lățime de bandă. WOFF2 folosește un algoritm de compresie numit Brotli pentru a comprima datele fonturilor, ceea ce poate duce la dimensiuni de fișiere semnificativ mai mici decât fonturile [WOFF](/font/woff/) echivalente. Acest format este acceptat de majoritatea browserelor web moderne, inclusiv Chrome, Firefox, Safari, Opera și Edge (versiunea 14 în continuare).

## Format de fișier WOFF2 - Mai multe informații

Structura internă a fișierului unui fișier de font WOFF2 este compusă din mai multe părți diferite, inclusiv un antet, metadate, un director de tabel și datele fontului în sine.

 1. Antetul conține informații despre formatul general al fișierului, inclusiv numărul versiunii și numărul de tabele care sunt prezente în fișier.

 1. Secțiunea de metadate conține informații precum numele fontului, drepturile de autor și alte informații legate de font.

 1. Directorul tabelelor conține informații despre diferitele tabele care alcătuiesc fontul, inclusiv locația lor în fișier și lungimea lor.

 1. Datele fontului în sine sunt împărțite în mai multe tabele diferite, fiecare dintre acestea conținând informații specifice despre font, cum ar fi caracterele acestuia și glifele corespunzătoare. Aceste tabele pot include:

 * Tabelul glyf” conține contururile reale ale fontului, inclusiv forma și dimensiunea fiecărui caracter.
 * Tabelul head” conține informații generale despre font, cum ar fi numărul versiunii sale, dimensiunea designului și așa mai departe.
 * Tabelul hmtx” conține informații despre valorile fontului, inclusiv lățimile și pozițiile caracterelor.
 * Fiecare tabel este comprimat și stocat în format de fișier WOFF2 după ce a finalizat procesul de codificare.

Structura generală este concepută pentru a permite analizarea și decodarea rapidă, astfel încât browserele web să poată încărca și afișa rapid și eficient fontul pe un site web.

### Antet WOFF2
Antetul WOFF constă dintr-o semnătură de identificare care indică tipul de date incluse în fișier. Antetul WOFF împreună cu câmpurile sale sunt după cum urmează.

|Tip|Nume câmp|Descriere|
---|---|---|
|UInt32|semnătură |0x774F4632 'wOF2' |
|UInt32| aromă |Versiunea sfnt” a fontului de intrare.|
|UInt32| lungime |Dimensiunea totală a fișierului WOFF.|
|UInt16| numTables |Numărul de intrări din directorul tabelelor cu fonturi.|
|UInt16| rezervat |Rezervat; pus la zero.|
|UInt32| totalSfntSize |Dimensiunea totală necesară pentru datele fonturilor necomprimate, inclusiv antetul sfnt, directorul și tabelele cu fonturi (inclusiv padding).|
|UInt32| totalCompressedSize Lungimea totală a blocului de date comprimate.|
|UInt16| majorVersion |Versiunea majoră a fișierului WOFF.|
|UInt16| minorVersion |Versiune minoră a fișierului WOFF.|
|UInt32| metaOffset |Decalaj către blocul de metadate, de la începutul fișierului WOFF.|
|UInt32| metaLength |Lungimea blocului de metadate comprimate.|
|UInt32| metaOrigLength |Dimensiunea necomprimată a blocului de metadate.|
|UInt32| privOffset |Decalaj către blocul de date private, de la începutul fișierului WOFF.|
|UInt32| privLength |Lungimea blocului de date private.|


## Referințe
 * [Format fișier W3 WOFF2](https://www.w3.org/TR/WOFF2/)

