{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Soubor STR - dBASE Structure List Object File - Co je soubor .str a jak jej otevřít?",
  "description" : "Přečtěte si o STR dBASE Structure List Object File a jak jej otevřít.",
  "linktitle" : "STR",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-str-cs",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## Co je soubor STR?

Formát souboru STR je běžně spojován s dBASE, systémem správy databází. V dBASE soubor .str obvykle představuje soubor objektu seznamu struktur. Tento soubor obsahuje strukturu databázové tabulky včetně informací o polích (sloupcích) a jejich vlastnostech.

Soubor objektů seznamu struktur (.str) obsahuje metadata, jako jsou názvy polí, datové typy, délky polí a jakékoli další vlastnosti spojené s každým polem v databázové tabulce. Slouží k definování struktury databázové tabulky bez obsahu aktuálních datových záznamů.

Programy jako dBASE nebo jiné nástroje pro správu databází mohou tento soubor využít k pochopení uspořádání databázové tabulky a provádění operací, jako je dotazování, aktualizace nebo vytváření nových záznamů na základě této struktury.

Zde je základní příklad toho, co může soubor STR obsahovat:

```
Field Name    Type      Length
-----------   ------    ------
ID            Numeric   5
Name          Character 30
Age           Numeric   3
DOB           Date
```

Tento příklad popisuje tabulku se čtyřmi poli: ID, Name, Age a DOB spolu s jejich příslušnými datovými typy a délkami.

## Jak otevřít soubor STR?

Primárním způsobem otevření souborů .str je použití samotného dBASE, zejména v operačních systémech Windows. dBASE je schopen číst a interpretovat obsah těchto souborů, což uživatelům umožňuje prohlížet a pracovat s databázovou strukturou.

Protože soubory .str jsou v podstatě prosté textové soubory, které obsahují informace o struktuře databáze, můžete je otevřít také pomocí textového editoru. Příklady textových editorů zahrnují Microsoft Notepad na Windows a Apple TextEdit na Mac. Po otevření v textovém editoru budete moci vidět obsah souboru, včetně názvů polí, datových typů a dalších strukturálních informací, ve formátu čitelném pro člověka.

## Reference
* [dBase](https://en.wikipedia.org/wiki/DBase)


