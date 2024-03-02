{
  "date": "2019-10-11",
  "keywords": [
"aicme",
".rang",
"cad is comhad ranga ann",
"conas comhad ranga a oscailt",
"síneadh",
"comhad",
"comhad ranga",
"formáid comhaid ranga",
"síneadh .rang",
"Comhad ranga i java"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Aicme - Java Formáid Chomhaid Aicme",
  "description": "Foghlaim faoi fhormáid comhaid Class agus APInna ar féidir comhaid Ranga a chruthú agus a oscailt.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-gas"
}
},
  "lastmod": "2020-09-10"
}

## Cad is comhad Ranga ann?

Is éard atá i **comhad ranga i Java** ná aschur tiomsaithe aicme [.java](/programming/java/) a dhéanann Meaisín Fíorúil Java (JVM). Is féidir comhaid ranga a rith ina n-aonar agus is féidir iad a bheith mar chuid de chomhad [JAR](/programming/jar/) mar bheart in éineacht le comhaid pacáiste eile. Is féidir iad seo a chruthú leis an ordú **`javac`** ón gcomhéadan líne ordaithe. Soláthraíonn roinnt IDEanna Java ar nós [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) agus NetBeans comhaid aschuir .class ó chomhaid Java an tionscadail.

## Formáid Chomhaid Ranga

Cuimsíonn comhad ranga Java seachchód ar cód idirmheánach é a bheidh á rith ag JVM. Is éard atá i gcomhad ranga ná sruth beart 8-giotán agus stóráiltear míreanna sonraí ilbhearta in ord mór-cheann i gcónaí.

### Struchtúr ClassFile

Tá struchtúr comhaid an ranga mar a thaispeántar thíos.
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
áit:

* u1 = cainníocht aon bheart gan síniú

* u2 = cainníocht dhá bheart gan síniú

* u4 = cainníocht ceithre bheart gan síniú


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `draíocht` - Soláthraíonn an mhír draíochta an uimhir draíochta a shainaithníonn formáid comhaid an ranga; tá an luach 0xCAFEBABE aige.

* `mion-leagan_`, `leagan_mór' - Is iad luachanna an mhionleagan_agus na mór-leaganacha ná mionuimhreacha agus mór-leaganacha an chomhaid ranga seo.

* `constant_pool_count` - Tá luach na míre constant_pool_count cothrom le líon na n-iontrálacha sa tábla constant_pool móide a haon. Meastar innéacs constant_pool a bheith bailí má tá sé níos mó ná nialas agus níos lú ná constant_pool_count, cé is moite de thairisisigh chineál fada agus dúbailte.

* `Constant_pool[]` - Is tábla de struchtúir é an tairiseach_pool (§4.4) a léiríonn tairisigh teaghrán éagsúla, ainmneacha aicme agus comhéadain, ainmneacha páirce, agus tairisigh eile a ndéantar tagairt dóibh laistigh de struchtúr ClassFile agus a fho-struchtúir. Léirítear formáid gach iontráil tábla constant_pool ag a chéad "chlib" beart.

* `access_flags` - Is éard atá i luach na míre access_flags ná masc bratach a úsáidtear chun ceadanna rochtana agus airíonna an aicme nó an chomhéadain seo a chur in iúl.

* `this_class` - Caithfidh luach na míre this_class a bheith ina innéacs bailí sa tábla constant_pool.

* `super_class` - I gcás aicme, ní mór luach na míre super_class a bheith nialasach nó a bheith ina innéacs bailí sa tábla constant_pool.

* `interfaces_count` - Tugann luach na míre interfaces_count líon na sár-chomhéadan díreach den aicme seo nó den chineál comhéadain seo.

* `comhéadain[]` - Caithfidh gach luach san eagar comhéadain a bheith ina innéacs bailí sa tábla constant_pool.

* `fields_count` - Tugann luach na míre fields_count líon na struchtúr field_info sa tábla réimsí.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` - Tugann luach na míre methods_count líon na struchtúr method_info sa tábla modhanna.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` - Tugann luach na míre attributes_count líon na n-airíonna (§4.7) i dtábla tréithe an aicme seo.

* `tréithe[]` - Ní mór struchtúr aitreabúide_info a bheith i ngach luach sa tábla tréithe.





## Tagairtí

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

