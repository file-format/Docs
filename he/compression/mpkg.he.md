{
  "date" : "2019-10-11",
  "keywords" :[ "קובץ mpkg", "פורמט קובץ mpkg", "מהו קובץ mpkg", "קובץ", "דוגמה ל-mpkg", "סיומת קובץ mpkg","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ MPKG - קובץ חבילת מטה",
  "description":"למד על פורמט קובץ MPKG וממשקי API שיכולים ליצור ולפתוח קובצי MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## מהו קובץ MPKG?

קובץ עם סיומת .mpkg הוא קובץ מתקין ארכיון, שנמצא בעיקר במערכות ההפעלה של MacOS. הוא מכיל את כל קבצי ההתקנה הנדרשים של היישום ללא צורך לשמור קבצים משויכים בנפרד. קובץ MPKG בודד יכול להכיל קבצי חבילה [PKG](/he/compression/pkg/) כאחד מקבצי ההתקנה בנוסף לקבצים אחרים. לא ניתן לפתוח קבצי MPKG עם תוכנה כללית כלשהי והם מופעלים אוטומטית ב-MacOS באמצעות Apple Installer.

## פורמט קובץ MPKG

קובץ MPKG מכיל סוגים שונים של קבצים הנדרשים להתקנה של מספר חבילות שהוא מכיל. ניתן לראות זאת מהתמונה למטה שהיא מבנה העץ של קובץ MPKG לדוגמה. מבנה עץ זה מיוצא באמצעות פקודת 'עץ' במסוף MacOS.

{{< figure src="../mpkg.png" alt="פורמט קובץ MPKG" >}}

התיאור של אלמנטים שונים בתמונה הוא כדלקמן.

`Packages Directory` - מאחסן רשימה של קבצי pkg, כלומר רשימה של תת-חבילות
`Resources Directory` - מאחסן משאבים המשמשים את pkg, כגון משאבים ותמונות מקומיות, מסמכי Rtf, מסמכי pdf וכו'.
`Distribution.dist file` - מסמך XML המכיל מידע כגון חבילות משנה להתקנה וסקריפטים בזמן ריצה

קובץ XML לדוגמה עבור קובץ MPKG יכול להיראות כדלקמן, בהתאם לחבילות המשנה המשויכות.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/he/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - היא חבילת המשנה שיש להתקין. זוהי ספרייה של מבנה החבילה בפורמט pkg. הוא מכיל תת ספריית תוכן.

## הפניות

* [חבילות שטוחות OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [מנהל חבילות C++ MPKG](https://github.com/puellavulnerata/mpkg)

