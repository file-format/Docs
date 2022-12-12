{
  "date" : "2019-10-11",
  "keywords" :[ "třída", ".class","co je soubor třídy","jak otevřít soubor třídy", "přípona", "soubor", "soubor třídy","formát souboru class", "přípona .class", "soubor třídy v jazyce Java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Class - Java Class File Format",
  "description":"Další informace o formátu souboru třídy a rozhraních API, která mohou vytvářet a otevírat soubory třídy.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Co je soubor třídy?

Soubor **Class v Javě** je zkompilovaný výstup třídy [.java](/cs/programming/java/), který je ve skutečnosti spuštěn Java Virtual Machine (JVM). Soubory třídy mohou být spouštěny jednotlivě, stejně jako mohou být součástí souboru [JAR](/cs/programming/jar/) jako balík spolu s dalšími soubory balíčků. Ty lze vytvořit pomocí příkazu **`javac`** z rozhraní příkazového řádku. Některá prostředí Java IDE, jako je [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) a NetBeans umožňují vytvářet výstupní soubory .class z jazyka Java projektu. soubory.

## Formát souboru třídy

Soubor třídy Java se skládá z bajtkódu, což je přechodný kód, který má spouštět JVM. Soubor třídy se skládá z proudu 8bitových bajtů a vícebajtové datové položky jsou vždy uloženy v pořadí big-endian.

### Struktura ClassFile

Struktura souboru třídy je uvedena níže.
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
kde:

* u1 = jednobajtové množství bez znaménka
* u2 = dvoubajtové množství bez znaménka
* u4 = čtyřbajtové množství bez znaménka

Podrobnosti o struktuře souboru .class jsou také dobře vysvětleny v Oracle [formát souboru třídy](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) a lze na ně odkazovat vývojáři pro referenci. Shrnutí těchto polí je následující.

* `magic` - Kouzelná položka poskytuje magické číslo identifikující formát souboru třídy; má hodnotu 0xCAFEBABE.
* `minor_version`, `major_version` - Hodnoty položek minor_version a major_version jsou čísla vedlejší a hlavní verze tohoto souboru třídy.
* `constant_pool_count` - Hodnota položky Constant_pool_count se rovná počtu záznamů v tabulce konstantních zdrojů plus jedna. Index konstantní_skupiny se považuje za platný, pokud je větší než nula a menší než počet_konstant, s výjimkou konstant typu long a double.
* `constant_pool[]` - fond konstant je tabulka struktur (§4.4) představující různé řetězcové konstanty, názvy tříd a rozhraní, názvy polí a další konstanty, na které se odkazuje ve struktuře ClassFile a jejích podstrukturách. Formát každého záznamu tabulky konstantního fondu je indikován jeho prvním "tag" bajtem.
* `access_flags` - Hodnota položky access_flags je maska příznaků používaných k označení přístupových oprávnění a vlastností této třídy nebo rozhraní.
* `this_class` - Hodnota položky this_class musí být platným indexem v tabulce konstantních_podílů.
* `super_class` – U třídy musí být hodnota položky super_class buď nula, nebo musí být platným indexem do tabulky konstantních_podílů.
* `interfaces_count` - Hodnota položky interfaces_count udává počet přímých super rozhraní této třídy nebo typu rozhraní.
* `rozhraní[]` - Každá hodnota v poli interfaces musí být platným indexem v tabulce konstantní_pool.
* `fields_count` - Hodnota položky Fields_count udává počet struktur field_info v tabulce polí.
* `fields[]` - Každá hodnota v tabulce polí musí být strukturou field_info poskytující úplný popis pole v této třídě nebo rozhraní.
* `methods_count` - Hodnota položky methods_count udává počet struktur method_info v tabulce metod.
* `methods[]` - Každá hodnota v tabulce metod musí být strukturou method_info poskytující úplný popis metody v této třídě nebo rozhraní. Pokud není nastaven žádný z příznaků ACC_NATIVE a ACC_ABSTRACT v položce access_flags struktury method_info, jsou dodány také instrukce Java Virtual Machine implementující metodu.
* `attributes_count` - Hodnota položky attribute_count udává počet atributů (§4.7) v tabulce atributů této třídy.
* `attributes[]` - Každá hodnota tabulky atributů musí být strukturou atribut_info.




## Reference

* [Formát souboru třídy](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

