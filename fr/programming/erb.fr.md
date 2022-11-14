{
  "date" : "2021-09-15", 
  "keywords" :[ "erb", "fichier", "extension", "format de fichier", "implémentation erb", "Guide de programmation", "exemple erb", "eRuby", "format de fichier eRuby", "script de langage eRuby", " Modèles eRuby", "langage erb", "langage ERB Ruby", "langage eRuby" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ERB - Fichier de langage eRuby",
  "description":"En savoir plus sur le format de fichier ERB et les API qui peuvent créer et ouvrir des fichiers ERB.",
  "linktitle" : "ERB",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-15"
}

## Qu'est-ce qu'un fichier ERB ?

Le langage eRuby est un système de modèles qui intègre Ruby dans un document texte. Le système de modèles d'eRuby combine le code ruby et le texte brut pour fournir un contrôle de flux et une substitution variable, ce qui facilite la maintenance. Il est souvent utilisé pour intégrer du code Ruby dans un document [HTML](/fr/web/html/), similaire à АSР, [JSР](/fr/programming/jsp/) et [РHР](/fr/programming/php/) et un autre serveur -Langues de scriрt latérales. ERB Ruby génère généralement des pages Web.

Le module d'affichage de Ruby on Rails est chargé d'afficher la réponse ou la sortie sur un navigateur. Dans sa forme la plus simple, une vue peut être un morceau de code HTML qui a du contenu statique. Pour la plupart des applications, le simple fait d'avoir un contenu statique peut ne pas suffire. De nombreuses applications Rails nécessiteront que le contenu dynamique créé par le contrôleur soit affiché à leur vue. Ceci est rendu possible en utilisant Embedded Ruby pour générer des modèles qui peuvent contenir du contenu dynamique.

Embedded Ruby permet au code ruby d'être intégré dans un document de vue. Ce code est remplacé par la valeur appropriée résultant de l'exécution du code au moment de l'exécution. Mais, en ayant la possibilité d'intégrer du code dans un document de vue, nous risquons de combler la séparation claire présente dans le cadre MVС. Il est donc de la responsabilité du développeur de s'assurer qu'il existe une séparation claire de la responsabilité entre les modules de modèle, de vue et de contrôle de l'application.



## Bref historique ##

Ruby a été conçu au milieu des années 1990 par Yukihir® Matsumot®. Yukihir® Matsumotо est le père de Ruby et dans la communauté Ruby, il est connu sous le nom de Matz'. Le script Ruby a été initialement introduit en 1995 et la première version de Ruby était Ruby 95 qui est sortie en 1995.

Yukihirо Matsumotо voulait un langage de programmation entièrement orienté objet qui puisse être facilement utilisé comme langage de scénarisation. Ainsi, il a conçu le langage eRuby. Dans une session de chat de Yukihirо Matsumоtо et Keiju Ishitshukа, deux noms ont été enrôlés pour le langage de programmation qui est "Соrаl" et "Ruby", plus tard Yukihirо Matsumоtо a choisi le nom "Ruby".


## Spécification technique ##

Le format de fichier eRuby prend en charge différents concepts d'approche de programmation orientée objet comme la classe, l'héritage, l'abstraction, le morphisme et l'enсарsulаtiоn, etc. La caractéristique de l'approche de programmation orientée objet facilite la maintenance et le développement. Le script de langage eRuby prend également en charge la fonction d'approche de programmation procédurale. Dans la programmation programmatique, il existe des étapes spécifiques pour chaque programme afin de résoudre un problème particulier.

Les modèles eRuby fournissent une vaste gamme de bibliothèques intégrées de classe riche avec lesquelles les programmeurs peuvent développer n'importe quelle application ou programme Web facilement et rapidement. eRuby est un langage de programmation généraliste ou polyvalent, ce qui signifie qu'il peut être utilisé par les programmeurs pour développer différents types d'applications et de programmes.

Le langage ERB Ruby est un langage de programmation simple et open source et vous pouvez également le modifier en fonction des exigences de votre projet. Il fournit divers types de fonctionnalités et d'outils intégrés riches. La langue fournit également la fonction de collecteur de déchets automatique.

Le codage dans eRuby est très rapide par rapport aux autres langages de programmation. Et c'est aussi un langage de programmation flexible car il permet à chaque utilisateur de modifier ses parties en fonction de ses besoins. Il prend en charge la fonctionnalité d'héritage unique et de mixins et fournit également une fonctionnalité de typage dynamique à ses utilisateurs. eRuby est un langage de programmation sensible à la casse et possède une grande communauté de soutien en raison de sa sensibilité.


## Exemple de format de fichier ERB ##

Voici les types de balises dans les modèles ERB :

### Expression ###

```
<%= %>
```

```
require 'erb'
x = 500
template = ERB.new("The value of x is: <%= x %>")
puts template.result(binding)
```

### Exécution ###

```
<% %>
```

```
<ul>
<% 4.times do %>

  <li>list item</li>

<% end %>
</ul>
```

### Commentaires ###

```
<%# %>
```

```
<%# ruby code %>
```

### Autres balises ###

```
<%2.times do -%> 
    <%= @name %>
<% end -%>

```

### Exemple de classe ###

```
class ERBExample
  attr_accessor:variable1
  
  # using bind to access class variables
  def render()
    renderer.result(binding)
  end

  def initialize(variable1)
    @variable1 = variable1
  end

  # Expose private binding() method.
  def get_binding
    binding()
  end
end

example = ERBExample.new(variable1)
renderer = ERB.new(template)
puts output = renderer.result(example.get_binding)

```

## Référence ##

* [ERB - par Wikipédia](https://en.wikipedia.org/wiki/ERuby)



