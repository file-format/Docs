{
  "date": "2021-06-28",
  "keywords": [
"comhad cgi",
"cad is comhad cgi ann",
"comhad",
"sampla cgi",
"síneadh comhad cgi",
"síneadh",
"formáid"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "Foghlaim faoi fhormáid comhaid CGI agus APIanna ar féidir leo comhaid CGI a chruthú agus a oscailt.",
  "title": "CGI - Comhad Script Chomhéadain Coiteann Geata",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-gai"
}
},
  "lastmod": "2021-06-28"
}

## Cad is comhad CGI ann?
Tugtar script Chomhéadain Choiteann Tairseach ar chomhad CGI a úsáideann freastalaí gréasáin chun clár seachtrach a rith chun iarratais úsáideoirí a phróiseáil. Is i dteangacha ríomhchlárúcháin C nó Perl a scríobhtar an script a shábháiltear i gcomhad le síneadh .cgi de ghnáth. Tugadh isteach é ó laethanta tosaigh an Ghréasáin, nuair a bhí forbróirí Gréasáin ag iarraidh bunachair shonraí a nascadh lena bhfreastalaithe Gréasáin. Bhí freastalaí a thacaigh le geata coiteann idir freastalaí Gréasáin agus bunachair shonraí oiriúnach go maith chun an cód CGI a fheidhmiú.

## Formáid Comhaid CGI
Úsáideann an freastalaí Gréasáin na scripteanna CGI chun éascú don úinéir conas a láimhseáiltear URL a chumrú. De ghnáth déantar an nós imeachta trí eolaire nua a mharcáil (ina bhfuil na doiciméid suite go príomha) mar a bhfuil scripteanna CGI ann; is é an t-ainm a thugtar air go coitianta ná cgi-bin. Mar shampla, d’fhéadfaí /usr/local/apache/htdocs/cgi-bin a phiocadh mar eolaire CGI ar an bhfreastalaí Gréasáin. Nuair a iarrann brabhsálaí Gréasáin URL a dhíríonn ar chomhad laistigh den eolaire CGI, ansin, in ionad an comhad sin (/ usr/local/apache/htdocs/cgi-bin/printenv.pl) a sheoladh chuig an mbrabhsálaí Gréasáin, an HTTP déanann an freastalaí an script sonraithe agus seolfaidh sé aschur na scripte chuig an mbrabhsálaí Gréasáin. I mbeagán focal, aistrítear aon rud a sheoltar an script CGI chuig aschur caighdeánach chuig an gcliant Gréasáin seachas é a thaispeáint i gcríochfort fuinneoige.

### Sampla CGI

Ag leanúint script CGI scríofa i Perl a thaispeánann na hathróga timpeallachta go léir a rith an freastalaí Gréasáin:
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

Beidh an t-aschur mar seo a leanas:
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
## Úsáidí scripteanna CGI
Úsáidtear na comhaid CGI ina bhfuil na scripteanna CGI de ghnáth chun sonraí ionchuir ón úsáideoir a phróiseáil agus na sonraí aschuir ábhartha a tháirgeadh. Tá cur i bhfeidhm vicí ar cheann de na samplaí de chlár CGI. Má sheolann an gníomhaire úsáideora iarratas ar ainm iontrála, ritheann an freastalaí Gréasáin an clár CGI. Faigheann an clár CGI foinse leathanach na hiontrála sin, tiontaigh go HTML é, agus prionnaíonn sé an toradh. Faigheann an freastalaí Gréasáin an t-aschur ón gclár CGI agus cuireann sé ar ais chuig an ngníomhaire úsáideora é. Ansin, má ghlaonn an gníomhaire úsáideora an fheidhm eagarthóireachta trí chliceáil ar an gcnaipe Cuir Leathanach in Eagar, taispeánann an clár CGI réimse téacs HTML nó rialú eagarthóireachta eile le hinneachar an leathanaigh. Ar deireadh, má chliceálann an gníomhaire úsáideora an cnaipe Foilsigh leathanach, athraíonn an clár CGI an HTML nuashonraithe isteach i bhfoinse leathanach na hiontrála sin agus sábhálann sé é.



## Tagairtí 

* [Common Gateway Interface - le Wikipewdia](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


