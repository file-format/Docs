{
  "date" : "2021-10-20",
  "keywords" :[ "קובץ bns", "פורמט קובץ bns", "מהו קובץ bns", "קובץ", "דוגמה של bns", "סיומת קובץ פורטל בונוס מפה", "הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ BNS של Ortal Bonus Map Script ועל ממשקי API שיכולים ליצור ולפתוח קובצי BNS.",
  "title" :"BNS - Portal Bonus Map Script File",
  "linktitle" : "BNS",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-10-20"
}

## מהו קובץ BNS?

קובץ עם סיומת .bns הוא קובץ סקריפט של משחק שנוצר עם משחק פתרון פאזלים של Portal Map שפותח על ידי Valve. הוא מכיל סקריפט טקסט להגדרת מידע על מפת פורטל המאוחסנת כקובץ .bsp. קובצי BNS משמשים כהתייחסות לקובץ המפה בפועל ומכיל רשימה של אתגרים שיש להשלים. בנוסף, הוא מכיל שם מפה, הערות על המפה והפניות לקובץ תמונות ממוזערות. ניתן לפתוח קובץ BNS בכל עורך טקסט כגון Notepad++, textEdit ו-Notepad.

## פורמט קובץ BNS

קובצי BNS נשמרים כקובצי טקסט רגיל הניתנים לקריאה אנושית. ניתן לפתוח אותם בעורכי טקסט ולערוך אותם גם כן. עם זאת, יש לערוך אותם בקפידה כדי למנוע שגיאות כלשהן בסקריפט.

## דוגמה לפורמט קובץ BNS

קובץ BNS עשוי להיראות בערך כמו הבא כאשר הוא נפתח בעורך טקסט כגון Notepad++.

```
"#Bonus_Map_Challenges"
{
	"map"		"testchmb_a_08"
	"chapter"	"chapter5.cfg"	[$X360]
	"image"		"bonusmaps/testchmb_a_08_challenges"
	"comment"	"#Bonus_Map_ChallengesComment"
	"lock"		"0"

	"challenges"
	{
		"#Bonus_Map_ChallengePortals"
		{
			"comment"	"#Bonus_Map_LeastPortalsComment"

			"bronze"	"9"
			"silver"	"5"
			"gold"		"4"
		}
		"#Bonus_Map_ChallengeSteps"
		{
			"comment"	"#Bonus_Map_LeastStepsComment"

			"bronze"	"30"
			"silver"	"20"
			"gold"		"10"
		}
		"#Bonus_Map_ChallengeTime"
		{
			"comment"	"#Bonus_Map_LeastTimeComment"

			"bronze"	"40"
			"silver"	"30"
			"gold"		"19"
		}
	}
}
```

## חלקים מקובץ BNS

בדוגמה לעיל,

* `#Bonus_Map_Challenges` - מייצג את שם המפה.
* `מפה` - מייצג את שם המפה שיש להכניס לתיקיית המפות של המשחק
* `פרק` - מייצג את הפרק אליו שייכת המפה. כל קבצי הפרקים ממוקמים בקובץ VPK על ידי הוספת שם המפה בפורמט `מפה את_שם_מפתך`
* `תמונה` - היא מכילה את התמונה הממוזערת של המפה ומאוחסנת בנתיב השורש steam\steamapps\common\portal\portal\materials\VGUI.
* `תגובה` - טקסט תיאורי על המפה שנוצרה.

## הפניות

* [תסריט אתגר פורטל](https://developer.valvesoftware.com/wiki/Portal_Challenge_Script)

