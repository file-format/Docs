{
  "date" : "2022-01-23",
  "keywords" :[ "xz-fil", "filformat", "vad är en xz-fil", "fil", "xz-exempel", "xz filtillägg", "tillägg", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XZ-fil - XZ-komprimerat arkiv",
  "description":"Läs mer om XZ-filformat och API:er som kan skapa och öppna XZ-filer.",
  "linktitle" : "XZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-01-23"
}

## Vad är XZ fil?

XZ är ett komprimerat filformat som använder LZMA2-komprimeringsalgoritmen. Den designades som en ersättning för de populära formaten gzip och bzip2 och erbjuder ett antal fördelar jämfört med dessa äldre standarder. XZ-filer stöds väl på många plattformar och kan dekomprimeras snabbt och enkelt. Även om de inte är lika vanliga som [ZIP](/sv/compression/zip/)- eller [RAR](/sv/compression/rar/)-filer, kan XZ-arkiv användas för att lagra stora mängder data utan att offra komprimeringskvaliteten. Om du behöver komprimera eller dekomprimera stora filer är filtillägget XZ värt att överväga.

## XZ filformat

XZ-filer genereras och sparas som binära filer på skiva. Den använder LZMA-algoritmen för att komprimera data och kan uppnå ett komprimeringsförhållande på upp till 50 %. XZ-filer används vanligtvis för programvarudistributioner och säkerhetskopieringsarkiv. De kan dekomprimeras med hjälp av XZ-verktyget, som ingår i de flesta Linux-distributioner.

## Packa upp XZ-filer på Linux/Unix

För att packa upp XZ-filer, installera först `xz-utils`-paketet:
```
$ sudo apt-get install xz-utils
```

Använd kommandot `unxz` för att extrahera .xz-filer:
```
$ unxz compressed_xz_file.xz
```

eller använda med --decompress alternativet XZ:
```
$ xz --decompress compressed_xz_file.xz
```

## Referenser

* [XZ Utils](https://en.wikipedia.org/wiki/XZ_Utils)

