{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ ADM - פורמט קובץ תבנית ניהולי",
  "description":"למד על פורמט קובץ ADM וכיצד לפתוח קבצי ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## מהו קובץ ADM?

קובץ ADM הוא קובץ תבנית המשמש את תוכנת Microsoft Group Policies לציון המיקום של הגדרות מדיניות מבוססות רישום בקובץ הרישום. הוא משמש את מנהלי המערכת כדי להגדיר את המדיניות לניהול קבוצת מחשבים שהם חלק מהקבוצה. מידע זה הופך לחלק מאובייקטי המדיניות הקבוצתית (GPOs) שנוצרו לניהול הקבוצה.

אתה יכול לפתוח קובצי ADM באמצעות Microsoft Group Policy Object Editor.

## פורמט קובץ ADM - מידע נוסף

קבצי ADM מאוחסנים כקבצי טקסט בפורמט Unicode. אלה שימשו בעיקר כדי לתאר את המיקום של הגדרות מדיניות מבוססות רישום ברישום של Windows Vista ו-Windows 7.

קובצי ADM אינם נתמכים יותר והם הוחלפו בקבצי [ADMX](/he/system/admx/). GPA מתעלם מקובצי ברירת המחדל הבאים של ADM במחשבים שבהם פועל Microsoft Windows Vista Service Pack 1 ואילך.

* system.adm
* inetres.adm
* conf.adm
* wmplayer.adm
* wuau.adm

## הפניות

* [קבצי תבנית ניהול - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - ניהול קבצי תבניות ניהוליות](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

