
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - File codice byte ActionScript",
  "description":"Scopri cos'è il formato di file ABC con esempi e API che possono creare e aprire file ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Che cos'è un file ABC?

Un file con estensione .abc è un file di codice byte ActionScript creato dal compilatore Flash come risultato della compilazione dei file di script ActionScript. Il codice byte contenuto nel file ABC viene eseguito dalla macchina virtuale ActionScript (AVM e AVM2). Il codice byte comprende dati costanti, istruzioni dal set di istruzioni AVM2 e vari tipi di metadati. Quando un file ABC viene caricato nell'AVM o nell'AVM2, viene sottoposto a verifica. Se non è conforme alla Panoramica AVM2, viene rifiutato. I file ABC possono essere aperti in Adobe Flash Player che è stato interrotto molto tempo fa.

## Formato file ABC - Ulteriori informazioni

I file ABC vengono salvati su disco in un formato di file binario leggibile da macchine virtuali AVM o AVM2. La sua struttura di file interna rappresenta un blocco di codice eseguibile con tutti i suoi dati costanti, descrittori di tipo, codice e metadati.

## Struttura del file ABC

La struttura del file ABC è quella mostrata di seguito.

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

### Campi del file ABC

|Nome campo|Descrizione|
---|---|
|minor_version, major_version|I valori di major_version e minor_version sono i numeri di versione maggiore e minore del formato abcFile.|
|constant_pool|Il constant_pool è una struttura a lunghezza variabile composta da numeri interi, doppi, stringhe, spazi dei nomi, insiemi di spazi dei nomi e multinomi.|
|method_count, metodo|Il valore dimethod_count è il numero di voci nell'array del metodo. Ogni voce nell'array del metodo è una struttura method_info di lunghezza variabile.|
|metadata_count, metadata|Il valore di metadata_count è il numero di voci nell'array di metadati. Ogni voce di metadati è una metadata_infostructure che associa un nome a un insieme di valori di stringa. |
|class_count, istanza, classe|Il valore di class_count è il numero di voci nell'istanza e negli array di classe. |
|script_count, script|Il valore di script_count è il numero di voci nell'array di script. Ogni voce di script è una struttura script_info che definisce le caratteristiche di un singolo script in questo file. |
|method_body_count, method_body|Il valore di method_body_count è il numero di voci nell'array method_body. Ogni method_bodyentry è costituito da una struttura method_body_info di lunghezza variabile che contiene le istruzioni per un singolo metodo o funzione.|

## Riferimenti

* [Robusto ABC (ActionScript Bytecode) [Dis-]Assembler - Github](https://github.com/CyberShadow/RABCDAsm)

