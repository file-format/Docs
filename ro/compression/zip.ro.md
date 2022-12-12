{
  "date" : "2019-12-09",
  "keywords" :[ "fișier zip", "format fișier zip", "ce este un fișier zip", "fișier", "exemplu zip", "extensie fișier zip", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ZIP",
  "description":"Ce este un fișier ZIP și API-urile care pot crea și deschide fișiere ZIP.",
  "linktitle" : "ZIP",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## Ce este un fișier ZIP? ##

Un fișier cu extensia .zip este o arhivă care poate deține unul sau mai multe fișiere sau directoare. Arhiva poate avea compresie aplicată fișierelor incluse pentru a reduce dimensiunea fișierului ZIP. Formatul fișierului ZIP a fost făcut public încă din februarie 1989 de Phil Katz pentru a realiza arhivarea fișierelor și folderelor. Formatul a fost făcut parte din utilitarul [PKZIP](https://www.pkware.com/pkzip), creat de PKWARE, Inc. Imediat după disponibilitatea [specificațiilor disponibile](https://pkware.cachefly.net/ webdocs/casestudies/APPNOTE.TXT), multe companii au făcut ca formatul de fișier ZIP să facă parte din utilitatile lor software, inclusiv Microsoft (din Windows 7), Apple (Mac OS X) și multe altele.

## Scurt istoric al formatului de fișier ZIP

Istoricul formatului de fișier ZIP datează de la evenimentul procesului lansat de System Enhancement Associates (SEA) împotriva PKWARE pentru utilizarea utilitarului său ARC fără permisiuni pentru marca sa comercială și drepturile de autor asupra aspectului produsului și a interfeței cu utilizatorul. Înainte de aceasta, Phil Katz a rescris codul sursă al SEA și a lansat PKXARC, un extractor ARC și PKARC, un compresor de fișiere, ca program gratuit pentru sistemele bazate pe MS-DOS. Pierzând în proces, PKWARE nu a mai putut folosi nimic legat de ARC. Aici a apărut crearea unei noi compresii de fișiere, numită ZIP, care a fost făcută parte din utilitarul PKZIP la PKWARE, Inc.

Katz a lansat specificațiile de format de fișier ZIP în domeniul public, păstrând în același timp drepturile de proprietate asupra utilitarului său de comprimare și extragere, adică PKZIP. Sistemul de compresie ZIP a fost (și este) capabil să arhiveze fișiere într-un folder prin intermediul unui algoritm de verificare a redundanței ciclice pe 32 de biți ([CRC](http://en.wikipedia.org/wiki/Cyclic_redundancy_check)) pentru a comprima fișierul dimensiuni. Spre deosebire de ARC, folderele .ZIP includeau un fișier director care juca rolul unei cărți de coduri a unui criptograf, deținând informațiile necesare pentru a reda fișierele comprimate.

## Metode de compresie acceptate în ZIP

Conform specificațiilor de format de fișier .ZIP, sunt acceptate următoarele metode de compresie.

* Store - nu implică compresie
* Se micsoreaza
* Reducere (Acest lucru implică factori de compresie variind de la nivelul 1 la nivelul 4)
* Implozie
* Dezumflați
* Deflat64
* BZIP2
* LZMA (EFS)
* WavPack
* PPMd versiunea I, Rev 1

DEFLATE este metoda de compresie folosită în mod obișnuit, care este un algoritm de comprimare a datei fără pierderi care utilizează o combinație de codare LZ77 și Huffman și este detaliată în [RFC 1951](https://tools.ietf.org/html/rfc1951).

## Specificații pentru formatul fișierului ZIP

Fișierele ZIP au capacitatea de a stoca mai multe fișiere folosind tehnici de compresie diferite, în timp ce în același timp acceptă stocarea unui fișier fără nicio compresie. Fiecare fișier este stocat/comprimat individual, ceea ce ajută la extragerea lor sau adăugarea altora noi, fără a aplica compresie sau decompresie întregii arhive.

### Format general de fișier ZIP

Fiecare fișier Zip este structurat în felul următor:


|ZIP Format de fișier
---|
| Antetul fișierului local 1
|Fișier de date 1
|Descriptor de date 1
| Antetul fișierului local 2
|Fișier de date 2
|Descriptor de date 2
| ....
| ....
| Antetul fișierului local N
|Fișier de date N
|Descriptor de date N
| Antet de decriptare arhivă
|Arhivați înregistrarea datelor suplimentare
|Directorul central

Formatul de fișier ZIP folosește algoritmul CRC pe 32 de biți pentru arhivare. Pentru a reda fișierele comprimate, o arhivă ZIP deține la capătul ei un director care păstrează intrarea fișierelor conținute și locația acestora în fișierul arhivă. Astfel, joacă rolul de codificare pentru încapsularea informațiilor necesare pentru a reda fișierele comprimate. Cititoarele ZIP folosesc directorul pentru a încărca lista de fișiere fără a citi întreaga arhivă ZIP. Formatul păstrează copii duble ale structurii directoarelor pentru a oferi o mai mare protecție împotriva pierderii de date.

Fiecare fișier dintr-o arhivă ZIP este reprezentat ca o intrare individuală, unde fiecare intrare constă dintr-un antet de fișier local urmat de datele fișierului comprimat. Directorul de la sfârșitul arhivei deține referințele la toate aceste intrări de fișier. Cititoarele de fișiere ZIP ar trebui să evite citirea antetelor fișierelor locale și tot felul de liste de fișiere ar trebui să fie citite din Director. Acest Director este singura sursă pentru intrări de fișiere valide în arhivă, deoarece fișierele pot fi adăugate și spre sfârșitul arhivei. De aceea, dacă un cititor citește anteturile locale ale unei arhive ZIP de la început, poate citi intrări nevalide (șterse), precum și acelea care nu fac parte din Directorul care este șters din arhivă.

Ordinea intrărilor de fișiere din directorul central nu trebuie să coincidă cu ordinea intrărilor de fișiere din arhivă.

### Intrări în fișierul ZIP

Intrările în fișierul ZIP sunt aranjate una după alta, unde fiecare intrare constă din:

* Antet fișier local
* Câmpuri de date suplimentare opționale
* Date utilizator (opțional comprimate/opțional criptate)

Antetul fișierului local al fiecărei intrări reprezintă informații despre fișier, cum ar fi comentariul, dimensiunea fișierului și numele fișierului. Câmpurile de date suplimentare (opțional) pot găzdui informații pentru opțiunile de extensibilitate ale formatului ZIP.

#### Antet fișier local

Antetul fișierului local are o structură de câmp specifică, constând din valori multi-octeți. Toate valorile sunt stocate în ordinea octeților little-endian unde lungimea câmpului numără lungimea în octeți. Toate structurile dintr-un fișier ZIP folosesc semnături de 4 octeți pentru fiecare intrare de fișier. Sfârșitul semnăturii directorului central este 0x06054b50 și poate fi distins folosind propria semnătură unică. Următoarea este ordinea informațiilor stocate în Antetul fișierului local.


|Offset|Bytes|Descriere
---|---|---|
|0|4|Semnătura antet fișierului local # 0x04034b50 (citit ca un număr little-endian)
|4|2|Versiunea necesară pentru extragere (minimum)
|6|2|Pavilion de biți de uz general
|8|2|Metoda compresiei
|10|2|Ora ultimei modificări ale fișierului
|12|2|Data ultimei modificări a fișierului
|14|4|CRC-32
|18|4|Dimensiune comprimată
|22|4|Dimensiune necomprimată
|26|2|Lungimea numelui fișierului (n)
|28|2|Lungimea câmpului suplimentară (m)
|30|n|Numele fișierului
|30+n|m|Câmp suplimentar

#### Antet fișier director central


|Offset|Bytes|Descriere
---|---|---|
|0|4|Semnătura antetului fișierului director central # 0x02014b50
|4|2|Versiune realizată de
|6|2|Versiunea necesară pentru extragere (minimum)
|8|2|Pavilion de biți de uz general
|10|2|Metoda compresiei
|12|2|Ora ultimei modificări ale fișierului
|14|2|Data ultimei modificări a fișierului
|16|4|CRC-32
|20|4|Dimensiune comprimată
|24|4|Dimensiune necomprimată
|28|2|Lungimea numelui fișierului (n)
|30|2|Lungimea câmpului suplimentară (m)
|32|2|Lungimea comentariului fișierului (k)
|34|2|Numărul discului de unde începe fișierul
|36|2|Atribute interne ale fișierului
|38|4|Atribute de fișiere externe
|42|4|Decalajul relativ al antetului fișierului local. Acesta este numărul de octeți dintre începutul primului disc pe care apare fișierul și începutul antetului fișierului local. Acest lucru permite software-ului să citească directorul central pentru a localiza poziția fișierului în interiorul fișierului ZIP.
|46|n|Numele fișierului
|46+n|m|Câmp suplimentar
|46+n+m|k|Comentariu la fișier

#### Sfârșitul înregistrării directorului central


|Offset|Bytes|Descriere
---|---|---|
|0|4|Sfârșitul semnăturii directorului central # 0x06054b50
|4|2|Numărul acestui disc
|6|2|Discul de unde începe directorul central
|8|2|Numărul de înregistrări din directorul central de pe acest disc
|10|2|Numărul total de înregistrări din directorul central
|12|4|Dimensiunea directorului central (octeți)
|16|4|Decalajul începutului directorului central, în raport cu începutul arhivei
|20|2|Lungimea comentariului (n)
|22|n|Comentariu

## Referințe

* [Specificații de format de fișier PKWARE ZIP](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [Structura fișierului PKZip](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)

