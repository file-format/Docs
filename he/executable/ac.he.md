{
  "date" : "2023-01-11",
  "keywords" : ["ac file", "what is an aci file", "file", "how to open ac file", "ac file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "למד על פורמט קבצי AC וממשקי API שיכולים ליצור ולפתוח קבצי ACCDB.",
  "title" : "פורמט קובץ AC - קובץ סקריפט אוטומטי",
  "linktitle" : "AC",
  "menu" : {
    "docs" : {
      "identifier":"executable-ac-he",
      "parent" : "executable"
}
},
  "lastmod" : "2020-01-11"
}

## מהו קובץ AC?

קובץ AC הוא קובץ הסקריפט Autoconf. **Autoconf** היא חבילה הניתנת להרחבה של פקודות מאקרו M4 המייצרות סקריפטים של מעטפת כדי להגדיר באופן אוטומטי חבילות קוד מקור תוכנה. סקריפטים אלו יכולים להתאים את החבילות לסוגים רבים של מערכות דמויות UNIX ללא התערבות ידנית של המשתמש. Autoconf יוצר סקריפט תצורה עבור חבילה מקובץ תבנית המפרט את תכונות מערכת ההפעלה בהן החבילה יכולה להשתמש, בצורה של קריאות מאקרו M4.

Producing configuration scripts using Autoconf requires GNU M4. עליך להתקין את GNU M4 (לפחות גרסה 1.4.6, אם כי מומלצת 1.4.13 ואילך) לפני הגדרת Autoconf, כך שסקריפט התצורה של Autoconf יוכל למצוא אותו. סקריפטי התצורה המיוצרים על ידי Autoconf הם עצמאיים, כך שהמשתמשים שלהם אינם צריכים להיות בעלי Autoconf (או GNU M4).

## איך פותחים קובץ AC?

AC קיצור של תצורה אוטומטית. זהו סקריפט שנוצר על ידי GNU Autoconf המאפשר להתאים את קוד מקור התוכנה למערכות שונות דמויות Posix על ידי בדיקת תכונות נחוצות בחבילה. הסקריפט נקרא קובץ AC.

## רכיבי כלי אוטומטי עיקריים

An understanding of GNU autotools (`automake`, `autoconf` etc.) can be useful when working with ebuilds:

Autotools הוא אוסף של חבילות קשורות אשר, כאשר משתמשים בהן יחד, מסירות חלק גדול מהקושי הכרוך ביצירת תוכנה ניידת. כלים אלה, יחד עם כמה קבצי קלט פשוטים יחסית שסופקו במעלה הזרם, משמשים ליצירת מערכת הבנייה עבור חבילה.

**סקירה בסיסית של האופן שבו מרכיבי הכלים האוטומטיים מתאימים זה לזה.**

![A basic overview of how the main autotools components fit together](https://devmanual.gentoo.org/general-concepts/autotools/diagram.png "A basic overview of how the main autotools components fit together")

בהגדרה פשוטה:

- תוכנית `autoconf` מייצרת סקריפט תצורה מ-`configure.in` או `configure.ac`.
- תוכנית `automake` מייצרת Makefile.in מתוך Makefile.am.
- הסקריפט `configure` מופעל כדי לייצר קובץ Makefile אחד או יותר מקבצי Makefile.in.
- תוכנית `make` משתמשת ב-Makefile כדי להדר את התוכנית.

## הפניות
* [Autoconf Software](https://www.gnu.org/software/autoconf/)
* [היסודות של הכלים האוטומטיים](https://devmanual.gentoo.org/general-concepts/autotools/index.html)



