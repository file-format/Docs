{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO – Format fișier imagine disc",
  "description":"Ce este un fișier ISO și API-uri care pot crea și deschide fișiere ISO.",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## Ce este un fișier ISO?

Un fișier cu extensia .iso este un fișier imagine de disc de arhivă necomprimat care reprezintă conținutul întregii date de pe un disc optic, cum ar fi CD sau DVD. Bazat pe standardul [ISO-9660](https://www.iso.org/standard/17505.html), formatul de fișier imagine ISO conține datele discului împreună cu informațiile despre sistemul de fișiere care sunt stocate în acesta. Capacitatea fișierelor ISO de a conține o replică exactă a conținutului îl face să fie tipul de fișier perfect pentru crearea de copii de CD-uri/DVD-uri și sunt utilizate în principal pentru a stoca date bootabile pentru instalare. De cele mai multe ori, fișierele ISO sunt arse pe USB/CD/DVD ca conținut bootabil pentru pornirea mașinii pentru instalare. Fișierele ISO au tip MIME application/x-iso9660-image.

## Format de fișier ISO

Formatul de fișier ISO nu este ca alte formate de fișiere container, deși arhivează conținutul specificat al datelor. Arhiva este creată ca fișier binar cu structura exactă a conținutului și informații despre sistemul de fișiere. Formatul de fișier ISO este descris de [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) după cum urmează.

### Structura de nivel superior a fișierului ISO

Structura generală a fișierului constă din:

* „Zona de sistem” - 32.768 de octeți și este neutilizată de ISO_9660
* `Zona de date` - constă dintr-un set de descriptori de volum și tabele, directoare și fișiere de cale

### Set de descriptori de volum

Zona de date începe cu setul de descriptori de volum, un set de unul sau mai mulți descriptori de volum terminat cu un terminator de set de descriptori de volum. Acestea acționează în mod colectiv ca un antet pentru zona de date, descriind conținutul acesteia (similar cu blocul de parametri BIOS utilizat de discurile formatate FAT, HPFS și NTFS).

Un set de descriptori de volum este prezentat mai jos.

|Setul de descriptori de volum|
---|
|Descriptor de volum #1|
|...|
|Descriptor de volum #N|
|Terminator de set de descriptori de volum|

#### Descriptor de volum

Fiecare descriptor de volum are o dimensiune de 2048 de octeți și are următoarea structură:

|Piesă |Tip |Identificator |Versiune |Date|
---|---|---|---|---|
|Dimensiune |1 octet |5 octeți (întotdeauna „CD001”) |1 octet (întotdeauna 0x01) |2.041 octeți|

## Referințe

* [Imagine de disc optic - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Semnături fișiere](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

