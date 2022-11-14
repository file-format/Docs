{
  "date" : "2022-02-17",
  "keywords" :["fichier gpg", "format de fichier gpg", "qu'est-ce qu'un fichier gpg", "fichier", "exemple gpg", "extension de fichier gpg","extension", "format"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Fichier GPG - Fichier de trousseau de clés publiques GNU Privacy Guard",
  "description":"En savoir plus sur le fichier GPG et les API qui peuvent créer et ouvrir des fichiers GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## Qu'est-ce qu'un fichier GPG ?

Un fichier GPG est un fichier de clé de chiffrement/déchiffrement utilisé par le programme de chiffrement GNU Privacy Guard (GnuPG). Le programme GnuPC lui-même est basé sur le standard OpenPGP tel que défini RFC4880 et est également connu sous le nom de PGP. La clé d'une utilisation réussie de GPG dans un système d'exploitation moderne est son système de gestion de clés polyvalent. L'utilitaire de ligne de commande de GPG lui permet de s'intégrer facilement à d'autres applications.

## Format de fichier GPG

Les fichiers GPG sont enregistrés sous forme de fichiers binaires cryptés et, bien sûr, ils ne sont pas lisibles par l'homme. Pour décrypter un fichier GPG crypté, vous devez utiliser la même clé sécurisée. Et c'est pourquoi le format de fichier interne de ces fichiers n'est pas connu.

## Crypter et décrypter des fichiers avec GPG sous Linux

L'utilitaire de ligne de commande GPG peut être utilisé pour chiffrer et déchiffrer des fichiers sous Linux.

### Chiffrement d'un fichier

Un fichier peut être chiffré à l'aide de la commande gpg avec l'option -c (créer) comme indiqué ci-dessous.

```
gpg -c file1.txt
```
L'exécution de cette commande demande une phrase clé avec laquelle chiffrer le contenu du fichier d'origine "file1.txt". Cela entraîne la création du fichier crypté file1.txt.gpg.

### Déchiffrer et extraire un fichier

Afin de décrypter et d'extraire un fichier crypté, la commande suivante peut être utilisée.

```
gpg cfile.txt.gpg
```

## Références

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipédia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

