{
  "date" : "2021-04-23",
  "keywords": [ "config File", "configuration files", "config File format", "extension", "format","git config file","Configuration files in Linux","what is a config file","Config file php", "ssh config file example", "aws config file example", "python config file example" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CONFIG - Yapılandırma Dosyası",
  "description":"CONFIG örneği ve CONFIG dosyalarını oluşturabilen ve açabilen API'ler ile CONFIG dosya formatı hakkında bilgi edinin.",
  "linktitle" : "CONFIG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-04-23"
}

## CONFIG dosyası nedir?
CONFIG dosyası, yapılandırma dosyası olarak bilinir; çeşitli bilgisayar yazılımları için parametreleri ve birincil ayarları yapılandırmak için kullanılır. Bazı yazılımlar başlangıçta yalnızca **yapılandırma dosyalarını** okur. Diğerleri, yapılandırma dosyalarını periyodik olarak değişiklikler için kontrol eder.

## YAPILANDIRMA Dosya biçimi
**CONFIG Dosya formatı** sunucu işlemleri, yazılım uygulamaları ve işletim sistemi ayarları için kullanılır. Bir programcı, bir yazılıma belirli bir süre sonra yapılandırma dosyalarını tekrar tekrar okuması ve değişiklikleri mevcut sürece uygulaması talimatını vermek için kod yazabilir. CONFIG dosya sistem dizini için kesin standartlar veya güçlü kurallar yoktur. Örneğin, Microsoft'un Web.config dosyası, [XML](/web/xml/) tabanlı etiket kümelerinden oluşan CONFIG dosya biçimine aittir; Microsoft Visual Studio veya başka bir metin düzenleyici ile düzenlenebilir.

## Yapılandırma dosyası örnekleri:
Konfigürasyon dosyaları herhangi bir kurala, standarda veya uzlaşıma göre oluşturulmadığından, bu dosyalar farklı formatlarda yazılmış olabilir. Bir .config dosyası XML, [JSON](/web/json/) veya başka herhangi bir formatı temel alabilir. Aşağıda, iyi bilinen işletim sistemleri ve yazılımlar için yapılandırma dosyası örnekleri verilmiştir:

### Linux'ta yapılandırma dosyaları
Her Linux programı, CPU'nun tipik işlemleri gerçekleştirmek için yürüttüğü **işlem kodları** listesini tutan yürütülebilir bir dosyadır. Hemen hemen her programın işlemleri, yapılandırma dosyaları değiştirilerek gereksinimlerinize göre özelleştirilebilir. Linux sistemindeki birçok yapılandırma dosyası /etc dizinindedir. Yapılandırma dosyaları aşağıdaki kategorilerde sınıflandırılabilir:
|Kategori|Örnek| Yorumlar|
---|---|---|
|Dosyalara erişim|/etc/host.conf|Ağ etki alanı sunucusuna ana bilgisayar adlarını nasıl arayacağını söyler.|
|Önyükleme ve oturum açma/çıkış|/etc/rc.d/rc.local|Resmi değil. rc, rc.sysinit veya /etc/inittab.|
|Dosya sistemi|/etc/mtools.conf|DOS tipi bir dosya sistemindeki tüm işlemler (mkdir, kopyalama, biçimlendirme vb.) için yapılandırma.|
|Sistem yönetimi|/etc/shells|Sistemin kullanabileceği olası "kabukların" listesini tutar.|
|Ağ oluşturma|/etc/gated.conf|Gated için yapılandırma. Yalnızca kapılı arka plan programı tarafından kullanılır.|
|Sistem komutları|/etc/logrotate.conf|Dinamik Bağlayıcı için Yapılandırma.|
|Daemons|/etc/httpd.conf|Web sunucusu Apache için yapılandırma dosyası. Bu dosya genellikle /etc.|
|Kullanıcı programları| /etc/lynx.cfg| Proxy ayarları|
### AWS CONFIG dosyası örneği
Sık kullanılan yapılandırma ayarları ve kimlik bilgileri, AWS CLI tarafından tutulan CONFIG dosyalarına kaydedilebilir. CONFIG dosyası, aşağıdaki biçimi kullanan bir düz metin dosyası olmalıdır:
```
[default]
region = us-west-2
output = json

[profile dev-user]
region = us-east-1
output = text

[profile developers]
role_arn = arn:aws:iam::123456789012:role/developers
source_profile = dev-user
region = us-west-2
output = json
```
### SSH CONFIG dosyası örneği
OpenSSH istemci tarafı yapılandırma dosyası CONFIG olarak adlandırılır ve .ssh dizininde depolanır. SSH CONFIG dosyası aşağıdaki yapıdan oluşur:
```
Host hostname1
    SSH_OPTION value
    SSH_OPTION value

Host hostname2
    SSH_OPTION value

Host *
    SSH_OPTION value
```
### Python CONFIG dosyası örneği
Bir Python CONFIG dosyası şöyle görünebilir:

```
#!/usr/bin/env python
import preprocessing

mysql = {
    "host": "localhost",
    "user": "root",
    "passwd": "my secret password",
    "db": "write-math",
}
preprocessing_queue = [
    preprocessing.scale_and_center,
    preprocessing.dot_reduction,
    preprocessing.connect_lines,
]
use_anonymous = True
```



## Referanslar

* [Linux yapılandırma dosyalarını anlama](https://developer.ibm.com/technologies/linux/articles/l-config/)
* [Yapılandırma ve kimlik bilgisi dosyası ayarları](https://docs.aws.amazon.com/cli/latest/userguide/cli-configure-files.html)
* [Python'daki yapılandırma dosyaları](https://martin-thoma.com/configuration-files-in-python/)

