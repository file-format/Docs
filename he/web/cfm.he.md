{
  "date" : "2021-07-13",
  "keywords" :[ "CFM", "הרחבה", "קובץ", "פורמט", "מערכת", "שפת סימון קר פיוז'ן", "שפה", "דפי אינטרנט של CFM", "מנוע CFML", "CFML" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFM - Cold Fusion Markup",
  "description":"למד על פורמט קובץ CFM וממשקי API שיכולים ליצור ולפתוח קובצי CFM.",
  "linktitle" : "CFM",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-07-13"
}

## מהו קובץ CFM? ##

דפי האינטרנט והקבצים המשמשים ב-**Cold Fusion Markup Language** מכילים הרחבות של CFM ונקראים דפי אינטרנט CFM. שפת סקריפטים זו לפיתוח אתרים פועלת על Google App Engine, .NET framework ו-JVM. זה יכול להכיל שפת תכנות או קוד של השפה. כאשר המשתמש ניגש לכל אחד מהדפים שלו, שרת האינטרנט של ColdFusion מבצע זאת. ניתן להשתמש ב-CFScript (שקרוב ל-JavaScript) או בתגים כדי לכתוב CFML. ניתן להשתמש ב-CFML ליצירת שפות אחרות מלבד [HTML](/he/web/html/) כמו [CSS](/he/web/css/), [JavaScript](/he/web/js/), [XML](/he/web/xml/), ועוד.

השימוש בשפה זו ובתגים שהיא תומכת בהם הוא בעיקר בפיתוח יישומי אינטרנט דינמיים ניתן להפעיל את הקבצים ישירות בדפדפן באופן מקוון אם מתרחשת שגיאה כלשהי במהלך שימוש לא מקוון בפלטפורמת הפיתוח של האפליקציה.
 

CFML פועל באופן שבו סיומות קבצי שרת ספציפיות (.cfc, .cfm) ניתנות לעיבוד למנוע CFML. אם המנועים מבוססים על Java, זה מושג באמצעות servlets של Java. המנוע של CFML מעבד רק פונקציות ותגיות והוא מחזיר פונקציות וטקסט מחוץ לתגיות CFML לשרת האינטרנט ללא כל שינוי.


## היסטוריה קצרה ##

בשנת 1995, הוא נוצר לראשונה על ידי תאגיד בשם Allaire. בשנת 2005 Adobe רכשה אותו והיא מספקת שירותים לפיתוח ColdFusion עד היום. בשנים שחלפו, הוא התפתח ושודרג על ידי אנשים וחברות רבות. בשנת 2012 הושקה קרן בשם OpenCFML. מאוחר יותר, בשנת 2015 Railo לשעבר סיפק את שירותיו כדי לשפר את הביצועים של CFM והפחית את המשאבים לפונקציונליות טובה יותר. העדכון האחרון שלו הושק בשנת 2020 שהוכרז על המשך עד 2028.

## פורמט קובץ CFM ##

הקוד של קבצי ה-CFM ודפי האינטרנט מורכב בעיקר מהתגים כמו HTML אבל עם הבדל קל. קבצים אלו אחראים לביצוע פעולות שונות שסקריפטים של ColdFusion מאפשרים להפעיל.
* ניתן לגשת לקבצים הללו ולהפעיל אותם ישירות ב-Windows וב-macOS באמצעות הדפדפן של כל מערכת הפעלה.
* Adobe ColdFusion מספקת את הפלטפורמה לפיתוח דפי אינטרנט ויישומים דינמיים במחשב.
* כל עורך טקסט כמו NotePad או כל עורך טקסט אחר במערכת הפעלה יכול לשמש לפתיחת קבצים אלה מכיוון שקבצים אלה מבוססים על טקסט.
* כאשר כל קובץ CFM נפתח בעורך טקסט הוא מציג קוד שמורכב מהתגים והסקריפטים שאדם לא יבין אלא אם הוא מפתח אינטרנט.

## דוגמה לשימוש ב-CFM ##

להלן מוצג קובץ CFM לדוגמה לשימוש פשוט.

### מסמך CFM ###

```html
<!--- temperature.cfc --->
<cfcomponent>
  <cffunction name="FtoC" access="public" returntype="numeric">
    <cfargument name="fahrenheit" required="yes" type="numeric" />
    <cfset answer= (fahrenheit - 32)*100/180 />
    <cfreturn answer />
  </cffunction>
</cfcomponent>
<!--- test.cfm --->
<cfset fDegrees = 212 />
<cfinvoke component="temperature" method="FtoC" returnvariable="result">
  <cfinvokeargument name="fahrenheit" value="#fDegrees#" />
</cfinvoke>
<cfoutput>#fDegrees#&deg;F = #result#&deg;C</cfoutput> <br />
```

## הפניות ##

- [CFM - ויקיפדיה](https://en.wikipedia.org/wiki/ColdFusion_Markup_Language)

