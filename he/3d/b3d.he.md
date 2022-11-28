{
  "date" : "2021-04-19",
  "keywords": [ "Blitz3D", "b3d", "file", "extension", "format", "blitz3d games" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"למד על פורמט קובץ B3D; משמש במשחקי blitz3d וממשקי API שיכולים לפתוח וליצור קבצי B3D.",
  "title" :"B3D - Blitz3D Entity Model File",
  "linktitle" : "B3D",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-04-19"
}

## מהו קובץ B3D?

קובץ עם סיומת .b3d הוא קובץ דגם המשמש את Blitz3D שעשוי להכיל מודלים של משחקי וידאו לדמויות, מבנים, שטח וחפצים אחרים. ה-Blitz3D היא שפת תכנות המשמשת ליצירת **משחקי blitz3d**. Blitz3D היא שפת תכנות עוצמתית, גמישה וקלה לשימוש המיועדת למטרת כתיבת משחקי וידאו בלבד. המפתחים יכולים ליצור משחקי תלת מימד עמוסי פעולה, חידות דו מימד, הרפתקאות, RPGS, מה שלא יהיה רק באמצעות Blitz3D.

ה-Blitz3D מבוסס על שפת התכנות BASIC; שגם קל ללמוד ולהשתמש. כל העובדות הללו הופכות את Blitz לאידיאלי עבור מתכנתים מתחילים ומנוסים יותר כאחד. למרות שתכונותיו נחשבות מיושנות במקצת ממה שנמצאות ברוב מנועי התלת-ממד המודרניים, Blitz3D ממשיכה לשמש מתכנתי משחקים רבים ברחבי העולם.

## היסטוריה קצרה של Blitz3D

ה-Blitz3D שוחרר בעיקרון עבור מערכת ההפעלה Microsoft Windows בספטמבר 2001, כדי להתחרות בשפות דומות אחרות לפיתוח משחקים. Blitz3D הייתה גרסה משודרגת על פני מנוע הדו-ממד הקודם BlitzBasic, שהרחיב את מערך הפקודות שלו עם תוספת של API עבור מנוע תלת מימד מבוסס DirectX 7. משתמשי Blitz3D צריכים גם להשוות את BlitzMax, שהוא מנוע מאוחר יותר של BlitzBasic. ה-BlitzMax הוא גרסה מורכבת אך חזקה יותר של Blitz3D, התומכת בשפות תכנות מונחה עצמים. זהו ממשק API גרפי מעודכן שיתאים יותר לתווי Unicode, OpenGL, ולייצוא ל-OSX ולינוקס במקום ל-Windows בלבד.

## דוגמה B3D
קובץ b3d שמכיל נתח TEXS אחד, נתח BRUS אחד וגוש NODE אחד, ייראה כך:

```
BB3D
  1
  TEXS
    ...list of textures...
  BRUS
    ...list of brushes...
  NODE
    ...stuff in the node...
```
רשת פשוטה, ללא אנימציה וללא מרקם תיראה כך:

```
BB3D
  1                           ;version
  NODE
    "root_node"               ;node name
    0,0,0                     ;position
    1,1,1                     ;scale
    1,0,0,0                   ;rotation
    MESH                      ;the mesh
      -1                      ;brush: no brush
      VRTS                    ;vertices in the mesh
        0                     ;no normal/color info in verts
        0,0                   ;no texture coords in verts
        {x,y,z...}            ;vertex coordinates
      TRIS                    ;triangles in the mesh
        -1                    ;no brush for this triangle
        {v0,v1,v2...}         ;vertices
```


## הפניות
* [B3D](https://moddb.fandom.com/wiki/B3D)
* [Blitz BASIC](https://en.wikipedia.org/wiki/Blitz_BASIC)

