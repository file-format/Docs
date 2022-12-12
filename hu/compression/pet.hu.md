{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PET fájlformátum - Puppy Linux telepítési csomagfájl",
  "description":"További információ a PET-fájlformátumról és az API-król, amelyek PET-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Mi az a Linux PET fájl?

A PET-fájl egy alkalmazástelepítő csomagfájl, amelyet a Linux operációs rendszer PuppyLinux változatával hoztak létre és használnak. Tömörített [TGZ](/hu/compression/tgz/) fájlként jön létre, amely csökkenti a tömörített archívum fájlméretét. A PET fájlformátum integritását az md5sum ellenőrző összeg biztosítja, amelyet a fájl végéhez csatolunk a távoli végén történő ellenőrzés céljából. A PET fájlok kibonthatók a szabványos TGZ fájlkibontó és a WinRAR segítségével. A PET-fájlok felváltották a régi [PUP](/hu/compression/pup/) csomagtelepítési fájlokat.

## PET fájl formátum

A PET-fájlok tömörített archívumként, bináris fájlformátumban kerülnek a lemezre. A PET fájlformátum belső fájlformátumának részletei azonban nem ismertek. Az [.exe](/hu/executable/exe/) és az [.msi](/hu/executable/msi/) csomagtelepítési fájlokhoz hasonlóan a PET-fájlok is elindítják a telepítést, amikor végrehajtják őket.

## Hivatkozások

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [PuppyLinux PET-csomagok indexe](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

