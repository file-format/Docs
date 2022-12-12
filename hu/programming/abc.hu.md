
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC – ActionScript byte kódfájl",
  "description":"Ismerje meg, mi az ABC fájlformátum, példákkal és API-kkal, amelyek ABC-fájlokat hozhatnak létre és nyithatnak meg.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Mi az ABC fájl?

Az .abc kiterjesztésű fájl egy ActionScript byte kódfájl, amelyet a Flash fordító hoz létre az ActionScript szkriptfájlok fordítása eredményeként. Az ABC fájlban található bájtkódot az ActionScript Virtual Machine (AVM és AVM2) hajtja végre. A bájtkód állandó adatokból, az AVM2 utasításkészletből származó utasításokból és különféle metaadatokból áll. Amikor egy ABC-fájlt betöltenek az AVM-be vagy az AVM2-be, az ellenőrzésen megy keresztül. Ha nem felel meg az AVM2 áttekintésének, akkor a rendszer elutasítja. Az ABC fájlok megnyithatók az Adobe Flash Playerben, amely már régen megszűnt.

## ABC fájlformátum - További információ

Az ABC-fájlokat a rendszer bináris fájlformátumban menti lemezre, amelyet az AVM vagy AVM2 virtuális gépek is tudnak olvasni. Belső fájlstruktúrája egy végrehajtható kódblokkot képvisel az összes állandó adattal, típusleíróval, kóddal és metaadattal együtt.

## ABC fájlszerkezet

Az ABC fájl szerkezete az alábbiak szerint látható.

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

### ABC fájlmezők

|Mező neve|Leírás|
---|---|
|minor_version, major_version|A major_version és minor_version értékei az abcFile formátum fő- és mellékverziószámai.|
|constant_pool|A konstans_készlet egy változó hosszúságú struktúra, amely egész számokból, kettősökből, karakterláncokból, névterekből, névtérkészletekből és többnevekből áll.|
|method_count, method|A method_count értéke a metódustömb bejegyzéseinek száma. A metódustömb minden bejegyzése egy változó hosszúságú method_info struktúra.|
|metadata_count, metadata|A metadata_count értéke a metaadattömb bejegyzéseinek száma. Minden metaadat-bejegyzés egy metadata_infostruktúra, amely egy nevet leképez egy karakterláncérték-készletre. |
|osztály_szám, példány, osztály|Az osztály_szám értéke a példányban és az osztálytömbökben található bejegyzések száma. |
|script_count, script|A script_count értéke a parancsfájltömb bejegyzéseinek száma. Minden szkriptbejegyzés egy script_info struktúra, amely meghatározza a fájl egyetlen szkriptjének jellemzőit. |
|method_body_count, method_body|A method_body_count értéke a method_body tömb bejegyzéseinek száma. Minden method_bodyentry egy változó hosszúságú method_body_info struktúrából áll, amely az egyes metódusokhoz vagy függvényekhez tartozó utasításokat tartalmazza.|

## Hivatkozások

* [Robust ABC (ActionScript Bytecode) [Dis-]Assembler – Github](https://github.com/CyberShadow/RABCDAsm)

