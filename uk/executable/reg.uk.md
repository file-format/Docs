{
  "date" : "2021-08-02",
  "keywords" :[ "файл reg", "формат файлу reg", "що таке файл reg", "файл", "приклад reg", "розширення файлу reg", "розширення", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу REG та API, які можуть створювати та відкривати файли REG.",
  "title" :"REG - файл реєстру Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Що таке файл REG?
Файл REG — це просто текстовий файл із розширенням .reg. Ці файли зазвичай створюються шляхом експорту типових ключів із реєстру. Ці файли також можна використовувати як резервну копію реєстру (цей крок особливо важливий перед внесенням змін!). Ви бачите, що деякі зробили їх доступними у вигляді файлів для завантаження на тих самих сайтах, де показано, як зламати реєстр. Файл REG корисний для ручного внесення змін до реєстру та експорту цих змін. Просто трохи очистіть файл, а потім поділіться ним з іншими.

## Формат файлу REG
Формат файлу REG розроблено для експорту та імпорту частин реєстру Windows за допомогою синтаксису на основі INI. Реєстр Windows — це реляційна або ієрархічна база даних, яка зберігає параметри низького рівня для операційної системи Microsoft Windows та інших програм, які використовують реєстр Windows. Альтернативно, можна сказати, реєстр або реєстр Windows складається з інформації, параметрів, налаштувань та інших значень для програм і обладнання, встановлених у всіх версіях операційних систем Microsoft Windows.
### Синтаксис файлу REG
Ось деякі ключові елементи як частина синтаксису файлу REG:
- **RegistryEditorVersion**: наприклад, «Редактор реєстру Windows версії 5.00» для Windows 2000, Windows XP і Windows Server 2003.
- **Порожній рядок**: визначає початок нового шляху реєстру.
- **RegistryPathx**: шлях до підрозділу, який містить перше значення, яке ви імпортуєте.
- **DataItemNamex**: назва елемента даних, який потрібно імпортувати.
- **DataTypex**: тип даних для значення реєстру.

Ключі зберігаються у файлах .reg із використанням такого синтаксису:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Ви можете редагувати значення за замовчуванням ключа, використовуючи «@» замість «Назви значення»:
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Приклад
Ось приклад файлу REG
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

## Список літератури

* [Реєстр Windows – Вікіпедія](https://en.wikipedia.org/wiki/Windows_Registry)
* [Як додати, змінити або видалити підрозділи реєстру та значення за допомогою файлу .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


