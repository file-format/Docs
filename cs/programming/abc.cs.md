
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript Byte Code File",
  "description":"Zjistěte, co je formát souboru ABC s příklady a rozhraními API, která mohou vytvářet a otevírat soubory ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Co je soubor ABC?

Soubor s příponou .abc je soubor bajtového kódu jazyka ActionScript vytvořený kompilátorem Flash jako výsledek kompilace souborů skriptu jazyka ActionScript. Bajtový kód obsažený v souboru ABC je spuštěn virtuálním strojem ActionScript (AVM a AVM2). Bytový kód se skládá z konstantních dat, instrukcí z instrukční sady AVM2 a různých druhů metadat. Když je soubor ABC načten do AVM nebo AVM2, prochází ověřením. Pokud neodpovídá Přehledu AVM2, bude zamítnut. Soubory ABC lze otevřít v přehrávači Adobe Flash Player, který byl již dávno ukončen.

## Formát souboru ABC – Další informace

Soubory ABC se ukládají na disk v binárním formátu souboru, který lze číst virtuálními stroji AVM nebo AVM2. Jeho vnitřní struktura souborů představuje spustitelný blok kódu se všemi jeho konstantními daty, deskriptory typů, kódem a metadaty.

## Struktura souboru ABC

Struktura souboru ABC je uvedena níže.

```
abcFile  
{
           u16        minor_version                
           u16        major_version                
           cpool_info        constant_pool                
           u30        method_count                
           method_info        method[method_count]                
           u30        metadata_count                
           metadata_info        metadata[metadata_count]                
           u30        class_count                
           instance_info        instance[class_count]                
           class_info        class[class_count]                
           u30        script_count                
           script_info        script[script_count]               
           u30        method_body_count                
           method_body_info        method_body[method_body_count]        
}
```

### Pole souboru ABC

|Název pole|Popis|
---|---|
|minor_version, major_version|Hodnoty major_version a minor_version jsou čísla hlavní a vedlejší verze formátu abcFile.|
|constant_pool|Constant_pool je struktura s proměnnou délkou složená z celých čísel, dvojic, řetězců, jmenných prostorů, sad jmenných prostorů a více jmen.|
|method_count, method|Hodnota ofmethod_count je počet položek v poli metod. Každá položka v poli metod má strukturu method_info s proměnnou délkou.|
|metadata_count, metadata|Hodnota metadata_count je počet položek v poli metadat. Každý záznam metadat je metadata_infostructure, která mapuje název na sadu řetězcových hodnot. |
|class_count, instance, class|Hodnota class_count je počet položek v polích instance a class. |
|script_count, script|Hodnota script_count je počet položek v poli skriptů. Každá položka skriptu je struktura script_info, která definuje vlastnosti jednoho skriptu v tomto souboru. |
|method_body_count, method_body|Hodnota method_body_count je počet položek v poli method_body. Každá method_bodyentry se skládá ze struktury method_body_info s proměnnou délkou, která obsahuje instrukce pro jednotlivou metodu nebo funkci.|

## Reference

* [Robustní ABC (ActionScript Bytecode) [Dis-]Assembler – Github](https://github.com/CyberShadow/RABCDAsm)

