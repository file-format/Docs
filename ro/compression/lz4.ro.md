{
  "date" : "2021-04-08",
  "keywords" :[ "fișier lz4", "format fișier lz4", "ce este un fișier lz4", "fișier", "exemplu lz4", "extensie fișier lz4", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ4 - LZ4 Format de fișier comprimat",
  "description":"Aflați despre formatul de fișier LBR și despre API-urile care pot crea și deschide fișiere LZ4.",
  "linktitle" : "LZ4",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Ce este un fișier LZ4?

Un fișier cu extensia .lz4 este un fișier de arhivă comprimat creat cu aplicații/utilități care acceptă compresia [LZ4](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm)). Algoritmul LZ4 se concentrează pe compromisul între viteză și raportul de compresie. Arhivele LZ4 comprimate pot fi create folosind utilitarul de linie de comandă LZ4 și pot fi decomprimate folosind același lucru.

## Format de fișier LZ4

Formatul de fișier LZ4, bazat pe algoritmul de compresie LZ4, este independent de tipul CPU, sistemul de operare, sistemul de fișiere și setul de caractere. Este potrivit pentru compresia fișierelor și compresia în flux folosind algoritmul LZ4. Implementarea inițială a formatului LZ4 a fost realizată în limbajul [C](/ro/programming/c/) de Yann Collet în 2011 și este disponibilă pentru referința dezvoltatorului pe [Github](https://github.com/lz4/lz4) .

### Format cadru LZ4

Structura generală a formatului de fișier LZ4 este prezentată mai jos.

|MagicNb|F. Descriptor| Block|(...)|EndMark |C. Sumă de control|
---|---|---|---|---|---|
|4 octeți| 3-15 octeți||| 4 octeți| 0-4 octeți|

#### Număr magic

4 octeți, format Little Endian. Valoare: 0x184D2204

#### Descriptor de cadru

Descriptorul de cadru constă din 3 t0 15 octeți și este cea mai importantă parte a specificațiilor. Împreună, câmpurile Magic_Number și Frame_Descriptor sunt denumite LZ4 Frame Header, iar dimensiunea acestuia variază între 7 și 19 octeți. Este așa cum se arată mai jos.

|FLG| BD| (Dimensiunea conținutului)| (ID dicționar)| HC|
---|---|---|---|---|
|1 octet| 1 octet| 0 - 8 octeți| 0 - 4 octeți| 1 octet|

#### Blocuri de date

Fiecare bloc de date urmează următoarea ordine.

|Dimensiunea blocului| date| (Block Checksum)|
---|---|---|
|4 octeți| |0 - 4 octeți|

#### EndMark

Fluxul de blocuri se termină când ultimul bloc de date este urmat de valoarea de 32 de biți 0x00000000.

#### Sumă de verificare a conținutului

Content_Checksum verifică validitatea conținutului care este decodat corect și este realizat folosind rezultatul algoritmului xxHash-32. Validează rezultatele transmiterii cu succes a tuturor blocurilor în ordinea corectă și fără nicio eroare.

## Referințe

* [LZ4 Frame Format](https://github.com/lz4/lz4/blob/dev/doc/lz4_Frame_format.md)
* [Algoritm de compresie LZ4 - Wikipedia](https://en.wikipedia.org/wiki/LZ4_(compression_algorithm))

