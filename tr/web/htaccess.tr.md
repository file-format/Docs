{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTACESS Dosyası - Apache HTACCESS Dosya Biçimi",
  "description" :"HTACCESS dosyasının ne olduğunu öğrenmek için dosya biçimi kılavuzunuz",
  "linktitle" : "HTACCESS",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## HTACCESS dosyası nedir?

HTACCESS dosyası, bir web sitesinin farklı klasörleri/dizinleri için yapılandırma değişikliklerine izin veren bir mekanizma sağlayan bir Apache yapılandırma dosyasıdır. Dizin ve alt dizinler için geçerli olan yapılandırma yönergelerini içerir.

Bir HTACCESS dosyası, bir web sitesinin dizin sayfasını tanımlama, 404 (Sayfa Bulunamadı) hata sayfasını listeleme, 301 veya 302 sayfa yönlendirmelerini gerçekleştirme, belirli bir IP adresinden veya diğer web sitelerinden erişimi engelleme gibi bir dizi kontrol gerçekleştirir. .htaccess dosyalarının kullanımı, bu nedenle, Apache [HTTP](/tr/web/http/) sunucunuzun genel performansını yavaşlatır.

## HTACCESS Dosya Biçimi

HTACCESS dosyaları, düz metin dosyası biçiminde diske kaydedilir. Bu, bu dosyaları herhangi bir metin düzenleyicide açıp düzenleyebileceğiniz anlamına gelir. "." den önce isim yoktur. .htaccess dosyasında, klasör içinde gizli bir dosya olduğunu gösterir.

## Bir HTACCESS Dosyasının yaygın kullanımları

Bir HTACCESS dosyasının beş yaygın kullanımı aşağıdaki gibidir.

### Mod_Yeniden Yazma

Bir web sitesindeki URL'lerin ve web sayfalarının kullanıcılara nasıl görüntüleneceğini belirlemek ve değiştirmek için bir HTACCESS dosyası kullanılabilir.

### Kimlik doğrulama

Kimlik doğrulama, .htaccess ile .htpasswd adlı bir şifre dosyası oluşturularak gerçekleştirilebilir. Bu, site ziyaretçilerinin web sayfasının belirli bir bölümünü ziyaret etmek isterlerse bir şifre sağlamalarını sağlar.

### Özel Hata Sayfaları

.htaccess dosyası ile 400 Bad Request, 401 Authorization Required, 403 Forbidden Page, 404 File Not Found, 500 Internal Error gibi özel hata sayfaları oluşturabilirsiniz. Ancak, tüm bu kontroller sayfalara erişildikçe gerçekleştirileceğinden sunucu performansını yavaşlatacaktır.

### MIME Türleri

Apache HTACCESS dosyaları, Çok Amaçlı İnternet Posta Uzantıları (MIME) türlerini içerecek şekilde değiştirilebilir. Bu, sunucunuzun site tarafından desteklenmeyen uygulama dosyalarının teslimini desteklemesini sağlar.

### SGK

Sunucu Tarafı İçeriği (SSI), bir web sitesinde harika bir zaman tasarrufu sağlar. SSI, .htaccess dosyanıza aşağıdaki kodu ekleyerek etkinleştirilebilir.

```
AddType text/html .shtml
AddHandler server-parsed .shtml</pre>
```

## Apache HTACCESS Dosya Örneği

```
AuthType Basic
AuthName "Restricted Content"
AuthUserFile /etc/apache2/.htpasswd
Require valid-user
```

## Referanslar

* [Apache HTTP Sunucusu Eğitimi: .htaccess dosyaları](https://httpd.apache.org/docs/current/howto/htaccess.html)

