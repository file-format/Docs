{
  "date" : "2022-05-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла PYC и API-интерфейсах, которые могут создавать и открывать файлы PYC.",
  "title" :"Формат файла PYC — скомпилированный файл Python",
  "linktitle" : "PYC",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-05-09"
}

## .PYC вариант №

Файл PYC представляет собой скомпилированный выходной файл, созданный из исходного кода, написанного на языке программирования Python. Когда файл PY запускается с использованием интерпретатора Python, он преобразуется в байт-код для выполнения. В то же время скомпилированный байт-код также сохраняется в виде файла .pyc, чтобы его можно было повторно использовать из кеша позже, если это применимо.

## Структура формата файла PYC

Файлы PYC находятся в байт-коде, и их спецификации формата файлов не доступны публично. Однако исследования некоторых источников показывают, что [структура файла PYC](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A% 20marshalled%20code%20object.) состоит из:

* `Четырехбайтовое магическое число`r - Просто два байта, которые изменяются при каждом изменении кода сортировки, а затем два байта 0d0a.
* `Четырехбайтная временная метка модификации` - временная метка модификации Unix исходного файла, который сгенерировал .pyc, чтобы его можно было перекомпилировать, если исходный код изменится.
* `Упорядоченный объект кода` - вывод marshal.dump объекта кода, являющегося результатом компиляции исходного файла.

## использованная литература

* [Структура файлов .pyc](https://nedbatchelder.com/blog/200804/the_structure_of_pyc_files.html#:~:text=pyc%20file%20is%20a%20binary,A%20marshalled%20code%20object.)
