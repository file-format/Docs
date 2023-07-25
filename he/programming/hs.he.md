{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Haskell Script File Format",
  "description":"למד על מה זה פורמט קובץ HS וממשקי API שיכולים ליצור ולפתוח קובצי HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - פורמט קובץ Java HelpSet

## מהו קובץ Java HS?

קובץ עם סיומת .hs בשפת התכנות Java הוא קובץ תיעוד עזרה המשמש את מערכת JavaHelp כאשר הוא מופעל על ידי אפליקציה. הוא מגדיר את ערכת העזרה עבור היישום המסוים המותקן ומורכב ממספר קבוצות משנה כחלק מעזרת המערכת עבור היישום. תוכנית Java חייבת להיות מסוגלת למצוא את קובץ העזרה ששמו מסתיים בסיומת .hs.

## מידע על Java Helpset

קובץ .hs עשוי להכיל את המידע הבא.

|מידע|תיאור|
---|---|
|קובץ מפה|קובץ המפה משמש כדי לשייך מזהי נושאים לאיתור המשאב האחיד או לשם הנתיב של קבצי נושא של שפת סימון היפרטקסט.|
|הצג מידע|מידע המתאר את הנווטים המועסקים בתוך ערכת העזרה. הנווטים האיכותיים הם: תוכן עניינים, אינדקס וחיפוש בטקסט מלא. נווטים נוספים כוללים את הגלוס וגם את הנווטים המועדפים. נתונים לגבי נווטים מותאמים אישית מצורפים כאן עוד.|
<html>|כותרת העזרה|ה\<title> מתואר בתוך קובץ העזרה (.hs). כותרת זו נראית בחלון הגבוה ביותר ובכל החלונות המשניים המתוארים בקובץ העזרה שלך.| </html>
|מזהה בית|כותרת המזהה (ברירת המחדל) שמוצגת כאשר מתקשרים לשומר הסיוע מבלי לציין מזהה.|
|מצגת|החלונות שבהם ניתן להציג את נושאי הסיוע. זה יכול להיות כולל מודרני של תוכנית המחשב JavaHelp 2 המתוארת ביתר פירוט מתחת ל-\<presentation> .|
|Sub-helpsets|אזור שיקול דעת זה משלב סטטית ערכות עזרה אחרות על ידי שימוש בתג. ערכות העזרה המוצגות על ידי תג זה משולבות באופן טבעי לתוך ערכת העזרה המכילה את התג. נקודות עניין נוספות סביב מיזוג ניתן למצוא ב-Blending Helpsets.|
|יישום|מקטע שיקול דעת זה יוצר רישום שנותן מיפוי מידע מפתח כדי לאפיין את מחלקת HelpBroker לשימוש בשיטת HelpSet.createHelpBroker. כמו כן, הרישום מחליט מהצופה החומר ללקוח עבור מיון נתון של Emulate.|

## פורמט קובץ Java HS

קבצי Java HS הם בפורמט קובץ XML ומבוססים על ההמלצה המוצעת של World Wide Web Consortium (W3C) Extended Markiup Language [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). משמעות הדבר היא שקובץ Java HS הוא בפורמט קובץ XML קריא אנושי, שניתן לפתוח בכל יישום קורא XML.

### דוגמה לפורמט קובץ Java HS

להלן דוגמה לקובץ עזרה מ-[תיעוד Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## הפניות
* [קובץ ערכת עזרה של Oracle Java](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - פורמט קובץ סקריפט Haskell

## מהו קובץ HS?

קובץ עם סיומת .hs הוא קובץ Haskell Script שנכתב ב-[Haskell](https://wiki.haskell.org/Haskell), שפת תכנות מתקדמת פונקציונלית גרידא בקוד פתוח. קוד שנכתב בקובץ HS מבוסס אך ורק על פונקציות, שלא כמו [C](/he/programming/c/), [C++](/he/programming/cpp/) וכדומה, העוקבות אחר עקרונות הפיתוח המהיר של תוכנות חזקות ותמציתיות. Haskell מספקת מקביליות ומקבילות מובנית יחד עם ממשקי API עשירים, פרופילי וניפוי באגים כדי לייצר יישומים גמישים ואיכותיים.

## פורמט קובץ HS

כמו כל שפת תכנות, קבצי HS נכתבים בפורמט טקסט רגיל הניתנים לקריאה אנושית. ניתן ליצור, לערוך ולהציג אותם בכל כלי טקסט זמינים. קובץ קוד המקור .hs מורכב עם מהדר Haskell, ויוצר את הקובץ הבינארי הניתן להפעלה.

### דוגמה לפורמט קובץ HS

ניתן לכתוב קוד בקובץ .hs ולהרכיב באמצעות מהדר Haskell כגון [GHC](https://haskell.org/ghc). שורת הקוד הבאה נשמרת בתור `HelloWorld.hs` כפי שמוצג בדוגמה הבאה.

```
main = putStrLn "Hello, World!"
```

זה מורכב באמצעות הפקודה:

```
$ ghc -o hello hello.hs
```
וניתן להפעיל את קובץ ההפעלה המתקבל כ:

```
$ ./hello
```
זה מדפיס את ה"שלום, עולם!" הצהרה לפלט.

## הפניות

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell ב-5 צעדים פשוטים](https://wiki.haskell.org/Haskell_in_5_steps)

