
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл ADS - формат файлу специфікації Ada",
  "description":"Дізнайтеся про формат файлу ADS із прикладом і API, які можуть створювати та відкривати файли ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## Що таке файл ADS?

Файл ADS — це файл специфікації для проекту програмування Ada. Це схоже на клас для Java або пару заголовка та реалізації у випадку C++. Загальнодоступні та приватні специфікації пакета Ada зберігаються у файлі .ads. Файл .adb, навпаки, містить реалізацію або тіла Ada. Як [C++](/uk/programming/cpp/), Ada пропонує розділення між специфікаціями та реалізаціями незалежно від ООП.

Файли ADS можна відкривати в будь-якому текстовому редакторі, наприклад Microsoft Notepad, Notepad++ і Atom.

## Формат файлу ADS

Файли ADS мають простий текстовий формат і їх можна відкривати/редагувати за допомогою будь-якого текстового редактора. Пакети Ada можуть бути організовані в ієрархії. Дочірню одиницю можна оголосити таким чином:

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

## Список літератури

* [Пакети Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

