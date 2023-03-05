
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ADS — формат файла спецификации Ada",
  "description":"Узнайте, что такое формат файла ADS, с примерами и API-интерфейсами, которые могут создавать и открывать файлы ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## .ADS вариант №

Файл ADS — это файл спецификации для проекта программирования на языке Ada. Это похоже на класс для Java или пару заголовка и реализации в случае C++. Публичные и частные спецификации пакета Ada хранятся в файле .ads. Файл .adb, напротив, содержит реализацию или тела Ады. Подобно [C++](/ru/programming/cpp/), Ada предлагает разделение спецификаций и реализаций независимо от ООП.

Файлы ADS можно открыть в любом текстовом редакторе, таком как Microsoft Notepad, Notepad++ и Atom.

## Формат файла ADS

Файлы ADS имеют простой текстовый формат и могут открываться/редактироваться в любом текстовом редакторе. Пакеты Ады могут быть организованы в иерархию. Дочерний модуль может быть объявлен следующим образом:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## использованная литература

* [Пакеты Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

