{
  "date" : "2019-10-11",
  "keywords" :[ "fichier aba", "format de fichier aba", "qu'est-ce qu'un fichier aba", "fichier", "exemple aba", "extension de fichier aba","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ABA - Format de fichier CemText",
  "description":"En savoir plus sur le format de fichier ABA et les API qui peuvent créer et ouvrir des fichiers ABA.",
  "linktitle" : "ABA",
  "menu" : {
    "docs" : {
      "identifier":"finance-aba",
      "parent" : "finance"
}
},
  "lastmod" : "2121-03-24"
}

## Qu'est-ce qu'un fichier ABA ?

Un fichier avec l'extension .aba est un format de fichier de l'Association australienne des banquiers (ABA) ou [Cemtext](https://www.cemtexaba.com/) utilisé par les banques pour les transactions par lots. Il est utilisé par la plupart des banques pour la tenue de dossiers financiers. Également connu sous le nom de fichier d'entrée directe, le format de fichier ABA a été adopté par la plupart des banques australiennes comme format par défaut pour les transactions par lots. Il n'a toujours pas été reconnu comme format standard malgré le fait qu'il ait été utilisé par Bank of Queensland, NAB et Westpac. Les fichiers ABA peuvent être ouverts avec n'importe quel éditeur de texte tel que Notepad ++.


## Format de fichier ABA

Un fichier ABA utilise le format ASCII pour stocker les données à transmettre ou à charger dans les systèmes bancaires. Le format est resté simple pour faciliter l'intégration dans le propre système financier de l'entreprise afin de traiter des lots de transactions. Par exemple, dans un système de paie, un lot de transactions peut être téléchargé pour être traité en un seul clic. Les spécifications du format de fichier ABA sont disponibles sous forme de transcription complète sur le site Web [Cemtext ABA](https://www.cemtexaba.com/aba-format/cemtex-aba-file-format-details) et peuvent être consultées à titre de référence pour les développeurs .

Un fichier ABA se compose de plusieurs lignes où chaque ligne est appelée "enregistrement". Il existe trois enregistrements principaux dans un fichier ABA :

* Notice descriptive
* Enregistrement détaillé
* Enregistrement total du fichier

### Notice descriptive

Un « enregistrement descriptif » contient des informations telles que le numéro de séquence de la bobine, le nom de l'institution financière de l'utilisateur, le nom de l'utilisateur fournissant le fichier et d'autres informations.

### Enregistrement détaillé

Le type "Enregistrement détaillé" comprend des informations telles que le numéro de banque/État/succursale, le numéro de compte à créditer/débiter, l'indicateur, le code de transaction, le montant et d'autres informations.

### Enregistrement total du fichier

Le type "Enregistrement total de fichier" comprend le type d'enregistrement 7, le remplissage de format BSB, le montant total net du fichier (utilisateur), le montant total du crédit du fichier (utilisateur), le montant total du débit du fichier (utilisateur) et d'autres informations.

### Codes de transaction

Une liste des codes de transaction valides est la suivante. La plupart du temps, le code "53 - Payer" est utilisé dans les fichiers ABA. Ces codes de transaction couvrent les débits, les crédits et les retenues à la source.

|Code|Description de la transaction|
---|---|
|13|Débits initiés de l'extérieur|
|50|Éléments de crédit initiés de l'extérieur à l'exception de ceux portant des codes de transaction|
|51|Intérêt de sécurité du gouvernement australien|
|52|Allocations familiales|
|53|Payer|
|54|Retraite|
|55|Attribution|
|56|Dividende|
|57|Intérêts sur les débentures/billets|

## Exemple de fichier ABA

```
0                 01BQL       MY NAME                   1111111004231633  230410
1123-456157108231 530000001234S R SMITH                       TEST BATCH        062-000 12223123MY ACCOUNT      00001200
1123-783 12312312 530000002200J K MATTHEWS                    TEST BATCH        062-000 12223123MY ACCOUNT      00000030
1456-789   125123 530003123513P R JONES                       TEST BATCH        062-000 12223123MY ACCOUNT      00000000
1121-232    11422 530000002300S MASLIN                        TEST BATCH        062-000 12223123MY ACCOUNT      00000000
7999-999            000312924700031292470000000000                        000004
```
## Références

* [Cemtext ABA](https://www.cemtexaba.com/)

