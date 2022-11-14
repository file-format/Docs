{
  "date" : "2019-10-11",
  "keywords" :[ "yaml", ".yaml","qu'est-ce qu'un fichier yaml","comment ouvrir un fichier yaml", "extension", "fichier", "fichier yaml","format de fichier yaml", "extension .yaml" , "yaml vs json" ,"exemple de fichier YAML", "exemple de fichier docker yaml"],
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "description" :" En savoir plus sur le format de fichier YAML et les API permettant de créer et d'ouvrir un fichier YAML.",
  "title" :"Format de fichier YAML",
  "linktitle" : "YAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-05"
}

## Qu'est-ce qu'un fichier YAML ? ##

Le **fichier YAML** consiste en un langage YAML (YAML Ain't Markup Language) qui est un langage de sérialisation de données basé sur Unicode ; utilisé pour les fichiers de configuration, la messagerie Internet, la persistance des objets, etc. YAML utilise l'extension .yaml pour ses fichiers. Sa syntaxe est indépendante d'un langage de programmation spécifique. Fondamentalement, le YAML est conçu pour l'interaction humaine et pour bien fonctionner avec les langages de programmation modernes. La prise en charge de la sérialisation de structures de données natives arbitraires a augmenté la lisibilité des fichiers YAML, mais cela a un peu compliqué le processus d'analyse et de génération de fichiers.

## Bref historique ##

YAML a été proposé pour la première fois en 2001 et a été développé par Clark Evans, Ingy döt Net et Oren Ben-Kiki. On a d'abord dit que YAML signifiait "Encore un autre langage de balisage" pour indiquer son objectif en tant que langage de balisage. Il a ensuite été réutilisé en tant que "YAML Aint Markup Language" pour indiquer que son objectif est orienté vers les données.


## Format de fichier YAML ##

Le fichier YAML comprend les types de données suivants

- **Scalaires** : les scalaires sont des valeurs telles que des chaînes, des entiers, des booléens, etc.
- **Séquences** : les séquences sont des listes dont chaque élément commence par un trait d'union (-). Les listes peuvent également être imbriquées.
- **Mappings** : le mappage permet de répertorier les clés avec des valeurs.

### Syntaxe ###

- **Whitespace** : l'indentation des espaces blancs est utilisée pour indiquer l'imbrication et la structure globale.

``` yaml
nom : John Smith
Contactez:
domicile : 1012355532
bureau: 5002586256
adresse:
rue : |
123 allée des tornades
Bureau 16
ville: East Centerville
état : KS
```

- **Commentaires** : les commentaires sont écrits en commençant par le symbole "#".

``` yaml
# Ceci est un commentaire YAML
```

- **Listes** : le trait d'union (-) est utilisé pour indiquer les membres de la liste, chaque membre étant sur une ligne distincte. Les membres de la liste peuvent également être placés entre crochets ([...]), les membres étant séparés par des virgules (,).

``` yaml
  - A
  - B
  - C
```

``` yaml
[A, B, C]
```

- **Tableau associatif** : un tableau associatif est entouré d'accolades ({...}). Les clés et les valeurs sont séparées par deux-points (:) et chaque paire est séparée par une virgule (,).

``` yaml
  {name: John Smith, age: 20}
```

- **Chaînes** : la chaîne peut être écrite avec ou sans guillemets doubles ("") ou guillemets simples (').

``` yaml
Exemple de chaîne
"Exemple de chaîne"
'Échantillon de chaîne'
```

- **Contenu de bloc scalaire** : le contenu scalaire peut être écrit en notation de bloc en utilisant ce qui suit :
  - **|**: All live breaks are significant.
  - **>**: Each line break is folded to space. It removes the leading whitespace for each line.

``` yaml
données : |
YAML
(YAML n'est pas un langage de balisage)
est un langage de sérialisation de données
```

``` yaml
Les données: ?
YAML (YAML n'est pas un langage de balisage)
est un langage de sérialisation de données
```

- **Documents multiples** : plusieurs documents sont séparés par trois traits d'union (---) dans un même flux. Les traits d'union indiquent le début du document. Les tirets sont également utilisés pour séparer les directives du contenu du document. La fin du document est indiquée par trois points (...).

``` yaml
  ---
Pièce 1
  ---
Pièce 2
...
```

- **Type** : pour spécifier le type de valeur, des points d'exclamation doubles (!!) sont utilisés.

``` yaml
un: !!float 123
b : !!str 123
```

- **Tag** : pour attribuer un tag à une note, une esperluette (&) est utilisée et pour référencer ce nœud, un astérisque (*) est utilisé.

``` yaml
nom : John Smith
à facturer : &id01
rue : |
123 allée des tornades
Bureau 16
ville: East Centerville
état : KS

destinataire : *id01
```

- **Directives** : les documents YAML peuvent être précédés de directives dans un flux. Les directives commencent par un signe de pourcentage (%) suivi du nom, puis des paramètres séparés par des espaces.

``` yaml
%YAML 1.2
  ---
Contenu des documents
```
## Exemple de fichier YAML
Ici, vous pouvez voir un **exemple de fichier docker yaml** ci-dessous :

```
topology:
database_node_name: docker_controller
docker_controller_node_name: docker_controller
self_service_portal_node_name: docker_controller
kvm_compute_node_names: kvm_compute1
docker_compute_node_names: docker_compute1
```

## YAML contre JSON
Fondamentalement, JSON et YAML sont développés pour fournir un format d'échange de données lisible par l'homme. Le YAML est réalisé comme un sur-ensemble du format JSON. Cela signifie que nous pouvons analyser JSON à l'aide d'un analyseur YAML. Bien que la mise en œuvre pratique de cette théorie soit peu délicate. Par conséquent, certaines différences fondamentales entre YAML et JSON sont indiquées ci-dessous :

|YAML| JSON |
---|---|
|Processus complexe et long d'analyse des données sérialisées |Analyse rapide et facile des données sérialisées JSON grâce à sa conception plus simple|
|Moins de soutien communautaire| Plus grand soutien et popularité de la communauté|
|Prend en charge les commentaires| Ne prend pas en charge les commentaires |
|Possibilité d'utiliser la référence d'autres objets de données| Impossible de sérialiser des structures complexes avec des références d'objets |
|La hiérarchie est indiquée à l'aide de caractères à double espace. Les caractères de tabulation ne sont pas autorisés|Les objets et les tableaux sont indiqués entre accolades et crochets.|
|Les guillemets de chaîne sont facultatifs, mais ils prennent en charge les guillemets simples et doubles.|Les chaînes doivent être entre guillemets doubles.|
|Le nœud racine peut être l'un des types de données valides|Le nœud racine doit être soit un tableau, soit un objet.|


## Références ##

- [YAML - Wikipédia](https://en.wikipedia.org/wiki/YAML)
- [YAML](https://yaml.org/spec/1.2/spec.html)

