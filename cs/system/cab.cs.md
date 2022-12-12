{
  "date" : "2021-06-29",
  "keywords" :[ "CAB", "rozšíření", "soubor", "formát", "systém", "Windows Cabinet File", "Microsoft", "Installer", "SetUp", "AdvPak" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CAB - Windows Cabinet File",
  "description":"Další informace o formátu souboru CAB a rozhraních API, která mohou vytvářet a otevírat soubory CAB.",
  "linktitle" : "CAB",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## Co je soubor CAB? ##

Soubor s příponou .cab patří do souboru CAB systému Windows, který patří do kategorie systémových souborů. Jedná se o soubor, který je uložen ve formátu archivního souboru ve verzích systému Microsoft Windows, které podporují algoritmy komprimovaných dat, jako je [LZX](/cs/compression/lzx/), Quantum a [ZIP](/cs/compression/zip/ ). Soubor je životně důležitý, když chce uživatel nebo vývojář obsahovat a sdílet data a soubory instalace softwaru. Díky funkcím bezztrátové komprese dat a digitální certifikaci obsažené v těchto souborech je tento soubor ideální pro ukládání a sdílení takových souborů. Podporuje různé instalační programy společnosti Microsoft, jako je Device Installer, SetUp API a AdvPak.

## Stručná historie ##

Soubor CAB je typ souboru pro kompresi dat, který byl vyvinut společností Microsoft. Původně se nazýval „Diamant“, ale pak se stal populárně známým jako soubor CAB, zkratka pro slovo „Cabinet“

## Technická specifikace ##

Soubor CAB může obvykle obsahovat maximálně 65535 složek, z nichž každá může obsahovat maximálně 65536 souborů. Mechanismus ukládání souborů CAB je časově a prostorově nenáročný, protože ukládá každou složku jako komprimovaný blok namísto komprimace a ukládání každého souboru samostatně. Prázdné složky nelze ukládat do archivních složek CAB. Soubor CAB byl poprvé vyvinut společností Microsoft a používá se v různých instalačních programech, jako je InstallShield s mírně odlišným formátem. Soubory CAB jsou běžně připojeny k samorozbalovacím programům. Soubory Microsoft CAB jsou snadno rozpoznatelné díky jejich jedinečné značce, která pomáhá při identifikaci formátu. Jedinečnou značkou pro všechny soubory Microsoft CAB je čtyřslovná předpona, MSCF. Když uživatel uvidí tento kód, může snadno odlišit soubor Microsoft CAB od jiných souborů a podle toho jej použít v kompresorech nebo verzích. Soubory mohou být komprimovány s více daty instalací softwaru nebo mohou být současná data dekomprimována pomocí správného softwaru.


## Příklad CAB ##

Následující příklad ilustruje vztah mezi soubory a složkami ve struktuře souborů CAB:

{{< figure src="../cab.png" alt="Formát souboru CAB" >}}

## reference ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
