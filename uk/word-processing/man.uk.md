{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Посібник Unix",
  "description":"Дізнайтеся про формат файлу FODT та API, які можуть створювати та відкривати файли MAN.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## Що таке файл MAN?

Файл із розширенням .man означає сторінку довідки, яка є посібником користувача з програмування Unix у формі програмної документації. Він використовується утилітою `Man`, яка входить до складу Unix і використовується для перегляду документації. Документація програмного забезпечення містить інформацію в розділах і на сторінках, які можна отримати за допомогою утиліти Man з командного терміналу шляхом видачі команд. Будучи доступним на комп’ютері у вигляді електронної копії документації, для доступу до неї не потрібна друкована копія чи підключення до Інтернету.

## Формат файлу Unix Manual Man - більше інформації

Сторінки Man зберігаються у форматі простого тексту, і їх можна створювати та відкривати в будь-якому текстовому редакторі для перегляду чи редагування. В UNIX інформація зі сторінок Man отримується шляхом видачі команд із терміналу, що містить посилання на розділи та номери сторінок із посібника.

### Розділи та сторінки

Unix man — це системний посібник, де кожен аргумент сторінки команди посилається на назву програми, утиліти або функції. команда, якщо надано інформацію про розділ, шукатиме сторінку в цьому конкретному розділі. Однак типовою поведінкою є пошук сторінки в усіх розділах і відображення першої сторінки, незалежно від того, чи існує вона в кількох розділах.

### Номери розділів

Далі наведено інформацію про номери розділів посібника та типи сторінок, які вони містять.

|Номер розділу|Тип сторінок|
---|---|
|1|Виконувані програми або команди оболонки|
|2|Системні виклики (функції, надані ядром)|
|3|Виклики бібліотек (функції в бібліотеках програм)|
|4|Спеціальні файли (зазвичай знаходяться в /dev)|
|5|Формати файлів і умови, наприклад, /etc/passwd|
|6|Ігри|
|7|Різне (включно з пакетами макросів і угодами), наприклад, man(7), groff(7)|
|8|Команди адміністрування системи (зазвичай лише для root)|
|9|Процедури ядра [Нестандартні]|

## Приклад - Як читати сторінки MAN?

Ось приклад того, як отримати інформацію про команду MkDir за допомогою команди Man.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Список літератури

* [Технічні характеристики OpenDocument - Вікіпедія](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — довідкова сторінка Linux](https://man7.org/linux/man-pages/man1/man.1.html)

