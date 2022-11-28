{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Muhammad Ahmad Chishti"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ MKV",
  "keywords" :[ "mkv", "סרטון matroska", "פורמט mkv", "איך לנגן קבצי mkv", "וידאו", "קובץ", "פורמט" ],
  "description":"למד על פורמט קובץ MKV וממשקי API שיכולים ליצור ולפתוח קבצי MKV.",
  "linktitle" : "MKV",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2020-17-11"
}


## מהו קובץ MKV? ##

MKV (Matroska Video) הוא מיכל מולטימדיה הדומה לפורמט [MOV](/he/video/mov/) ו-[AVI](/he/video/avi/) אך הוא תומך ביותר מרצועת שמע וכתוביות אחת באותו קובץ. קובץ MKV הוא פורמט מיכל המולטימדיה של Matroska המשמש לווידאו. MKV מבוסס על Extensible Binary Meta Language והיא תומכת במספר פורמטים של דחיסת וידאו ואודיו. ההבדל העיקרי בין MKV לפורמטים אחרים של וידאו הוא ש-MKV הוא מיכל ולא קודק. קבצי MKV נשמרים עם סיומת הקובץ .mkv. MKV יכול לשלב אודיו, וידאו וכתוביות בקובץ בודד גם אם אלמנטים אלה משתמשים בסוגים שונים של קידוד. לדוגמה, יכול להיות לך קובץ MKV המכיל וידאו H.264 ו-MP3 או AAC עבור אודיו. MKV תומך גם בתיאורים, דירוגים, אמנות כריכה ואפילו נקודות פרק. ישנן מספר תכונות עיקריות ש-MKV מוגן לעתיד. תכונות אלה כוללות:

- תמיכה בחיפוש מהיר.
- יכולת לבחור זרמי אודיו ווידאו שונים.
- תמיכה בכתוביות (מקודדות קשיחות ומקודדות רך).
- תמיכה במטא נתונים, פרקים ותפריטים.
- יכולת להזרים באינטרנט.
- יכולת לשחזר קבצים שגויים המספקים את היכולת לנגן קבצים פגומים.

## היסטוריה קצרה ##

מקורו של קובץ MKV בשנת 2002 ברוסיה. המפתח הראשי היה Lasse Kärkkäinen שעבד עם מייסד Matroska, Steve Lhomme, וצוות מתכנתים. MKV פותח כפרויקט סטנדרטים פתוחים, מה שאומר שהוא קוד פתוח וחינמי לשימוש. ככל שחלף הזמן, הפורמט שופר והפך לבסיס של פורמט המולטימדיה של WebM ב-2010.

## Matroska Design ##

Matroska מוסיפה את האילוצים הבאים למפרט EBML.

- **docType** של **EBML Header** חייב להיות 'matroska'.
- **EBMLMaxIDLength** של **EBML Header** חייב להיות 4.
- **EBMLMaxSizeLength** של **EBML Header** חייב להיות בין 1 ל-8 (כולל).

כל האלמנטים ברמה העליונה מקודדים ב-4 אוקטטים.

