{
  "date" : "2021-06-28",
  "keywords" :[ "fișier cgi", "ce este un fișier cgi", "fișier", "exemplu cgi", "extensie fișier cgi", "extensie", "format"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aflați despre formatul de fișier CGI și despre API-urile care pot crea și deschide fișiere CGI.",
  "title" :"CGI - Common Gateway Interface Script File",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## Ce este un fișier CGI?
Un fișier CGI este cunoscut sub numele de script Common Gateway Interface care este utilizat de un server web pentru a rula un program extern pentru a procesa cererile utilizatorilor. Scriptul care a fost salvat într-un fișier cu extensia .cgi este de obicei scris în limbaje de programare C sau Perl. A fost introdus încă din primele zile ale Web-ului, când dezvoltatorii Web doreau să conecteze bazele de date la serverele lor Web. Un server care a suportat o poartă comună între serverul Web și baze de date era foarte potrivit pentru a executa codul CGI.

## Format de fișier CGI
Scripturile CGI sunt folosite de serverul Web pentru a facilita proprietarului să configureze modul în care va fi gestionată o adresă URL. Procedura se face de obicei prin marcarea unui director nou (unde sunt localizate în principal documentele) ca conţinând scripturi CGI; numele său cunoscut este cgi-bin. De exemplu, /usr/local/apache/htdocs/cgi-bin ar putea fi ales ca director CGI pe serverul Web. Când un browser Web solicită o adresă URL care indică un fișier din directorul CGI, atunci, în loc să trimită pur și simplu acel fișier (/ro/usr/local/apache/htdocs/cgi-bin/printenv.pl) către browserul Web, HTTP serverul execută scriptul specificat și returnează rezultatul scriptului în browserul Web. Pe scurt, orice script-ul CGI este trimis la ieșirea standard este transferat către clientul Web în loc să fie afișat într-un terminal al ferestrei.

### Exemplu CGI

Urmează scriptul CGI scris în Perl care arată toate variabilele de mediu transmise de serverul web:
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

Ieșirea va fi astfel:
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
## Utilizări ale scripturilor CGI
Fișierele CGI care conțin scripturile CGI sunt de obicei folosite pentru a procesa datele de intrare de la utilizator și pentru a produce datele de ieșire relevante. Implementarea unui wiki este unul dintre exemplele de program CGI. Dacă agentul utilizator trimite o cerere pentru numele unei intrări, serverul Web rulează programul CGI. Programul CGI obține sursa paginii acelei intrări, o convertește în HTML și tipărește rezultatul. Serverul Web primește rezultatul de la programul CGI și îl returnează agentului utilizator. Apoi, dacă agentul utilizator apelează funcția de editare făcând clic pe butonul „Editare pagină”, programul CGI arată o zonă de text HTML sau alt control de editare cu conținutul paginii. În cele din urmă, dacă agentul utilizator face clic pe butonul „Publicare pagină”, programul CGI convertește HTML actualizat în sursa paginii acelei intrări și o salvează.



## Referințe

* [Common Gateway Interface - de la Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

