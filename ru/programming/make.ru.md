{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Создать файл — файл сценария Xcode Makefile",
  "description":"Узнайте о формате XCode MakeFile и API-интерфейсах, которые могут создавать и открывать файлы MakeFile.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## .MAKE вариант №

Файл MAKE — это файл сценария XCode, который организует компиляцию кода. Он используется для компиляции и компоновки программ из нескольких файлов исходного кода. Это помогает решить, какие части большого приложения необходимо перекомпилировать, когда приложение необходимо обновить. Заставить файлы использовать серию инструкций для запуска в зависимости от того, какие файлы были изменены.

## Пример формата файла MAKE

Следующее содержимое выполняется с помощью утилиты Make и выводит следующее.

```
hello:
	echo "hello world"
```
**Сделать вывод**

```
$ make
echo "hello world"
hello world
```

## использованная литература
* [XCode и Make — форумы Apple] (https://developer.apple.com/forums/thread/657458)
* [Руководство по Object-C] (https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

