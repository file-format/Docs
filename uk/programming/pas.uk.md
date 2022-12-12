{
  "date" : "2021-04-22",
  "keywords": [ ".pas file", "pas file format", "extension", "format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PAS - вихідний файл модуля Delphi",
  "description":"Дізнайтеся про формат файлу PAS із прикладом PAS та API, які можуть створювати та відкривати файли PAS.",
  "linktitle" : "PAS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-22"
}

## Що таке файл PAS?
Файл .pas насправді є файлом вихідного коду, який можна знайти в проекті програмування Delphi. Delphi — це програма розробки програмного забезпечення, яка використовується розробниками для створення програмного забезпечення на основі Windows; написаний мовою Delphi. Мова Delphi є варіантом мови Object Pascal. Таким чином, його можна скомпілювати у рідний код Win32 за допомогою компілятора Delphi.

## Формат файлу PAS

Формат файлу PAS — це файл кодування, зарезервований для джерела Delphi. Блоки реалізовані як основні будівельні блоки програм Delphi. Ви можете переглянути вихідний код поточного проекту Delphi через меню **Проект > Переглянути вихідний код**. Програмісти можуть створити та зберегти модуль як окремий файл, який може використовувати будь-який проект. Щойно одиницю додано до проекту, Delphi реєструє її в розділі uses файлу проекту .DPR.

## Приклад файлу PAS
Коли ми пишемо один рядок коду. Delphi пише для нас багато рядків розумно. Весь вихідний код записаний у файлі PAS. Нижче наведено базовий приклад вихідного блоку Delphi або файлу PAS:
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


## Список літератури

* [Розуміння проектів Delphi та вихідних файлів модулів](https://www.thoughtco.com/understanding-delphi-project-files-dpr-1057652)
* [Написання вашої першої програми Delphi](http://www.delphibasics.co.uk/Article.asp?Name=FirstPgm)

