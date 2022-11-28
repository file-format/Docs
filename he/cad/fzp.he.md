{
  "date" : "2022-06-20",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"למד על פורמט קובץ FZP וממשקי API שיכולים ליצור ולפתוח קובצי FZP.",
  "title" :"פורמט קובץ FZP - קובץ תיאור חלקי XML של Fritzing",
  "linktitle" : "FZP",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2022-06-20"
}

## מהו קובץ FZP?

קובץ FZP הוא קובץ XML שנוצר על ידי [Fritzing](https://fritzing.org/) יישום אבות טיפוס ועיצוב של מעגלים אלקטרוניים. הוא מכיל מידע על המאפיינים, המחברים והאוטובוסים של החלק בפורמט קובץ [XML](/he/web/xml/). לא ניתן להשתמש בקבצי FPZ באופן עצמאי ב- Fritzing. במקום זאת, הם מיובאים כחלק מקובץ ארכיון FZPZ.

## פורמט קובץ FZP - מידע נוסף

קבצי FZP הם קבצי XML המכילים מידע על מאפייני החלק, המחברים והאוטובוסים של החלק. בנוסף לאלה, קבצי FZP מכילים גם מידע על הכותרת, התיאור, המחבר ותאריך הפרסום של קובץ ה-FZP. כאשר מיוצא קובץ חלק של Fritzing, אפליקציית Fritzing יוצרת ארכיון דחוס [FZPZ](/he/compression/fzpz/) המכיל קובץ FZP וארבעה קבצי [SVG](/he/image/svg/).

[מפרט פורמט קובץ FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md) זמינים ב-Github מאת Fritzing.

## דוגמה למבנה קובץ FZP

לקובץ FZP טיפוסי יש את מבנה ה-XML הבא.

```
<?xml version="1.0" encoding="UTF-8"?>
<module fritzingVersion="x.y.z" moduleId="mod-id-rev" referenceFile="ref.file">
  <version>x.y.z</version>
  <title>part-name</title>
  <description>some words about the part</description>
  <author>your-name</author>
  <date>yyyy-mm-dd</date>
  <url>http://part.org</url>
  <label>IC</label>
  <tags>...</tags>
  <taxonomy>...</taxonomy>
  <language>...</language>
  <family>...</family>
  <variant>...</variant>
  <properties>...</properties>
  <views>...</views>
  <connectors>...</connectors>
  <buses>...</buses>
</module>
```
## הפניות

* [מפרט פורמט קובץ FZP](https://github.com/fritzing/fzp/blob/master/docs/README.md)
* [חלקים חדשים עם סיומת fzpz](https://forum.fritzing.org/t/new-parts-with-fzpz-extension/8007/2)

