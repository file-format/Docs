{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Създаване на файл – Xcode Makefile скриптов файл",
  "description":"Научете за XCode MakeFile формат и API, които могат да създават и отварят MakeFile файлове.",
  "linktitle" : "MAKE",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}


## Какво е MAKE файл?

MAKE файлът е XCode скрипт файл, който организира компилация на код. Използва се за компилиране и свързване на програми от множество файлове с изходен код. Това помага да се реши кои части от голямо приложение трябва да бъдат прекомпилирани, когато приложението трябва да се актуализира. Накарайте файловете да използват серия от инструкции за изпълнение в зависимост от това какви файлове са променени.

## Пример за файлов формат MAKE

Следното съдържание се изпълнява с помощта на помощната програма Make и резултатите са както следва.

```
hello:
	echo "hello world"
```
**Направете изход**

```
$ make
echo "hello world"
hello world
```

## Препратки
* [XCode и Make - Форуми на Apple](https://developer.apple.com/forums/thread/657458)
* [Ръководство за Object-C](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

