
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript-bytecodebestand",
  "description":"Meer informatie over het ABC-bestandsformaat met voorbeelden en API's die ABC-bestanden kunnen maken en openen.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Wat is een ABC-bestand?

Een bestand met de extensie .abc is een ActionScript-bytecodebestand dat door Flash-compiler is gemaakt als resultaat van het compileren van de ActionScript-scriptbestanden. De bytecode in het ABC-bestand wordt uitgevoerd door de ActionScript Virtual Machine (AVM en AVM2). De bytecode bestaat uit constante data, instructies uit de AVM2-instructieset en verschillende soorten metadata. Wanneer een ABC-bestand in de AVM of AVM2 wordt geladen, ondergaat het een verificatie. Als het niet voldoet aan het AVM2-overzicht, wordt het afgewezen. ABC-bestanden kunnen worden geopend in Adobe Flash Player die al lang niet meer bestaat.

## ABC-bestandsindeling - Meer informatie

ABC-bestanden worden op schijf opgeslagen in binaire bestandsindeling die leesbaar zijn voor AVM- of AVM2-virtuele machines. De interne bestandsstructuur vertegenwoordigt een uitvoerbaar codeblok met al zijn constante gegevens, typebeschrijvingen, code en metagegevens.

## ABC-bestandsstructuur

De ABC-bestandsstructuur is zoals hieronder weergegeven.

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

### ABC-bestandsvelden

|Veldnaam|Beschrijving|
---|---|
|minor_version, major_version|De waarden van major_version en minor_version zijn de hoofd- en secundaire versienummers van het abcFile-formaat.|
|constant_pool|De constante_pool is een structuur met variabele lengte die bestaat uit gehele getallen, dubbele getallen, tekenreeksen, naamruimten, naamruimtesets en multinamen.|
|method_count, method|De waarde vanmethod_count is het aantal items in de methode-array. Elk item in de methode-array is een method_info-structuur met variabele lengte.|
|metadata_count, metadata|De waarde van metadata_count is het aantal items in de metadata-array. Elk metagegevensitem is een metadata_infostructure die een naam toewijst aan een reeks tekenreekswaarden. |
|class_count, instance, class|De waarde van class_count is het aantal items in de instance- en class-arrays. |
|script_count, script|De waarde van script_count is het aantal items in de scriptarray. Elk scriptitem is een script_info-structuur die de kenmerken van een enkel script in dit bestand definieert. |
|method_body_count, method_body|De waarde van method_body_count is het aantal items in de array method_body. Elke method_bodyentry bestaat uit een method_body_info-structuur met variabele lengte die de instructies voor een individuele methode of functie bevat.|

## Referenties

* [Robuuste ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

