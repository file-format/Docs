{
  "date" : "2021-06-24",
  "keywords" :[ "RSS", "חלקי", "הרחבה", "קובץ", "פורמט", "אינטרנט", "הפצה ממש פשוטה", "תוכנת Userland" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RSS - Really Simple Syndication",
  "description":"למד על פורמט קובץ RSS וממשקי API שיכולים ליצור ולפתוח קובצי RSS.",
  "linktitle" : "RSS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-06-24"
}

## מהו קובץ RSS? ##

קובץ עם הסיומת rss ידוע בשם Really Simple Syndication. RSS הוא סוג קובץ שנקרא בקלות או בקלות על ידי המחשב, קובץ ה-XML. קובצי XML אלה מתעדכנים אוטומטית עם כל שינוי בנתונים או עדכונים של אתר אינטרנט או דף אינטרנט. המידע המעודכן יחד עם המטא נתונים (שם המחבר, שם המפרסם, תאריך פרסום וכו'), ותכני אינטרנט אחרים של האתר נשלפים על ידי קבצי ה-RSS של המשתמש ומוצגים בפורמט קל לקריאה. התכונה הטובה ביותר של קבצי RSS אלה היא שהם פועלים בזמן אמת, והעדכונים, החדשות, הפרסומים, כלומר האחרונים, מוצגים בראש הקובץ. באמצעות קובץ RSS, אתה יכול בקלות ליצור קובץ המכיל את העדכונים האחרונים של כל נושא שאתה מעוניין בו, על ידי שליפת התוכן הקשור מהאינטרנט וקריאתו באמצעות קובץ RSS.

## היסטוריה קצרה ##

על בשרו, קובץ ה-RSS נוצר לראשונה על ידי נטסקייפ, הם המציאו את הגרסה הראשונה של קובץ ה-RSS אבל אז נטשו את הרעיון, ולא המשיכו עם גרסאות חדשות יותר. זו הייתה אז **Userland Software** שעבדה על פורמט קובץ ה-RSS והמשיכה לחדש אותו עם גרסה חדשה יותר, כך הגיעה לשוק RSS v2. עם זאת, ניתן לקשר את המצאת ה-RSS בחזרה ל-Resource Description Framework, מאת Ramanathan V בשנת 1997. פעולתם של שני הקבצים די דומות, וניתן להניח שהמושג RSS נוצר על סמך פעולתו של RDF, קורא קבצים ששימש לאיסוף מטא נתונים.

## מפרט טכני ##

קובץ ה-RSS הוא סוג של קובץ XML וכל קבצי ה-RSS חייבים לעמוד בסטנדרטים של XML 1.0. ישנן גרסאות שונות של קבצי RSS שונים, כגון 0.91, 0.92, 2.0, בין היתר. הקובץ של כל גרסה תואם למפרטים ולסטנדרטים של אותה גרסה ספציפית.

## דוגמה ל-RSS ##

להלן דוגמה פשוטה של RSS.

```
<?xml version="1.0" encoding="UTF-8" ?>
<rss version="2.0">
	<channel>
		<title>RSS Title</title>
		<description>This is a simplified example of the RSS feed</description>
		<link>https://blog.fileformat.com/</link>
		<copyright>2021 fileformat.com All rights reserved</copyright>
		<lastBuildDate>Wed, 22 Jun 2021 00:01:00 +0000</lastBuildDate>
		<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		<ttl>1800</ttl>
		<item>
			<title>Example entry</title>
			<description>Here is some text containing an interesting description.</description>
			<link>https://blog.fileformat.com/blog/post/1</link>
			<guid isPermaLink="false">9bd605d5-1921-8i67-dgft-65g635d3587u</guid>
			<pubDate>Wed, 22 Jun 2021 16:20:00 +0000</pubDate>
		</item>
	</channel>
</rss>

```
## התייחסות ##

* [RSS - WIKIPEDIA](https://en.wikipedia.org/wiki/RSS)
