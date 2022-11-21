{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml", "arquivo rhtml", "formato de arquivo rhtml", "tipo de arquivo rhtml", "arquivo", "tipo", "o que é um arquivo rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Página HTML Ruby",
  "description":"Saiba mais sobre o formato de arquivo RHTML e APIs que podem criar e abrir arquivos RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## O que é um arquivo RHTML?

Um arquivo com extensão .rhtml é um arquivo [HTML](/pt/web/html/) do lado do servidor que contém código ou scripts Ruby. O código é executado no servidor usando o Ruby on Rails rodando no backend. Para quem não conhece Ruby on Rails, é um framework full-stack para desenvolvimento de aplicações web com banco de dados backend baseado no padrão Model-View-Control. Simplificando, RHTML é uma combinação de HTML e Ruby onde o poder do script/programação Ruby está disponível para desenvolvedores web usando tags HTML.

## Formato de arquivo RHTML

Os arquivos RHTML são escritos em formato de texto simples como qualquer outro arquivo da Web baseado em texto. O código a ser executado está dentro de `<% %>` enquanto para saída, o código é escrito dentro de instruções `<%= %>`.

## Exemplo RHTML

O exemplo a seguir usa a combinação mais simples de HTML e Ruby on Rails para gerar o nome de cada produto de uma lista de produtos.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referências

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

