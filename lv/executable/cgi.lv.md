{
  "date": "2021-06-28",
  "keywords": [
"cgi failu",
"kas ir cgi fails",
"failu",
"cgi piemērs",
"cgi faila paplašinājums",
"pagarinājumu",
"formātā"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Uzziniet par CGI failu formātu un API, kas var izveidot un atvērt CGI failus.",
  "title": "CGI — kopējās vārtejas interfeisa skripta fails",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-lvi"
}
},
  "lastmod": "2021-06-28"
}

## Kas ir CGI fails?
CGI fails ir pazīstams kā Common Gateway Interface skripts, ko izmanto tīmekļa serveris, lai palaistu ārēju programmu lietotāju pieprasījumu apstrādei. Skripts, kas saglabāts failā ar paplašinājumu .cgi, parasti ir rakstīts C vai Perl programmēšanas valodās. Tas tika ieviests kopš tīmekļa sākuma, kad tīmekļa izstrādātāji vēlējās savienot datu bāzes ar saviem tīmekļa serveriem. Serveris, kas atbalstīja kopēju vārteju starp Web serveri un datu bāzēm, bija labi piemērots CGI koda izpildei.

## CGI faila formāts
CGI skriptus izmanto tīmekļa serveris, lai atvieglotu īpašniekam konfigurēt, kā tiks apstrādāts URL. Procedūra parasti tiek veikta, atzīmējot jaunu direktoriju (kurā galvenokārt atrodas dokumenti), kas satur CGI skriptus; tā vispārzināmais nosaukums ir cgi-bin. Piemēram, /usr/local/apache/htdocs/cgi-bin var izvēlēties kā CGI direktoriju tīmekļa serverī. Kad tīmekļa pārlūkprogramma pieprasa URL, kas norāda uz failu CGI direktorijā, tad tā vietā, lai vienkārši nosūtītu šo failu (/usr/local/apache/htdocs/cgi-bin/printenv.pl) uz tīmekļa pārlūkprogrammu, HTTP serveris izpilda norādīto skriptu un atgriež skripta izvadi Web pārlūkprogrammā. Īsāk sakot, viss, kas CGI skripts tiek nosūtīts uz standarta izvadi, tiek pārsūtīts uz Web klientu, nevis tiek parādīts loga terminālī.

### CGI piemērs

Pēc Perl rakstītā CGI skripta, kas parāda visus Web servera nodotos vides mainīgos:
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

Izvade būs šāda:
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
## CGI skriptu izmantošana
CGI faili, kas satur CGI skriptus, parasti tiek izmantoti, lai apstrādātu lietotāja ievadītos datus un iegūtu attiecīgos izvades datus. Wiki ieviešana ir viens no CGI programmas piemēriem. Ja lietotāja aģents nosūta pieprasījumu pēc ieraksta nosaukuma, tīmekļa serveris palaiž CGI programmu. CGI programma iegūst šī ieraksta lapas avotu, pārvērš to HTML formātā un izdrukā rezultātu. Web serveris saņem CGI programmas izvadi un atgriež to lietotāja aģentam. Pēc tam, ja lietotāja aģents izsauc rediģēšanas funkciju, noklikšķinot uz pogas Rediģēt lapu, CGI programma parāda HTML teksta apgabalu vai citu rediģēšanas vadīklu ar lapas saturu. Visbeidzot, ja lietotāja aģents noklikšķina uz pogas Publicēt lapu, CGI programma pārvērš atjaunināto HTML par šī ieraksta lapas avotu un saglabā to.



## Atsauces 

* [Common Gateway Interface — Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


