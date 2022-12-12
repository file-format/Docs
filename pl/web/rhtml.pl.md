{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","plik rhtml", "format pliku rhtml", "typ pliku rhtml", "plik", "typ", "co to jest plik rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Rubinowa strona HTML",
  "description":"Poznaj format plików RHTML i interfejsy API, które mogą tworzyć i otwierać pliki RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## Czym jest plik RHTML?

Plik z rozszerzeniem .rhtml to plik [HTML](/pl/web/html/) po stronie serwera, który zawiera kod Ruby lub skrypty. Kod jest wykonywany na serwerze za pomocą Ruby on Rails działającego na zapleczu. Dla tych, którzy nie znają Ruby on Rails, jest to pełny framework do tworzenia aplikacji internetowych z backendowymi bazami danych opartymi na wzorcu Model-View-Control. Mówiąc najprościej, RHTML to połączenie HTML i Ruby, w którym moc skryptów/programowania w Ruby jest dostępna dla twórców stron internetowych za pomocą znaczników HTML.

## Format pliku RHTML

Pliki RHTML są zapisywane w formacie zwykłego tekstu, podobnie jak inne tekstowe pliki internetowe. Kod do wykonania jest zawarty w `<% %>`, podczas gdy kod wyjściowy jest zapisany w instrukcjach `<%= %>`.

## Przykład RHTML

Poniższy przykład wykorzystuje najprostszą kombinację HTML i Ruby on Rails do wyprowadzenia nazwy każdego produktu z listy produktów.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Bibliografia

* [TutorialsPoint — Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

