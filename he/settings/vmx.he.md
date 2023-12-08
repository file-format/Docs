{
"date": "2023-06-08",
  "keywords": [
"קובץ vmx",
"מהו קובץ vmx",
"דוגמה לקובץ vmx",
"כיצד לפתוח קובץ vmx",
"מה מכיל קובץ vmx",
"מהו הפורמט של קובץ vmx",
"קוֹבֶץ",
"סיומת קובץ vmx",
"סיומת"
],
  "author": {
"display_name": "שייק פאיז"
},
"draft": "false",
"toc": true,
"title": "פורמט קובץ VMX - קובץ תצורה של מכונה וירטואלית של VMware",
  "description":"למד על פורמט VMX וממשקי API שיכולים ליצור ולפתוח קובצי VMX.",
  "linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
      "parent": "settings"
}
},
"lastmod": "2023-06-08"
}

## מהו קובץ VMX?

קובץ VMX, הידוע גם כקובץ תצורת מחשב וירטואלי, הוא קובץ טקסט רגיל המשמש את תוכנת הווירטואליזציה של VMware להגדרת הגדרות ותצורה של מחשב וירטואלי (VM). קובצי VMX מכילים מידע כגון תצורת החומרה של VM, מיפוי דיסק וירטואלי, הגדרות רשת ופרמטרים נוספים.

## דוגמה לקובץ VMX

הנה דוגמה לאיך יכול להיראות קובץ VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## מה מכיל קובץ VMX?

קובץ VMX מכיל הגדרות תצורה שונות עבור מחשב וירטואלי (VM). להלן כמה מההגדרות הנפוצות בקובץ VMX:

- `.encoding:` מציין את קידוד התווים בשימוש בקובץ.
- `config.version:` מציין את הגרסה של פורמט הקובץ VMX.
- `virtualHW.version:` מציין את הגרסה של החומרה הווירטואלית עבור ה-VM.
- `guestOS:` מציין את מערכת ההפעלה האורחת המותקנת ב-VM.
- `memSize:` מגדיר את כמות הזיכרון המוקצה ל-VM.
- `displayName:` מגדיר את שם התצוגה או התווית עבור ה-VM.
- `powerType:` מגדיר את התנהגות הכוח עבור פעולות שונות (כיבוי, הדלקה, איפוס, השעיה).
- `floppyX:` הגדרות תצורה הקשורות לכונני תקליטונים, כגון נוכחות ומיפוי קבצים.
- `numvcpus:` מציין את מספר המעבדים הווירטואליים שהוקצו ל-VM.
- `scsiX:` הגדרות תצורה עבור בקרי SCSI והדיסקים הווירטואליים המשויכים אליהם.
- `ethernetX:` הגדרות תצורה עבור מתאמי רשת, כולל סוג ההתקן הווירטואלי, שם הרשת וסוג הכתובת.
- `ideX:` הגדרות תצורה עבור בקרי IDE והדיסקים הווירטואליים המשויכים אליהם.
- `usbX:` הגדרות תצורה עבור התקני USB, כגון פרטי נוכחות וחיבור.
- `סאונד:` הגדרות תצורה עבור מתאם הסאונד הווירטואלי.
- `tools.syncTime:` מציין אם סנכרון זמן עם המערכת המארחת מופעל.
- `uuid.bios:` מציין את ה-BIOS UUID של ה-VM.
- `uuid.location:` מציין את המיקום UUID של ה-VM.

## איך פותחים קובץ VMX?

לא מומלץ לפתוח קובץ VMX באופן ידני. כאשר אתה מפעיל מכונה וירטואלית באמצעות VMware Fusion, התוכנה טוענת אוטומטית את המידע מקובץ VMX.

עם זאת, אם ברצונך לערוך ידנית קובץ VMX, תוכל לעשות זאת באמצעות כל עורך טקסט, למשל Notepad (Windows) או TextEdit (Mac).

## מהו הפורמט של קובץ VMX?

קובץ VMX הוא קובץ טקסט רגיל עם פורמט ספציפי. הפורמט עוקב אחר מבנה זוג מפתח-ערך שבו כל שורה מייצגת אפשרות תצורה נפרדת.

הפורמט הכללי של קובץ VMX הוא כדלקמן:

```
key1 = value1
key2 = value2
key3 = value3
```

כל שורה מורכבת ממפתח ואחריו סימן שווה (=) והערך המתאים. המפתח מייצג הגדרת תצורה ספציפית והערך מייצג את הערך שהוקצה להגדרה זו.

לדוגמה, `memSize = "8192"` בקובץ VMX מציין שמגבלת הזיכרון של מחשב וירטואלי היא 8192MB של זיכרון RAM.

הפורמט של קובץ VMX עשוי לכלול גם הערות, המסומנות בסימן פאונד (#) בתחילת השורה, מהן מתעלמות תוכנת VMware בעת ניתוח הקובץ. הערות משמשות לעתים קרובות כדי לספק מידע נוסף או הסברים להגדרות ספציפיות.

## הפניות
* [קובץ VMX לדוגמה](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




