{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "הרחבה", "קובץ", "פורמט", "מערכת", "קובץ לוח הבקרה", "Windows", "תוכניות", "מחשב", "יישום" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - קובץ לוח הבקרה",
  "description":"למד על פורמט קובץ CPL וממשקי API שיכולים ליצור ולפתוח קובצי CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## מהו קובץ CPL? ##

קובץ CPL הוא סוג של קובץ "מערכת". הוא משמש את מערכת ההפעלה Windows. קובץ CPL הוא קיצור של קובץ לוח הבקרה. קבצים אלו הם קבצים בינאריים הנפתחים עם לוח הבקרה במערכת הפעלה של Microsoft Windows ומשמשים לייצוג ופתיחת הכלים הזמינים בלוח הבקרה, כגון עכבר, תצוגות, רשתות, בין היתר. קבצי CPL מאוחסנים בדרך כלל בתיקיית המערכת במכשיר שלך. אין לפתוח קבצים אלה באופן ידני.


## פורמט קובץ CPL ##

קבצי CPL שונים במערכת ההפעלה Windows שלך מחוברים כדי לייצג פריטי לוח בקרה שונים. כל פריטי לוח הבקרה מקושרים לקובץ CPL והסיומת ".cpl" מצורפת לפריטים שלהם.

כמה סוגים נפוצים של קבצי CPL עם הפורמטים שלהם הם:

* Inetcpl.cpl - לנכסי אינטרנט במכשיר שלך
* Appwiz.cpl - כדי להוסיף או להסיר מאפייני תוכניות במכשיר שלך
* Desk.cpl - עבור מאפייני התצוגה
* Main.cpl - למאפיינים הקשורים לעכבר, גופנים, מקלדת ומדפסות.
* Netcpl.cpl - עבור נכסים הקשורים לרשת
* System.cpl - עבור מאפיינים הקשורים למערכת ואשף הוספת חומרה חדשה
* TimeDate.cpl - עבור מאפייני תאריך או שעה
* Mlcfg32.cpl - עבור מאפייני Microsoft Exchange או Windows Messaging
* Intl.cpl - זה מתייחס למאפיינים של הגדרות אזוריות
* Modem.cpl - למאפיינים הקשורים למודם
* Themes.cpl - מאחסן ערכות נושא ומאפיינים של שולחן העבודה.
* Password.cpl - למאפייני סיסמה
* Mmsys.cpl - למאפייני מולטימדיה
* Wgpocpl.cpl - מתייחס ל-Microsoft Mail Post Office

## היסטוריה קצרה ##

סוג קובץ CPL פותח על ידי Microsoft Windows והוא חלק בלתי נפרד ממערכת ההפעלה Windows מאז Windows 1.0. הוא עדיין בשימוש בכל גרסאות Windows, וכל מאפייני פריטי לוח הבקרה מאוחסנים באמצעות סוג קובץ זה.

## CPL דוגמה ##

ניתן לראות קובץ CPL לדוגמה להלן:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
