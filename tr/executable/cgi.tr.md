{
  "date" : "2021-06-28",
  "keywords" :[ "cgi dosyası", "cgi dosyası nedir", "dosya", "cgi örneği", "cgi dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CGI dosya formatı ve CGI dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CGI - Ortak Ağ Geçidi Arabirimi Komut Dosyası",
  "linktitle" : "CGI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-28"
}

## CGI dosyası nedir?
Bir CGI dosyası, bir web sunucusu tarafından kullanıcı isteklerini işlemek için harici bir program çalıştırmak için kullanılan bir Ortak Ağ Geçidi Arayüzü komut dosyası olarak bilinir. .cgi uzantılı bir dosyaya kaydedilen script, genellikle C veya Perl programlama dillerinde yazılır. Web geliştiricileri veritabanlarını Web sunucularına bağlamak istediklerinde, Web'in ilk günlerinden beri tanıtılmıştı. Web sunucusu ile veritabanları arasında ortak bir ağ geçidini destekleyen bir sunucu, CGI kodunu yürütmek için çok uygundur.

## CGI Dosya Biçimi
CGI betikleri, Web sunucusu tarafından, sahibinin bir URL'nin nasıl işleneceğini yapılandırmasını kolaylaştırmak için kullanılır. Prosedür genellikle yeni bir dizini (belgelerin esas olarak bulunduğu yer) CGI betiklerini içeriyor olarak işaretleyerek yapılır; yaygın olarak bilinen adı cgi-bin'dir. Örneğin /usr/local/apache/htdocs/cgi-bin, Web sunucusunda bir CGI dizini olarak seçilebilir. Bir Web tarayıcısı, CGI dizini içindeki bir dosyaya işaret eden bir URL istediğinde, o dosyayı (/tr/usr/local/apache/htdocs/cgi-bin/printenv.pl) Web tarayıcısına göndermek yerine, HTTP sunucu belirtilen betiği yürütür ve betiğin çıktısını Web tarayıcısına döndürür. Kısacası, CGI betiğinin standart çıktıya gönderdiği her şey, bir pencere terminalinde gösterilmek yerine Web istemcisine aktarılır.

### CGI Örneği

Web sunucusu tarafından iletilen tüm ortam değişkenlerini gösteren Perl ile yazılmış aşağıdaki CGI betiği:
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

Çıktı aşağıdaki gibi olacaktır:
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
## CGI betiklerinin kullanımları
CGI betiklerini içeren CGI dosyaları genellikle kullanıcıdan gelen girdi verilerini işlemek ve ilgili çıktı verilerini üretmek için kullanılır. Bir wiki uygulamak, CGI programının örneklerinden biridir. Kullanıcı aracısı bir girdinin adı için bir istek gönderirse, Web sunucusu CGI programını çalıştırır. CGI programı, bu girdi sayfasının kaynağını alır, HTML'ye dönüştürür ve sonucu yazdırır. Web sunucusu, CGI programından çıktı alır ve kullanıcı aracısına geri gönderir. Ardından, kullanıcı aracısı "Sayfayı Düzenle" düğmesine tıklayarak düzenleme işlevini çağırırsa, CGI programı sayfa içeriğiyle birlikte bir HTML metin alanı veya başka bir düzenleme kontrolü gösterir. Son olarak, kullanıcı aracısı "Sayfayı yayınla" düğmesini tıklarsa, CGI programı güncellenmiş HTML'yi o giriş sayfasının kaynağına dönüştürür ve kaydeder.



## Referanslar

* [Ortak Ağ Geçidi Arayüzü - Wikipewdia tarafından](https://en.wikipedia.org/wiki/Common_Gateway_Interface)

