{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class", "che cos'è un file di classe", "come aprire un file di classe", "estensione", "file", "file di classe", "formato di file di classe", "estensione .class ", "file di classe in java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Classe - Formato file classe Java",
  "description":"Ulteriori informazioni sul formato del file di classe e sulle API che possono creare e aprire file di classe.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Che cos'è un file di classe?

Un **file di classe in Java** è l'output compilato della classe [.java](/it/programming/java/) che viene effettivamente eseguito da una Java Virtual Machine (JVM). I file di classe possono essere eseguiti individualmente e possono essere parte di un file [JAR](/it/programming/jar/) come pacchetto insieme ad altri file di pacchetto. Questi possono essere creati usando il comando **`javac`** dall'interfaccia della riga di comando. Alcuni IDE Java come [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) e NetBeans forniscono file di output .class di creazione dal Java del progetto File.

## Formato file di classe

Un file di classe Java comprende bytecode che è un codice intermedio che deve essere eseguito da JVM. Un file di classe è costituito da un flusso di byte a 8 bit e gli elementi di dati multibyte vengono sempre archiviati in ordine big-endian.

### Struttura del file di classe

La struttura del file di classe è come mostrato di seguito.
```
ClassFile {
    u4             magic;
    u2             minor_version;
    u2             major_version;
    u2             constant_pool_count;
    cp_info        constant_pool[constant_pool_count-1];
    u2             access_flags;
    u2             this_class;
    u2             super_class;
    u2             interfaces_count;
    u2             interfaces[interfaces_count];
    u2             fields_count;
    field_info     fields[fields_count];
    u2             methods_count;
    method_info    methods[methods_count];
    u2             attributes_count;
    attribute_info attributes[attributes_count];
}
```
dove:

* u1 = quantità di un byte senza segno
* u2 = quantità di due byte senza segno
* u4 = quantità di quattro byte senza segno

I dettagli della struttura del file .class sono anche spiegati in Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) e possono essere referenziati da sviluppatori per riferimento. Un riepilogo di questi campi è il seguente.

* `magic` - L'oggetto magico fornisce il numero magico che identifica il formato del file di classe; ha il valore 0xCAFEBABE.
* `minor_version`, `major_version` - I valori degli elementi minor_version e major_version sono i numeri di versione minore e maggiore di questo file di classe.
* `constant_pool_count` - Il valore dell'elemento constant_pool_count è uguale al numero di voci nella tabella constant_pool più uno. Un indice constant_pool è considerato valido se è maggiore di zero e minore di constant_pool_count, ad eccezione delle costanti di tipo long e double.
* `constant_pool[]` - Il constant_pool è una tabella di strutture (§4.4) che rappresentano varie costanti di stringa, nomi di classi e interfacce, nomi di campi e altre costanti a cui si fa riferimento all'interno della struttura ClassFile e delle sue sottostrutture. Il formato di ogni voce della tabella constant_pool è indicato dal suo primo byte "tag".
* `access_flags` - Il valore dell'elemento access_flags è una maschera di flag usata per denotare i permessi di accesso e le proprietà di questa classe o interfaccia.
* `this_class` - Il valore dell'elemento this_class deve essere un indice valido nella tabella constant_pool.
* `super_class` - Per una classe, il valore dell'elemento super_class deve essere zero o deve essere un indice valido nella tabella constant_pool.
* `interfaces_count` - Il valore dell'elemento interfaces_count fornisce il numero di super interfacce dirette di questa classe o tipo di interfaccia.
* `interfaces[]` - Ogni valore nell'array delle interfacce deve essere un indice valido nella tabella constant_pool.
* `fields_count` - Il valore dell'elemento fields_count fornisce il numero di strutture field_info nella tabella dei campi.
* `fields[]` - Ogni valore nella tabella dei campi deve essere una struttura field_info che fornisce una descrizione completa di un campo in questa classe o interfaccia.
* `methods_count` - Il valore dell'elemento method_count fornisce il numero di strutture method_info nella tabella dei metodi.
* `methods[]` - Ogni valore nella tabella dei metodi deve essere una struttura method_info che fornisce una descrizione completa di un metodo in questa classe o interfaccia. Se nessuno dei flag ACC_NATIVE e ACC_ABSTRACT è impostato nell'elemento access_flags di una struttura method_info, vengono fornite anche le istruzioni Java Virtual Machine che implementano il metodo.
* `attributes_count` - Il valore della voce attributi_count fornisce il numero di attributi (§4.7) nella tabella degli attributi di questa classe.
* `attributes[]` - Ogni valore della tabella degli attributi deve essere una struttura attribute_info.




## Riferimenti

* [Il formato file della classe](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

