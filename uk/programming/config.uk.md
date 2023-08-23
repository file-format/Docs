{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - файл конфігурації",
  "description":"Дізнайтеся про формат файлу CONFIG з прикладом CONFIG та API, які можуть створювати та відкривати файли CONFIG.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## Що таке файл CONFIG?
Файл CONFIG відомий як файл конфігурації; використовується для налаштування параметрів і основних параметрів для кількох комп’ютерних програм. Деякі програми зчитують свої **конфігураційні файли** лише під час запуску. Інші періодично перевіряють файли конфігурації на наявність змін.

## CONFIG Формат файлу
**Формат файлу CONFIG** використовується для серверних процесів, програмних програм і налаштувань операційної системи. Програміст може написати код, щоб наказати програмному забезпеченню знову і знову читати конфігураційні файли через певний проміжок часу та застосовувати зміни до поточного процесу. Немає чітких стандартів або жорстких конвенцій для системного файлу CONFIG. Наприклад, файл Web.config від Microsoft належить до формату файлу CONFIG, який складається з наборів тегів на основі [XML](/web/xml/); можна редагувати за допомогою Microsoft Visual Studio або будь-якого іншого текстового редактора.

## Приклади конфігураційних файлів:
Оскільки файли конфігурації не створюються за будь-якими правилами, стандартами чи угодами, ці файли могли бути записані з використанням інших форматів. Файл .config може базуватися на XML, [JSON](/web/json/) або будь-якому іншому форматі. Нижче наведено приклади файлів конфігурації для відомих операційних систем і програмного забезпечення:

### Конфігураційні файли в Linux
Кожна програма Linux є виконуваним файлом, який містить список **операцій**, які ЦП виконує для виконання типових операцій. Роботу майже кожної програми можна налаштувати відповідно до ваших вимог, змінивши її конфігураційні файли. Кілька файлів конфігурації в системі Linux знаходяться в каталозі /etc. Конфігураційні файли можна класифікувати за такими категоріями:
|Категорія|Приклад| Коментарі|
---|---|---|
|Доступ до файлів|/etc/host.conf|Вказує серверу мережевого домену, як шукати імена хостів.|
|Завантаження та вхід/вихід|/etc/rc.d/rc.local|Не офіційно. Можна викликати з rc, rc.sysinit або /etc/inittab.|
|Файлова система|/etc/mtools.conf|Конфігурація для всіх операцій (mkdir, копіювання, форматування тощо) у файловій системі типу DOS.|
|Адміністрування системи|/etc/shells|Зберігає список можливих «оболонок», доступних системі.|
|Мережа|/etc/gated.conf|Конфігурація для закритого. Використовується лише закритим демоном.|
|Системні команди|/etc/logrotate.conf|Конфігурація для динамічного компонувальника.|
|Daemons|/etc/httpd.conf|Файл конфігурації для Apache, веб-сервера. Цей файл зазвичай не знаходиться в /etc.|
|Програми користувача| /etc/lynx.cfg| Налаштування проксі|
### Приклад файлу AWS CONFIG
Часто використовувані параметри конфігурації та облікові дані можна зберегти у файлах CONFIG, які підтримуються AWS CLI. Файл CONFIG має бути відкритим текстом у такому форматі:
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
### Приклад файлу CONFIG SSH
Клієнтський файл конфігурації OpenSSH називається CONFIG і зберігається в каталозі .ssh. Файл SSH CONFIG складається з такої структури:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Приклад файлу CONFIG Python
Файл CONFIG Python може виглядати так:

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



## Список літератури

* [Розуміння файлів конфігурації Linux](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Налаштування файлу конфігурації та облікових даних](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Файли конфігурації в Python](https://martin-thoma.com/configuration-files-in-python/)

