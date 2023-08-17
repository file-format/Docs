{
  "date" : "2019-10-11",
  "keywords" :[ "xbrl", "קובץ xbrl", "פורמט קובץ xbrl", "סוג קובץ xbrl", "קובץ", "סוג", "מהו קובץ xbrl" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XBRL - פורמט קובץ דיווח עסקי ופיננסי",
  "description":"למד על פורמט קובץ XBRL וממשקי API שיכולים ליצור ולפתוח קובצי XBRL.",
  "linktitle" : "XBRL",
  "menu" : {
    "docs" : {
      "identifier":"finance-xbrl",
      "parent" : "finance"
}
},
  "lastmod" : "2021-02-25"
}

## מהו קובץ XBRL?

קובץ עם סיומת ‎.xbrl (eXtensible Business Reporting Language) הוא מסגרת זמינה וגלובלית באופן חופשי להחלפת מידע עסקי. כיום הוא נמצא בשימוש נרחב כאחד מהפורמטים הסטנדרטיים שהחליף את הדוחות הישנים יותר מבוססי נייר ברשומות דיגיטליות שימושיות ומדויקות יותר. נתונים שהוחלפו באמצעות קובצי XBRL כוללים פנקסי חשבונות, פרטים פיננסיים ומאזנים. הוא תומך בתגי נתונים המאפשרים עיבוד נתונים מהכנה ועד שלב הניתוח של מידע עסקי מכל הסוגים. ניתן לפתוח קובצי XBRL באמצעות תוכנה כגון Rivet Software Dragon View XBRL Viewer וממשקי API כמו [Aspose.Finance](https://products.aspose.com/finance/).

## פורמט קובץ XBRL

XBRL הוא תקן בינלאומי פתוח לדיווח עסקי דיגיטלי שנמצא בשימוש נרחב ברחבי העולם. זוהי שפה מבוססת [XML](/he/web/xml/) המשתמשת ברכיבי XBRL, הידועים בתור תגים, כדי לתאר כל פריט של נתונים עסקיים כדי לגבש נתונים למיון וניתוח דוחות. מפרטי פורמט הקובץ XBRL מפותחים ומתפרסמים על ידי XBRL International, Inc, עם [XBRL גרסה 2.1](https://specifications.xbrl.org/work-product-index-group-base-spec-base-spec.html) כרגע זמין למשתמשים.

### מבנה מסמך XBRL

מידע מלא על [תגי XBRL 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html) מתכנתים יכולים להפנות לכתיבת יישומים לעבודה בפורמט קובץ זה. XBRL מורכב ממופע XBRL ומאוסף של טקסונומיות.

**`XBRL Instance`** - מופע XBRL מתחיל ב-<xbrl> אלמנט שורש. מסמך XML גדול יכול להכיל יותר ממופע XBRL אחד המוטבע בו.

**`טקסונומיה XBRL`** - [טקסונומיה XBRL](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html#_5) מוגדר כמבני סכימת XML ומערכת של רכיב קישורים חיצוניים עם הפניה ישירה. סכימת טקסונומיה ניתנת להרחבה המציגה את ההפניות ל-linkbase היא כדלקמן.

```
<schema
  xmlns:link="http://www.xbrl.org/2003/linkbase"
  xmlns:ci="http://www.mycompany.com/taxonomy/2003-10-19"
  xmlns="http://www.w3.org/2001/XMLSchema" targetNamespace="http://www.mycompany.com/taxonomy/2003-10-19">
<annotation>
<appinfo>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_presentation.xml" xlink:role="http://www.xbrl.org/2003/role/presentationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_calculation.xml" xlink:role="http://www.xbrl.org/2003/role/calculationLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_definition.xml" xlink:role="http://www.xbrl.org/2003/role/definitionLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_label.xml" xlink:role="http://www.xbrl.org/2003/role/labelLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
<link:linkbaseRef xlink:type="simple" xlink:href="linkbase_reference.xml" xlink:role="http://www.xbrl.org/2003/role/referenceLinkbaseRef" xlink:arcrole="http://www.w3.org/1999/xlink/properties/linkbase"/>
</appinfo>
</annotation>
<import namespace="http://www.xbrl.org/2003/instance" schemaLocation="http://www.xbrl.org/2003/xbrl-instance-2003-12-31.xsd"/>
<!-- ... taxonomy elements declaration starts here ... -->
</schema>
```


## הפניות ##

* [XBRL - מאת ויקיפדיה](https://en.wikipedia.org/wiki/XBRL)
* [שפת דיווח עסקית הרחבה (XBRL) 2.1](https://www.xbrl.org/Specification/XBRL-2.1/REC-2003-12-31/XBRL-2.1-REC-2003-12-31+corrected-errata-2013-02-20.html)

