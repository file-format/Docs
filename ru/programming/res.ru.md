{
  "date" : "2021-04-23",
  "keywords": [ "RES File", "how to open a res file", "what is a res file", "extension", "format", "RES file format" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RES — Скрипт ресурсов, скомпилированный на C++",
  "description":"Узнайте о формате файла RES на примере RES и API, которые могут создавать и открывать файлы RES.",
  "linktitle" : "RES",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## .RES вариант №
Файл с суффиксом или расширением .res может относиться ко многим категориям форматов файлов. Здесь мы обсуждаем формат файла RES, который представляет собой скомпилированный ресурсный сценарий C++; двоичный файл, созданный компилятором ресурсов Microsoft (rc), который содержит данные о ресурсах; на основе содержимого файла определения ресурсов; относящийся к его родительскому программному проекту. Файл .res обычно переформатируется в объектный файл ресурсов, чтобы связать его с исполняемым файлом приложения.

## формат файла RES
Формат файла RES принадлежит компилятору ресурсов Microsoft (rc). Компилятор ресурсов — это инструмент, который компилирует ресурсы, такие как курсоры, значки, меню и диалоговые окна, используемые вашим приложением. Файлы ресурсов обычно имеют расширение .res; содержит ресурсы, такие как курсоры, изображения и информацию о версии. Файл RES может быть 16- или 32-битным файлом ресурсов.
## Структура файла ресурсов
Файл ресурсов содержит ряд различных записей ресурсов. Каждая запись содержит заголовок ресурса и соответствующие данные. Заголовок ресурса обычно выравнивается по DWORD в файле и содержит следующее:

- Параметр **DWORD** для указания размера заголовка ресурса.
- **DWORD** для указания размера данных ресурса.
- Тип ресурса
- Имя ресурса
- Дополнительная информация о ресурсах

Структура заголовка ресурса определяет формат файла RES. Данные для ресурса следуют за заголовком ресурса. Некоторые ресурсы также добавляют шаблон заголовка группы для конкретного ресурса, чтобы предоставить информацию о группе ресурсов. Ниже приведены некоторые типы записей ресурсов и их описание:

### Ресурсы таблицы ускорителей
Таблица ускорителей — это запись ресурса в файле RES без заголовка группы. Шаблон **ACCELTABLEENTRY** определяет каждую запись в таблице ускорителей. Файл RES может иметь несколько таблиц ускорителей.

### Ресурсы курсоров и значков
Несмотря на то, что система рассматривает каждую иконку и курсор как один файл, они хранятся в файлах RES как группа ресурсов значка или группа ресурсов курсора. Форматы файлов ресурсов значка и курсора одинаковы. Заголовок группы ресурсов следует за всеми отдельными значками или компонентами группы курсоров в файле .res.

### Ресурсы диалогового окна
Диалоговое окно также реализовано как запись ресурса в файле RES. Он содержит один шаблон заголовка диалогового окна **DLGTEMPLATE** и один шаблон **DLGITEMTEMPLATE** для каждого конкретного элемента управления в диалоговом окне. Шаблоны **DLGTEMPLATEEX** и **DLGITEMTEMPLATEEX** объясняют формат расширенных ресурсов диалоговых окон.

### Шрифтовые ресурсы
Ресурс меню содержит шаблон **MENUHEADER**, за которым следует один или несколько шаблонов **NORMALMENUITEM** или **POPUPMENUITEM**, по одному для каждого пункта меню в шаблоне меню. Шаблоны **MENUEX_TEMPLATE_HEADER** и **MENUEX_TEMPLATE_ITEM** объясняют формат ресурсов расширенного меню.

### Ресурсы таблицы сообщений
Таблица сообщений состоит из форматированного текста для отображения в виде сообщения об ошибке или в окне сообщения. Основным шаблоном в ресурсе таблицы сообщений является структура **MESSAGE_RESOURCE_DATA**.

### Ресурсы версий
Основным шаблоном в ресурсе версии является **VS_FIXEDFILEINFO**. Дополнительные шаблоны включают **VarFileInfo** для хранения данных, связанных с информацией о языке, и **StringFileInfo** для информации о пользовательских строках.




## использованная литература

* [Форматы файлов ресурсов] (https://docs.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 


 


