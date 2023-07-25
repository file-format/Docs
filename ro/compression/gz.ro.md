{
  "date" : "2019-10-11",
  "keywords" :[ "fișier gz", "format fișier gz", "ce este un fișier gz", "fișier", "exemplu gz", "extensie fișier gz", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Format de fișier GZ - Fișier arhivă GNU Zipped",
  "description":"Aflați despre ce este un fișier GZ și API-urile care pot crea și deschide fișiere GZ.",
  "linktitle" : "GZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## Ce este un fișier GZ?

Un fișier GZ este o arhivă comprimată care este creată folosind algoritmul de compresie standard [gzip](https://en.wikipedia.org/wiki/Gzip) (GNU zip). Poate conține mai multe fișiere comprimate, directoare și stub-uri de fișiere. Acest format a fost dezvoltat inițial pentru a înlocui formatele de compresie pe sistemele UNIX. și este încă unul dintre cele mai comune tipuri de arhive pe sistemele Linux. Aplicații precum [WinZip](https://www.winzip.com/en/) pot deschide fișiere GZ pentru a-și vizualiza conținutul atât pe Windows, cât și pe MacOS.

## Format de fișier GZ - Mai multe informații

Gzip folosește algoritmul [DEFLATE](https://en.wikipedia.org/wiki/DEFLATE) pentru comprimarea arhivei și diferă de formatul de arhivă [ZIP](/ro/compression/zip/) în aplicarea algoritmului de compresie pe arhiva completă mai degrabă decât fișiere individuale. Specificațiile de format de fișier GZIP versiunea 4.3 publicate de Internet Engineering Task Force (IETF) conține informații detaliate despre formatul fișierului. Formatul de fișier este format din:

* Antet fișier
* Anteturi opționale
* Date comprimate
* Subsol fișier

## Antet fișier GZ ##

Antetul fișierului GZ este format din 10 octeți, după cum urmează:

|Offset|Dimensiune|Valoare|Descriere
---|---|---|---|
|0|2|0x1f 0x8b|Număr magic care identifică tipul de fișier
|2|1| |Metoda de compresie * 0-7 (Rezervat) * 8 (Dezumflare)
|3|1| |Fișier Steaguri
|4|4| |Amprenta temporală de 32 de biți
|8|1| |Drapele de compresie
|9|1| |ID sistem de operare

### Steaguri de fișiere ###

|Valoare|Identificator|Descriere
---|---|---|
|0x01|FTEXT|Dacă este setată, datele necomprimate trebuie tratate ca text în loc de date binare. Acest semnalizare indică conversia de final de linie pentru fișierele text pe mai multe platforme, dar nu o impune.
|0x02|FHCRC|Fișierul conține o sumă de control antet (CRC-16)
|0x04|FEXTRA|Fișierul conține câmpuri suplimentare
|0x08|FNAME|Fișierul conține un șir de nume de fișier original
|0x10|FCOMMENT|Fișierul conține comentarii
|0x20| |Rezervat
|0x40| |Rezervat
|0x80| |Rezervat

### Sistem de operare ###

|Valoare|Descriere
---|---|
|0|Sistem de fișiere FAT (MS-DOS, OS/2, NT/Win32)
|1|Amiga
|2|VMS (sau OpenVMS)
|3|Unix
|4|VM/CMS
|5|Atari TOS
|6|Sistem de fișiere HPFS (OS/2, NT)
|7|Macintosh
|8|Sistem Z
|9|CP/M
|10|TOPS-20
|11|Sistem de fișiere NTFS (NT)
|12|QDOS
|13|Gindă RISCOS
|255|necunoscut

## Anteturi opționale GZ ##

Anteturile suplimentare opționale sunt cele indicate de steagurile fișierului și includ informații precum numele original al fișierului, câmpuri suplimentare, comentarii și suma de verificare a antetului.

## Date comprimate ##

Această secțiune conține datele comprimate folosind algoritmul de compresie DEFLATE.

## Subsol fișier GZ ##

Subsolul fișierului are o dimensiune de 8 octeți și conține următoarele informații.

|Offset|Dimensiune|Descriere
---|---|---|
|0|4|Suma de control (CRC-32)
|4|4|Valoare necomprimată a dimensiunii datelor în octeți

## Referințe ##

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)
* [RFC1952: specificația formatului fișierului GZIP](https://datatracker.ietf.org/doc/html/rfc1952), de la IETF.

