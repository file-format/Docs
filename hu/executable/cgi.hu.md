{
  "date" : "2021-06-28",
  "keywords" :[ "cgi fájl", "mi az a cgi fájl", "fájl", "cgi példa", "cgi fájl kiterjesztése", "kiterjesztés", "formátum" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"További információ a CGI-fájlformátumról és az API-król, amelyek CGI-fájlokat hozhatnak létre és nyithatnak meg.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Mi az a CGI fájl?
A CGI-fájlt Common Gateway Interface parancsfájlként ismerik, amelyet a webszerver külső program futtatására használ felhasználói kérések feldolgozására. A .cgi kiterjesztésű fájlba mentett szkript általában C vagy Perl programozási nyelven íródott. Ezt a web kezdete óta vezették be, amikor a webfejlesztők adatbázisokat akartak csatlakoztatni webszervereikhez. A webszerver és az adatbázisok közötti közös átjárót támogató szerver kiválóan alkalmas volt a CGI kód végrehajtására.

## CGI fájl formátum
A CGI-szkripteket a webszerver arra használja, hogy megkönnyítse a tulajdonosnak az URL kezelésének beállítását. Az eljárás általában úgy történik, hogy egy új könyvtárat (ahol a legtöbb dokumentum található) megjelölünk CGI-szkripteket tartalmazóként; közismert neve cgi-bin. Például a /usr/local/apache/htdocs/cgi-bin kiválasztható CGI-könyvtárként a webszerveren. Amikor egy webböngésző olyan URL-t kér, amely a CGI könyvtárban lévő fájlra mutat, akkor ahelyett, hogy egyszerűen elküldené a fájlt (/hu/usr/local/apache/htdocs/cgi-bin/printenv.pl) a webböngészőnek, a HTTP szerver végrehajtja a megadott parancsfájlt, és visszaküldi a szkript kimenetét a webböngészőnek. Röviden, bármi, amit a CGI-szkript a szabványos kimenetre küld, átkerül a webes kliensbe, ahelyett, hogy az ablak termináljában jelenne meg.

### CGI példa

A következő Perl-ben írt CGI-szkript, amely megmutatja a webszerver által átadott összes környezeti változót:
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

A kimenet a következő lesz:
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
## A CGI-szkriptek használata
A CGI-szkripteket tartalmazó CGI-fájlok általában a felhasználó bemeneti adatainak feldolgozására és a vonatkozó kimeneti adatok előállítására szolgálnak. A wiki megvalósítása a CGI program egyik példája. Ha a felhasználói ügynök kérelmet küld egy bejegyzés nevére, a webszerver futtatja a CGI programot. A CGI program lekéri a bejegyzés oldalának forrását, HTML-be konvertálja, és kinyomtatja az eredményt. A webszerver megkapja a CGI program kimenetét, és visszaküldi azt a felhasználói ügynöknek. Ezután, ha a felhasználói ügynök az "Oldal szerkesztése" gombra kattintva meghívja a szerkesztési funkciót, a CGI program egy HTML szövegterületet vagy más szerkesztési vezérlőt jelenít meg az oldal tartalmával. Végül, ha a felhasználói ügynök rákattint az "Oldal közzététele" gombra, a CGI program a frissített HTML-t a bejegyzés oldalának forrásává alakítja, és elmenti.



## Hivatkozások

* [Common Gateway Interface – Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

