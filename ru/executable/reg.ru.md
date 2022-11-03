{
  "date" : "2021-08-02",
  "keywords" :[ "рег-файл", "формат рег-файла", "что такое рег-файл", "файл", "пример рег-файла", "расширение рег-файла", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла REG и API-интерфейсах, которые могут создавать и открывать файлы REG.",
  "title" :"REG — файл реестра Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## .REG вариант №
REG-файл — это просто текстовый файл с расширением .reg. Эти файлы обычно создаются путем экспорта типичных ключей из реестра. Эти файлы также можно использовать в качестве резервной копии реестра (особенно важен этот шаг перед внесением изменений!). Вы можете видеть, что некоторые сделали их доступными в виде загружаемых файлов на тех же сайтах, которые показывают вам, как выполнить взлом реестра. Файл REG полезен для внесения изменений в реестр вручную и экспорта этих изменений. Просто немного очистите файл, а затем поделитесь им с другими.

## Формат REG-файла
Формат файла REG был разработан для экспорта и импорта частей реестра Windows с использованием синтаксиса на основе INI. Реестр Windows — это реляционная или иерархическая база данных, в которой хранятся настройки нижнего уровня для операционной системы Microsoft Windows и других приложений, использующих реестр Windows. Альтернативно, можно сказать, реестр или реестр Windows состоит из информации, опций, настроек и других значений для программ и оборудования, установленных во всех версиях операционных систем Microsoft Windows.
### Синтаксис REG-файла
Вот некоторые ключевые элементы синтаксиса REG-файла:
- **RegistryEditorVersion**: например, «Редактор реестра Windows версии 5.00» для Windows 2000, Windows XP и Windows Server 2003.
- **Пустая строка**: обозначает начало нового пути реестра.
- **RegistryPathx**: путь к подразделу, содержащему первое импортируемое значение.
- **DataItemNamex**: имя элемента данных, который вы хотите импортировать.
- **DataTypex**: тип данных для значения реестра.

Ключи хранятся в файлах .reg с использованием следующего синтаксиса:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Вы можете изменить значение по умолчанию для ключа, используя «@» вместо «Имя значения»:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Пример
Вот пример REG-файла
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## использованная литература

* [Реестр Windows — по Википедии] (https://en.wikipedia.org/wiki/Windows_Registry)
* [Как добавить, изменить или удалить подразделы и значения реестра с помощью файла .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- разделы-и-значения-реестра-путем-использования-рег-файла-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


