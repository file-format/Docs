{
  "date": "2019-10-11",
  "keywords": [
"klasė",
".klasė",
"kas yra klasės failas",
"kaip atidaryti klasės failą",
"pratęsimas",
"failą",
"klasės failą",
"klasės failo formatas",
".klasės plėtinys",
"klasės failą java"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Klasė – Java klasės failo formatas",
  "description": "Sužinokite apie Class failo formatą ir API, kurios gali kurti ir atidaryti Class failus.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-lts"
}
},
  "lastmod": "2020-09-10"
}

## Kas yra klasės failas?

**Klasės failas Java** yra sukompiliuota [.java](/programming/java/) klasės išvestis, kurią iš tikrųjų vykdo Java virtuali mašina (JVM). Klasės failai gali būti vykdomi atskirai, taip pat gali būti [JAR](/programming/jar/) failo dalis kaip paketas kartu su kitais paketo failais. Juos galima sukurti naudojant komandų eilutės sąsajos komandą **`javac`**. Kai kurios Java IDE, tokios kaip [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) ir NetBeans, leidžia sukurti .class išvesties failus iš projekto Java failų.

## Klasės failo formatas

Java klasės failą sudaro baitinis kodas, kuris yra tarpinis kodas, kurį paleidžia JVM. Klasės failą sudaro 8 bitų baitų srautas, o kelių baitų duomenų elementai visada saugomi didele tvarka.

### ClassFile struktūra

Klasės failo struktūra yra tokia, kaip parodyta žemiau.
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
kur:

* u1 = nepasirašytas vieno baito kiekis

* u2 = nepasirašytas dviejų baitų kiekis

* u4 = nepasirašytas keturių baitų kiekis


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` – stebuklingas elementas pateikia stebuklingą numerį, identifikuojantį klasės failo formatą; jo reikšmė yra 0xCAFEBABE.

* `minor_version`, `major_version` – minor_version ir major_version elementų reikšmės yra šios klasės failo mažosios ir pagrindinės versijos numeriai.

* „constant_pool_count“ – elemento „constant_pool_count“ vertė yra lygi įrašų skaičiui lentelėje „constant_pool_count“ plius vienas. Constant_pool indeksas laikomas galiojančiu, jei jis yra didesnis nei nulis ir mažesnis už konstantos_pulo_skaičius, išskyrus ilgo ir dvigubo tipo konstantas.

* `constant_pool[]` – Constant_pool yra struktūrų lentelė (§4.4), vaizduojanti įvairias eilučių konstantas, klasių ir sąsajų pavadinimus, laukų pavadinimus ir kitas konstantas, kurios nurodytos ClassFile struktūroje ir jos postruktūrose. Kiekvieno nuolatinio_puldinimo lentelės įrašo formatas nurodomas pirmuoju "žymos" baitu.

* `access_flags` – elemento access_flags reikšmė yra vėliavėlių, naudojamų šios klasės arba sąsajos prieigos leidimams ir ypatybėms žymėti, kaukė.

* „this_class“ – elemento this_class vertė turi būti galiojantis lentelės „constant_pool“ indeksas.

* `super_klasė` – klasėje super_class elemento vertė turi būti lygi nuliui arba turi būti galiojantis lentelės konstantos_puldas indeksas.

* `interfaces_count` – elemento interfaces_count reikšmė nurodo šios klasės arba sąsajos tipo tiesioginių super sąsajų skaičių.

* `interfaces[]` – kiekviena sąsajų masyvo reikšmė turi būti galiojantis lentelės konstantos_puldas indeksas.

* `fields_count` – elemento fields_count reikšmė nurodo lauko_informacijos struktūrų skaičių laukų lentelėje.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` – elemento Methods_count vertė nurodo metodų_informacijos struktūrų skaičių metodų lentelėje.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` – elemento attributes_count vertė nurodo atributų skaičių (§4.7) šios klasės atributų lentelėje.

* `attributes[]` – kiekviena atributų lentelės reikšmė turi būti atributo_info struktūra.





## Nuorodos

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

