{
  "date" : "2021-08-02",
  "keywords" :[ "reg файл", "reg файл формат", "какво е reg файл", "файл", "reg пример", "reg файл разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за файловия формат REG и API, които могат да създават и отварят REG файлове.",
  "title" :"REG - Файл на системния регистър на Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## Какво е REG файл?
REG файлът е просто текстов файл с разширение .reg. Тези файлове обикновено се създават чрез експортиране на типични ключове от системния регистър. Тези файлове могат да се използват и като резервно копие на системния регистър (Тази стъпка е особено важна преди извършване на промени!). Можете да видите, че някои ги направиха достъпни като файлове за изтегляне на същите сайтове, които ви показват как да извършите хакване на системния регистър. REG файлът е полезен при извършване на ръчни промени в системния регистър и експортиране на тези промени. Просто почистете малко файла и след това го споделете с други.

## REG файлов формат
Файловият формат REG е предназначен за експортиране и импортиране на части от системния регистър на Windows с помощта на базиран на INI синтаксис. Регистърът на Windows е релационна или йерархична база данни, която съхранява настройките на ниско ниво за операционната система Microsoft Windows и други приложения, които използват системния регистър на Windows. Като алтернатива, можем да кажем, регистърът или регистърът на Windows се състои от информация, опции, настройки и други стойности за програми и хардуер, инсталирани на всички версии на операционните системи Microsoft Windows.
### Синтаксис на REG файл
Ето някои ключови елементи като част от синтаксиса на REG файл:
- **RegistryEditorVersion**: Напр. "Windows Registry Editor Version 5.00" за Windows 2000, Windows XP и Windows Server 2003.
- **Празен ред**: Идентифицира началото на нов път в регистъра.
- **RegistryPathx**: Пътят на подключа, който съдържа първата стойност, която импортирате.
- **DataItemNamex**: Името на елемента с данни, който искате да импортирате.
- **DataTypex**: Типът данни за стойността в регистъра.

Ключовете се съхраняват в .reg файлове, като се използва следният синтаксис:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Можете да редактирате стойността по подразбиране на ключ, като използвате "@" вместо "Име на стойност":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Пример
Ето пример за REG файл
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

## Препратки

* [Регистър на Windows - от Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Как да добавяте, променяте или изтривате подключове и стойности в системния регистър с помощта на .reg файл](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- подключове-и-стойности на регистъра-с-използване-на-reg-файл-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


