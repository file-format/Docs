{
  "date" : "2021-09-08",
  "keywords" :[ "קובץ mgx", "פורמט קובץ mgx", "מהו קובץ mgx", "קובץ", "דוגמה ל-mgx", "סיומת קובץ mgx","הרחבה", "פורמט" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על Age of Empires 2 Expansion Replay תבנית קובץ MGX וממשקי API שיכולים ליצור ולפתוח קבצי MGX.",
  "title" :"MGX - Age of Empires 2 Expansion Replay",
  "linktitle" : "MGX",
  "menu" : {
    "docs" : {
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## מהו קובץ MGX?

קובץ עם סיומת .mgx הוא קובץ מוקלט למשחק Age of Empires II: The Conquerors שניתן לשחק מחדש בתוכנית Age of Empires II. הוא מכיל הקלטה מלאה של הקמפיין שנוגן על ידי המשתמש. ניתן לטעון אותו ולהשמיע אותו בתוכנית Age of Empires II. לאחר השידור החוזר, המשחק מציג את כל האירועים והתרחישים שהמשתמש תכנן עבור הקמפיין ושיחק.

## פורמט קובץ MGX - מידע נוסף

פורמט הקובץ הפנימי של קובץ MGX עובד וזמין כמידע מאומת חלקית על [Age of Empires 2: The Conquerors — Savegame Format File Format](https://github.com/stefan-kolb/aoc-mgx-format) פוּרמָט. המפרטים מתארים את הפרטים בסעיפים הבאים.

### הגדרות מבנה

מאמינים שהגדרות המבנה של פורמט קובץ GPX מבוססות על [הצהרות BinData Ruby Gem](https://github.com/dmendel/bindata/wiki) המספקות דרך לקרוא ולכתוב נתונים בינאריים מובנים. זה מאפשר למתכנת לציין את הפורמט של הנתונים הבינאריים אשר לאחר מכן נקרא וכתוב על ידי BinData.

### MGX Messaging

הודעות MGX מבוססות על שני סוגים של הודעות.

* GAMESTART - מציין את פקודות התחלת המשחק ואינו מאומת עד היום
* CHAT - מתאר את הודעות הצ'אט במשחק. גם השחקנים וגם המשחק עצמו (Gaia) יכולים לשדר הודעות במשחק.

### פעולות משחק

ישנן מספר [פעולות GAMEPLAY](https://github.com/stefan-kolb/aoc-mgx-format/blob/master/README.md#actions) שאוחזרו ושפרטיהן זמינים.

## הפניות

* [עידן האימפריות 2: הכובשים - מפרט פורמט הקובץ של Savegame](https://github.com/stefan-kolb/aoc-mgx-format)

