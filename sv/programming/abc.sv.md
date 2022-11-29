
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript Byte Code File",
  "description":"Lär dig mer om vad ABC-filformat är med exempel och API:er som kan skapa och öppna ABC-filer.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Vad är ABC fil?

En fil med tillägget .abc är en ActionScript-bytekodfil som skapats av Flash-kompilatorn som ett resultat av kompileringen av ActionScript-skriptfilerna. Bytekoden som finns i ABC-filen exekveras av ActionScript Virtual Machine (AVM och AVM2). Bytekoden består av konstanta data, instruktioner från AVM2-instruktionsuppsättningen och olika typer av metadata. När en ABC-fil läses in i AVM eller AVM2 genomgår den verifiering. Om den inte överensstämmer med AVM2-översikten avvisas den. ABC-filer kan öppnas i Adobe Flash Player som har upphört för länge sedan.

## ABC-filformat - Mer information

ABC-filer sparas på skiva i binärt filformat som kan läsas av virtuella AVM- eller AVM2-maskiner. Dess interna filstruktur representerar ett körbart kodblock med alla dess konstanta data, typbeskrivningar, kod och metadata.

## ABC-filstruktur

ABC-filstrukturen är som visas nedan.

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

### ABC-filfält

|Fältnamn|Beskrivning|
---|---|
|minor_version, major_version|Värdena för major_version och minor_version är major- och minorversionsnumren för abcFile-formatet.|
|constant_pool|Konstant_poolen är en struktur med variabel längd som består av heltal, dubblar, strängar, namnrymder, namnutrymmesuppsättningar och multinamn.|
|method_count, method|Värdet ofmethod_count är antalet poster i metodmatrisen. Varje post i metodmatrisen är en metod_info-struktur med variabel längd.|
|metadata_count, metadata|Värdet på metadata_count är antalet poster i metadatamatrisen. Varje metadatapost är en metadata_infostructure som mappar ett namn till en uppsättning strängvärden. |
|class_count, instans, class|Värdet på class_count är antalet poster i instans- och klassmatriserna. |
|script_count, script|Värdet för script_count är antalet poster i scriptarrayen. Varje skriptpost är en script_info-struktur som definierar egenskaperna för ett enda skript i den här filen. |
|method_body_count, method_body|Värdet på method_body_count är antalet poster i method_body-matrisen. Varje method_bodyentry består av en method_body_info-struktur med variabel längd som innehåller instruktionerna för en enskild metod eller funktion.|

## Referenser

* [Robust ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

