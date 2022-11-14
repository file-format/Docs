
{
  "date" : "2021-12-14",
  "keywords": [ ".abc file", "extension", "format","ActionScript Byte Code File", "how to open .abc file","abc file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABC - Fichier de code d'octet ActionScript",
  "description":"Découvrez ce qu'est le format de fichier ABC avec des exemples et des API qui peuvent créer et ouvrir des fichiers ABC.",
  "linktitle" : "ABC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-14"
}

## Qu'est-ce qu'un fichier ABC ?

Un fichier avec l'extension .abc est un fichier de code d'octet ActionScript créé par le compilateur Flash à la suite de la compilation des fichiers de script ActionScript. Le bytecode contenu dans le fichier ABC est exécuté par la machine virtuelle ActionScript (AVM et AVM2). Le code d'octet comprend des données constantes, des instructions du jeu d'instructions AVM2 et divers types de métadonnées. Lorsqu'un fichier ABC est chargé dans l'AVM ou l'AVM2, il subit une vérification. S'il n'est pas conforme à l'AVM2 Overview, il est rejeté. Les fichiers ABC peuvent être ouverts dans Adobe Flash Player qui a été interrompu il y a longtemps.

## Format de fichier ABC - Plus d'informations

Les fichiers ABC sont enregistrés sur un disque au format de fichier binaire lisible par les machines virtuelles AVM ou AVM2. Sa structure de fichier interne représente un bloc de code exécutable avec toutes ses données constantes, ses descripteurs de type, son code et ses métadonnées.

## Structure du fichier ABC

La structure du fichier ABC est comme indiqué ci-dessous.

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

### Champs du fichier ABC

|Nom du champ|Description|
---|---|
|minor_version, major_version|Les valeurs de major_version et minor_version sont les numéros de version majeure et mineure du format abcFile.|
|constant_pool|Le constant_pool est une structure de longueur variable composée d'entiers, de doubles, de chaînes, d'espaces de noms, d'ensembles d'espaces de noms et de noms multiples.|
|method_count, method|La valeur demethod_count est le nombre d'entrées dans le tableau de méthodes. Chaque entrée du tableau de méthodes est une structure method_info de longueur variable.|
|metadata_count, metadata|La valeur de metadata_count est le nombre d'entrées dans le tableau de métadonnées. Chaque entrée de métadonnées est une metadata_infostructure qui associe un nom à un ensemble de valeurs de chaîne. |
|class_count, instance, class|La valeur de class_count est le nombre d'entrées dans les tableaux d'instance et de classe. |
|script_count, script|La valeur de script_count est le nombre d'entrées dans le tableau de script. Chaque entrée de script est une structure script_info qui définit les caractéristiques d'un seul script dans ce fichier. |
|method_body_count, method_body|La valeur de method_body_count est le nombre d'entrées dans le tableau method_body. Chaque method_bodyentry consiste en une structure method_body_info de longueur variable qui contient les instructions pour une méthode ou une fonction individuelle.|

## Références

* [Robust ABC (ActionScript Bytecode) [Dés-]Assembleur - Github](https://github.com/CyberShadow/RABCDAsm)

