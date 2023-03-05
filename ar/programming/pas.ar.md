{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
} ,
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - ملف مصدر وحدة دلفي" ,
  "description":"تعرف على تنسيق ملف PAS باستخدام مثال PAS وواجهات برمجة التطبيقات التي يمكنها إنشاء ملفات PAS وفتحها." ,
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
} ,
  "lastmod" : "2021-04-22"
}

## ما هو ملف PAS؟
ملف .pas هو في الواقع ملف كود مصدر يمكن العثور عليه في مشروع برمجة دلفي. دلفي هو تطبيق لتطوير البرمجيات يستخدمه المطورون لبناء برامج قائمة على Windows. مكتوب بلغة دلفي. لغة دلفي هي نوع مختلف من لغة Object Pascal. لذلك يمكن تجميعها في كود Win32 الأصلي مع مترجم دلفي.

## تنسيق ملف PAS

تنسيق ملف PAS هو ملف ترميز محجوز لمصدر وحدة دلفي. يتم تحقيق الوحدات على أنها اللبنات الأساسية لتطبيقات دلفي. يمكنك عرض الكود المصدري لمشروع دلفي الحالي من خلال قائمة ** المشروع> عرض المصدر **. يمكن للمبرمجين إنشاء وحفظ وحدة كملف مستقل يمكن لأي مشروع استخدامه. بمجرد إضافة وحدة إلى المشروع ، تقوم دلفي بتسجيلها في بند الاستخدامات في ملف .DPR الخاص بالمشروع.

## مثال على ملف PAS
عندما نكتب سطر واحد من التعليمات البرمجية. تكتب دلفي العديد من الأسطر لنا بذكاء. تمت كتابة جميع التعليمات البرمجية المصدر في ملف PAS. فيما يلي مثال أساسي لوحدة دلفي المصدر أو ملف PAS:
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


## مراجع

* [Understanding Delphi Project and Unit Source Files](https://www. reasontco.com/understanding-delphi-project-files-dpr-1057652)
* [كتابة برنامج دلفي الأول](http://www.delphibasics.co.uk/Article.asp؟Name=FirstPgm)

