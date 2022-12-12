{
  "date" : "2022-03-02",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TGZ File - Gzipped Tar File",
  "description":"Další informace o formátu souboru TGZ a rozhraních API, která mohou vytvářet a otevírat soubory TGZ.",
  "linktitle" : "TGZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-02"
}

## Co je soubor TGZ?

Soubor s příponou .tgz je archivní soubor TAR sestávající z více souborů a složek, který byl komprimován pomocí komprimačního softwaru Gnu Zip (gzip). Soubor [TAR](/cs/compression/tar/) obvykle kombinuje více souborů do jednoho souboru pro zálohování nebo distribuci přes internet. Je to dekomprimovaný soubor, dokud není komprimován pomocí softwaru gzip, poté se stane souborem TGZ. Soubory TGZ jako komprimované soubory zabírají méně místa na disku a lze je snadno přenášet pomocí internetu prostřednictvím e-mailu. Některé aplikace, které mohou otevřít soubory TGZ, zahrnují WinZip, Apple Archive Utility, 7-Zip a WinRAR. Soubory TGZ se většinou používají v systémech UNIX a Linux.

## Formát souboru TGZ

Soubory TGZ se ukládají jako komprimované binární soubory pomocí kompresního algoritmu [GZ](/cs/compression/gz/).

## Jak rozbalit soubor .tgz na Linuxu

V OS Linux/Unix lze k rozbalení souborů TGZ z příkazového řádku použít následující příkaz.

```
tar zxvf tgzCompressedFile.tgz
```

Výše uvedený příkaz dekomprimuje komprimovaný soubor TGZ a extrahuje jeho soubory z archivu TAR na disk.
## Reference ##

* [TGS](https://core.telegram.org/animated_stickers)
* [gzip – Wikipedia](https://en.wikipedia.org/wiki/Gzip)

