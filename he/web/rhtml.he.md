{
  "date" : "2021-05-24",
  "keywords" :[ "rhtml","קובץ rhtml", "פורמט קובץ rhtml", "סוג קובץ rhtml", "קובץ", "סוג", "מהו קובץ rhtml" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RHTML - Ruby HTML Page",
  "description":"למד על פורמט קבצי RHTML וממשקי API שיכולים ליצור ולפתוח קובצי RHTML.",
  "linktitle" : "RHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-05-24"
}

## מהו קובץ RHTML?

קובץ עם סיומת rhtml הוא קובץ [HTML](/he/web/html/) בצד השרת המכיל קוד או סקריפטים של רובי. הקוד מבוצע בשרת באמצעות Ruby on Rails הפועל בקצה האחורי. למי שלא יודע על Ruby on Rails, זוהי מסגרת מלאה לפיתוח אפליקציות אינטרנט עם מסדי נתונים עורפיים המבוססים על דפוס Model-View-Control. במילים פשוטות, RHTML הוא שילוב של HTML ו-Ruby שבו הכוח של רובי סקריפטים/תכנות זמין למפתחי אינטרנט המשתמשים בתגי HTML.

## פורמט קובץ RHTML

קובצי RHTML נכתבים בפורמט טקסט רגיל כמו כל קבצי אינטרנט מבוססי טקסט אחרים. הקוד לביצוע מוקף בתוך `<% %>` בעוד עבור פלט, הקוד כתוב בתוך הצהרות `<%= %>`.

## דוגמה ל-RHTML

הדוגמה הבאה משתמשת בשילוב הפשוט ביותר של HTML ו-Ruby on Rails כדי להוציא את השם של כל מוצר מרשימת מוצרים.
```
<ul>
   <% @products.each do |p| %>
      <li><%=  @p.name %></li>
   <% end %>
</ul>
```
## הפניות

* [TutorialsPoint - Ruby on Rails](https://www.tutorialspoint.com/ruby-on-rails/rails-and-rhtml.htm)

