{
  "date" : "2022-12-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor ZST - Zstandardní formát komprimovaného souboru",
  "description":"Přečtěte si o formátu souboru ZST a rozhraních API, která mohou vytvářet a otevírat soubory ZST.",
  "linktitle" : "ZST",
  "menu" : {
    "docs" : {
      "identifier":"compression-zst-cs",
      "parent" : "compression"
}
},
  "lastmod" : "2022-12-26"
}

## Co je soubor ZST?

Soubor ZST je komprimovaný soubor, který je generován pomocí kompresního algoritmu Zstandard (zstd). Jedná se o komprimovaný soubor, který je algoritmem vytvořen bezeztrátovou kompresí. Soubory ZST lze použít ke kompresi různých typů souborů, jako jsou databáze, systémy souborů, sítě a hry. Zstandard se řídí [RFC 8878](https://www.rfc-editor.org/rfc/rfc8878), který popisuje celkový mechanismus komprese, typ média a kódování obsahu.

## Formát souboru ZST

Soubory ZST se ukládají na disk ve formátu komprimovaného souboru. Mechanismus komprese je popsán v dokumentu RFC 8878, který zastarává RFC 8478.

## Rámy ZST

Soubor ZST se skládá z jednoho nebo více snímků. Každý snímek může být buď Zstandardní snímek, nebo přeskočitelný snímek. Rámeček Zstandard obsahuje komprimovaná data, zatímco přeskočitelný rámec obsahuje uživatelská metadata.

### Standardní rám

Rám Zstandard má následující strukturu.

|Pole|Velikost v bajtech|
---|---|
|Magic_Number |4 bajty|
|Frame_Header |2-14 bajtů|
|Datový_blok |n bajtů|
|[Více datových_bloků] ||
|[Kontrolní součet obsahu] |4 bajty|

### Přeskočitelný snímek

Přeskočitelný snímek umožňuje vkládání uživatelem definovaných metadat do toku zřetězených snímků. Struktura přeskočitelného rámce je následující.

|Magic_Number |Frame_Size |User_Data|
---|---|---|
|4 bajty |4 bajty |n bajtů|

## Reference ##

* [RFC 8878 Zstandardní komprese](https://www.rfc-editor.org/rfc/rfc8878)


