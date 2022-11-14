{
  "date" : "2021-09-01", 

  "keywords" :[ "RS", "fichier", "extension", "format de fichier", "langage de programmation Rust", "Guide de programmation", "exemple RS", "Rust", "VBScript" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RS - Fichier de programmation Rust",
  "description":"En savoir plus sur le format de fichier RS et les API qui peuvent créer et ouvrir des fichiers RS.",
  "linktitle" : "RS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-01"
}

## Qu'est-ce qu'un fichier RS ?

Un fichier avec l'extension RS appartient au langage de programmation Rust, il s'agit d'un langage de programmation multi-paramètres, de haut niveau et général conçu pour la performance et la sécurité, en particulier la sécurité. Rust est syntaxiquement similaire à С++ mais peut garantir la sécurité de la mémoire en utilisant un vérificateur d'emprunt pour valider les références. Le langage Rust assure la sécurité de la mémoire sans collecte de déchets, et le comptage de références est facultatif.

## Format de fichier RS ##

Rust a été conçu à l'origine par Graydon Hоare de Mozilla Research, avec les contributions de Dave Herman, Brendan Eiсh et d'autres. Il est de plus en plus utilisé dans l'industrie et Microsoft a expérimenté le langage pour des composants logiciels sécurisés et critiques pour la sécurité.

Rust a été élu "langage de programmation le plus aimé" dans l'enquête auprès des développeurs de Stack Оverflow chaque année depuis 2016, bien qu'il ne soit utilisé que par 7% des répondants de l'enquête de 2021. En plus du typage statique conventionnel, avant la version 0.4, Rust prenait également en charge les typages.

Le système de typographie a modélisé les assertions avant et après les déclarations de programme, grâce à l'utilisation d'une déclaration de vérification spéciale. Les divergences pourraient être découvertes au moment de la compilation, plutôt qu'au moment de l'exécution, comme cela pourrait être le cas avec les assertions dans le code C ou C++. Le concept de type n'était pas unique à Rust, car il a été introduit pour la première fois dans le langage NIL. Les types ont été supprimés car, dans la pratique, ils étaient peu utilisés, bien que la même fonctionnalité puisse être obtenue en tirant parti de la sémantique de mouvement de Rust.

Le langage de programmation Rust vous aide à écrire des logiciels plus rapides et plus fiables. L'ergonomie de haut niveau et le contrôle de bas niveau sont souvent en désaccord dans la conception du langage de programmation ; La rouille défie ce conflit. En équilibrant une puissante capacité technique et une grande expérience de développement, Rust vous donne la possibilité de contrôler les détails de bas niveau (tels que l'utilisation de la mémoire) sans tous les tracas traditionnellement rencontrés.

 

## Bref historique ##

La langue est née d'un projet personnel lancé en 2006 par l'employé de Mozilla, Graydоn Hore, qui a déclaré que le projet avait probablement été nommé d'après la famille des champignons de la rouille. Mozilla a commencé à parrainer le projet en 2009 et l'a annoncé en 2010. Rust 1.0, la première version stable, a été publiée le 15 mai 2015. versions, puis testées avec des versions bêta qui durent six semaines. Le 6 avril 2021, Google a annoncé un support pour Rust dans Android Open Sоurсe Рrоjeсt comme alternative à С/С++.

## Spécification technique ##

Rust est destiné à être un langage pour les systèmes hautement simultanés et hautement sûrs, et à programmer dans le grand, c'est-à-dire à créer et à maintenir des limites qui préservent l'intégrité du grand système. Cela a conduit à un ensemble de fonctionnalités mettant l'accent sur la sécurité, le contrôle de la disposition de la mémoire et la simultanéité.


Le langage Rust est conçu pour être sans danger pour la mémoire. Il n'autorise pas les pointeurs nuls, les pointeurs suspendus ou les courses de données. Les valeurs de données ne peuvent être initialisées que par le biais d'un ensemble fixe de formulaires, qui nécessitent tous que leurs entrées soient déjà initialisées. Pour reproduire les pointeurs valides ou nuls, comme dans les structures de données de liste chaînée ou d'arborescence binaire, la bibliothèque principale de Rust fournit un type d'option. Rust a ajouté une syntaxe pour gérer les durées de vie. Un code non sécurisé peut renverser certaines de ces restrictions en utilisant le mot-clé non sécurisé.


Le langage Rust n'utilise pas la collecte automatique des déchets. La mémoire et les autres ressources sont gérées par le biais de l'acquisition de ressources est une convention d'initialisation, avec un compte de référence facultatif.


Rust fournit une gestion déterministe des ressources, avec des frais généraux très faibles. La rouille favorise l'empilement de toutes les valeurs et n'effectue pas de boxe implicite. Il y a le concept de références (utilisant le symbole), qui n'implique pas le comptage de références au moment de l'exécution. La sécurité de ces pointeurs est vérifiée à tout moment, empêchant les pointeurs suspendus et d'autres formes de comportement indéfini.


Rust a un système de propriété où toutes les valeurs ont un propriétaire unique. Les valeurs peuvent être évaluées par référence immuable, en utilisant &T, par référence mutable, en utilisant & mut T, ou par valeur, en utilisant T. Le compilateur Rust applique ces règles au moment de la compilation et vérifie également que toutes les références sont valides.


## Exemple de format de fichier RS ##

```
use serde::{Serialize, Deserialize};

#[derive(Serialize, Deserialize, Debug)]
struct Point {
    x: i32,
    y: i32,
}

fn main() {
    let point = Point { x: 1, y: 2 };

    let serialized = serde_json::to_string(&point).unwrap();
    println!("serialized = {}", serialized);

    let deserialized: Point = serde_json::from_str(&serialized).unwrap();
    println!("deserialized = {:?}", deserialized);
}
```

## Référence ##

* [RS - par Wikipédia](https://en.wikipedia.org/wiki/Rust_(programming_language))



