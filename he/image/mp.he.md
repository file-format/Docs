{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"קובץ MP - קובץ LaTeX MetaPost",
  "description":"למד על פורמט קבצי MP וממשקי API שיכולים ליצור ולפתוח קובצי MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## מהו קובץ MP?

קובץ MP הוא קובץ תמונה וקטור שנוצר על ידי שפת התכנות MetaPost ליצירת תמונות. תמונות וקטוריות שנוצרות באמצעות פורמט קובץ MP נשמרות כקבצי [EPS](/he/image/eps/) (Encapsulated PostScript). בנוסף, MetaPost מגיע מופץ עם מסגרות TeX ו-Metafont וניתן להפיק קבצי MP מתוך קבצי ה-TEX וה-LTX המשמשים את היישומים הללו. קבצי MP מכילים הצהרות ציור ושרטוט אלגוריתמי מתמטי לעיבוד קובץ הפלט EPS. מנוע PDFTex יכול להשתמש ב-EPS שנוצר כדי ליצור קבצי [PDF](/he/pdf/) ישירות.

## פורמט קובץ MP

קבצי MP נשמרים בדיסק כקבצים בינאריים ומייצרים פלט EPS כאשר מיוצאים לפורמט קובץ תמונה וקטור פלט. ציורים שנוצרו באמצעות MetaPost נכללים בצורה מעוצבת בתוך מסמכים טכניים ופרסומי כתב עת שנוצרו עם LaTex.

### דוגמה לקובץ MetaPost MP

להלן דוגמה, עם הפניה מ-[Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), המכילה חץ ואת האות "A" ממש מעל אמצע חֵץ.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## הפניות ##

* [MetaPost מאת ויקיפדיה](https://en.wikipedia.org/wiki/MetaPost)
* [Metapost לדוגמה לטקס מאת Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

