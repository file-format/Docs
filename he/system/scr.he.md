{
  "date" : "2021-07-13",
  "keywords" :[ "קובץ scr", "מהו קובץ scr", "קובץ", "דוגמה ל-scr", "סיומת קובץ scr","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SCR - קובץ שומר מסך של Windows",
  "description":"למד על פורמט קובץ SCR וממשקי API שיכולים ליצור ולפתוח קובצי SCR.",
  "linktitle" : "SCR",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-13"
}

## מהו קובץ SCR?
קובץ עם סיומת .scr הוא קובץ שומר מסך המשמש את מערכת ההפעלה Microsoft Windows. הוא כולל אנימציות, גרפיקה, מצגת שקופיות או וידאו שיכולים לשמש כשומר מסך של Windows. קבצי SCR מאוחסנים בדרך כלל בספרייה הראשית של Microsoft Windows. שומרי המסך היו אמורים למנוע מצגי מחשב CRT או פלזמה לסבול ממצב המתרחש כאשר המסך מציג את אותה תמונה במשך זמן רב מדי. אמנם, המסכים העדכניים ביותר אינם סובלים במצב כזה, אך שומרי המסך עדיין משמשים כדי למנוע את המסך מסיבות אבטחה.

## פורמט קובץ SCR
שומר מסך הוא תוכנת מחשב שממלאת אותו בתמונות מונפשות או דפוסים כאשר לא מתבצעת פעילות במחשב במשך זמן רב. שומרי המסך הוצגו כדי למנוע צריבת זרחן בפלזמה, צגי מחשב קתודית (CRT) ו-OLED. שומרי מסך מוגדרים בדרך כלל להחיל שכבת אבטחה בסיסית, על ידי דרישת סיסמה כדי לפתוח מחדש את המכשיר. שומרי מסך מפותחים ומקודדים בדרך כלל באמצעות שפות תכנות שונות כמו גם ממשקים גרפיים. בעיקר מפתחי שומרי מסך משתמשים בשפות התכנות C או C++, יחד עם ספריות גרפיות או GDIs, כגון OpenGL, שעובדת על פלטפורמות רבות המסוגלות לעיבוד תלת מימד. הפלט של שומרי המסך נשמר כקובץ הפעלה נייד.

### שימוש בקובץ SCR
במסכים מבוססי CRT או פלזמה הישנים דווח על צריבת המסך מכיוון שאותה תמונה הוצגה על המסך במשך תקופה ארוכה. צריבת המסך היא מקרה שבו המאפיינים של האזורים החשופים של ציפוי זרחן בתוך המסך משתנים בהדרגה ובסופו של דבר מובילים לתמונת צל כהה על המסך. אז שומרי המסך היו אמורים לשנות את תמונת המסך ברציפות ובדרך כלל הם קבצי .scr היו חיוניים לצגים של מכונות כרטוס כספומט או רכבת. מאוחר יותר, מסכי LCD וגרסאות מתקדמות יותר של מסכים פתרו את הבעיה. לכן שומרי המסך עדיין משמשים בעידן המודרני כדי להגן על המכשירים הבלתי פעילים מפני שימוש בגוף שני. זה דורש את הסיסמה או התבנית כדי לגשת מחדש למכשיר.

## יצירת שומר מסך באמצעות C#
למרות שאנו יכולים ליצור שומר מסך בכל אחת משפות התכנות NET, כאן ניתנת שפת התכנות C#:

```
class MyCoolScreensaver : Screensaver
{
   public MyCoolScreensaver()
   {
      Initialize += new EventHandler(MyCoolScreensaver_Initialize);
      Update += new EventHandler(MyCoolScreensaver_Update);
      Exit += new EventHandler(MyCoolScreensaver_Exit);
   }

   void MyCoolScreensaver_Initialize(object sender, EventArgs e)
   {
   }

   void MyCoolScreensaver_Update(object sender, EventArgs e)
   {
      Graphics0.Clear(Color.Black);
      Graphics0.DrawString(
         DateTime.Now.ToString(),
         SystemFonts.DefaultFont, Brushes.Blue,
         0, 0);
   }

   void MyCoolScreensaver_Exit(object sender, EventArgs e)
   {
   }

   [STAThread]
   static void Main()
   {
      Screensaver ss = new MyCoolScreensaver();
      ss.Run();
   }
}
```
שנה את הסיומת של קובץ ההפעלה מ-.exe ל-.scr. אז ניתן לקרוא לקובץ SCR בשם ScreenSaver.scr.

## הפניות

* [שומר מסך](https://en.wikipedia.org/wiki/Screensaver)
* [כתוב שומר מסך שבאמת עובד](https://www.codeproject.com/Articles/14081/Write-a-Screensaver-that-Actually-Works)


