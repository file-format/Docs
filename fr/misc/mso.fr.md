{
  "date" : "2022-03-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSO - Fichier de référence des macros Microsoft Office",
  "description":"En savoir plus sur le fichier MSO et les API qui peuvent créer et ouvrir des fichiers MSO.",
  "linktitle" : "MSO",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-03-12"
}

## Qu'est-ce qu'un fichier MSO ?

Un fichier MSO est un format de fichier conteneur de données qui est créé lorsqu'un message HTML est envoyé à l'aide de Microsoft Outlook. Cela se produit principalement avec les applications Microsoft Office 2000. Dans la plupart des cas, le message électronique est joint avec le nom de fichier **Oledata.mso**. Le destinataire de l'e-mail, lorsqu'il ouvre un tel e-mail, peut afficher le fichier correctement même s'il n'a pas installé le même logiciel. Les fichiers MSO font référence au [Microsoft Compound Document File Format (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b).

## Format de fichier Microsoft MSO

Les fichiers MSO sont enregistrés au format Microsoft Compound Document File Format (MCDF), également connu sous le nom de format de fichier binaire d'implémentation de fichier composé de stockage structuré Object Linking and Embedding (OLE) ou Component Object Model (COM).

### Structure du format de fichier MSO

La structure de format de fichier interne du format de fichier MSO est bien définie dans les [Structures](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/28488197-8193-49d7-84d8-dfd692418ccd ) section de la documentation MCDF. La table d'allocation de fichiers (FAT) gère l'allocation des secteurs et les chaînes de secteurs. Il contient un tableau de numéros de secteur 32 bits. Chaque index du tableau représente un numéro de secteur alors que sa valeur représente le secteur suivant dans la chaîne ou une valeur spéciale.

## Références

* [Stockage structuré COM](https://en.wikipedia.org/wiki/COM_Structured_Storage)
* [Format de fichier de document composé Microsoft (MCDF)](https://docs.microsoft.com/en-us/openspecs/windows_protocols/ms-cfb/53989ce4-7b05-4f8d-829b-d08d6148375b)

