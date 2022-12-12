{
  "date" : "2021-06-28",
  "keywords" :["plik cgi", "co to jest plik cgi", "plik", "przykład cgi", "rozszerzenie pliku cgi", "rozszerzenie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Poznaj format plików CGI i interfejsy API, które mogą tworzyć i otwierać pliki CGI.",
  "title" :"CGI - plik skryptowy wspólnego interfejsu bramy",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Czym jest plik CGI?
Plik CGI jest znany jako skrypt Common Gateway Interface, który jest używany przez serwer WWW do uruchamiania zewnętrznego programu do przetwarzania żądań użytkowników. Skrypt zapisany w pliku z rozszerzeniem .cgi jest zazwyczaj napisany w językach programowania C lub Perl. Został wprowadzony od początków sieci Web, kiedy twórcy stron internetowych chcieli łączyć bazy danych ze swoimi serwerami sieciowymi. Serwer, który obsługiwał wspólną bramę między serwerem WWW a bazami danych, dobrze nadawał się do wykonania kodu CGI.

## Format pliku CGI
Skrypty CGI są używane przez serwer WWW, aby ułatwić właścicielowi skonfigurowanie sposobu obsługi adresu URL. Procedura zwykle polega na oznaczeniu nowego katalogu (gdzie głównie znajdują się dokumenty) jako zawierającego skrypty CGI; jego powszechnie znana nazwa to cgi-bin. Na przykład /usr/local/apache/htdocs/cgi-bin może zostać wybrany jako katalog CGI na serwerze WWW. Kiedy przeglądarka internetowa żąda adresu URL wskazującego plik w katalogu CGI, zamiast po prostu wysłać ten plik (/pl/usr/local/apache/htdocs/cgi-bin/printenv.pl) do przeglądarki internetowej, HTTP serwer wykona określony skrypt i zwróci dane wyjściowe skryptu do przeglądarki internetowej. Krótko mówiąc, wszystko, co skrypt CGI jest wysyłane na standardowe wyjście, jest przesyłane do klienta WWW zamiast pokazywane w terminalu okna.

### Przykład CGI

Poniższy skrypt CGI napisany w Perlu, który pokazuje wszystkie zmienne środowiskowe przekazywane przez serwer WWW:
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

Dane wyjściowe będą wyglądać następująco:
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
## Zastosowania skryptów CGI
Pliki CGI zawierające skrypty CGI są zwykle używane do przetwarzania danych wejściowych od użytkownika i generowania odpowiednich danych wyjściowych. Implementacja wiki jest jednym z przykładów programu CGI. Jeśli agent użytkownika wyśle żądanie nazwy wpisu, serwer WWW uruchamia program CGI. Program CGI pobiera źródło strony tego wpisu, konwertuje je do formatu HTML i drukuje wynik. Serwer WWW odbiera dane wyjściowe z programu CGI i zwraca je do klienta użytkownika. Następnie, jeśli agent użytkownika wywoła funkcję edycji, klikając przycisk „Edytuj stronę”, program CGI wyświetli pole tekstowe HTML lub inną kontrolkę edycji z zawartością strony. Wreszcie, jeśli agent użytkownika kliknie przycisk „Opublikuj stronę”, program CGI konwertuje zaktualizowany kod HTML na źródło strony tego wpisu i zapisuje go.



## Bibliografia

* [Common Gateway Interface – Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

