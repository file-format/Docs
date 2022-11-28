{
  "date" : "2022-07-12",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"IDX - Codec וידאו ביעילות גבוהה",
  "description":"למד על פורמט קובץ IDX וממשקי API שיכולים ליצור ולפתוח קובצי IDX.",
  "linktitle" : "IDX",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2022-07-12"
}

## מהו קובץ IDX?

קובץ IDX הוא קובץ אינדקס כתוביות המצביע על רשימת מידע המטא נתונים עבור כתוביות בתוך קובץ .sub (VobSub Subtitles). הוא נוצר ומשמש את אפליקציית התוכנה VobSub המאפשרת למשתמשים לחלץ כתוביות מתקליטורי DVD ולזרוק לקובץ SUB. קובצי IDX מכילים חותמות זמן וקיזוז בתים המשמשים להצביע על כל כתובית בודדת. VobSub תמיד יוצר קובץ IDX יחד עם קובץ ה-SUB המתאים.

## פורמט קובץ IDX - מידע נוסף

קבצי IDX נוצרים ונשמרים כקבצי טקסט רגיל שניתן לפתוח בכל עורך טקסט. קובץ IDX מכיל מידע הנקרא על ידי נגני המדיה לקריאת פרמטרים כגון צבע טקסט הכתוביות להצגה על המסך, מיקום טקסט הכתוביות על המסך.

### הגדרות כתוביות של IDX

קובץ IDX טיפוסי מאחסן את מידע המטא נתונים הזה בתחילת הקובץ. הגדרות כתוביות מתחילות ב-**#**. חותמות זמן והפניות לתמונה מתווספות לאחר כל הגדרות הכתוביות הללו ומתחילות ב-**חותמת זמן:**.

## דוגמה לפורמט קובץ IDX

```
# VobSub index file, v7 (do not modify this line!)
#
# To repair desyncronization, you can insert gaps this way:
# (it usually happens after vob id changes)
#
#	 delay: [sign]hh:mm:ss:ms
#
# Where:
#	 [sign]: +, - (optional)
#	 hh: hours (0 <= hh)
#	 mm/ss: minutes/seconds (0 <= mm/ss <= 59)
#	 ms: milliseconds (0 <= ms <= 999)
#
#	 Note: You can't position a sub before the previous with a negative value.
#
# You can also modify timestamps or delete a few subs you don't like.
# Just make sure they stay in increasing order.


# Settings

# Original frame size
size: 720x576

# Origin, relative to the upper-left corner, can be overloaded by aligment
org: 0, 0

# Image scaling (hor,ver), origin is at the upper-left corner or at the alignment coord (x, y)
scale: 100%, 100%

# Alpha blending
alpha: 100%

# Smoothing for very blocky images (use OLD for no filtering)
smooth: OFF

# In millisecs
fadein/out: 50, 50

# Force subtitle placement relative to (org.x, org.y)
align: OFF at LEFT TOP

# For correcting non-progressive desync. (in millisecs or hh:mm:ss:ms)
# Note: Not effective in DirectVobSub, use "delay: ... " instead.
time offset: 0

# ON: displays only forced subtitles, OFF: shows everything
forced subs: OFF

# The original palette of the DVD
palette: 000000, 828282, 828282, 828282, 828282, 828282, 828282, ffffff, 828282, bababa, 828282, 828282, 828282, 828282, 828282, 828282

# Custom colors (transp idxs and the four colors)
custom colors: OFF, tridx: 1000, colors: 000000, bababa, 828282, 000000

# Language index in use
langidx: 0

# English
id: en, index: 0
# Decomment next line to activate alternative name in DirectVobSub / Windows Media Player 6.x
# alt: English
# Vob/Cell ID: 1, 1 (PTS: 0)
timestamp: 00:01:25:880, filepos: 000003800
timestamp: 00:01:46:160, filepos: 000008000
timestamp: 00:02:08:880, filepos: 00000c800
# Vob/Cell ID: 1, 2 (PTS: 222840)
timestamp: 00:03:58:800, filepos: 000011000
timestamp: 00:04:00:680, filepos: 000016800
timestamp: 00:04:04:640, filepos: 00001d800
```

## כיצד להשתמש בקובץ IDX?

אם יש לך את קבצי המשנה וה-IDX עבור סרט, תוכל להפעיל את הכתוביות הללו יחד עם הסרט שעבורו נוצרו. ליישומים רבים כגון VLC, GOM Player, PotPlayer או PowerDVD יש את היכולת לטעון קבצי SUB ו-IDX אלה, ולהפעיל אותם לצד הסרט. יישומי תוכנה יכולים גם להטביע קובצי כתוביות SUB ו-IDX בקבצי [.mkv](/he/video/mkv/).

## המרת IDX ל-SRT

ה-[SRT](/he/video/srt/) (פורמט קובץ SubRip) הוא קובץ כתוביות פשוט שנשמר בפורמט קובץ SubRip. הוא נפוץ יותר בהשוואה לפורמט הקובץ VobSub. לפיכך, אם ברצונך להמיר קבצי SUB/IDX לפורמט קובץ SRT, ישנם כלים זמינים של צד שלישי שניתן להשתמש בהם כדי להשיג זאת. ממיר SUB/IDX ל-SRT, זמין ב-SubtitleTools.com הוא כלי כזה שלוקח קבצי SUB ו-IDX כקלט וממיר כתוביות VobSub אלו לקובצי SRT.

## הפניות

* [VobSub](https://www.videohelp.com/software/VobSub)
* [VOBsub - Wiki Multimedia](https://wiki.multimedia.cx/index.php?title=VOBsub)

