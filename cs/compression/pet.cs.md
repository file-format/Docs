{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru PET - soubor instalačního balíčku Puppy Linux",
  "description":"Další informace o formátu souborů PET a rozhraních API, která mohou vytvářet a otevírat soubory PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## Co je to soubor Linux PET?

Soubor PET je soubor instalačního balíčku aplikace vytvořený a používaný s variantou operačního systému Linux PuppyLinux. Je vytvořen jako komprimovaný soubor [TGZ](/cs/compression/tgz/), který zmenšuje velikost souboru komprimovaného archivu. Integrita formátu souboru PET je zajištěna kontrolním součtem md5sum, který je připojen na konec souboru pro ověření na vzdáleném konci. Soubory PET lze extrahovat pomocí standardního extraktoru souborů TGZ a WinRAR. Soubory PET nahradily staré instalační soubory balíčku [PUP](/cs/compression/pup/).

## Formát souboru PET

Soubory PET se ukládají na disk jako komprimované archivy v binárním formátu souboru. Podrobnosti o interním formátu souboru ve formátu PET však nejsou známy. Podobně jako u instalačních souborů balíčků [.exe](/cs/executable/exe/) a [.msi](/cs/executable/msi/), soubory PET zahájí instalaci po svém spuštění.

## Reference

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Index PET balíčků PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

