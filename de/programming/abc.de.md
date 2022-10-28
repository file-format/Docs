
{
  "date" : "2021-12-14",
"Schlüsselwörter": [ ".abc-Datei", "Erweiterung", "Format", "ActionScript-Bytecode-Datei", "wie man eine .abc-Datei öffnet", "abc-Dateiformat" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - ActionScript-Bytecode-Datei",
  "description":"Erfahren Sie anhand von Beispielen und APIs, mit denen ABC-Dateien erstellt und geöffnet werden können, was das ABC-Dateiformat ist.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Was ist eine ABC-Datei?

Eine Datei mit der Erweiterung .abc ist eine ActionScript-Bytecode-Datei, die vom Flash-Compiler als Ergebnis der Kompilierung der ActionScript-Skriptdateien erstellt wird. Der in der ABC-Datei enthaltene Bytecode wird von der ActionScript Virtual Machine (AVM und AVM2) ausgeführt. Der Bytecode besteht aus konstanten Daten, Anweisungen aus dem AVM2-Befehlssatz und verschiedenen Arten von Metadaten. Wenn eine ABC-Datei in den AVM oder AVM2 geladen wird, wird sie überprüft. Entspricht es nicht der AVM2-Übersicht, wird es abgelehnt. ABC-Dateien können in Adobe Flash Player geöffnet werden, der vor langer Zeit eingestellt wurde.

## ABC-Dateiformat - Weitere Informationen

ABC-Dateien werden im binären Dateiformat auf der Disc gespeichert, das von virtuellen AVM- oder AVM2-Maschinen gelesen werden kann. Seine interne Dateistruktur repräsentiert einen ausführbaren Codeblock mit all seinen konstanten Daten, Typdeskriptoren, Code und Metadaten.

## ABC-Dateistruktur

Die ABC-Dateistruktur ist wie unten gezeigt.

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

### ABC-Dateifelder

|Feldname|Beschreibung|
---|---|
|minor_version, major_version|Die Werte von major_version und minor_version sind die Haupt- und Nebenversionsnummern des abcFile-Formats.|
|constant_pool|Der constant_pool ist eine Struktur mit variabler Länge, die aus ganzen Zahlen, Doubles, Strings, Namespaces, Namespace-Sets und Multinames besteht.|
|method_count, method|Der Wert vonmethod_count ist die Anzahl der Einträge im Methodenarray. Jeder Eintrag im Methoden-Array ist eine method_info-Struktur variabler Länge.|
|metadata_count, metadata|Der Wert von metadata_count ist die Anzahl der Einträge im Metadaten-Array. Jeder Metadateneintrag ist eine metadata_infostructure, die einen Namen einem Satz von Zeichenfolgewerten zuordnet. |
|class_count, instance, class|Der Wert von class_count ist die Anzahl der Einträge in den Instanz- und Klassenarrays. |
|script_count, script|Der Wert von script_count ist die Anzahl der Einträge im script-Array. Jeder Skripteintrag ist eine script_info-Struktur, die die Eigenschaften eines einzelnen Skripts in dieser Datei definiert. |
|method_body_count, method_body|Der Wert von method_body_count ist die Anzahl der Einträge im method_body-Array. Jeder method_body-Eintrag besteht aus einer method_body_info-Struktur variabler Länge, die die Anweisungen für eine einzelne Methode oder Funktion enthält.|

## Verweise

* [Robustes ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

