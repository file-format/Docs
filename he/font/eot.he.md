{
  "date" : "2020-08-20",
  "keywords" :[ "קובץ eot", "פורמט קובץ eot", "מהו קובץ eot", "קובץ", "דוגמה ל-eot", "סיומת קובץ eot","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EOT - פורמט קובץ גופן TrueType",
  "description":"למד על פורמט קובץ EOT וממשקי API ליצירה ופתיחה של קובצי EOT.",
  "linktitle" : "EOT",
  "menu" : {
    "docs" : {
      "parent" : "font"
}
},
  "lastmod" : "2020-10-21"
}

## מהו קובץ EOT?

קובץ עם סיומת .eot הוא גופן OpenType המוטמע במסמך. אלה משמשים בעיקר בקבצי אינטרנט כגון דף אינטרנט. הוא נוצר על ידי Microsoft ונתמך על ידי מוצרי Microsoft כולל קובץ מצגת PowerPoint [.pps](/he/presentation/pps). הקובץ אינו בשימוש עיקרי והוא מעין מסמך נלווה למסמך הראשי או לדף האינטרנט. בדומה לגופני OTF, EOT תומך גם בקווי מתאר Postscript וגם TrueType עבור הגליפים. קבצי EOT קטנים יותר בגודלם מהסיבה שהם דחוסים באמצעות דחיסת LZ. EOT משתמש בכלי של Microsoft כדי ליצור גופן מגופני TTF/OTF קיימים.

## היסטוריה קצרה

הגופן EOT הוגש ל-W3C בשנת 2007 כחלק מ-CSS3 אך בשל הדרישות שלו להיות מותקן לצמיתות במערכת מרוחקת הפך לסיבת דחייתו. זה הוגש מחדש במרץ 2008, אבל W3C בחרה בסופו של דבר ב-[פורמט גופן אינטרנט](/he/font/woff/) (WOFF) שהיה סטנדרטי אז.

## פורמט קובץ EOT

ניתן למצוא פרטים על פורמט קובץ EOT ב[דף הגשת W3](https://www.w3.org/Submission/EOT/#FileFormat) ומשכלל את המבנה המשמש את פורמט הגופן הזה. ה-EOT מורכב ממבנה EMBEDDEDFONT יחיד המספק מספיק מידע בסיסי על שם הגופן והתווים הנתמכים. האריזה של מידע זה מאפשרת לסוכני משתמש להימנע מפירוק, ביטול דחיסה או התקנת הגופן אם הוא כבר קיים במכשיר.

### מבנה EMBEDDEDFONT
מבנה EMBEDDEDFONT עבר שלושה תיקונים, עם הוספת נתונים נוספים בסוף המבנה עם כל גרסה. הגרסה האחרונה של מבנה EMBEDDEDFONT היא כמתואר להלן.

|סוג נתונים|שם ערך|תיאור|
---|---|---|
|לא חתום ארוך|EOTSize|אורך מבנה כולל בבתים (כולל נתוני מחרוזת וגופן)|
|לא חתום ארוך|FontDataSize|אורך גופן OpenType (FontData) בבתים|
|לא חתום ארוך|גרסה|מספר גרסה של פורמט זה - 0x00020002|
|לא חתום ארוך|דגלים|עיבוד דגלים|
|byte[10]|FontPANOSE|ערך PANOSE עבור גופן זה - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#pan|
|byte|Charset|ב-Windows זה נגזר מ-TEXTMETRIC.tmCharSet. ערך זה מציין את ערכת התווים של הגופן. DEFAULT_CHARSET (0x01) מציין שאין העדפה. - ראה https://learn.microsoft.com/en-us/windows/win32/api/wingdi/ns-wingdi-textmetrica|
|byte|Italic|אם ה-bit עבור ITALIC מוגדר ב-OS/2.fsSelection, הערך יהיה 0x01 - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fss|
|לא חתום ארוך|משקל|ערך המשקל עבור גופן זה - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#wtc|
|לא חתום קצר|fsType|דגלי סוג המספקים מידע על הרשאות הטמעה - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#fst|
|לא חתום קצר|MagicNumber|מספר קסם לקובץ EOT - 0x504C. משמש לבדיקת שחיתות בנתונים.|
|unsigned long|UnicodeRange1|os/2.UnicodeRange1 (סיביות 0-31) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange2|os/2.UnicodeRange2 (סיביות 32-63) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange3|os/2.UnicodeRange3 (סיביות 64-95) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|UnicodeRange4|os/2.UnicodeRange4 (סיביות 96-127) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#ur|
|unsigned long|CodePageRange1|CodePageRange1 (סיביות 0-31) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|unsigned long|CodePageRange2|CodePageRange2 (סיביות 32-63) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/os2#cpr|
|לא חתום ארוך|CheckSumAdjustment|head.CheckSumAdjustment - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/head|
|לא חתום ארוך|שמור1|שמור - חייב להיות 0|
|לא חתום ארוך|שמור2|שמור - חייב להיות 0|
|לא חתום ארוך|שמור3|שמור - חייב להיות 0|
|לא חתום ארוך|שמור4|שמור - חייב להיות 0|
|לא חתום קצר|ריפוד1|ריפוד לשמירה על יישור ארוך. ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|לא חתום קצר|FamilyNameSize|מספר בתים בשימוש מערך FamilyName|
|byte|FamilyName[FamilyNameSize]|מערך של תווי UTF-16 באורך של בתים FamilyNameSize. זוהי מחרוזת ה-Font Family בשפה האנגלית שנמצאת בטבלת השמות של הגופן (שם מזהה = 1) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding2|ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|unsigned short|StyleNameSize|מספר בתים בשימוש ה- StyleName|
|byte|StyleName[StyleNameSize]|מערך של תווי UTF-16 באורך של בתים StyleNameSize. זוהי מחרוזת ה-Font Subfamily בשפה האנגלית שנמצאת בטבלת השמות של הגופן (שם מזהה = 2) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding3|ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|unsigned short|VersionNameSize|מספר בתים בשימוש על ידי VersionName|
|bytes|VersionName[VersionNameSize]|מערך של תווי UTF-16 באורך של Bytes VersionNameSize. זוהי מחרוזת הגרסה בשפה האנגלית שנמצאת בטבלת השמות של הגופן (מזהה שם = 5) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding4|ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|unsigned short|FullNameSize|מספר בתים בשימוש ה-FullName|
|byte|FullName[FullNameSize]|מערך של תווי UTF-16 באורך של Bytes FullNameSize. זוהי מחרוזת השם המלא בשפה האנגלית שנמצאת בטבלת השמות של הגופן (שם מזהה = 4) - ראה https://learn.microsoft.com/en-us/typography/opentype/spec/name|
|unsigned short|Padding5|ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|unsigned short|RootStringSize|מספר בתים המשמשים את מערך RootString|
|byte|RootString[RootStringSize]|מערך של תווי UTF-16 באורך של בתים RootStringSize.|
|לא חתום ארוך|RootStringCheckSum|ערך CheckSum של RootString. ראה את האלגוריתם לעיבוד RootStringChecksum למטה.|
|לא חתום ארוך|EUDCCodePage|ערך דף קוד נדרש לתמיכה בגופן EUDC.|
|unsigned short|Padding6|ערך ריפוד חייב להיות מוגדר תמיד ל-0x0000.|
|unsigned short|SignatureSize|מספר בתים המשמשים את מערך החתימה. שמור כרגע ויש להגדיר אותו ל-0x0000.|
|byte|חתימה[SignatureSize]|שמורה כרגע. אם ה-SignatureSize הוא 0x0000, אין אורך למערך הזה.|
|לא חתום ארוך|EUDCFlags|עיבוד דגלים לגופן EUDC. ערכים טיפוסיים עשויים להיות TTEMBED_XORENCRYPTDATA ו-TTEMBED_TTCOMPRESSED.|
|unsigned long|EUDCFontSize|מספר בתים המשמשים את מערך החתימה.|
|byte|EUDCFontData[EUDCFontSize]|מספר בתים המשמשים לנתוני הגופן של EUDC. אם ה-EUDCFontSize הוא 0x00000000, אין אורך למערך הזה.|
|byte|FontData[FontDataSize]|נתוני הגופן עבור קובץ EOT זה. הנתונים עשויים להיות דחוסים או מוצפנים XOR כפי שמצוין בדגלי העיבוד.|

## הפניות

* [פורמט קובץ EOT](https://www.w3.org/Submission/EOT/)
* [OpenType מוטבע](https://en.wikipedia.org/wiki/Embedded_OpenType)
* [הטבעת גופנים](https://en.wikipedia.org/wiki/Font_embedding)

