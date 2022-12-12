
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ADS файл – Ada спецификационен файлов формат",
  "description":"Научете какво е ADS файлов формат с пример и API, които могат да създават и отварят ADS файлове.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Какво е ADS файл?

ADS файлът е файл със спецификация за проект за програмиране на Ada. Подобен е на клас за Java или двойката заглавка и реализация в случай на C++. Публичните и частните спецификации на пакета Ada се съхраняват във файла .ads. Файлът .adb, за разлика от това, съдържа изпълнението или телата на Ada. Подобно на [C++](/bg/programming/cpp/), Ada предлага разделение между спецификациите и имплементациите независимо от ООП.

ADS файловете могат да се отварят във всеки текстов редактор като Microsoft Notepad, Notepad++ и Atom.

## Файлов формат ADS

ADS файловете са в обикновен текстов формат и могат да се отварят/редактират с всеки текстов редактор. Ada пакетите могат да бъдат организирани в йерархии. Дъщерна единица може да бъде декларирана по следния начин:

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

## Препратки

* [Пакети на Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

