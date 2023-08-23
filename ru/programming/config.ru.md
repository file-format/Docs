{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Конфигурационный файл",
  "description":"Узнайте о формате файла CONFIG с помощью примера CONFIG и API-интерфейсов, которые могут создавать и открывать файлы CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## .CONFIG вариант №
Файл CONFIG известен как файл конфигурации; используется для настройки параметров и основных настроек для нескольких компьютерных программ. Некоторые программы читают свои **файлы конфигурации** только при запуске. Другие периодически проверяют файлы конфигурации на наличие изменений.

## КОНФИГУРАЦИЯ Формат файла
**Формат файла CONFIG** используется для серверных процессов, программных приложений и настроек операционной системы. Программист может написать код, чтобы заставить программное обеспечение читать файлы конфигурации снова и снова через определенный период времени и применять изменения к текущему процессу. Для sysntax файла CONFIG не существует четких стандартов или строгих соглашений. Например, файл Microsoft Web.config относится к формату файла CONFIG, который состоит из наборов тегов на основе [XML](/web/xml/); можно редактировать с помощью Microsoft Visual Studio или любого другого текстового редактора.

## Примеры конфигурационных файлов:
Поскольку файлы конфигурации не создаются в соответствии с какими-либо правилами, стандартами или соглашениями, эти файлы могут быть написаны с использованием разных форматов. Файл .config может быть основан на XML, [JSON](/web/json/) или любом другом формате. Ниже приведены примеры файлов конфигурации для известных операционных систем и программ:

### Файлы конфигурации в Linux
Каждая программа Linux представляет собой исполняемый файл, содержащий список **кодов операций**, которые ЦП выполняет для выполнения типичных операций. Работа почти каждой программы может быть настроена в соответствии с вашими требованиями путем изменения ее конфигурационных файлов. Несколько файлов конфигурации в системе Linux находятся в каталоге /etc. Файлы конфигурации можно разделить на следующие категории:
|Категория|Пример| Комментарии|
---|---|---|
|Доступ к файлам|/etc/host.conf|Сообщает серверу сетевого домена, как искать имена хостов.|
|Загрузка и вход/выход из системы|/etc/rc.d/rc.local|Неофициально. Может вызываться из rc, rc.sysinit или /etc/inittab.|
|Файловая система|/etc/mtools.conf|Конфигурация для всех операций (mkdir, копирование, форматирование и т. д.) в файловой системе типа DOS.|
|Системное администрирование|/etc/shells|Содержит список возможных «оболочек», доступных системе.|
|Сеть|/etc/gated.conf|Конфигурация для gated. Используется только демоном gated.|
|Системные команды|/etc/logrotate.conf|Конфигурация динамического компоновщика.|
|Демоны|/etc/httpd.conf|Файл конфигурации для Apache, веб-сервера. Обычно этот файл находится не в каталоге /etc.|
|Пользовательские программы| /etc/lynx.cfg| Настройки прокси|
### Пример файла AWS CONFIG
Часто используемые параметры конфигурации и учетные данные можно сохранить в файлах CONFIG, которые поддерживаются интерфейсом командной строки AWS. Файл CONFIG должен быть текстовым файлом в следующем формате:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### Пример файла SSH CONFIG
Файл конфигурации OpenSSH на стороне клиента называется CONFIG и хранится в каталоге .ssh. Файл SSH CONFIG имеет следующую структуру:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Пример файла конфигурации Python
Файл конфигурации Python может выглядеть так:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## использованная литература

* [Понимание файлов конфигурации Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Настройки файла конфигурации и учетных данных](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Файлы конфигурации в Python](https://martin-thoma.com/configuration-files-in-python/)

