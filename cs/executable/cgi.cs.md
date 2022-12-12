{
  "date" : "2021-06-28",
  "keywords" :[ "soubor cgi", "co je soubor cgi", "soubor", "příklad cgi", "přípona souboru cgi", "přípona", "formát" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Další informace o formátu souborů CGI a rozhraních API, která mohou vytvářet a otevírat soubory CGI.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Co je soubor CGI?
Soubor CGI je známý jako skript Common Gateway Interface, který používá webový server ke spuštění externího programu pro zpracování požadavků uživatelů. Skript uložený v souboru s příponou .cgi je obvykle napsán v programovacích jazycích C nebo Perl. Byl zaveden od počátků webu, kdy weboví vývojáři chtěli připojit databáze ke svým webovým serverům. Server, který podporoval společnou bránu mezi webovým serverem a databázemi, se dobře hodil ke spuštění kódu CGI.

## Formát souboru CGI
Skripty CGI používá webový server, aby umožnil vlastníkovi nakonfigurovat, jak bude s URL nakládáno. Procedura se obvykle provádí označením nového adresáře (kde jsou převážně umístěny dokumenty) jako obsahující CGI skripty; jeho obecně známý název je cgi-bin. Například /usr/local/apache/htdocs/cgi-bin lze vybrat jako adresář CGI na webovém serveru. Když webový prohlížeč požaduje adresu URL, která ukazuje na soubor v adresáři CGI, pak namísto pouhého odeslání tohoto souboru (/cs/usr/local/apache/htdocs/cgi-bin/printenv.pl) do webového prohlížeče, server provede zadaný skript a vrátí výstup skriptu do webového prohlížeče. Stručně řečeno, cokoli, co je skript CGI odeslán na standardní výstup, je přeneseno do webového klienta místo toho, aby bylo zobrazeno v terminálu okna.

### Příklad CGI

Následující skript CGI napsaný v Perlu, který zobrazuje všechny proměnné prostředí předané webovým serverem:
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

Výstup bude vypadat následovně:
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
## Použití CGI skriptů
Soubory CGI obsahující skripty CGI se obvykle používají ke zpracování vstupních dat od uživatele a vytváření příslušných výstupních dat. Implementace wiki je jedním z příkladů CGI programu. Pokud uživatelský agent odešle požadavek na název položky, webový server spustí program CGI. Program CGI získá zdroj stránky tohoto záznamu, převede jej do HTML a vytiskne výsledek. Webový server obdrží výstup z programu CGI a vrátí jej uživatelskému agentovi. Pokud pak uživatelský agent zavolá funkci úprav kliknutím na tlačítko „Upravit stránku“, program CGI zobrazí textovou oblast HTML nebo jiný ovládací prvek pro úpravy s obsahem stránky. Nakonec, pokud uživatelský agent klikne na tlačítko „Publikovat stránku“, program CGI převede aktualizovaný kód HTML na zdrojový kód stránky tohoto záznamu a uloží jej.



## Reference

* [Common Gateway Interface – od Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

