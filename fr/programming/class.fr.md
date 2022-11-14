{
  "date" : "2019-10-11",
  "keywords" :[ "classe", ".class","qu'est-ce qu'un fichier de classe","comment ouvrir un fichier de classe", "extension", "fichier", "fichier de classe","format de fichier de classe", "extension .class ", "fichier de classe en java" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Classe - Format de fichier de classe Java",
  "description":"En savoir plus sur le format de fichier Class et les API permettant de créer et d'ouvrir des fichiers Class.",
  "linktitle" : "Class",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## Qu'est-ce qu'un fichier Classe ?

Un fichier **Class en Java** est la sortie compilée de la classe [.java](/fr/programming/java/) qui est réellement exécutée par une machine virtuelle Java (JVM). Les fichiers de classe peuvent être exécutés individuellement et peuvent faire partie d'un fichier [JAR](/fr/programming/jar/) en tant que bundle avec d'autres fichiers de package. Ceux-ci peuvent être créés à l'aide de la commande **`javac`** à partir de l'interface de ligne de commande. Certains IDE Java comme [Eclipse](https://www.eclipse.org/downloads/packages/release/2020-06/r/eclipse-ide-java-developers) et NetBeans fournissent des fichiers de sortie .class à partir du Java du projet des dossiers.

## Format de fichier de classe

Un fichier de classe Java comprend un bytecode qui est un code intermédiaire à exécuter par JVM. Un fichier de classe consiste en un flux d'octets de 8 bits et les éléments de données multi-octets sont toujours stockés dans l'ordre big-endian.

### Structure du fichier de classe

La structure du fichier de classe est comme indiqué ci-dessous.
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
où:

* u1 = quantité non signée d'un octet
* u2 = quantité de deux octets non signés
* u4 = quantité non signée de quatre octets

Les détails de la structure du fichier .class sont également expliqués dans Oracle [class file format](https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html) et peuvent être référencés par développeurs pour référence. Un résumé de ces champs est le suivant.

* `magic` - L'élément magique fournit le nombre magique identifiant le format de fichier de classe ; il a la valeur 0xCAFEBABE.
* `minor_version`, `major_version` - Les valeurs des éléments minor_version et major_version sont les numéros de version mineure et majeure de ce fichier de classe.
* `constant_pool_count` - La valeur de l'élément constant_pool_count est égale au nombre d'entrées dans la table constant_pool plus un. Un index constant_pool est considéré comme valide s'il est supérieur à zéro et inférieur à constant_pool_count, à l'exception des constantes de type long et double.
* `constant_pool[]` - Le constant_pool est une table de structures (§4.4) représentant diverses constantes de chaîne, des noms de classe et d'interface, des noms de champ et d'autres constantes auxquelles il est fait référence dans la structure ClassFile et ses sous-structures. Le format de chaque entrée de la table constant_pool est indiqué par son premier octet "tag".
* `access_flags` - La valeur de l'élément access_flags est un masque d'indicateurs utilisé pour indiquer les autorisations d'accès et les propriétés de cette classe ou interface.
* `this_class` - La valeur de l'élément this_class doit être un index valide dans la table constant_pool.
* `super_class` - Pour une classe, la valeur de l'élément super_class doit être zéro ou doit être un index valide dans la table constant_pool.
* `interfaces_count` - La valeur de l'élément interfaces_count donne le nombre de super interfaces directes de cette classe ou de ce type d'interface.
* `interfaces[]` - Chaque valeur du tableau interfaces doit être un index valide dans la table constant_pool.
* `fields_count` - La valeur de l'élément fields_count donne le nombre de structures field_info dans la table des champs.
* `fields[]` - Chaque valeur dans la table des champs doit être une structure field_info donnant une description complète d'un champ dans cette classe ou interface.
* `methods_count` - La valeur de l'élément method_count donne le nombre de structures method_info dans la table des méthodes.
* `methods[]` - Chaque valeur de la table des méthodes doit être une structure method_info donnant une description complète d'une méthode dans cette classe ou interface. Si aucun des drapeaux ACC_NATIVE et ACC_ABSTRACT n'est défini dans l'élément access_flags d'une structure method_info, les instructions de la machine virtuelle Java implémentant la méthode sont également fournies.
* `attributes_count` - La valeur de l'item attributes_count donne le nombre d'attributs (§4.7) dans la table des attributs de cette classe.
* `attributes[]` - Chaque valeur de la table des attributs doit être une structure attribute_info.




## Références

* [Le format de fichier de classe] (https://docs.oracle.com/javase/specs/jvms/se7/html/jvms-4.html)

