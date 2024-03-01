{
  "date": "2019-10-11",
  "keywords": [
"luokkaa",
".luokka",
"mikä on luokkatiedosto",
"kuinka avata luokkatiedosto",
"laajennus",
"tiedosto",
"luokan tiedosto",
"luokan tiedostomuoto",
".luokan laajennus",
"luokan tiedosto javassa"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "Luokka - Java-luokan tiedostomuoto",
  "description": "Opi Class-tiedostomuodosta ja sovellusliittymistä, jotka voivat luoda ja avata Class-tiedostoja.",
  "linktitle": "Class",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-clas-fis"
}
},
  "lastmod": "2020-09-10"
}

## Mikä on Class-tiedosto?

**Javan luokkatiedosto** on luokan [.java](/programming/java/) käännetty tulos, jonka Java Virtual Machine (JVM) itse asiassa suorittaa. Luokkatiedostot voidaan suorittaa yksitellen sekä ne voivat olla osa [JAR](/programming/jar/)-tiedostoa pakettina muiden pakettitiedostojen kanssa. Nämä voidaan luoda käyttämällä **`javac`**-komentoa komentoriviliittymästä. Jotkut Java-IDE:t, kuten [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) ja NetBeans, tarjoavat .class-tulostetiedostoja projektin Java-tiedostoista.

## Luokan tiedostomuoto

Java-luokkatiedosto koostuu tavukoodista, joka on JVM:n suorittama välikoodi. Luokkatiedosto koostuu 8-bittisten tavujen virrasta, ja monitavuiset tietokohteet tallennetaan aina big endian -järjestyksessä.

### Luokkatiedostorakenne

Luokan tiedostorakenne on alla olevan kuvan mukainen.
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
missä:

* u1 = etumerkitön yhden tavun määrä

* u2 = etumerkitön kaksitavuinen määrä

* u4 = etumerkitön neljän tavun määrä


Details of the .class file structure as well explained in the Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) and can be referred by developers for reference. A summary of these fields are as follow.

* `magic` - Magic-kohde antaa maagisen numeron, joka tunnistaa luokan tiedostomuodon; sen arvo on 0xCAFEBABE.

* `minor_version`, `major_version` - Alaversio- ja major_version-kohteiden arvot ovat tämän luokkatiedoston sivu- ja pääversionumerot.

* `vakio_poolin_määrä` - Kohteen vakio_pooli_määrä arvo on yhtä suuri kuin vakio_poolitaulukon merkintöjen määrä plus yksi. Vakiovarastoindeksiä pidetään kelvollisena, jos se on suurempi kuin nolla ja pienempi kuin vakiopoolimäärä, lukuun ottamatta vakiotyyppiä long ja double.

* `constant_pool[]` - Vakiovarasto on taulukko rakenteista (§4.4), joka edustaa erilaisia merkkijonovakioita, luokkien ja käyttöliittymien nimiä, kenttien nimiä ja muita vakioita, joihin ClassFile-rakenteessa ja sen alirakenteissa viitataan. Kunkin vakio_poolitaulukkomerkinnän muoto ilmaistaan sen ensimmäisellä "tag"-tavulla.

* `access_flags` - Access_flags-kohteen arvo on lippujen maski, jota käytetään ilmaisemaan tämän luokan tai käyttöliittymän käyttöoikeuksia ja ominaisuuksia.

* "this_class" - This_class kohteen arvon on oltava voimassa oleva indeksi vakio_poolitaulukossa.

* `super_class` - Luokassa super_luokka-kohteen arvon on oltava joko nolla tai sen on oltava voimassa oleva indeksi vakio_poolitaulukossa.

* `liitäntöjen_määrä` - Interfaces_count-kohteen arvo antaa tämän luokan tai liitäntätyypin suorien superliitäntöjen määrän.

* `liitännät[]` - Jokaisen rajapintataulukon arvon on oltava voimassa oleva indeksi vakio_poolitaulukossa.

* `fields_count` - Kohteen fields_count arvo antaa kenttätaulukon kenttätietorakenteiden määrän.

* `fields[]` - Each value in the fields table must be a field_info structure giving a complete description of a field in this class or interface.
* `methods_count` - Method_count-kohteen arvo antaa menetelmätaulukon method_info-rakenteiden lukumäärän.

* `methods[]` - Each value in the methods table must be a method_info structure giving a complete description of a method in this class or interface. If neither of the ACC_NATIVE and ACC_ABSTRACT flags are set in the access_flags item of a method_info structure, the Java Virtual Machine instructions implementing the method are also supplied.
* `attributes_count` - Attribuuttien_määrä -kohteen arvo antaa määritteiden määrän (§4.7) tämän luokan attribuuttitaulukossa.

* `attributes[]` - Attribuuttitaulukon jokaisen arvon on oltava attribuuttitietorakenne.





## Viitteet

 * [The class File Format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

