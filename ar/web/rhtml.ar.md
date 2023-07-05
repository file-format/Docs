{
  "date" : "2021-05-24",
  "keywords" :["rhtml", "rhtml file", "rhtml file format", "rhtml file type", "file", "type", "what is a rhtml file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - صفحة HTML روبي" ,
  "description":"تعرف على تنسيق ملف RHTML وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات RHTML وفتحها." ,
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
} ,
  "lastmod" : "2021-05-24"
}

## ما هو ملف RHTML؟

الملف بامتداد .rhtml هو ملف من جانب الخادم [HTML](/ar/web/html/) يحتوي على كود Ruby أو نصوص برمجية. يتم تنفيذ الكود على الخادم باستخدام Ruby on Rails الذي يعمل في الواجهة الخلفية. بالنسبة لأولئك الذين لا يعرفون عن Ruby on Rails ، فهو إطار عمل متكامل لتطوير تطبيقات الويب مع قواعد بيانات الخلفية بناءً على نمط Model-View-Control. ببساطة ، RHTML عبارة عن مزيج من HTML و Ruby حيث تتوفر قوة البرمجة النصية / البرمجة Ruby لمطوري الويب باستخدام علامات HTML.

## تنسيق ملف RHTML

تتم كتابة ملفات RHTML بتنسيق نص عادي مثل أي ملفات ويب نصية أخرى. يتم تضمين الكود المراد تنفيذه داخل `<٪٪>` بينما بالنسبة للإخراج ، تتم كتابة الكود داخل عبارات `<٪ =٪>`.

## مثال RHTML

يستخدم المثال التالي أبسط تركيبة من HTML و Ruby on Rails لإخراج اسم كل منتج من قائمة المنتجات.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## مراجع

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

