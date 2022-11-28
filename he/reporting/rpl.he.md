{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - דוח פריסת עמוד",
  "keywords" :[ "rpl", "פריסת עמוד דיווח", "XSD", "שרת SQL", "דיווח"],
  "description":"למד על פורמט זרם RPL שהוא פורמט בינארי פנימי המשמש את שירותי הדיווח של Microsoft SQL Server בעת יצירת קשר עם בקרי הצופה.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## מהו קובץ RPL? ##

פורמט הזרם RPL (Report Page Layout) הוא פורמט בינארי פנימי המשמש את שירותי הדיווח של MS SQL Server בעת יצירת קשר עם בקרות הצופה כדי לצמצם חלק מעבודת העיבוד מהשרת לבקרת הצופה בלקוח. מפתחים יכולים ליצור מעצבי דוחות מותאמים אישית על ידי שימוש ב-RPL, שייצור RPL כמו גם מעבדי דוחות מותאמים אישית שמעבדים ומציגים את קובץ ה-RPL כדי להציג דוחות.

## מבני RPL

זרם RPL כולל מבנה זרם, מבנה דו"ח, מאפייני דו"ח וספירות. כל מבנה כולל את הדברים הבאים:

- הגדרה של המבנה.

- דקדוק ה-Augmented Backus-Naur Form (ABNF) למבנה.

- תרשים סיביות של המבנה.

- הגדרות של כל השדות הכלולים במבנה.

להלן ההערות הקצרות לגבי חלק ממבני ה-RPL:

### מבנה הזרם
מבנה הנחל מורכב מסדרה של רשומות. רשומה מכילה אפס או יותר שדות מובנים המכילים את פריסת הדוח.

#### זרם RPL
לזרם RPL חייב להיות רק רשומת דוח אחת והזרם חייב להיות סדרה של רשומות בינאריות השומרות על היררכיית הדוח.

#### תקליט
הרשומה היא אבן בניין בסיסית המשמשת לשמירת המידע על דוח. רשומה מורכבת מרצף של בתים באורך משתנה. רשומה מורכבת משני מרכיבים:
- סוג רשומה
- נתוני הרשומה הספציפיים לאותו סוג רשומה.
סוג הרשומה הוא בת אחד המגדיר איזה סוג מידע מצוין ברשומה וכיצד מסודר ומובנה מבנה נתוני הרשומה הנוגעים לרשומה. ערך הרשומה תלוי בסוג הנתונים הספציפיים לרשומה זו.

#### מבני סוג נתונים פשוטים

הטבלה הבאה מגדירה את סוגי הנתונים בזרם RPL.

|תיאור| פורמט|
---|---|
|Char|מייצג ערך מספרי (אורדיאלי) של 16 סיביות (2-בתים).|
|Byte|מייצג מספר שלם ללא סימן של 8 סיביות (1-בתים).|
|Int16|מייצג מספר שלם עם סימן של 16 סיביות (2 בתים).|
|סינגל|מייצג ערך של נקודה צפה בודדת של 32 סיביות (4 בתים).|
|עשרוני|מייצג סוג נתונים של 128 סיביות (16 בייט).|
|DateTime|מייצג קידוד של 64 סיביות (8-בתים) של ערך תאריך ושעה.|
|Int64|מייצג מספר שלם עם סימן של 64 סיביות (8 בתים).|
|Int32|מייצג מספר שלם עם סימן של 32 סיביות (4 בתים).|
|Float|מייצג ערך של נקודה צפה בודדת של 32 סיביות (4 בתים).|
|בוליאנית|מייצגת ערך סוג לוגי של 8 סיביות (1-בתים). הערכים החוקיים הם true (1) ו-false (0).|
|Long|מייצג מספר שלם עם סימן של 64 סיביות (8-בתים).|
|String|כל ערכי המחרוזת בפרוטוקול חייבים להיות UNICODE UTF-16. כברירת מחדל, כל ערכי המחרוזת מתחילים במספר שלם המגדיר את אורך המחרוזת. ערכי מחרוזת מיוצגים בפרוטוקול כמערך של בתים; מספר הבתים חייב להיות שווה למספר התווים במחרוזת כפול שניים.|

### מבני דיווח
מבני הדוח כוללים את ההגדרות והגדלים של המבנים והאלמנטים הרלוונטיים שלהם.

הרשימה הבאה מציינת את מבני הדוח:

- להגיש תלונה
- גרסה
- מאפייני דוח
- אלמנט מערך אופסט
- תוכן הדף
- עמוד
- מאפייני עמוד
- פריסת דף
- מדור
- קטע פשוט
- מדור מעורב
- מאפייני מדור
- אלמנט אזור הגוף
- רכיב כותרת עמוד
- אלמנט עמוד תחתון
- אלמנט גוף
- מאפייני אלמנט
- מאפייני אלמנט משותפים
- השתמש במאפיינים משותפים
- InlineSharedElementProperties
- NonSharedElementProperties
- סגנון
- SharedStyleProperties
- NonSharedStyleProperties
- ActionInfo
- ActionInfoContent
- פעולה
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- ReportItem
- קו
- תמונה
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- תרשים
- לוח מד
- מפה
- מלבן
- דוח משנה
- RichTextBox
- ParagraphContent
- TextRun
- פסקה
- RichTextBoxStructure
- טבליקס
- TablixContent
- TablixStructure
- TablixMeasurements
- רוחב עמודות
- ColumnInfo
- RowHeights
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- מידות
- מדידה
- ReportElementEnd

### נכסים
להלן רשימת המאפיינים שניתן להשתמש בהם בזרם RPL:

- תעודת זהות
- ספירת עמודות
- ריווח עמודות
- שם ייחודי
- שם
- תווית
- סימניה
- עצה
- ToggleItem
- תיאור
- מקום
- ConsumeContainerWhiteSpace (RPL 10.6)
- שפה
- זמן ביצוע
- מחבר
- רענון אוטומטי
- ReportName
- PageHeight
- רוחב עמודים
- MarginTop
- שוליים שמאלה
- ימין שוליים
- MarginBottom
- עמודות
- שם עמוד (RPL 10.6)
- אלכסון
- יכול לגדול
- CanShrink
- ערך
- ToggleState
- CanSort
- SortState
- נוסחה
- IsToggleParent
- TypeCode
- ערך מקורי
- זה פשוט
- ContentOffset
- שם זרם
- גודל
- LinkToChild
- PrintOnFirstPage
- PrintBetweenSections (RPL 10.4)
- FormattedValueExpressionBased
- ProcessedWithError
- ImageMIMEType
- שם תמונה
- רוחב
- גובה
- רזולוציה אופקית
- רזולוציה אנכית
- RawFormat
- היפר קישור
- BookmarkLink
- DrillthroughId
- DrillthroughUrl
- צבע גבול
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- BorderStyle
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- רוחב גבול
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- ריפוד שמאלה
- ריפוד נכון
- PaddingTop
- PaddingBottom
- סיגנון גופן
- משפחת גופן
- גודל גופן
- משקל גופן
- פורמט
- קישוט טקסט
- יישור טקסט
- יישור אנכי
- צבע
- גובה קו
- כיוון
- מצב כתיבה
- UnicodeBiDi
- תמונת רקע
- צבע רקע
- BackgroundRepeat
- NumeralLanguage
- NumeralVariant
- לוח שנה
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- LayoutDirection
- DefinitionPath
- רמה
- MemberCellIndex
- CellItemOffset
- ColSpan
- RowSpan
- DefIndex
- ColumnIndex
- RowIndex
- GroupLabel
- RecursiveToggleLevel
- סגנון רשימה
- רמת רשימה
- ParagraphNumber
- כניסת ימין
- LeftIndent
- HangingIndent
- SpaceBefore
- SpaceAfter
- שורה ראשונה
- סימון
- ContentTop
- ContentLeft
- רוחב תוכן
- ContentHeight
- מדינה
- CellItemState
- MemberDefState

### ספירות
הרשימה הבאה מציגה את הספירות שניתן להשתמש בהן בזרם RPL:

- SortOptions
- מידות
- ShapeType
- ImageRawFormat
- FontStyles
- FontWeights
- קישוטי טקסט
- יישור טקסט
- יישור אנכי
- הוראות הגעה
- מצבי כתיבה
- UnicodeBiDiTypes
- לוחות שנה
- BorderStyles
- BackgroundRepeatTypes
- סגנונות רשימה
- MarkupStyles
- TypeCode
- ערכי מדינה
- TablixMemberStateValues
- TablixMemberDefStateValues
- גודל RPLS





## הפניות ##

- [פורמט זרם בינארי של דיווח דף (RPL)](https://docs.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

