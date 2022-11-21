{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","rhtml dosyası", "rhtml dosya formatı", "rhtml dosya türü", "dosya", "tür", "rhtml dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML Sayfası",
  "description":"RHTML dosya formatı ve RHTML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## RHTML dosyası nedir?

.rhtml uzantılı bir dosya, Ruby kodu veya betikleri içeren bir sunucu tarafı [HTML](/tr/web/html/) dosyasıdır. Kod, arka uçta çalışan Ruby on Rails kullanılarak sunucuda yürütülür. Ruby on Rails hakkında bilgisi olmayanlar için, Model-Görünüm-Kontrol modeline dayalı arka uç veritabanları ile web uygulamaları geliştirmeye yönelik tam yığın bir çerçevedir. Basitçe söylemek gerekirse, RHTML, HTML etiketlerini kullanan web geliştiricilerinin Ruby betik oluşturma/programlama gücünün mevcut olduğu HTML ve Ruby'nin bir kombinasyonudur.

## RHTML Dosya Biçimi

RHTML dosyaları, diğer metin tabanlı web dosyaları gibi düz metin biçiminde yazılır. Yürütülecek kod `<% %>` içine alınırken, çıktı için kod `<%= %>` deyimlerinin içine yazılır.

## RHTML Örneği

Aşağıdaki örnek, bir ürün listesinden her ürünün adını çıkarmak için HTML ve Ruby on Rails'in en basit birleşimini kullanır.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## Referanslar

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

