{
"дата": "15.05.2023",
  "keywords": [
"файл csx",
"що таке файл csx",
"що містить файл csx",
"який формат файлу csx",
"файл",
"розширення файлу csx",
"розширення"
],
  "author": {
"display_name": "Шейкіл Фаїз"
},
"draft": "false",
"toc": true,
"title": "Формат файлу CSX - сценарій Visual C#",
  "description":"Дізнайтеся про формат CSX та API, які можуть створювати та відкривати файли CSX.",
  "linktitle": "CSX",
  "menu": {
    "docs": {
      "identifier": "programming-csx",
      "parent": "programming"
}
},
"lastmod": "2023-05-15"
}

## Що таке файл CSX?

Visual C# Script (також відомий як CSX) — це формат файлів, який використовується механізмом сценаріїв Roslyn в екосистемі Microsoft .NET. Файли CSX містять код C#, який можна виконувати безпосередньо без необхідності окремого етапу компіляції.

Формат CSX є специфічним для екосистеми Microsoft і не є широко використовуваним форматом файлів у загальному програмуванні. Файли CSX часто використовуються в сценаріях, де потрібне швидке створення прототипів або сценаріїв. Вони дають змогу створювати та запускати програми на C# більш легким способом порівняно зі створенням повноцінної скомпільованої програми.

Для виконання файлів CSX можна використовувати такі інструменти, як .NET Interactive Notebooks, які надають інтерактивне середовище для виконання коду C#. Visual Studio Code з розширенням C# і .NET Core SDK також можна використовувати для роботи з файлами CSX.

## Що містить файл CSX?

Файл CSX (C# Script) містить код C#, який можна виконати безпосередньо. Він може містити будь-який дійсний код C#, наприклад оголошення змінних, функції, класи та інші конструкції програмування.

Ось приклад того, що може містити файл CSX:

```
using System;

// Define a class
public class MyClass
{
    public void Greet(string name)
    {
        Console.WriteLine("Hello, " + name + "!");
}
}

// Create an instance of the class and call a method
var myObject = new MyClass();
myObject.Greet("John");

```

Файли CSX також можуть містити оператори імпорту, посилання на зовнішню бібліотеку та інші функції мови C# для підтримки функціональності коду. Код інтерпретується та виконується на льоту без необхідності компіляції, що робить його придатним для виконання сценаріїв і завдань швидкого створення прототипів.

## Який формат файлу CSX?

Формат CSX (C# Script) відповідає простому текстовому формату. Зазвичай він має розширення файлу .csx, щоб відрізняти його від звичайних файлів вихідного коду C# (.cs).

Файли CSX можна редагувати за допомогою будь-якого текстового редактора або інтегрованого середовища розробки (IDE), що підтримує підсвічування синтаксису C#. Коли файл CSX буде готовий, його можна буде виконати за допомогою таких інструментів, як .NET Interactive Notebooks, інтерфейс командного рядка (CLI) .NET Core або IDE із підтримкою сценаріїв C#.

## Список літератури
* [Програмування на C# за допомогою Visual Studio Code](https://code.visualstudio.com/docs/languages/csharp)

