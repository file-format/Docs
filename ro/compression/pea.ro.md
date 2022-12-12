{
  "date" : "2021-04-21",
  "keywords" :[ "fișier de mazăre", "format de fișier de mazăre", "ce este un fișier de mazăre", "fișier", "exemplu de mazăre", "extensie fișier mazăre", "extensie", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PEA – PeaZip Archive File Format",
  "description":"Aflați despre formatul de fișier PEA și despre API-urile care pot crea și deschide fișiere PEA.",
  "linktitle" : "PEA",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-21"
}

## Ce este un fișier PEA?

Un fișier cu extensia .pea, acronim pentru Pack, Encrypt și Authenticate, este o arhivă [zip](/ro/compression/zip/) creată cu aplicația software de arhivare [PeaZip](https://peazip.github.io/). Dispune de compresie și de ieșire cu mai multe volume și oferă un model de securitate flexibil prin criptare și criptare autentificată. Acest lucru asigură atât confidențialitatea, cât și autentificarea datelor. Utilitarul PeaZip este disponibil ca motor open-source care poate fi compilat pentru diferite sisteme de operare, conform cerințelor.

## Format de fișier PEA

[Specificațiile formatului fișierului PEA](https://peazip.github.io/pea_help.pdf) sunt disponibile public pentru referință de către dezvoltatori. Arhivele PEA sunt fișiere binare cu model de securitate flexibil și verificări de integritate redundante, de la sume de control până la hashuri criptografic puternice. Aceasta definește trei niveluri diferite de comunicare de controlat:

* Fluxuri - fluxul real de date de ieșire care este format din mai multe fișiere de intrare și poate fi scris scris pe mai multe volume de ieșire
* Obiecte - fișiere de intrare și foldere trimise la arhiva .pea
* Volume - fișier arhivă de ieșire care poate fi extins la dimensiunea definită de utilizator

Fiecare dintre acestea sunt opționale și pot fi încorporate în funcție de cerințele utilizatorului. Formatul de fișier PEA poate stoca un singur flux care conține obiecte nelimitate. Fiecare flux are o dimensiune de până la 2^64 de octeți.

Fișierele PEA oferă opțional verificarea integrității și criptare autentificată folosind AES în modul EAX sau HMAC, alternativ Twofish și Serpent în modul EAX.

### Antet arhivă PEA

Antetul arhivei are 10 octeți și este structurat după cum urmează.

|Octeți|Descriere|
---|---|
|1 | Câmp de octeți magici pentru dezambiguizarea formatului de fișier: $EA|
|1 | Numărul versiunii|
|1 | Numărul revizuirii|
|1 | Schema de control al volumului|
|1 | Declararea sistemului de operare unde a fost construit fluxul|
|1 | Se declară codificarea datei și orei OS|
|1 | Declararea numelui obiectelor codificarea caracterelor|
|1 | Declararea tipului CPU (codificat pe 7 biți) și endianness (în msb)|
|1 | Rezervat pentru utilizare viitoare|

## Referințe

* [Specificații de format de fișier PEA](https://peazip.github.io/pea_help.pdf)
* [Format fișier PEA](https://peazip.github.io/pea-file-format.html#.pea_specifications)

