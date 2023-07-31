{
  "date" : "2019-10-11",
   "keywords": [ "sln file", "how to run a sln file", "sln", "extension", "format", "What is sln file", "sln file format", "Visual Studio Solution", "Visual Studio solution VS project" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SLN",
  "description":"למד על פורמט קובץ SLN וממשקי API שיכולים ליצור ולפתוח קבצי SLN.",
  "linktitle" : "SLN",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2019-09-10"
}

## מהו קובץ SLN?
קובץ עם סיומת SLN מייצג קובץ **Visual Studio** השומר מידע על ארגון הפרויקטים בקובץ פתרון. התוכן של קובץ פתרון כזה כתוב בטקסט רגיל בתוך הקובץ וניתן לצפות/לערוך אותו על ידי פתיחת הקובץ בכל עורך טקסט. המידע הכלול בקובץ פתרון נשאר קבוע ומשמש לטעינת המידע המשויך לפתרון כגון [projects ](/he/programming/csproj/) וכל מידע נדרש אחר. קובצי הפרויקט שאליהם מתייחס קובץ הפתרון מכילים מידע נוסף כדי לאפשר לסביבה לאכלס את ההיררכיה בפריטי הפרויקט הזה. לא מאוחסנים נתונים בקובץ .sln, אם כי ניתן לכתוב מידע על הפרויקט לקובץ .sln במידת הצורך.

## **היסטוריית גרסאות SLN** ##

גרסת פורמט הפתרון התפתחה עם כל פתרון של Microsoft Visual Studio עם חלוף הזמן. הפרטים לגבי אלה הם כדלקמן.


|גרסת סטודיו ויזואלית|גרסת פורמט פתרון
---|---|
|2003|8.00
|2005|9.00
|2008|10.00
|2010|11.00
|2013|12.00
|2015|12.00
|2017|12.00

### **תוכן של קובץ פתרון** ###

קובץ פתרון מורכב ממספר סעיפים הנקראים על ידי הסביבה כדי לטעון את הפרויקט. תוכן קובץ ‎.sln לדוגמה הוא כפי שמוצג להלן.

```
Project("{F184B08F-C81C-45F6-A57F-5ABD9991F28F}") # "Project1", "Project1.vbproj", "{8CDD8387-B905-44A8-B5D5-07BB50E05BEA}"  
EndProject  
Global  
  GlobalSection(SolutionNotes) # postSolution  
  EndGlobalSection  
  GlobalSection(SolutionConfiguration) # preSolution  
       ConfigName.0 # Debug  
       ConfigName.1 # Release  
  EndGlobalSection  
  GlobalSection(ProjectDependencies) # postSolution  
  EndGlobalSection  
  GlobalSection(ProjectConfiguration) # postSolution  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.ActiveCfg # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Debug.Build.0 # Debug|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.ActiveCfg # Release|x86  
   {8CDD8387-B905-44A8-B5D5-07BB50E05BEA}.Release.Build.0 # Release|x86  
  EndGlobalSection  
  GlobalSection(ExtensibilityGlobals) # postSolution  
  EndGlobalSection  
  GlobalSection(ExtensibilityAddIns) # postSolution  
  EndGlobalSection  
EndGlobal
```

### **הצהרת פרויקט** ###

קובץ פתרון יכול להכיל יותר מהצהרת פרויקטים אחת וגם זו מסוגי פרויקטים שונים. לדוגמה, קובץ פתרון יחיד יכול להכיל CSharp כמו גם פרויקט VB.NET. סוגים אלה מובחנים בפתרון המשתמש ב-[Project-Type-GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs). ניתן להכליל את הצהרת הפרויקט לעיל באופן הבא להבנה ברורה.

```
Project("{Project-Type-GUID}") # "Project-Name", "Project-Path.extension", "{Project-GUID}"
```

`Project-Type-GUID:` Project-Type-GUID ייחודי לסוגי פרוייקטים שונים ומשמש את קורא הפתרונות כדי לזהות את סוג הפרוייקט. במקרה זה, F184B08F-C81C-45F6-A57F-5ABD9991F28F מראה שזהו פרויקט VB.NET.

`Project GUID:` ה-GUID הייחודי של הפרויקט שמבדיל אותו מפרויקטים אחרים בפתרון. המזהה הייחודי של פרויקט בפתרון מאפשר לפרויקטים אחרים בפתרון לגשת אליו.

בהתבסס על המידע הכלול בקטע הפרויקט של קובץ ה-.sln, הסביבה טוענת כל קובץ פרויקט. הפרויקט עצמו אחראי לאחר מכן לאכלוס היררכיית הפרויקט וטעינת כל הפרויקטים המקוננים. כל שינוי שנעשה בפתרון נשמר בחזרה לקובץ הפתרון עם שמירה או סגירה של הפרויקט.

## פתרון Visual Studio VS פרוייקט

**פרויקט:** באופן הגיוני, כאשר אתה מתחיל ליצור אפליקציה או תוכנה באמצעות Visual Studio, אתה מתחיל פרויקט חדש. פרויקט מכיל את כל הקבצים הדרושים כגון קוד מקור, אייקונים, תמונות, קבצי נתונים ועוד, שיורכבו לאפליקציה ניתנת להפעלה, אתר אינטרנט או ספריה.

**פתרון:** פתרון מכיל פרויקט אחד או יותר. אז הפתרון הוא בדיוק כמו מיכל לפרויקטים של Visual Studio. באופן הגיוני, אנו יכולים לומר שמישהו רוצה לקבל פתרון מלא לעסק שלו כולל אתר אינטרנט, אפליקציית שולחן עבודה, שירות נינוח ואפליקציה לנייד.

### **הפניות** ###

* [קובץ פתרון - מאת MSDN](https://learn.microsoft.com/en-us/visualstudio/extensibility/internals/solution-dot-sln-file?view#vs-2017)
* [פרוייקטים מסוג GUID](https://www.codeproject.com/Reference/720512/List-of-Visual-Studio-Project-Type-GUIDs)

