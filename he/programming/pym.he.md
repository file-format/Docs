---
date: 2022-05-09
מְחַבֵּר:
  display_name: Kashif Iqbal
draft: false
toc: true
title: פורמט קובץ PYM - קובץ PYM Macro Preprocessor
linktitle: PYM
description: "למד על פורמט קובץ PYM וממשקי API שיכולים ליצור ולפתוח קובצי PYM."
menu:
  docs:
    parent: "programming"
lastmod: 2022-05-09
---

## מהו קובץ PYM?

קובץ PYM הוא קובץ קדם-מעבד מאקרו המבוסס על שפת התכנות Python. זה פותח על ידי VRVis Research וקיצורי מאקרו בחנות. כאשר קובץ ה-PYM מתפרש על ידי שלב העיבוד המקדים של מתורגמן Python, קיצורי דרך אלו מורחבים כתחליף לטקסט המלא שלהם. בנוסף, פעולה שלישית, אופציונלית, שיכולה להתבצע על ידי מעבד מאקרו מראש היא הכללת קבצים. ניתן לפתוח קבצי PYM בעורכי טקסט כגון Notepad, Notepad++, Apple TextEdit ו-VI ב-Linux.

## פורמט קובץ PYM

קובצי PYM נשמרים כקובצי טקסט רגיל לדיסק. קובץ PYM יכול לכלול גם קבצים אחרים באמצעות ההנחיה '#include'.

### תחביר PYM

הצהרות PYM נכללות בין סמני ""#begin python ו-"#end python" כפי שמוצג להלן.

```
we decided to use a line based special sequence to introduce PYM macros:

#begin python

#python code for defining "macros" goes here

#end python
```
### הרחבת מאקרו PYM

הרחבת המאקרו PYM מיוצגת על ידי שני רצפים כלומר <[ ו-]>. אלו הם תגי html מיוחדים ויכולים להופיע בכל מקום בשורה. דוגמה קטנה של PYM היא כדלקמן.

```
#begin python
TITLE = "My Web page"
def EXP(e): return str(e)
#end python
<head>
<title><[TITLE]></title>
</head>
<body>
<h4><[TITLE]></h4>
<p>The value of 2 raised to the 4th power is <[EXP(2**4)]>.</p>
</body>
```

הפלט של הפעלת זה דרך PYM הוא כדלקמן:

```
<head>
<title>My Web Page</title>
</head>
<body>
<h4>My Web Page</h4>
<p>The value of 2 raised to the 4th power is 16.</p>
</body>
```

## הפניות ##

* [PYM - מאקרו מקדים המבוסס על Python](http://web.archive.org/web/20051122185426/http://ray.cg.tuwien.ac.at/rft/Papers/PYM/pym.html)
* [מתורגמני PYM](https://github.com/interpreters/pym)

