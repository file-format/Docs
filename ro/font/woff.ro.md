{
  "date" : "2020-08-20",
  "keywords" :[ "fișier Woff", "format fișier Woff", "ce este un fișier woff", "fișier", "exemplu Woff", "extensie fișier Woff", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WOFF – Web Open File Format",
  "description":"Un fișier WOFF este un format de font deschis creat în formatul Web Open Font.",
  "linktitle" : "WOFF",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-09-30"
}

## Ce este un fișier WOFF?

Un fișier cu extensia .woff este un fișier de font web bazat pe Web Open Font Format (WOFF). Are un container comprimat specific formatului, bazat pe tipuri de fonturi TrueType (.TTF) sau OpenType (.OTT). WOFF a fost introdus cu scopul de a diferenția fonturile web de fișierele cu fonturi utilizate în aplicațiile desktop. În plus, formatul vizează reducerea latenței transferului de fonturi de la server la computerul clientului prin rețea. Sunt disponibile mai multe instrumente care pot converti fișierele WOFF în TTF și alte formate de fișiere cu fonturi.

## **Format fișier WOFF**

Formatul de font WOFF comprimă tabelele de date ale fonturilor din structurile sfnt bazate pe tabel utilizate în diferite tipuri de fonturi, cum ar fi TrueType, OpenType și Open Font Format. Este ca un container pentru aceste tipuri de fonturi și are, de asemenea, spațiu pentru a include metadatele fontului și datele de utilizare privată pentru a fi incluse în container. Convertizorii folosesc fișierele sfnt într-un fișier formatat WOFF, iar agenții utilizator restaurează fișierul codificat pentru a fi utilizat cu documentul web. Trebuie remarcat faptul că datele de font restaurate se potrivesc exact cu formatul fontului de intrare din toate punctele de vedere.

Utilitarele fișierelor WOFF conțin adesea caracteristici suplimentare, cum ar fi subsetarea glifelor, validarea sau adăugarea de caracteristici de font, dar nu este necesar. Atât creatorul, cât și agenții de utilizare trebuie să se asigure că este păstrată valabilitatea datelor fontului de bază.

### Structura fișierului WOFF

Structura fișierului WOFF este similară cu cea a fonturilor sfnt. Se bazează pe un director de tabel care conține lungimile și decalajele pentru fiecare tabel cu date de font. Toate tabelele sunt urmate după aceste informații inițiale. Fișierul conține baza de date de fonturi care sunt aceleași ca în fonturile originale. Ordinea tabelelor este, de asemenea, aceeași, dar fiecare poate fi comprimată. Directorul tabelului WOFF înlocuiește directorul tabelului original.

Un fișier WOFF este format din următoarele:

* WOFFHeader - Antetul fișierului cu tipul de font și versiunea de bază, împreună cu decalaje ale metadatelor și blocurilor de date private.
* TableDirectory - Director de tabele cu fonturi, indicând dimensiunea originală, dimensiunea comprimată și locația fiecărui tabel în fișierul WOFF.
* FontTables - Tabelele cu date de font din fontul sfnt de intrare, comprimate pentru a reduce cerințele de lățime de bandă.
* ExtendedMetadata - Un bloc opțional de metadate extinse, reprezentate în format XML și comprimate pentru stocare în fișierul WOFF.
* PrivateData- Un bloc opțional de date private pe care să îl folosească designerul de fonturi, turnatoriul sau furnizorul.

### Antet WOFF
Antetul WOFF constă dintr-o semnătură de identificare care indică tipul de date incluse în fișier. Antetul WOFF împreună cu câmpurile sale sunt după cum urmează.

|Tip|Nume câmp|Descriere|
---|---|---|
|UInt32|semnătură |0x774F4646 'wOFF' |
|UInt32| aromă |„Versiunea sfnt” a fontului de intrare.|
|UInt32| lungime |Dimensiunea totală a fișierului WOFF.|
|UInt16| numTables |Numărul de intrări din directorul tabelelor cu fonturi.|
|UInt16| rezervat |Rezervat; pus la zero.|
|UInt32| totalSfntSize |Dimensiunea totală necesară pentru datele fonturilor necomprimate, inclusiv antetul sfnt, directorul și tabelele cu fonturi (inclusiv padding).|
|UInt16| majorVersion |Versiunea majoră a fișierului WOFF.|
|UInt16| minorVersion |Versiune minoră a fișierului WOFF.|
|UInt32| metaOffset |Decalaj către blocul de metadate, de la începutul fișierului WOFF.|
|UInt32| metaLength |Lungimea blocului de metadate comprimate.|
|UInt32| metaOrigLength |Dimensiunea necomprimată a blocului de metadate.|
|UInt32| privOffset |Decalaj către blocul de date private, de la începutul fișierului WOFF.|
|UInt32| privLength |Lungimea blocului de date private.|


## **Referințe**
* [W3 WOFF File Format](https://www.w3.org/TR/WOFF/)

