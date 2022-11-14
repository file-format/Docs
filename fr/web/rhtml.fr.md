{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","fichier rhtml", "format de fichier rhtml", "type de fichier rhtml", "fichier", "type", "qu'est-ce qu'un fichier rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML Page",
  "description":"En savoir plus sur le format de fichier RHTML et les API qui peuvent créer et ouvrir des fichiers RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Qu'est-ce qu'un fichier RHTML ?

Un fichier avec l'extension .rhtml est un fichier [HTML](/fr/web/html/) côté serveur qui contient du code ou des scripts Ruby. Le code est exécuté sur le serveur à l'aide de Ruby on Rails exécuté sur le backend. Pour ceux qui ne connaissent pas Ruby on Rails, il s'agit d'un framework complet pour le développement d'applications Web avec des bases de données backend basées sur le modèle Model-View-Control. En termes simples, RHTML est une combinaison de HTML et Ruby où la puissance des scripts/programmation Ruby est disponible pour les développeurs Web utilisant des balises HTML.

## Format de fichier RHTML

Les fichiers RHTML sont écrits au format texte brut comme tout autre fichier Web textuel. Le code à exécuter est entouré de `<% %>` tandis que pour la sortie, le code est écrit à l'intérieur des instructions `<%= %>`.

## Exemple RHTML

L'exemple suivant utilise la combinaison la plus simple de HTML et Ruby on Rails pour générer le nom de chaque produit à partir d'une liste de produits.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Références

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

