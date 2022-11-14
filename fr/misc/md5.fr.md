{
  "date" : "2021-07-29",
  "keywords" :[ "fichier md5", "format de fichier md5", "qu'est-ce qu'un fichier md5", "fichier", "exemple md5", "extension de fichier md5","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD5 - Fichier de somme de contrôle MD5",
  "description":"En savoir plus sur le fichier MD5 et les API qui peuvent créer et ouvrir des fichiers MD5.",
  "linktitle" : "MD5",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2021-07-29"
}

## Qu'est-ce qu'un fichier MD5 ?

Un fichier MD5 est un fichier de somme de contrôle utilisé pour la vérification de l'intégrité d'un fichier. Il est similaire à une empreinte digitale pour le fichier associé et est généré de manière unique à l'aide d'un algorithme qui utilise le nombre de bits dans le fichier. Il est utilisé pour vérifier le fichier avec un logiciel tel que [md5sum](http://www.gnu.org/software/coreutils/manual/html_node/md5sum-invocation.html). L'un des avantages de l'utilisation des fichiers MD5 est de vérifier que les fichiers téléchargés ne sont pas corrompus.

## Format de fichier MD5 - Plus d'informations

Habituellement, un fichier MD5 est enregistré avec le même nom que le nom de fichier d'origine mais avec l'extension .md5. Par exemple, si le nom de fichier associé est `abc_987_123456.grb`, le nom de fichier MD5 correspondant sera `abc_987_123456.grb.md5`. Les fichiers MD5 aident à identifier qu'un fichier reçu ou téléchargé n'est pas corrompu ou affecté par un contenu malveillant. En bref, les fichiers MD5 garantissent l'exhaustivité d'un fichier.


## Comment vérifier la somme de contrôle MD5 ?

Un seul fichier peut être contrôlé/vérifié pour MD5 à l'aide de l'outil [md5sum](https://en.wikipedia.org/wiki/Md5sum) comme suit.

```
md5sum -c abc_987_123456.grb.md5
```

## Références

* [md5sum - Wikipédia](https://en.wikipedia.org/wiki/Md5sum)

