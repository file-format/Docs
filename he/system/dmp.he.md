{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "הרחבה", "קובץ", "פורמט", "מערכת", "MemoryDump", "Minidump", "תוכניות", "מחשב", "אפליקציה" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - MemoryDump File Format",
  "description":"למד על פורמט קובץ DMP וממשקי API שיכולים ליצור ולפתוח קובצי DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## מהו קובץ DMP? ##

קובץ ה-DMP משויך בעיקר לפורמט הקובץ MemoryDump או Minidump. הוא משמש במערכת ההפעלה Microsoft Windows לאחסון נתונים שהושלכו מחלל הזיכרון של המחשב. בדרך כלל, קבצי DMP נוצרים כאשר קובץ קורס או מתרחשת שגיאה. לפעמים קבצי DMP חשובים מאוד למומחים טכניים או למשתמשי מחשב מתקדמים כדי לפתור את הבעיות שעומדות בפניכם ולפתור כל סוג של בעיה באפליקציה. קבצי ה-DMP מאוחסנים כפורמט קנייני ב-Microsoft המשמש את מערכת ההפעלה לאיפוי באגים בכל יישום המותקן במערכת.


## מפרט טכני של פורמט קובץ DMP

ב-Windows, כלי המערכת "savedump.exe" יוצר קבצי .dmp אשר לאחר מכן ניתן לעבד אותם על ידי כלי עזר שונים לניפוי באגים הזמינים. Mini dump (64/128 Kb) מאוחסן על ידי חלונות בספריית '%SystemRoot%\Minidump'. מצד שני, זיכרון הליבה ו-dump זיכרון מלא מאוחסנים בשורש המערכת כקבצי 'Memory.dmp'. קבצי dump של זיכרון הם קבצים גדולים יחסית, ולכן יכולים לקחת כמות מספקת של שטח אחסון. אז מומלץ שקובצי ה-.dmp חסרי התועלת שלדעתך לא יהיו שימושיים לפתרון בעיות ואז למחוק אותם.

אתה יכול למחוק קבצי .dmp באופן ידני או באמצעות ברירת המחדל של "אשף דיסק נקי" במחשב שלך. הרחבות DMP משמשות את מוצרי מסד הנתונים של Oracle כדי להשתמש בקבצי ה-.dmp בקבצי מסד נתונים של גיבוי ושחזור שנוצרו והשתמשו בהם. קבצי ה-DMP שנוצרו על ידי Oracle הם גיבויים של מסדי נתונים שיכולים לשמש לייבוא או שחזור לתוך מופע מסד נתונים פועל דרך שרת מסד נתונים. ברוב המקרים, לקבצי .dmp יש חותמות זמן ותאריך כשמות הקבצים שלהם.

### התוכן של קובץ DMP

קובץ dump של זיכרון מכיל:

* הצהרת הסטופ והפרמטרים שלה;
* רשימה של מנהלי התקנים טעונים;
* ההקשר של המעבד (PRCB) עבור התהליכים שעצרו את הפעולה הרגילה של Windows;
* הקשר הליבה ומידע המעבד (EPROCESSES) עבור התהליכים שהופסקו;
* הקשר הליבה ומידע המעבד (ETHREAD) עבור השרשור שנפסק;
* מחסנית הקריאה במצב הקרנל עבור השרשור שסיים את ביצוע התהליך.


## דוגמה ל-DMP

שגיאת העצירה 0XC0000218 (Registry_File_Failure) יוצרת קובץ DMP באופן הבא:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## התייחסות ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

