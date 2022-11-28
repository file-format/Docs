{
  "date" : "2021-08-10",
  "keywords" :[ "קובץ .ova", "פורמט קובץ", "מהו קובץ .ova", "קובץ", "סיומת קובץ"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"למד על מה זה פורמט קובץ .ova וממשקי API שיכולים ליצור ולפתוח קובצי ova.",
  "title" :"פורמט קובץ OVA - פתח קובץ Virtual Appliance",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## מהו קובץ OVA?

קובץ OVA (Open Virtual Appliance) הוא ספריית OVF שנשמרה כארכיון באמצעות פורמט הארכיון .tar. זהו קובץ חבילת מכשיר וירטואלי המכיל קבצים להפצה של תוכנה הפועלת על מחשב וירטואלי. חבילת OVA מכילה קובץ מתאר [.ovf](/he/disc-and-media/ovf/), קובצי אישור, קובץ [.mf](/he/programming/mf/) אופציונלי יחד עם קבצים קשורים אחרים. לקבצי OVA יש סוג מדיה כיישום/ovf.

## פורמט קובץ OVA

כאמור, קובץ OVA הוא קובץ ארכיון שנוצר באמצעות ספריית OVF בפורמט קובץ TAR. הקובץ עצמו נשמר כקובץ בינארי. רוב פלטפורמות הווירטואליזציה, כגון VMware, Microsoft, Oracle ו-Citrix, יכולות להתקין מכשירים וירטואליים מקובץ OVF שהוא קובץ מתאר הכולל את פרטי התמונה שיש לטעון במחשב וירטואלי.

## היתרונות של קובץ OVA

* קבצי OVA דחוסים, מה שמאפשר הורדות מהירות יותר.
* לקוח vSphere מאמת קובץ OVA לפני ייבואו, ומבטיח שהוא תואם לשרת היעד המיועד. אם המכשיר אינו תואם למארח שנבחר, לא ניתן לייבא אותו ומופיעה הודעת שגיאה.
* OVA יכול להכיל יישומים רב-שכבתיים ויותר ממכונה וירטואלית אחת.

## הפניות

* [תבניות ותבניות קובץ OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [מפרטי פורמט קובץ OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

