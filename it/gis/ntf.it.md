{
  "date" : "2021-07-28",
  "keywords" :[ "file ntf", "formato file ntf", "cos'è un file ntf", "file", "esempio ntf", "estensione file ntf", "estensione", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"NTF - File in formato di trasferimento nazionale",
  "description":"Scopri il formato di file NTF e le API che possono creare e aprire file NTF.",
  "linktitle" : "NTF",
  "menu" : {
    "docs" : {
      "parent" : "gis"
}
},
  "lastmod" : "2021-07-28"
}

## Che cos'è un file NTF?
I file con estensione .ntf sono chiamati file **National Transfer Format (NTF)**; utilizzato principalmente dall'Ordnance Survey (OS) del Regno Unito; specificatamente per il trasferimento di dati geospaziali. È gestito dalla British Standards Institution. È diventato il formato di trasferimento standard per i dati digitali di Ordnance Survey. La proiezione della National Grid del Regno Unito, che è un tipo di Transverse Mercator, contiene tutte le informazioni georeferenziate per i file NTF.

## Formato file NTF
Il formato di file NTF è di proprietà di Ordnance Survey nel Regno Unito; supportato dalla libreria GDB per l'importazione. La versione attuale del formato file NTF è 2.0. Questo formato di file è stato introdotto per risolvere una limitazione del segmento vettoriale **PCIDSK** che ha un solo campo di attributo per struttura, ma è possibile estrarre una varietà di attributi con i dati vettoriali. Per aggirare il formato file NTF è costituito da due segmenti. Ogni segmento è costituito dagli stessi vettori, ma con attributi diversi. Il primo segmento di un file vettoriale NTF contiene i vettori con il numero di codice caratteristica come attributo. Il secondo segmento contiene i vettori con il valore come attributo.

### Sistema di riferimento delle coordinate
La libreria GDB rappresenta dati raster e vettoriali con le caratteristiche di proiezione TM appropriate:

- Longitudine di riferimento: 49.0
- Latitudine di riferimento: 2.0
- Falso oriente: 400000
- Falso nord: -100000
- Scala: 0,9996012717
- Ellissoide: Airy 1830 (E009)
Non è disponibile alcun supporto per l'aggiornamento o la scrittura di file NTF, né è possibile collegare i file DTM.

### Esempio di Ogrinfo
L'esempio seguente utilizza **ogrinfo** su un file NTF per recuperare i numeri di livello:
```
> ogrinfo llcontours.ntf
    INFO: Open of 'llcontours.ntf'
    using driver 'UK .NTF' successful.
    1: LANDLINE_POINT (Point)
    2: LANDLINE_LINE (Line String)
    3: LANDLINE_NAME (Point)
    4: FEATURE_CLASSES (None)
```




## Riferimenti

* [UK National Transfer Format (NTF)](https://catalyst.earth/catalyst-system-files/help/references/gdb_r/gdb3N292.html)
* [Web Mapping - Illustrato da Tyler Mitchell](https://www.oreilly.com/library/view/web-mapping-illustrated/0596008651/re15.html)

