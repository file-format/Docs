{
  "date" : "2022.01.31",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"P7S Dosyası - Dijital Olarak İmzalanmış E-posta Mesajı",
  "description":"P7S dosya formatı ve P7S dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "P7S",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2022.01.31"
}

## P7S dosyası nedir?

P7S dosyası, dijital olarak imzalanmış bir e-posta ile alınan bir dijital imzadır. Bu dosyanın e-posta eki olarak bulunması, e-postanın gerçek bir kaynaktan gönderildiğini doğrular. Bu, gönderenin bilgisayarında yüklü bir E-posta İmzalama sertifikası olmasını sağlar. Kullanıcının bilgisayarından böyle bir imzalı e-posta gönderildiğinde, gönderenin adını içeren P7S dosyası e-postaya eklenir. İmzalı e-postaları destekleyen e-posta istemcileri, gönderenin bilgilerini görebilir.

## P7S Dosya Biçimi - Daha Fazla Bilgi

S/MIME (Güvenli/Çok Amaçlı İnternet Posta Uzantıları) P7S dosyaları, bilgileri insanların okuyabileceği düz metin biçiminde içerir. Microsoft Outlook, Apple Mail ve Mozilla Thunderbird gibi e-posta istemcileri, bir S/MIME e-postasından dijital olarak imzalanmış bilgileri okumayı destekler. Bir e-postayı imzalamak, gönderenin kimliğini doğrular ve alıcıya mesajın orijinal olduğunu söyler. E-posta istemcilerinden ([EML](/tr/email/eml/) veya [MSG](/tr/email/msg/) olarak) e-postalar indirildiğinde, bu P7S dosyaları bu e-postaların ekinde bulunur.

Bir P7S dosyası aşağıdaki bilgileri içerir:

* E-postanın kaynak kaynağı
* Gönderildiği tarih ve saat,
* İletim sırasında değiştirilip değiştirilmediği

Bu bilgiler, şifrelenmiş imzaları e-postaya dijital olarak eklemek için Açık Anahtar Şifreleme Standardı #7 (PKCS7) teknolojisi kullanılarak yerleştirilmiştir.

## Referanslar ##

* [Microsoft Sign Aracı](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)

