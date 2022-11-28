{
  "date" : "2021-06-16",
  "keywords" :[ "LZH", "Сжатый", "Файл", "Расширение", "Формат файла", "Лемпель-Зив", "Харуясу", "LHA" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Формат файла LZH",
  "description":"Узнайте о формате файла LZH и API-интерфейсах, которые могут создавать и открывать файлы LZH.",
  "linktitle" : "LZH",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-06-16"
}

## .LZH вариант № ##

Файл с расширением .lzh и .lha обычно относится к формату файла сжатия архива. Этот формат файла аналогичен другим форматам сжатия файлов, таким как [ZIP](/ru/compression/zip/), [RAR](/ru/compression/rar/) и т. д. Основная цель этих форматов файлов — уменьшить размер архива. формате для удобной отправки, а также для хранения их вместе в сжатом виде. По сравнению с другими западными компаниями файлы LZH очень популярны в Японии и обычно используются для сжатия данных видеоигр. Надстройка LZH для Windows 7 встроена в японскую версию Windows 7. Microsoft впервые выпустила надстройку Microsoft Compressed Folder (LZH) для японской версии Windows XP. Этот формат файла реализуется с помощью средств сжатия и функций, используемых алгоритмом Лемпеля-Зива и Харуясу.

## Спецификация ЛЗХ ##

Метод сжатия архива LZH отображается в виде пятибайтовой текстовой строки, например -lz1-. Это байты с третьего по седьмой в сжатом файле.

|Спецификация|Описание|
---|---|
|Расширение | .лж, .лха|
|Тип носителя| приложение /x-lzh-сжатый |
|Код типа| "LHA_" (LHA-SPACE)|
|ИМП| публичный.архив.lha|
|Разработано| Харуясу Йошизаки (Йоши) |
|Тип| Сжатие|
|Расширено из| LArc|

## Проблемы с открытием файла LZH ##

Ниже приведены несколько проблем, которые могут привести к плохой работе формата файла LZH:
  

* Файл может быть поврежден. Чтобы решить эту проблему, снова загрузите файл или попросите отправителя повторно отправить файл.
* Вторая причина - зараженный файл, в этом случае правильно сканируйте файл
* Некорректные ссылки на файл LZH
* Удаление описания ЛЖ
* Недостаточно аппаратных ресурсов
* Устаревшие драйвера оборудования

## Использованная литература ##

* [LZH - By Wikipedia](https://en.wikipedia.org/wiki/LHA_(file_format))