{
  "date" : "2019-10-11",
  "keywords" :[ "class", ".class","wat is een class-bestand","hoe een class-bestand te openen", "extensie", "file", "class file","class bestandsformaat", ".class extension ", "klassebestand in java"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Klasse - Java-klasse-bestandsindeling",
  "description":"Meer informatie over Class-bestandsindeling en API's die Class-bestanden kunnen maken en openen.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Wat is een Class-bestand?

Een **Class-bestand in Java** is de gecompileerde uitvoer van de klasse [.java](/nl/programming/java/) die daadwerkelijk wordt uitgevoerd door een Java Virtual Machine (JVM). Klassebestanden kunnen zowel afzonderlijk worden uitgevoerd als deel uitmaken van een [JAR](/nl/programming/jar/)-bestand als een bundel samen met andere pakketbestanden. Deze kunnen worden gemaakt met de opdracht **`javac`** vanuit de opdrachtregelinterface. Sommige Java-IDE's zoals [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) en NetBeans bieden .class-uitvoerbestanden van de Java van het project bestanden.

## Klasse Bestandsformaat

Een Java-klassebestand bestaat uit bytecode die tussencode is die door JVM moet worden uitgevoerd. Een klassebestand bestaat uit een stroom van 8-bits bytes en multibyte-gegevensitems worden altijd in big-endian-volgorde opgeslagen.

### ClassFile-structuur

De structuur van het klassenbestand is zoals hieronder weergegeven.
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
waar:

* u1 = niet-ondertekende hoeveelheid van één byte
* u2 = niet-ondertekende hoeveelheid van twee bytes
* u4 = ongetekende hoeveelheid van vier bytes

Details van de .class bestandsstructuur zoals ook uitgelegd in de Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) en kan worden verwezen door ontwikkelaars ter referentie. Een samenvatting van deze velden is als volgt.

* `magic` - Het magische item levert het magische getal dat het class-bestandsformaat identificeert; het heeft de waarde 0xCAFEBABE.
* `minor_version`, `major_version` - De waarden van de minor_version en major_version items zijn de secundaire en primaire versienummers van dit klassenbestand.
* `constant_pool_count` - De waarde van het item constant_pool_count is gelijk aan het aantal items in de constant_pool-tabel plus één. Een constant_pool-index wordt als geldig beschouwd als deze groter is dan nul en kleiner dan constant_pool_count, met uitzondering van constanten van het type long en double.
* `constant_pool[]` - De constante_pool is een tabel met structuren (§4.4) die verschillende stringconstanten, klasse- en interfacenamen, veldnamen en andere constanten vertegenwoordigt waarnaar wordt verwezen in de ClassFile-structuur en zijn substructuren. Het formaat van elk item in de constante_pooltabel wordt aangegeven door zijn eerste "tag"-byte.
* `access_flags` - De waarde van het item access_flags is een masker van vlaggen die worden gebruikt om toegangsrechten en eigenschappen van deze klasse of interface aan te duiden.
* `this_class` - De waarde van het item this_class moet een geldige index zijn in de constant_pool-tabel.
* `super_class` - Voor een klasse moet de waarde van het item super_class ofwel nul zijn, ofwel een geldige index in de constante_pooltabel zijn.
* `interfaces_count` - De waarde van het interfaces_count item geeft het aantal directe superinterfaces van deze klasse of interfacetype.
* `interfaces[]` - Elke waarde in de interfaces-array moet een geldige index zijn in de constant_pool-tabel.
* `fields_count` - De waarde van het field_count item geeft het aantal field_info structuren in de veldentabel.
* `fields[]` - Elke waarde in de veldentabel moet een field_info-structuur zijn die een volledige beschrijving geeft van een veld in deze klasse of interface.
* `methods_count` - De waarde van het item methods_count geeft het aantal method_info-structuren in de methodetabel.
* `methods[]` - Elke waarde in de methodetabel moet een method_info-structuur zijn die een volledige beschrijving geeft van een methode in deze klasse of interface. Als geen van de vlaggen ACC_NATIVE en ACC_ABSTRACT zijn ingesteld in het item access_flags van een method_info-structuur, worden de Java Virtual Machine-instructies die de methode implementeren ook geleverd.
* `attributes_count` - De waarde van het attributes_count item geeft het aantal attributen (§4.7) in de attributentabel van deze klasse.
* `attributen[]` - Elke waarde van de attributentabel moet een attribute_info-structuur zijn.




## Referenties

* [De bestandsindeling van de klasse](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

