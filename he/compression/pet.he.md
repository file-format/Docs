{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ PET - Puppy Linux Install Package File",
  "description":"למד על פורמט קובץ PET וממשקי API שיכולים ליצור ולפתוח קובצי PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## מהו קובץ Linux PET?

קובץ PET הוא קובץ חבילת התקנת יישומים שנוצר והשתמש בו עם גרסת PuppyLinux של מערכת ההפעלה לינוקס. הוא נוצר כקובץ [TGZ](/he/compression/tgz/) דחוס שמקטין את גודל הקובץ של הארכיון הדחוס. שלמות פורמט קובץ PET מובטחת על ידי סכום הבדיקה md5sum שצורף לסוף הקובץ לצורך אימות בקצה המרוחק. ניתן לחלץ קבצי PET באמצעות מחלץ הקבצים הסטנדרטי של TGZ ו-WinRAR. קובצי PET החליפו את קבצי ההתקנה של חבילת [PUP](/he/compression/pup/) הישנים.

## פורמט קובץ PET

קבצי PET נשמרים בדיסק כארכיונים דחוסים בפורמט קובץ בינארי. עם זאת, פרטי פורמט הקובץ הפנימי של פורמט קובץ PET אינם ידועים. בדומה לקובצי ההתקנה של חבילות [.exe](/he/executable/exe/) ו-[.msi](/he/executable/msi/), קובצי ה-PET מתחילים התקנה כאשר הם מבוצעים.

## הפניות

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [אינדקס של חבילות PET של PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

