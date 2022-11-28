{
  "date" : "2021-04-08",
  "keywords" :[ "קובץ lz", "פורמט קובץ lz", "מהו קובץ lz", "קובץ", "דוגמה lz", "סיומת קובץ lz","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"LZ - Lzip פורמט קובץ דחוס",
  "description":"למד על פורמט קובץ LZ וממשקי API שיכולים ליצור ולפתוח קבצי LZ.",
  "linktitle" : "LZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## מהו קובץ LZ?

קובץ עם סיומת .lz הוא קובץ ארכיון דחוס שנוצר עם Lzip, שהוא כלי חינמי של שורת פקודה לדחיסה. זה תומך בשרשור כדי לדחוס קבצי תמיכה. לקבצי LZ יש יישום מסוג מדיה/lzip ותומכים בקצבי דחיסה גבוהים יותר מ-[BZ2](/he/compression/bz2). LZ מבוססים על אלגוריתם LZMA (Lempel-Ziv-Markov chain) וכוללים סכום בדיקה של 32 סיביות CRC ובייטים מזהים לבדיקת תקינות הקובץ.

## LZMA דחוס פורמט

הפורמט הדחוס LZMA מורכב מזרם דחוס של ביטים המקודד באמצעות קודן טווח בינארי אדפטיבי. הזרם מחולק למנות. כל מנה מתארת בייט בודד או רצף LZ77. האורך והמרחק של כל חבילה מקודדים באופן מרומז או מפורש.

שבעת סוגי החבילות הם כדלקמן ([Wikipedia](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview))

|קוד ארוז (רצף סיביות) |שם החבילה |תיאור החבילה|
---|---|---|
|0 + byteCode| LIT| בית בודד מקודד באמצעות קודן טווח בינארי אדפטיבי.|
|1+0 + len + dist| MATCH| רצף LZ77 טיפוסי המתאר אורך ומרחק רצף.|
|1+1+0+0| SHORTREP| רצף LZ77 של בית אחד. המרחק שווה למרחק LZ77 האחרון שנעשה בו שימוש.|
|1+1+0+1 + len| LONGREP[0]| רצף LZ77. המרחק שווה למרחק LZ77 האחרון שנעשה בו שימוש.|
|1+1+1+0 + len| LONGREP[1]| רצף LZ77. המרחק שווה למרחק ה-LZ77 השני בשימוש.|
|1+1+1+1+0 + len| LONGREP[2]| רצף LZ77. המרחק שווה למרחק השלישי האחרון בשימוש LZ77.|
|1+1+1+1+1 + len| LONGREP[3]| רצף LZ77. המרחק שווה למרחק הרביעי האחרון בשימוש LZ77.|


## הפניות

* [LZMA - ויקיפדיה](https://en.wikipedia.org/wiki/Lempel%E2%80%93Ziv%E2%80%93Markov_chain_algorithm#Compressed_format_overview)
* [Lzip](https://en.wikipedia.org/wiki/Lzip)

