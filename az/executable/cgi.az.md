{
  "date": "2021-06-28",
  "keywords": [
"cgi faylı",
"cgi faylı nədir",
"fayl",
"cgi nümunəsi",
"cgi fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "CGI faylları yarada və aça bilən CGI fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "CGI - Ümumi Şlüz İnterfeysi Skript Faylı",
  "linktitle": "CGI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-cg-azi"
}
},
  "lastmod": "2021-06-28"
}

## CGI faylı nədir?
CGI faylı, istifadəçi sorğularını emal etmək üçün xarici proqramı işə salmaq üçün veb server tərəfindən istifadə edilən Ümumi Şlüz İnterfeysi skripti kimi tanınır. .cgi uzantılı faylda saxlanılan skript adətən C və ya Perl proqramlaşdırma dillərində yazılır. Veb tərtibatçıları verilənlər bazalarını öz Veb serverlərinə qoşmaq istədikləri zaman İnternetin ilk günlərindən təqdim edilmişdir. Veb server və verilənlər bazası arasında ümumi şlüzü dəstəkləyən server CGI kodunu yerinə yetirmək üçün çox uyğun idi.

## CGI fayl formatı
CGI skriptləri veb server tərəfindən URL-nin necə idarə olunacağını konfiqurasiya etmək üçün sahibinə kömək etmək üçün istifadə olunur. Prosedur adətən yeni kataloqu (sənədlərin əsasən yerləşdiyi yer) CGI skriptləri kimi qeyd etməklə həyata keçirilir; onun ümumi adı cgi-bindir. Məsələn, /usr/local/apache/htdocs/cgi-bin Veb serverdə CGI kataloqu kimi seçilə bilər. Veb brauzer CGI qovluğunda fayla işarə edən URL tələb etdikdə, həmin faylı sadəcə olaraq (/usr/local/apache/htdocs/cgi-bin/printenv.pl) Veb brauzerə göndərmək əvəzinə, HTTP server müəyyən edilmiş skripti icra edir və skriptin çıxışını Veb brauzerə qaytarır. Bir sözlə, CGI skriptinin standart çıxışa göndərildiyi hər şey pəncərənin terminalında göstərilmək əvəzinə Veb müştəriyə ötürülür.

### CGI Nümunəsi

Veb server tərəfindən ötürülən bütün mühit dəyişənlərini göstərən Perl-də yazılmış aşağıdakı CGI skripti:
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

Çıxış aşağıdakı kimi olacaq:
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
## CGI skriptlərinin istifadəsi
CGI skriptlərini ehtiva edən CGI faylları adətən istifadəçinin giriş məlumatlarını emal etmək və müvafiq çıxış məlumatlarını istehsal etmək üçün istifadə olunur. Viki tətbiq etmək CGI proqramının nümunələrindən biridir. İstifadəçi agenti girişin adı üçün sorğu göndərirsə, Veb server CGI proqramını işə salır. CGI proqramı həmin girişin səhifəsinin mənbəyini alır, onu HTML-yə çevirir və nəticəni çap edir. Veb server CGI proqramından çıxışı alır və onu istifadəçi agentinə qaytarır. Bundan sonra, istifadəçi agenti Səhifəni redaktə et düyməsini klikləməklə redaktə funksiyasını çağırarsa, CGI proqramı HTML mətn sahəsini və ya səhifənin məzmunu ilə digər redaktə nəzarətini göstərir. Nəhayət, əgər istifadəçi agenti Səhifəni dərc et düyməsini klikləsə, CGI proqramı yenilənmiş HTML-ni həmin girişin səhifəsinin mənbəyinə çevirir və onu saxlayır.



## İstinadlar 

* [Ümumi Gateway İnterfeysi - Wikipewdia tərəfindən](https://en.wikipedia.org/wiki/Common_Gateway_Interface)


