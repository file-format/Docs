{
  "date": "2021-06-28",
  "keywords": [
"cgi failą",
"kas yra cgi failas",
"failą",
"cgi pavyzdys",
"cgi failo plėtinys",
"pratęsimas",
"formatu"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Sužinokite apie CGI failo formatą ir API, kurios gali kurti ir atidaryti CGI failus.",
  "title": "CGI – bendrojo šliuzo sąsajos scenarijaus failas",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-lti"
}
},
  "lastmod": "2021-06-28"
}

## Kas yra CGI failas?
CGI failas yra žinomas kaip Common Gateway Interface scenarijus, kurį žiniatinklio serveris naudoja išorinei programai paleisti, kad apdorotų vartotojo užklausas. Scenarijus, išsaugotas faile su plėtiniu .cgi, paprastai yra parašytas C arba Perl programavimo kalbomis. Jis buvo pristatytas nuo pirmųjų žiniatinklio dienų, kai žiniatinklio kūrėjai norėjo prijungti duomenų bazes prie savo žiniatinklio serverių. Serveris, palaikantis bendrus vartus tarp žiniatinklio serverio ir duomenų bazių, puikiai tiko vykdyti CGI kodą.

## CGI failo formatas
CGI scenarijus naudoja žiniatinklio serveris, kad savininkas galėtų konfigūruoti, kaip bus tvarkomas URL. Procedūra paprastai atliekama pažymint naują katalogą (kur daugiausia yra dokumentai), kuriame yra CGI scenarijų; jos plačiai žinomas pavadinimas yra cgi-bin. Pavyzdžiui, /usr/local/apache/htdocs/cgi-bin gali būti pasirinktas kaip CGI katalogas žiniatinklio serveryje. Kai žiniatinklio naršyklė prašo URL, nukreipiančio į failą CGI kataloge, užuot tiesiog siuntęs tą failą (/usr/local/apache/htdocs/cgi-bin/printenv.pl) į žiniatinklio naršyklę, HTTP serveris vykdo nurodytą scenarijų ir grąžina scenarijaus išvestį į žiniatinklio naršyklę. Trumpai tariant, viskas, kas CGI scenarijus siunčiama į standartinę išvestį, perkeliama į žiniatinklio klientą, o ne rodoma lango terminale.

### CGI pavyzdys

Po CGI scenarijaus, parašyto Perl, kuris rodo visus aplinkos kintamuosius, kuriuos perduoda žiniatinklio serveris:
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

Išvestis bus tokia:
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
## CGI scenarijų naudojimas
CGI failai, kuriuose yra CGI scenarijų, paprastai naudojami apdoroti įvesties duomenis iš vartotojo ir sukurti atitinkamus išvesties duomenis. Wiki diegimas yra vienas iš CGI programos pavyzdžių. Jei vartotojo agentas siunčia užklausą dėl įrašo pavadinimo, žiniatinklio serveris paleidžia CGI programą. CGI programa gauna to įrašo puslapio šaltinį, konvertuoja jį į HTML ir išspausdina rezultatą. Žiniatinklio serveris gauna išvestį iš CGI programos ir grąžina ją vartotojo agentui. Tada, jei vartotojo agentas iškviečia redagavimo funkciją spustelėdamas mygtuką Redaguoti puslapį, CGI programa parodo HTML teksto sritį arba kitą redagavimo valdiklį su puslapio turiniu. Galiausiai, jei vartotojo agentas spusteli mygtuką Paskelbti puslapį, CGI programa konvertuoja atnaujintą HTML į to įrašo puslapio šaltinį ir išsaugo jį.



## Nuorodos 

* [Bendroji šliuzo sąsaja – pateikė Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


