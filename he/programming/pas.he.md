{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - קובץ מקור יחידת דלפי",
  "description":"למד על פורמט קובץ PAS עם דוגמה של PAS וממשקי API שיכולים ליצור ולפתוח קובצי PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## מהו קובץ PAS?
קובץ .pas הוא למעשה קובץ קוד מקור שניתן למצוא בפרויקט תכנות של דלפי. ה-Delphi הוא אפליקציית פיתוח תוכנה המשמשת מפתחים לבניית תוכנות מבוססות Windows; כתוב בשפת דלפי. שפת דלפי היא גרסה של שפת האובייקט פסקל. אז ניתן להרכיב אותו לקוד Win32 מקורי עם המהדר של Delphi.

## פורמט קובץ PAS

פורמט הקובץ PAS הוא קובץ קידוד השמור למקור יחידת דלפי. היחידות מתממשות כאבני הבניין העיקריות של אפליקציות דלפי. אתה יכול להציג את קוד המקור של פרויקט דלפי הנוכחי דרך התפריט **פרויקט > הצג מקור**. המתכנתים יכולים ליצור ולשמור יחידה כקובץ עצמאי שכל פרויקט יכול להשתמש בו. לאחר הוספת יחידה לפרויקט, דלפי רושמת אותה בסעיף השימושים של קובץ ה-DPR של הפרויקט.

## דוגמה לקובץ PAS
כאשר אנו כותבים שורת קוד בודדת. דלפי כותבת לנו שורות רבות בתבונה. כל קוד המקור כתוב בקובץ PAS. להלן דוגמה בסיסית של יחידת מקור של Delphi או קובץ PAS:
```
unit Unit1;
 
 interface
 
 uses
   Windows, Messages, SysUtils, Variants, Classes, Graphics, Controls, Forms,
   Dialogs, StdCtrls;
 
 type
   TForm1 = class(TForm)
     Label1: TLabel;      // The label we have added
     Button1: TButton;    // The button we have added
     procedure Button1Click(Sender: TObject);
   private
     { private declarations }
   public
     { public declarations }
   end;
 
 var
   Form1: TForm1;
 
 implementation
 
 {$R *.dfm}
 
 // The button action we have added
 procedure TForm1.Button1Click(Sender: TObject);
 begin
   Label1.Caption := 'Hello World';    // Label changed when button pressed
 end;
 
 end.
```


## הפניות

* [הבנת קבצי פרויקט דלפי ומקור יחידה](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [כותבת תוכנית דלפי הראשונה שלך](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

