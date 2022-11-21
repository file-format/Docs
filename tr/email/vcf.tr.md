{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCF - Sanal Kişi Dosyası",
  "description":"VCF dosya formatı ve VCF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "VCF",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## .vcf dosyası nedir?

VCF (Sanal Kart Formatı) veya vCard, iletişim bilgilerini saklamak için kullanılan bir dijital dosya formatıdır. Biçim, popüler bilgi alışverişi uygulamaları arasında veri alışverişi için yaygın olarak kullanılır. Windows ve MacOS gibi çoğu işletim sistemi, bu dosyaları oluşturmak ve açmak için varsayılan uygulamalarla birlikte gelir. Tek bir VCF dosyası, bir veya daha fazla kişinin iletişim bilgilerini içerebilir. Bir VCF dosyası genellikle kişinin adı, adresi, telefon numarası, e-postası, doğum günü, fotoğrafları ve sesi gibi bilgileri ve bir dizi başka alanı içerir. E-posta istemcileri ve hizmetleri tarafından desteklendiğinden, vCard formatı kullanılarak kişilerin aktarımı sırasında veri kaybı olmaz. VCF dosya biçimi için ortam türü metin/vcard'dır.

## VCF Dosya Biçimi

VCF dosyaları doğası gereği metinseldir ve insanlar tarafından okunabilir. Bunlar, Microsoft Windows'ta Notepad ve MacOS'ta TextEdit gibi metin editörlerinde açılabilir. Ancak dosyada bir resim varsa, metin düzenleyicide gösterilmez.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) için destek sağlar VCF dosyalarını açmanın yanı sıra popüler [MSG](/tr/email/msg/) biçimi gibi bir dizi başka biçime dönüştürün. VCF dosya formatı, dosya formatına ayrıntılı bilgiler ekleyerek sürüm 2.1'den 4.0'a zamanla geliştirildi. Format, telefon kişilerini dışa aktarmak ve daha sonra başka bir cihaza aktarmak için de kullanılır.

{{< figure src="../VCF.png" alt="VCF Dosya Biçimi" >}}

### VCF 2.1 Örneği

Aşağıda 2.1 sürümünün bir örneği verilmiştir.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 Örneği

Aşağıda 3.0 sürümünün bir örneği verilmiştir.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 Örneği

Aşağıda 4.0 sürümünün bir örneği verilmiştir.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## Referanslar

* [VCF - Wikipedia'dan](https://en.wikipedia.org/wiki/VCard)

