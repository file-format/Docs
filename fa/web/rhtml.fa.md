{
  "date": "2021-05-24",
  "keywords": [
"rhtml",
"فایل rhtml",
"فرمت فایل rhtml",
"نوع فایل rhtml",
"فایل",
"نوع",
"فایل rhtml چیست"
]،
  "author": {
    "display_name": "Kashif Iqbal"
}،
  "draft": "false",
  "toc": true,
  "title": "RHTML - صفحه HTML روبی",
  "description": "درباره فرمت فایل RHTML و APIهایی که می توانند فایل های RHTML ایجاد و باز کنند، بیاموزید.",
  "linktitle": "RHTML",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-rhtm-fal"
}
}،
  "lastmod": "2021-05-24"
}

## فایل RHTML چیست؟

فایلی با پسوند rhtml. یک فایل [HTML](/web/html/) سمت سرور است که حاوی کد یا اسکریپت های روبی است. کد بر روی سرور با استفاده از Ruby on Rails اجرا می شود که در باطن اجرا می شود. برای کسانی که در مورد Ruby on Rails نمی‌دانند، این یک چارچوب تمام پشته برای توسعه برنامه‌های کاربردی وب با پایگاه‌های داده پشتیبان بر اساس الگوی Model-View-Control است. به زبان ساده، RHTML ترکیبی از HTML و Ruby است که در آن قدرت اسکریپت‌نویسی/برنامه‌نویسی Ruby در دسترس توسعه‌دهندگان وب با استفاده از تگ‌های HTML است.

## فرمت فایل RHTML

فایل های RHTML در قالب متن ساده مانند سایر فایل های وب مبتنی بر متن نوشته می شوند. کدی که باید اجرا شود در «<% %>» محصور می‌شود، در حالی که برای خروجی، کد در داخل دستورات «<%= %>» نوشته می‌شود.

## مثال RHTML

مثال زیر از ساده ترین ترکیب HTML و Ruby on Rails برای خروجی نام هر محصول از لیست محصولات استفاده می کند.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## منابع

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)


