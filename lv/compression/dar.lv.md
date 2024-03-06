{
  "date": "2021-04-08",
  "keywords": [
"dar fails",
"dar faila formāts",
"kas ir dar fails",
"failu",
"dar piemērs",
"dar faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DAR — diska arhivētāja faila formāts",
  "description": "Uzziniet par DAR faila formātu un API, kas var izveidot un atvērt DAR failus.",
  "linktitle": "DAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-da-lvr"
}
},
  "lastmod": "2021-04-09"
}

## Kas ir DAR fails?

Fails ar paplašinājumu .dar ir saspiests arhīvs, kas izveidots, izmantojot DAR diska arhīvu. Tas var izveidot dublējumu / arhīvu pilnam diskam vai failu grupai. Tas tika izveidots, lai aizstātu [TAR](/compression/tar/) faila formātu UNIX OS, un to var izveidot kā sadalītus arhīva failus lielam skaitam failu. DAR arhīvs atbalsta iespēju dzēst failus no sistēmas, kas ir saistīti ar galvenajiem failiem arhīvā. Tās iespējas nodrošināt diferenciālo, pakāpenisko un dekrementālo dublējumu padara to pārāku par TAR failiem.

## DAR faila formāts

DAR faili ir saspiesti arhīvi, kuros var izmantot jebkuru failu saspiešanu, piemēram, [gzip](/compression/gz/), [bzip2](/compression/bz2/), lzo, xz vai lzma. Precīzs DAR faila faila formāts ir atkarīgs no tā, kāda veida formatējums tiek izmantots, lai saspiestu arhīva saturu. Tas nodrošina arī izvēles Blowfish, Twofish, AES, Serpent, Camellia šifrēšanu un publiskās atslēgas šifrēšanu un parakstu (OpenPGP).

### DAR funkcijas

Dažas no DAR faila formāta funkcijām ir šādas.

 * Rūpējas par jebkura veida inode (direktorijs, vienkārši faili, simboliskās saites, īpašas ierīces, nosauktas caurules, kontaktligzdas, durvis, ...)
 * Rūpējas par cietajām saitēm (cieti saistītiem vienkāršiem failiem, char ierīcēm, blokierīcēm, cieši saistītām simbolu saitēm)
 * Rūpējas par retajiem failiem
 * Rūpējas par Linux faila paplašinātajiem atribūtiem,
 * Rūpējas par Linux failu ACL
 * Rūpējas par Mac OS X failu dakšām
 * Rūpējas par dažiem failu sistēmai raksturīgiem atribūtiem, piemēram, HFS+ failu sistēmas dzimšanas datums un ext2/3/4 failu sistēmas nemainīgajiem, datu žurnālu, drošas dzēšanas, bezastes sapludināšanas, neizdzēšamiem, noatime atribūtiem.
 * Failu saspiešana ar gzip, bzip2, lzo, xz vai lzma (pretstatā visa arhīva saspiešanai). Persona var izvēlēties nesaspiest jau saspiestos failus, pamatojoties uz viņu faila nosaukuma sufiksu.
 * Ātra failu izvilkšana no jebkuras vietas arhīvā
 * Ātra arhīva satura uzskaitīšana, saglabājot failu katalogu arhīvā
 * Tiešsaistes failu sistēmas dublējums: nosaka, kad fails ir mainīts, kamēr tas tika lasīts dublēšanai, un var mēģināt to atkārtoti saglabāt līdz noteiktam maksimālajam atkārtojumu skaitam
 * Jaukšanas fails (MD5, SHA1 vai SHA-512), kas tiek ģenerēts lidojumā katrai daļai, iegūtais fails ir saderīgs ar md5sum vai sha1sum, lai varētu ātri pārbaudīt katras šķēles integritāti.
 * Neatkarīga no failu sistēmas: to var izmantot, lai atjaunotu sistēmu cita izmēra nodalījumā un/vai nodalījumā ar citu failu sistēmu[5]

## Atsauces

* [DAR](http://dar.linux.free.fr/)

* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))


