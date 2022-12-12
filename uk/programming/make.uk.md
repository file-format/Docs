{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Створити файл — файл сценарію Makefile Xcode",
  "description":"Дізнайтеся про формат XCode MakeFile і API, які можуть створювати та відкривати файли MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Що таке файл MAKE?

Файл MAKE — це файл сценарію XCode, який організовує компіляцію коду. Він використовується для компіляції та компонування програм із кількох файлів вихідного коду. Це допомагає вирішити, які частини великої програми потрібно перекомпілювати, коли програму потрібно оновити. Змусити файли використовувати ряд інструкцій для запуску залежно від того, які файли було змінено.

## Приклад формату файлу MAKE

Наступний вміст виконується за допомогою утиліти Make, а результати виводяться таким чином.

```
hello:
	echo "hello world"
```
**Зробити вихід**

```
$ make
echo "hello world"
hello world
```

## Список літератури
* [XCode і Make – форуми Apple](https://developer.apple.com/forums/thread/657458)
* [Посібник Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

