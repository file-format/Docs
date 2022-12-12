{
  "date" : "2021-04-08",
  "keywords" :[ "dar fájl", "dar fájlformátum", "mi az a dar fájl", "fájl", "dar példa", "dar fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Lemezarchiváló fájlformátum",
  "description":"További információ a DAR fájlformátumról és az API-król, amelyek DAR fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## Mi az a DAR fájl?

A .dar kiterjesztésű fájl a DAR Disk archívum használatával létrehozott tömörített archívum. Biztonsági mentést/archívumot tud készíteni a teljes lemezről vagy fájlok csoportjáról. Létrehozták a [TAR](/hu/compression/tar/) fájlformátum helyettesítésére UNIX OS rendszeren, és felosztott archív fájlként hozható létre nagyszámú fájl számára. A DAR archívum támogatja a fájlok törlését a rendszerből, amelyek az archívum fő fájljaihoz kapcsolódnak. A differenciális, növekményes és dekrementális biztonsági mentési képessége felülmúlja a TAR fájlokat.

## DAR fájlformátum

A DAR fájlok tömörített archívumok, amelyek bármilyen fájlonkénti tömörítést használhatnak, például [gzip](/hu/compression/gz/), [bzip2](/hu/compression/bz2/), lzo, xz vagy lzma. A DAR-fájlok pontos fájlformátuma attól függ, hogy milyen típusú formázást használnak az archívum tartalmának tömörítésére. Lehetővé teszi az opcionális Blowfish, Twofish, AES, Serpent, Camellia titkosítást, valamint a nyilvános kulcsú titkosítást és aláírást (OpenPGP).

### DAR jellemzők

A DAR fájlformátum néhány funkciója a következő.

* Gondoskodik bármilyen típusú inode-ról (könyvtár, egyszerű fájlok, szimbolikus hivatkozások, speciális eszközök, elnevezett csövek, aljzatok, ajtók, ...)
* Gondoskodik a kemény linkekkel összekapcsolt inode-okról (keményhivatkozású sima fájlok, char eszközök, blokkeszközök, merev hivatkozások)
* Gondoskodik a ritka fájlokról
* Gondoskodik a Linux fájl kiterjesztett attribútumairól,
* Gondoskodik a Linux fájl ACL-ről
* Gondoskodik a Mac OS X fájlvillákról
* Gondoskodik néhány fájlrendszer-specifikus attribútumról, mint például a HFS+ fájlrendszer születési dátuma, valamint az ext2/3/4 fájlrendszer megváltoztathatatlan, adatnaplózó, biztonságos törlés, farok-összevonás nélküli, nem törölhető, noatime attribútumok.
* Fájlonkénti tömörítés gzip, bzip2, lzo, xz vagy lzma segítségével (a teljes archívum tömörítésével szemben). Az egyén dönthet úgy, hogy nem tömöríti a már tömörített fájlokat a fájlnév utótagja alapján.
* Fájlok gyors kibontása az archívum bárhonnan
* Az archívum tartalmának gyors listázása a fájlok katalógusának az archívumban való elmentésével
* Élő fájlrendszer biztonsági mentés: észleli, ha egy fájl módosult, miközben azt biztonsági mentés céljából olvasta, és újra megpróbálhatja elmenteni egy adott maximális számú újrapróbálkozásig
* Minden szelethez menet közben generált hash fájl (MD5, SHA1 vagy SHA-512), az eredményül kapott fájl kompatibilis az md5sum vagy sha1sum fájlokkal, hogy gyorsan ellenőrizni tudja az egyes szeletek integritását
* Fájlrendszertől független: a rendszer visszaállítására használható egy eltérő méretű partícióra és/vagy egy másik fájlrendszerű partícióra[5]

## Hivatkozások

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

