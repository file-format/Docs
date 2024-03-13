{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"rhtml faylı",
"rhtml fayl formatı",
"rhtml fayl növü",
"fayl",
"növü",
"rhtml faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RHTML - Ruby HTML Səhifəsi",
  "description": "RHTML fayl formatı və RHTML faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-azl"
}
},
  "lastmod": "2021-05-24"
}

## RHTML faylı nədir?

.rhtml uzantılı fayl Ruby kodu və ya skriptləri ehtiva edən server tərəfindəki [HTML](/web/html/) faylıdır. Kod serverdə arxa tərəfdə işləyən Ruby on Rails istifadə edərək icra olunur. Ruby on Rails haqqında məlumatı olmayanlar üçün bu, Model-View-Control modelinə əsaslanan backend verilənlər bazası ilə veb proqramlar hazırlamaq üçün tam stekli çərçivədir. Sadəcə olaraq, RHTML HTML və Ruby birləşməsidir, burada Ruby scripting/proqramlaşdırma gücü HTML teqlərindən istifadə edən veb tərtibatçıları üçün mövcuddur.

## RHTML fayl formatı

RHTML faylları hər hansı digər mətn əsaslı veb faylları kimi düz mətn formatında yazılır. İcra ediləcək kod `<% %>` daxilində, çıxış üçün isə kod `<%= %>` ifadələrinin içərisində yazılır.

## RHTML nümunəsi

Aşağıdakı nümunə məhsullar siyahısından hər bir məhsulun adını çıxarmaq üçün HTML və Ruby on Rails-in ən sadə birləşməsindən istifadə edir.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## İstinadlar

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


