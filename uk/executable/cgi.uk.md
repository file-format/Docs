{
  "date" : "2021-06-28",
  "keywords" :[ "файл cgi", "що таке файл cgi", "файл", "приклад cgi", "розширення файлу cgi", "розширення", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Дізнайтеся про формат файлу CGI та API, які можуть створювати та відкривати файли CGI.",
  "title" :"CGI - файл сценарію загального інтерфейсу шлюзу",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Що таке файл CGI?
Файл CGI відомий як сценарій загального інтерфейсу шлюзу, який використовується веб-сервером для запуску зовнішньої програми для обробки запитів користувачів. Сценарій, збережений у файлі з розширенням .cgi, зазвичай написаний мовами програмування C або Perl. Було представлено з перших днів Інтернету, коли веб-розробники хотіли підключити бази даних до своїх веб-серверів. Сервер, який підтримував загальний шлюз між веб-сервером і базами даних, добре підходив для виконання коду CGI.

## Формат файлу CGI
Сценарії CGI використовуються веб-сервером, щоб допомогти власнику налаштувати спосіб обробки URL-адреси. Процедура зазвичай виконується шляхом позначення нового каталогу (де в основному знаходяться документи) як такий, що містить сценарії CGI; його загальновідома назва - cgi-bin. Наприклад, /usr/local/apache/htdocs/cgi-bin можна вибрати як каталог CGI на веб-сервері. Коли веб-браузер запитує URL-адресу, яка вказує на файл у каталозі CGI, тоді замість того, щоб просто надсилати цей файл (/uk/usr/local/apache/htdocs/cgi-bin/printenv.pl) веб-браузеру, HTTP сервер виконує вказаний сценарій і повертає результат сценарію веб-браузеру. Коротше кажучи, усе, що сценарій CGI надсилається на стандартний вихід, передається веб-клієнту замість того, щоб показуватися в терміналі або вікні.

### Приклад CGI

Наступний сценарій CGI, написаний на Perl, який показує всі змінні середовища, передані веб-сервером:
```
#!/usr/bin/env perl

=head1 DESCRIPTION

printenv — a CGI program that just prints its environment

=cut
print "Content-Type: text/plain\n\n";

for my $var ( sort keys %ENV ) {
    printf "%s=\"%s\"\n", $var, $ENV{$var};
}
```

Результат буде таким:
```
COMSPEC="C:\Windows\system32\cmd.exe"
DOCUMENT_ROOT="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/htdocs"
GATEWAY_INTERFACE="CGI/1.1"
HOME="/home/SYSTEM"
HTTP_ACCEPT="text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8"
HTTP_ACCEPT_CHARSET="ISO-8859-1,utf-8;q=0.7,*;q=0.7"
HTTP_ACCEPT_ENCODING="gzip, deflate, br"
HTTP_ACCEPT_LANGUAGE="en-us,en;q=0.5"
HTTP_CONNECTION="keep-alive"
HTTP_HOST="example.com"
HTTP_USER_AGENT="Mozilla/5.0 (Windows NT 6.1; WOW64; rv:67.0) Gecko/20100101 Firefox/67.0"
PATH="/home/SYSTEM/bin:/bin:/cygdrive/c/progra~2/php:/cygdrive/c/windows/system32:..."
PATHEXT=".COM;.EXE;.BAT;.CMD;.VBS;.VBE;.JS;.JSE;.WSF;.WSH;.MSC"
PATH_INFO="/foo/bar"
PATH_TRANSLATED="C:\Program Files (x86)\Apache Software Foundation\Apache2.4\htdocs\foo\bar"
QUERY_STRING="var1=value1&var2=with%20percent%20encoding"
REMOTE_ADDR="127.0.0.1"
REMOTE_PORT="63555"
REQUEST_METHOD="GET"
REQUEST_URI="/cgi-bin/printenv.pl/foo/bar?var1=value1&var2=with%20percent%20encoding"
SCRIPT_FILENAME="C:/Program Files (x86)/Apache Software Foundation/Apache2.4/cgi-bin/printenv.pl"
SCRIPT_NAME="/cgi-bin/printenv.pl"
SERVER_ADDR="127.0.0.1"
SERVER_ADMIN="(server admin's email address)"
SERVER_NAME="127.0.0.1"
SERVER_PORT="80"
SERVER_PROTOCOL="HTTP/1.1"
SERVER_SIGNATURE=""
SERVER_SOFTWARE="Apache/2.4.39 (Win32) PHP/7.3.7"
SYSTEMROOT="C:\Windows"
TERM="cygwin"
WINDIR="C:\Windows"
```
## Використання сценаріїв CGI
Файли CGI, що містять сценарії CGI, зазвичай використовуються для обробки вхідних даних від користувача та отримання відповідних вихідних даних. Реалізація вікі є одним із прикладів програми CGI. Якщо агент користувача надсилає запит на назву запису, веб-сервер запускає програму CGI. Програма CGI отримує вихідний код сторінки цього запису, перетворює його на HTML і друкує результат. Веб-сервер отримує вихідні дані від програми CGI і повертає їх агенту користувача. Тоді, якщо агент користувача викликає функцію редагування, натиснувши кнопку «Редагувати сторінку», програма CGI показує текстове поле HTML або інший елемент керування редагуванням із вмістом сторінки. Нарешті, якщо агент користувача натискає кнопку «Опублікувати сторінку», програма CGI перетворює оновлений HTML у вихідний код сторінки цього запису та зберігає його.



## Список літератури

* [Загальний інтерфейс шлюзу – від Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

