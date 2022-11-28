{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "קובץ", "הרחבה", "פורמט קובץ", "Visual C++ Project", "מדריך תכנות" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"למד על פורמט קובץ VCXPROJ וממשקי API שיכולים ליצור ולפתוח קובצי VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## מהו קובץ VCXPROJ?

קובץ עם סיומת .vcxproj הוא קובץ פרויקט Microsoft Visual C++ המאחסן את פרטי הפרויקט [C++](/he/programming/cpp/). הוא מכיל מידע המשמש את מערכת פרויקט MSBuild כדי להדר ולבנות את הפלט הסופי. VCXPROJ של פרויקטים של Visual C++ זהה לזה של [CSPROJ](/he/programming/csproj/) עבור פרויקטי NET. קבצי VCXPROJ אינם מכילים שום קוד אך מתייחסים לכל המחלקות, היעדים והמאפיינים שהוגדרו עבור הפרויקט לבניית הפרויקט. ניתן לפתוח אותם בעורכי טקסט רגיל או רצוי ב-Microsoft Visual Studio IDE.


## פורמט קובץ VCXPROJ - מידע נוסף

קבצי VCXPROJ הם קבצי טקסט שנוצרים בפורמט קובץ [XML](/he/web/xml/). ניתן לפתוח אותם בכל עורך טקסט אך מומלץ מאוד להשתמש ב-Microsoft Visual Studio IDE לפתיחה ועריכה של קבצים אלו. אלה לא נועדו לעריכה ידנית. טעויות עלולות לגרום ל-IDE לקרוס או להתנהג בדרכים בלתי צפויות.

התוכן של קובץ VCXPROJ לדוגמה הוא כדלקמן.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### רכיבי קובץ VCXPROJ

קובץ VCXPROJ טיפוסי מכיל מספר אלמנטים כפי שניתן לראות ב-XML לדוגמה למעלה. [מבנה VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) מאת מיקרוסופט מסביר כל רכיב קובץ בפירוט וניתן להתייחס אליו מנקודת מבטו של המפתח.

#### אלמנט פרויקט

זהו צומת השורש של קובץ VCXPROJ. MSBuild משתמש באלמנט זה כדי לקרוא את גרסת ה-build ויעד ברירת המחדל להידור.

#### ProjectConfigurations ItemGroup Element

הוא מכיל את מידע תצורת הפרויקט שיכול לכלול את שיטת הבנייה (Debug או Release), קומפילציה של 32 או 64 סיביות, אפשרויות אופטימיזציה ואחרות. המידע בקבוצה זו משמש את IDE לטעינת הפרויקט.

#### ProjectConfiguration Elements

רכיבי ProjectConfiguration בקובץ VCXPROJ מכילים מידע על ה-build והפלטפורמה שעבורם הפרויקט נטען. השם שלו צריך לעקוב אחר הפורמט `$(Configuration)|$(Platform)`.

#### Globals PropertyGroup Element

חלק זה מכיל הגדרות המספקות מידע לרמת הפרויקט כגון:

* ProjectGuid
* RootNamespace
* ApplicationType או ApplicationTypeRevision


## הפניות

* [מבנה VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [קבצי פרויקט C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