- קודי שפה: Matroska (גרסה 1 עד 3) השתמשה בקודי שפה שיכולים להיות בצורת 3 האותיות הביבליוגרפית ISO-639-2 (כמו "fre" עבור צרפתית), או שניתן להשתמש בקוד מדינה נוסף כמו "fre-ca" "עבור צרפתית קנדית. החל מגרסה 4 של Matroska, ייתכן שישמשו ISO 639-2 או BCP 47 עבור קודי שפה, אם כי BCP 47 מומלץ.
- סוגים פיזיים: יש משמעות שונה עבור קובצי אודיו ווידאו. לדוגמה, ChapterPhysicalEquiv = 60 פירושו (CD / 12" / 10" / 7" / TAPE / MINIDISC / DAT) עבור אודיו ו-(DVD / VHS / LASERDISC) עבור וידאו.
- מבנה בלוק - כותרת בלוק: כותרת בלוק מכילה מידע לגבי מספר רצועה, חותמות זמן, סוג השרוך וכו'.
- שרוכים: זהו מנגנון לחיסכון במקום בעת אחסון נתונים המשמש בדרך כלל עבור בלוקים קטנים של נתונים (מסגרות). ישנם 3 סוגי שרוכים:
  - Xiph: Frame with a size multiple of 255 coded with a 0 at the end of the size. For example, The code for 765 is 255;255;255;0.
  - EBML: The frame size is coded as a difference between the previous size and this size. The first size in the lace is unsigned but others use a range shift to get a sign on each value.
  - fixed-size: The size remains the same.
- SimpleBlock Structure: הוא בהשראת **מבנה הבלוק** כשההבדל העיקרי הוא הוספת דגלים **Keyframe** ו**Discardable**. חוץ מזה הכל אותו דבר.

## מבנה Matroska ##

מסמך Matroska חייב להיות מורכב מ-**EBML Document** אחד לפחות באמצעות **Matroska Document Type**. כל **EBML Document** חייב להתחיל ב-**EBML Header** ואחריו **EBML Root Element** המוגדר כפלח. Matroska מגדיר כמה אלמנטים ברמה העליונה שעשויים להתרחש בתוך **הפלח**.

EBML משתמש במערכת של אלמנטים כדי ליצור מסמך EBML, להלן רשימת הרכיבים ברמה העליונה בקובץ Matroska:

- **מסמך EBML**: עטיפה לכל הקובץ.
- **כותרת EBML**: היא מכילה את פרטי הכותרת של הקובץ כמו DocType.
- **מקטע**: הרכיב העליון שמכיל את כל שאר הרכיבים ברמה העליונה.
- **SeekHead**: הוא מכיל את המיקום של פלחים של אלמנטים ברמה עליונה אחרים.
- **מידע**: הוא מכיל מידע כללי על הפלח.
- **מסלולים**: אלמנט ברמה העליונה של מידע עם מסלולים רבים המתוארים.
- **פרקים**: הוא משמש להגדרת תפריטים בסיסיים ונתוני מחיצות.
- **אשכול**: האלמנט ברמה העליונה המכיל את מבנה הבלוק.
- **סימנים**: רכיב ברמה העליונה המכיל את כל הערכים המקומיים לפלח שמאיצים את חיפוש הגישה.
- **קבצים מצורפים**: זה מכיל קבצים מצורפים.
- **תגים**: אלמנט זה מכיל מטא נתונים המתארים רצועות, מהדורות, פרקים, קבצים מצורפים או הפלח בכללותו.

הטבלה הבאה מציגה את המבנה של מסמך Matroska כאשר רוב האלמנטים מוצגים בהיררכיה:

| | | | | | | |
| -- | -- | -- | -- | -- | -- | -- |
| כותרת EBML | | | |
| פלח | SeekHead| חפש | SeekID |
| | | | SeekPosition |
| | מידע | SegmentUID | |
| | | SegmentFilename | |
| | | PrevUID | |
| | | PrevFilename | |
| | | NextUID | |
| | | שם הקובץ הבא | |
| | | SegmentFamily | |
| | | תרגום פרק | |
| | | חותמת זמן | |
| | | משך | |
| | | DateUTC | |
| | | כותרת | |
| | | MuxingApp | |
| | | WritingApp | |
| | מסלולים | TrackEntry | TrackNumber |
| | | | TrackUID |
| | | | TrackType |
| | | | שם |
| | | | שפה |
| | | | CodecID |
| | | | CodecPrivate |
| | | | CodecName |
| | | | וידאו | FlagInterlaced |
| | | | | FieldOrder |
| | | | | מצב סטריאו |
| | | | | AlphaMode |
| | | | | PixelWidth |
| | | | | PixelHeight |
| | | | | DisplayWidth |
| | | | | DisplayHeight |
| | | | | AspectRatioType |
| | | | | צבע |
| | | | אודיו | תדירות דגימה |
| | | | | ערוצים |
| | | | | BitDepth |
| | פרקים | מהדורה כניסה | EditionUID |
| | | | EditionFlagHidden |
| | | | EditionFlagDefault |
| | | | EditionFlagOrdered |
| | | | ChapterAtom | ChapterUID |
| | | | | ChapterStringUID |
| | | | | ChapterTimeStart |
| | | | | ChapterTimeEnd |
| | | | | פרק דגל מוסתר |
| | | | | תצוגת פרק | ChapString |
| | | | | | ChapLanguage |
| | אשכול | חותמת זמן |
| | | SilentTracks |
| | | עמדה |
| | | PrevSize |
| | | SimpleBlock |
| | | BlockGroup |
| | | חסום מוצפן |
| | רמזים | CuePoint | CueTime |
| | | | CueTrackPositions |
| | קבצים מצורפים | מצורף קובץ | תיאור קובץ |
| | | | שם קובץ |
| | | | FileMimeType |
| | | | FileUID |
| | | | הפניה לקובץ |
| | | | FileUsedStartTime |
| | | | FileUsedEndTime |
| | תגיות | תג | יעדים | TargetTypeValue |
| | | | | TargetType |
| | | | | TagTrackUID |
| | | | | TagEditionUID |
| | | | | TagChapterUID |
| | | | | TagAttachmentUID |
| | | | SimpleTag | TagName |
| | | | | TagLanguage |
| | | | | TagDefault |
| | | | | TagString |
| | | | | TagBinary |
| | | | | SimpleTag |


### שימוש ב-Codec ###

אם אינך רוצה נגן מדיה חדש ומעדיף להשתמש בנגן הקיים שלך, תצטרך להתקין כמה קודקים (קיצור לדחיסה/פירוק). למרות שהורדת רכיבי קודקים היא אפשרות חוקית, עליך להיות זהיר לגבי המקור ואלה עשויים להכיל תוכנות זדוניות.

## הפניות ##

- [Matroska מאת ויקיפדיה](https://en.wikipedia.org/wiki/Matroska)

