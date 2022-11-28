{
  "date" : "2021-01-20",
  "keywords" :["xslt", "קובץ", "הרחבה", "פורמט קובץ", "הרחבת קובץ", "שפת גיליון סגנונות הרחבה"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ XSLT",
  "description":"למד על פורמט קובץ XSLT וממשקי API שיכולים ליצור ולפתוח קובצי XSLT.",
  "linktitle" : "XSLT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-01-20"
}

## מהו קובץ XSLT?

קובץ עם סיומת .xslt הוא קובץ Transformation Language של גיליון סגנונות להרחבה המשמש להמרה ולסגנון של קובץ XML באמצעות הוראות XSL. הפורמט משמש להפיכת מסמכי XML לפורמטי פלט סטנדרטיים כגון מסמך טקסט או דף אינטרנט .html. טרנספורמציה זו יוצרת מסמך חדש המבוסס על התוכן של מסמך ה-XML הקיים. XSLT הופך אותו ליכול תיאורטית לחישובים שרירותיים.

## פורמט קובץ XSLT

פורמט הקובץ XLST מכיל הוראות טרנספורמציה בפורמט טקסט רגיל שניתן לראות בכל עורך טקסט. היו שלושה תיקונים לשפה.

* `XSLT 1.0` - XSLT 1.0 פורסם כהמלצת W3C בנובמבר 1999.
* `XSLT 2.0` - הוא כולל שינויים כגון מניפולציה של מחרוזות באמצעות ביטויים רגולריים, פונקציות ואופרטורים למניפולציה של תאריכים, שעות ומשכי זמן, מסמכי פלט מרובים, קיבוץ ומערכת סוגים עשירה יותר ובדיקת סוגים חזקה.
* `XSLT 3.0` - זה הפך לחלק מהמלצת W3C ב-8 ביוני 2017 והתכונות החדשות העיקריות כוללות שינוי סטרימינג, חבילות לשיפור המודולריות של גיליונות סגנונות גדולים, טיפול משופר בשגיאות דינמיות עם, למשל, הוראת xsl:try, ותמיכה במפות ומערכים, מה שמאפשר ל-XSLT לטפל ב-JSON וגם ב-XML.

### XSLT דוגמה

הדוגמה הבאה לקוחה מ-[w3schools](https://www.w3schools.com/xml/xsl_intro.asp).
```
<?xml version="1.0"?>

<xsl:stylesheet version="1.0"
xmlns:xsl="http://www.w3.org/1999/XSL/Transform">

<xsl:template match="/">
  <html>
  <body>
    <h2>My CD Collection</h2>
    <table border="1">
      <tr bgcolor="#9acd32">
        <th>Title</th>
        <th>Artist</th>
      </tr>
      <xsl:for-each select="catalog/cd">
        <tr>
          <td><xsl:value-of select="title"/></td>
          <td><xsl:value-of select="artist"/></td>
        </tr>
      </xsl:for-each>
    </table>
  </body>
  </html>
</xsl:template>

</xsl:stylesheet>
```
## הפניות ##

* [XSLT - מאת ויקיפדיה](https://en.wikipedia.org/wiki/XSLT)
* [אלמנטים XSLT](https://en.wikipedia.org/wiki/XSLT_elements)

