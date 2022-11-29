{
  "date" : "2019-10-11",
  "keywords" :[ "klass", ".klass","vad är en klassfil","hur man öppnar en klassfil", "tillägg", "fil", "klassfil","klassfilformat", ".klasstillägg", "klassfil i java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Klass - Java Class File Format",
  "description":"Läs mer om klassfilformat och API:er som kan skapa och öppna klassfiler.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Vad är en klassfil?

En **Klassfil i Java** är den kompilerade utdata från klassen [.java](/sv/programming/java/) som faktiskt exekveras av en Java Virtual Machine (JVM). Klassfiler kan köras individuellt och kan vara en del av en [JAR](/sv/programming/jar/)-fil som en bunt tillsammans med andra paketfiler. Dessa kan skapas med kommandot **`javac`** från kommandoradsgränssnittet. Vissa Java IDEs som [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) och NetBeans tillhandahåller skapa .class-utdatafiler från projektets Java filer.

## Klass filformat

En Java-klassfil består av bytekod som är en mellankod som ska köras av JVM. En klassfil består av en ström av 8-bitars byte och multibyte dataobjekt lagras alltid i big-endian ordning.

### Klassfilstruktur

Klassfilstrukturen är som visas nedan.
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
var:

* u1 = unsigned one-byte kvantitet
* u2 = osignerad två-byte kvantitet
* u4 = osignerad fyra-byte kvantitet

Detaljer om .class-filstrukturen förklaras också i Oracle [klassfilformat](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) och kan refereras av utvecklare som referens. En sammanfattning av dessa fält är följande.

* `magic` - Det magiska objektet tillhandahåller det magiska numret som identifierar klassens filformat; den har värdet 0xCAFEBABE.
* `minor_version`, `major_version` - Värdena för minor_version- och major_version-objekten är minor- och major-versionsnumren för denna klassfil.
* `constant_pool_count` - Värdet på constant_pool_count-objektet är lika med antalet poster i constant_pool-tabellen plus en. Ett constant_pool-index anses giltigt om det är större än noll och mindre än constant_pool_count, med undantag för konstanter av typen long och double.
* `constant_pool[]` - konstant_poolen är en tabell med strukturer (§4.4) som representerar olika strängkonstanter, klass- och gränssnittsnamn, fältnamn och andra konstanter som refereras till inom ClassFile-strukturen och dess understrukturer. Formatet för varje konstant_pool-tabellpost indikeras av dess första "tagg"-byte.
* `access_flags` - Värdet på access_flags-objektet är en mask av flaggor som används för att ange åtkomstbehörigheter till och egenskaper för denna klass eller gränssnitt.
* `this_class` - Värdet för this_class-objektet måste vara ett giltigt index i constant_pool-tabellen.
* `super_class` - För en klass måste värdet på super_class-objektet antingen vara noll eller måste vara ett giltigt index i constant_pool-tabellen.
* `interfaces_count` - Värdet för objektet interfaces_count anger antalet direkta supergränssnitt av denna klass eller gränssnittstyp.
* `interfaces[]` - Varje värde i interfaces-arrayen måste vara ett giltigt index i tabellen constant_pool.
* `fields_count` - Värdet på fields_count-objektet anger antalet field_info-strukturer i fälttabellen.
* `fields[]` - Varje värde i fälttabellen måste vara en field_info-struktur som ger en fullständig beskrivning av ett fält i denna klass eller gränssnitt.
* `methods_count` - Värdet på methods_count-objektet anger antalet metodinfo-strukturer i metodtabellen.
* `methods[]` - Varje värde i metodtabellen måste vara en method_info-struktur som ger en fullständig beskrivning av en metod i denna klass eller gränssnitt. Om ingen av flaggorna ACC_NATIVE och ACC_ABSTRACT är inställda i access_flags-objektet i en metod_info-struktur, tillhandahålls Java Virtual Machine-instruktionerna som implementerar metoden också.
* `attributes_count` - Värdet på attributes_count-objektet anger antalet attribut (§4.7) i attributtabellen för denna klass.
* `attribut[]` – Varje värde i attributtabellen måste vara en attribute_info-struktur.




## Referenser

* [Klassens filformat](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

