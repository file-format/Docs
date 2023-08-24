{
  "date" : "2021-04-08",
  "keywords" :[ "קובץ שוער", "פורמט קובץ שוער", "מהו קובץ משוט", "קובץ", "דוגמה לשער", "סיומת קובץ ארה", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"OAR - OpenSimulator Archive Format",
  "description":"למד על פורמט קובץ OAR וממשקי API שיכולים ליצור ולפתוח קובצי OAR.",
  "linktitle" : "OAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-15"
}

## מהו קובץ OAR?

קובץ עם סיומת .oar הוא קובץ ארכיון המשמש את אפליקציית OpenSimulator שהיא שרת אפליקציות תלת מימד בקוד פתוח ליצירת סביבה וירטואלית נגישה לריבוי משתמשים דרך הרשת. פורמט הקובץ OAR מספק נתוני נכסים הדרושים לטעינה מלאה של השטח, מרקמי האובייקט והמלאי במערכת אחרת. ל-OpenSimulator יש גם hypergrid אופציונלי המאפשר למשתמשים לבקר בהתקנות אחרות של OpenSimulator ברחבי האינטרנט. לקובצי OAR יש יישום/אואר מסוג MIME באינטרנט והם מכילים קובץ אחד או יותר בארכיון.


## פורמט קובץ OAR

OAR הם קבצים בינאריים המאוחסנים בפורמט קובץ ארכיון דחוס. הגרסה העדכנית ביותר של פורמט קובץ OAR היא [גרסה 1.0](http://opensimulator.org/wiki/OAR_Format_1.0) שיש בה שינויים גדולים לעומת [גרסה.8](http://opensimulator.org/wiki/OAR_Format_0.8) הקודמת שלה .הגרסה האחרונה תומכת באחסון מספר אזורים ב-OAR יחיד ואינה תואמת לאחור עם גרסאות של OpenSimulator לפני 0.7.5. קובץ OAR הוא קובץ tar עם gzip (tar.gz) בפורמט ה-unix tar המקורי (לא USTAR).

## דוגמה אזורי OAR
קבצי AOR יכולים להכיל מספר אזורים. מבנה הארכיון הוא כדלקמן (דוגמה זו מכילה 4 אזורים):

```
archive.xml
assets/
regions/
  1_1_Arizona/
    landdata/
    objects/
    settings/
    terrain/
  2_1_New_Mexico/
    landdata/
    objects/
    settings/
    terrain/
  1_2_Utah/
    landdata/
    objects/
    settings/
    terrain/
  2_2_Colorado/
    landdata/
    objects/
    settings/
    terrain/
```
## OAR Archive.xml

קובץ בקרת הארכיון מכיל מספר גרסה ראשי להגדרת תאימות לשינויי פורמט עתידיים. הנוכחות של נכסים בפורמט OAR מסומנת על ידי האלמנט הבוליאני<assets_included> . מידע על האזורים הכלולים כלול במניפסט הקיים בקובץ הבקרה. דוגמה של Archive.xml היא כדלקמן.

```
<?xml version="1.0" encoding="utf-16"?>
<archive major_version="1" minor_version="0">
  <creation_info>
    <datetime>1343204139</datetime>
  </creation_info>
  <assets_included>True</assets_included>
  <regions>
    <row>
      <region>
        <id>12345678-1111-1111-1111-111111111111</id>
        <dir>1_1_Arizona</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-2222-2222-2222-222222222222</id>
        <dir>2_1_New_Mexico</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
    <row>
      <region>
        <id>12345678-3333-3333-3333-333333333333</id>
        <dir>1_2_Utah</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
      <region>
        <id>12345678-4444-4444-4444-444444444444</id>
        <dir>2_2_Colorado</dir>
        <is_megaregion>False</is_megaregion>
        <size_in_meters>256,256</size_in_meters>
      </region>
    </row>
  </regions>
</archive>
```

## הפניות

* [פורמט OAR v 1.0](http://opensimulator.org/wiki/OAR_Format_1.0)
* [OpenSimulator](http://opensimulator.org/wiki/Main_Page)

