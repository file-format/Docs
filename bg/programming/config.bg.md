{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - конфигурационен файл",
  "description":"Научете за файловия формат CONFIG с пример за CONFIG и API, които могат да създават и отварят CONFIG файлове.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Какво е CONFIG файл?
CONFIG файлът е известен като конфигурационен файл; използва се за конфигуриране на параметрите и основните настройки за няколко компютърни софтуера. Някои софтуери четат своите **конфигурационни файлове** само при стартиране. Други периодично проверяват конфигурационните файлове за промени.

## CONFIG Файлов формат
**Файловият формат CONFIG** се използва за сървърни процеси, софтуерни приложения и настройки на операционната система. Програмистът може да напише код, за да инструктира софтуер да чете конфигурационните файлове отново и отново след определен период от време и да прилага промените към текущия процес. Няма окончателни стандарти или строги конвенции за системния файл CONFIG. Например файлът Web.config на Microsoft принадлежи към файловия формат CONFIG, който се състои от набори от етикети, базирани на [XML](/web/xml/); може да се редактира с Microsoft Visual Studio или всеки друг текстов редактор.

## Примери за конфигурационни файлове:
Тъй като конфигурационните файлове не са създадени чрез спазване на правила, стандарти или конвенции, тези файлове може да са написани с помощта на различни формати. .config файл може да е базиран на XML, [JSON](/web/json/) или друг формат. Следват примери за конфигурационни файлове за добре познати операционни системи и софтуери:

### Конфигурационни файлове в Linux
Всяка Linux програма е изпълним файл, който съхранява списъка с **opcodes**, които процесорът изпълнява, за да изпълни типичните операции. Операциите на почти всяка програма могат да бъдат персонализирани според вашите изисквания чрез промяна на нейните конфигурационни файлове. Няколко конфигурационни файла в системата Linux са в директорията /etc. Конфигурационните файлове могат да бъдат класифицирани в следните категории:
|Категория|Пример| Коментари|
---|---|---|
|Достъп до файлове|/etc/host.conf|Казва на мрежовия домейн сървър как да търси имена на хостове.|
|Стартиране и влизане/излизане|/etc/rc.d/rc.local|Не е официално. Може да се извика от rc, rc.sysinit или /etc/inittab.|
|Файлова система|/etc/mtools.conf|Конфигурация за всички операции (mkdir, копиране, форматиране и др.) на файлова система от тип DOS.|
|Системна администрация|/etc/shells|Съдържа списъка с възможните „обвивки“, достъпни за системата.|
|Мрежа|/etc/gated.conf|Конфигурация за gated. Използва се само от затворения демон.|
|Системни команди|/etc/logrotate.conf|Конфигурация за динамичния линкер.|
|Daemons|/etc/httpd.conf|Конфигурационният файл за Apache, уеб сървъра. Този файл обикновено не е в /etc.|
|Потребителски програми| /etc/lynx.cfg| Настройки на прокси сървъра|
### Пример за AWS CONFIG файл
Често използваните конфигурационни настройки и идентификационни данни могат да бъдат записани в CONFIG файлове, които се поддържат от AWS CLI. Файлът CONFIG трябва да бъде файл с обикновен текст, който използва следния формат:
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
### Пример за SSH CONFIG файл
Конфигурационният файл от страна на клиента на OpenSSH се нарича CONFIG и се съхранява в директорията .ssh. SSH CONFIG файлът се състои от следната структура:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Пример за CONFIG файл на Python
CONFIG файл на Python може да изглежда така:

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



## Препратки

* [Разбиране на конфигурационните файлове на Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Настройки на файла за конфигурация и идентификационни данни](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Конфигурационни файлове в Python](https://martin-thoma.com/configuration-files-in-python/)

