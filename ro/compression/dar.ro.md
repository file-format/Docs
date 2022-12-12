{
  "date" : "2021-04-08",
  "keywords" :[ "fișier dar", "format fișier dar", "ce este un fișier dar", "fișier", "exemplu dar", "extensie fișier dar", "extensie", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Format de fișier pentru arhivarea discurilor",
  "description":"Aflați despre formatul de fișier DAR și despre API-urile care pot crea și deschide fișiere DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Ce este un fișier DAR?

Un fișier cu extensia .dar este o arhivă comprimată creată folosind arhiva DAR Disk. Poate crea backup/arhivă pentru un disc complet sau un grup de fișiere. A fost creat pentru a înlocui formatul de fișier [TAR](/ro/compression/tar/) pe sistemul de operare UNIX și poate fi creat ca fișiere de arhivă divizate pentru un număr mare de fișiere. Arhiva DAR acceptă opțiunea de ștergere a fișierelor din sistem care sunt legate la fișierele principale din arhivă. Capacitățile sale de a oferi backup diferențial, incremental și decremental îl fac superior fișierelor TAR.

## Format de fișier DAR

Fișierele DAR sunt arhive comprimate care pot utiliza orice compresie per fișier, cum ar fi [gzip](/ro/compression/gz/), [bzip2](/ro/compression/bz2/), lzo, xz sau lzma. Formatul exact al fișierului DAR depinde de tipul de formatare utilizat pentru a comprima conținutul arhivei. De asemenea, permite criptarea opțională Blowfish, Twofish, AES, Serpent, Camellia și criptarea și semnătura cu cheie publică (OpenPGP).

### Caracteristici DAR

Unele dintre caracteristicile formatului de fișier DAR sunt următoarele.

* Se ocupă de orice tip de inod (director, fișiere simple, legături simbolice, dispozitive speciale, conducte denumite, prize, uși, ...)
* Se ocupă de inoduri cu legături rigide (fișiere simple legate de hard, dispozitive char, dispozitive de blocare, linkuri simbolice hard linkate)
* Are grijă de fișierele rare
* Are grijă de atributele extinse ale fișierului Linux,
* Are grijă de fișierul Linux ACL
* Se ocupă de furcăturile de fișiere Mac OS X
* Are grijă de unele atribute specifice sistemului de fișiere, cum ar fi Data nașterii sistemului de fișiere HFS+ și atributele imuabile, jurnalizarea datelor, ștergerea securizată, fuziunea fără coadă, neștergibile, atributele noatime ale sistemului de fișiere ext2/3/4.
* Compresie pe fișier cu gzip, bzip2, lzo, xz sau lzma (spre deosebire de comprimarea întregii arhive). O persoană poate alege să nu comprima fișierele deja comprimate pe baza sufixului numelui de fișier.
* Extragerea rapidă a fișierelor de oriunde în arhivă
* Listare rapidă a conținutului arhivei prin salvarea catalogului de fișiere din arhivă
* Copiere de rezervă live a sistemului de fișiere: detectează când un fișier a fost modificat în timp ce a fost citit pentru backup și poate reîncerca să-l salveze până la un anumit număr maxim de încercări
* Fișier hash (MD5, SHA1 sau SHA-512) generat din mers pentru fiecare felie, fișierul rezultat este compatibil cu md5sum sau sha1sum, pentru a putea verifica rapid integritatea fiecărei felii
* Independent de sistemul de fișiere: poate fi folosit pentru a restabili un sistem pe o partiție de dimensiune diferită și/sau pe o partiție cu un sistem de fișiere diferit[5]

## Referințe

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

