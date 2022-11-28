{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"פורמט קובץ LRC - מהו קובץ LRC?",
  "description":"למד על קובץ LRC Lyric וממשקי API שיכולים ליצור ולפתוח קובצי LRC.",
  "linktitle" : "LRC",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## מהו קובץ LRC?

קובץ LRC הוא קובץ מילים מבוסס טקסט המכיל את המילים של שיר אודיו. כאשר שיר השמע מושמע עם נגן מוזיקה או תוכנת נגן שמע במחשב, קובץ ה-LRC נקרא במקביל ומוצג עם הזמן. קבצי LRC מכילים נקודות סימן להצגת מילים כאשר השיר מתנגן. באופן כללי, לקבצי LRC יש שם זהה לקובץ האודיו המתאים כגון audio.mp3 ו-audio.lrc. קבצי LRC דומים לקבצי כתוביות כגון [SRT](/he/video/srt/).

## פורמט קובץ LRC - מידע נוסף

קבצי פורמט לירי LRC נשמרים כקבצי טקסט רגיל וניתנים לפתיחה ולעריכה בקובץ טקסט. התוכן של קובץ LRC מכיל מידע צבעוני להצגת טקסט מילות השיר.

## פורמטים של LRC

ישנם מספר פורמטים של קבצי LRC שפותחו לאורך זמן. אלה

### פורמט LRC פשוט

תגי זמן השורה הם בפורמט [mm:ss.xx] כאשר mm הוא דקות, ss הוא שניות ו-xx הוא מאיות השנייה.

```
[00:12.00]Line 1 lyrics
[00:17.20]Line 2 lyrics
[00:21.10]Line 3 lyrics
...
mm:ss.xxlast lyrics line
```

### פורמט פשוט מורחב

זה כולל את היכולת לשנות ולציין את המין של המילים באמצעות M: זכר, F: נקבה, D: דואט.

```
[00:12.00]Line 1 lyrics
[00:17.20]F: Line 2 lyrics
[00:21.10]M: Line 3 lyrics
[00:24.00]Line 4 lyrics
[00:28.25]D: Line 5 lyrics
[00:29.02]Line 6 lyrics
```
### פורמט LRC משופר

פורמט LRC המשופר הוא גרסה מורחבת של פורמט Simple LRC. זה מוסיף תג זמן של Word בפורמט<mm:ss.xx> בסוף המילה הקודמת.

```
[ar: Jade Michael]
[al: Sarah Hi]
[au: Jade Michael]
[length: 2:58]
[by: lrc-maker]
[ti: Somebody to Love]

[00:00.00] <00:00.04> When <00:00.16> the <00:00.82> truth <00:01.29> is <00:01.63> found <00:03.09> to <00:03.37> be <00:05.92> lies
[00:06.47] <00:07.67> And <00:07.94> all <00:08.36> the <00:08.63> joy <00:10.28> within <00:10.53> you <00:13.09> dies
[00:13.34] <00:14.32> Don't <00:14.73> you <00:15.14> want <00:15.57> somebody <00:16.09> to <00:16.46> love
```

## הפניות

* [LRC Lyrics File Format - ויקיפדיה](https://en.wikipedia.org/wiki/LRC_(file_format))

