{
  "date" : "2021-06-28",
  "keywords" :[ "файл cgi", "что такое файл cgi", "файл", "пример cgi", "расширение файла cgi", "расширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Узнайте о формате файла CGI и API-интерфейсах, которые могут создавать и открывать файлы CGI.",
  "title" :"CGI — файл сценария общего интерфейса шлюза",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## .CGI вариант №
Файл CGI известен как сценарий общего интерфейса шлюза, который используется веб-сервером для запуска внешней программы для обработки запросов пользователей. Скрипт, сохраненный в файле с расширением .cgi, обычно написан на языках программирования C или Perl. Они были введены с первых дней существования Интернета, когда веб-разработчики хотели подключать базы данных к своим веб-серверам. Сервер, который поддерживал общий шлюз между веб-сервером и базами данных, хорошо подходил для выполнения кода CGI.

## Формат файла CGI
Сценарии CGI используются веб-сервером, чтобы облегчить владельцу настройку обработки URL-адреса. Процедура обычно выполняется путем пометки нового каталога (где в основном находятся документы) как содержащего сценарии CGI; его общеизвестное имя - cgi-bin. Например, /usr/local/apache/htdocs/cgi-bin может быть выбран как каталог CGI на веб-сервере. Когда веб-браузер запрашивает URL-адрес, указывающий на файл в каталоге CGI, вместо того, чтобы просто отправить этот файл (/ru/usr/local/apache/htdocs/cgi-bin/printenv.pl) в веб-браузер, HTTP сервер выполняет указанный сценарий и возвращает результат выполнения сценария в веб-браузер. Короче говоря, все, что сценарий CGI отправляет на стандартный вывод, передается веб-клиенту, а не отображается в терминале или окне.

### Пример компьютерной графики

Следующий CGI-скрипт, написанный на Perl, показывает все переменные среды, передаваемые веб-сервером:
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

Вывод будет примерно следующим:
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
## Использование CGI-скриптов
Файлы CGI, содержащие сценарии CGI, обычно используются для обработки входных данных от пользователя и создания соответствующих выходных данных. Реализация вики является одним из примеров программы CGI. Если пользовательский агент отправляет запрос имени записи, веб-сервер запускает программу CGI. Программа CGI получает исходный код страницы этой записи, преобразует его в HTML и печатает результат. Веб-сервер получает вывод программы CGI и возвращает его пользовательскому агенту. Затем, если пользовательский агент вызывает функцию редактирования, нажимая кнопку «Редактировать страницу», программа CGI показывает текстовую область HTML или другой элемент управления редактированием с содержимым страницы. Наконец, если пользовательский агент нажимает кнопку «Опубликовать страницу», программа CGI преобразует обновленный HTML в исходный код страницы этой записи и сохраняет его.



## использованная литература

* [Общий интерфейс шлюза — от Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

