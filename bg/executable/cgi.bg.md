{
  "date" : "2021-06-28",
  "keywords" :[ "cgi файл", "какво е cgi файл", "файл", "cgi пример", "cgi файлово разширение", "разширение", "формат" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Научете за CGI файловия формат и API, които могат да създават и отварят CGI файлове.",
  "title" :"CGI - файл със скрипт за общ интерфейс на шлюза",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Какво е CGI файл?
CGI файлът е известен като скрипт на Common Gateway Interface, който се използва от уеб сървър за стартиране на външна програма за обработка на потребителски заявки. Скриптът, който се записва във файл с разширение .cgi, обикновено е написан на езици за програмиране C или Perl. Беше въведен от ранните дни на мрежата, когато уеб разработчиците искаха да свържат бази данни към своите уеб сървъри. Сървър, който поддържа общ шлюз между уеб сървъра и базите данни, е много подходящ за изпълнение на CGI кода.

## CGI файлов формат
CGI скриптовете се използват от уеб сървъра, за да улеснят собственика да конфигурира как ще се обработва даден URL адрес. Процедурата обикновено се извършва чрез маркиране на нова директория (където се намират основно документите) като съдържаща CGI скриптове; общоизвестното му име е cgi-bin. Например /usr/local/apache/htdocs/cgi-bin може да се избере като CGI директория на уеб сървъра. Когато уеб браузър поиска URL адрес, който сочи към файл в CGI директорията, тогава, вместо просто да изпрати този файл (/bg/usr/local/apache/htdocs/cgi-bin/printenv.pl) към уеб браузъра, HTTP сървърът изпълнява посочения скрипт и връща резултата от скрипта на уеб браузъра. Накратко, всичко, което CGI скриптът се изпраща към стандартния изход, се прехвърля към уеб клиента, вместо да се показва в терминал или прозорец.

### Пример за CGI

Следва CGI скрипт, написан на Perl, който показва всички променливи на средата, предадени от уеб сървъра:
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

Резултатът ще бъде като следното:
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
## Използване на CGI скриптове
CGI файловете, съдържащи CGI скриптовете, обикновено се използват за обработка на входни данни от потребителя и създаване на съответните изходни данни. Внедряването на wiki е един от примерите за CGI програма. Ако потребителският агент изпрати заявка за името на запис, уеб сървърът изпълнява CGI програмата. Програмата CGI получава източника на страницата на този запис, преобразува го в HTML и отпечатва резултата. Уеб сървърът получава изхода от CGI програмата и го връща на потребителския агент. След това, ако потребителският агент извика функцията за редактиране чрез щракване върху бутона "Редактиране на страница", CGI програмата показва HTML текстово поле или друг контрол за редактиране със съдържанието на страницата. И накрая, ако потребителският агент щракне върху бутона „Публикуване на страницата“, програмата CGI преобразува актуализирания HTML в източника на страницата на този запис и го запазва.



## Препратки

* [Общ интерфейс на шлюза - от Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

