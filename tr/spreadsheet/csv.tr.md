{
  "date" : "2019-12-10",
  "keywords" :[ "CSV", "dosya", "uzantı", "dosya formatı", "Virgülle Ayrılmış Değerler", "Elektronik Tablo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"CSV dosya formatı ve CSV dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CSV Dosya Biçimi",
  "linktitle" : "CSV",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## CSV dosyası nedir?

.csv (Virgülle Ayrılmış Değerler) uzantılı dosyalar, virgülle ayrılmış değerler içeren veri kayıtlarını içeren düz metin dosyalarını temsil eder. Bir CSV dosyasındaki her satır, dosyada bulunan kayıt kümesinden yeni bir kayıttır. Bu tür dosyalar, bir depolama sisteminden diğerine veri aktarımı amaçlandığında oluşturulur. Tüm uygulamalar virgülle ayrılmış kayıtları tanıyabildiğinden, bu tür veri dosyalarının veri tabanına aktarımı çok rahat bir şekilde yapılır. Microsoft Excel veya OpenOffice Calc gibi hemen hemen tüm elektronik tablo uygulamaları, CSV'yi fazla çaba harcamadan içe aktarabilir. Bu tür dosyalardan içe aktarılan veriler, kullanıcıya gösterilmek üzere bir elektronik tablonun hücrelerinde düzenlenir.

## Kısa Tarih ##

Aşağıda, CSV dosya formatının kökeni ve tarihçesi hakkında bazı kısa bilgiler yer almaktadır.

* 1972 - IBM Fortran (seviye H genişletilmiş) derleyicisi bunları OS/360 altında destekledi

* 1978 - Ayırıcılar için virgül ve boşluk kullanan FORTRAN 77 tarafından listeye yönelik girdi/çıktı desteklendi

* 2005 - CSV, MIME İçerik Türü olarak [RFC4180](https://tools.ietf.org/html/rfc4180) ile standardize edildi.

* 2013 - RFC4180'in eksiklikleri bir W3C tavsiyesi ile giderildi

* 2015 - W3C, Aralık 2015'te tavsiye olarak başlayan CSV meta veri standartları için ilk tavsiye taslaklarını yaptı.

## CSV Dosyalarını Dönüştür ##

CSV dosyaları, bu dosyaları açabilen uygulamalar kullanılarak birkaç farklı dosya biçimine dönüştürülebilir. Örneğin, Microsoft Excel, CSV dosya biçiminden verileri içe aktarabilir ve onu XLS, [XLSX](/tr/spreadsheet/xlsx/), [PDF](/tr/pdf/), [TXT](/tr/word-processing/txt/) olarak kaydedebilir. , XML ve [HTML](/tr/web/html/) dosya biçimleri. Benzer şekilde, diğer masaüstü ve çevrimiçi hizmetler, CSV dosyalarını HTML, ODS ve [RTF](/tr/word-processing/rtf/) olarak dışa aktarma yeteneği sağlar.

## CSV Dosya Biçimi ##

CSV dosya biçiminin [RFC4180](https://tools.ietf.org/html/rfc4180) altında belirtildiği bilinmektedir. Aşağıdaki durumlarda herhangi bir dosyayı CSV uyumlu olarak tanımlar:

* Her kayıt, satır sonu (CRLF) ile ayrılmış ayrı bir satırda bulunur. Örneğin:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* Dosyadaki son kaydın bitiş satırı sonu olabilir veya olmayabilir. Örneğin:
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx
* Normal kayıt satırlarıyla aynı formatta dosyanın ilk satırı olarak görünen isteğe bağlı bir başlık satırı olabilir. Bu başlık, dosyadaki alanlara karşılık gelen adları içerecek ve dosyanın geri kalanındaki kayıtlarla aynı sayıda alanı içermelidir (başlık satırının varlığı veya yokluğu, bunun isteğe bağlı "başlık" parametresi aracılığıyla belirtilmelidir. MIME türü). Örneğin:
* alan_adı,alan_adı,alan_adı CRLF
* aaa,bbb,ccc CRLF
* zzz,yyy,xxx CRLF
* ﻿Başlık ve her kayıt içinde virgülle ayrılmış bir veya daha fazla alan olabilir. Her satır, dosya boyunca aynı sayıda alan içermelidir. Boşluklar bir alanın parçası olarak kabul edilir ve göz ardı edilmemelidir. Kayıttaki son alandan sonra virgül gelmemelidir. Örneğin:
* aaa,bbb,ccc
* Her alan çift tırnak içine alınabilir veya alınmayabilir (ancak Microsoft Excel gibi bazı programlar hiç çift tırnak kullanmaz). Alanlar çift tırnak içine alınmadıysa, alanların içinde çift tırnak görünmeyebilir. Örneğin:\
* "aaa","bbb","ccc" CRLF
* zzz,yyy,xxx
* Satır sonu (CRLF), çift tırnak ve virgül içeren alanlar çift tırnak içine alınmalıdır. Örneğin:
* "aaa","b CRLF
* bb","ccc" CRLF
* zzz,yyy,xxx
* Alanları çevrelemek için çift tırnak kullanılıyorsa, bir alanın içinde görünen çift tırnak, önüne başka bir çift tırnak koyarak kaçınılmalıdır. Örneğin:
* "aaa","b""bb","ccc"

Bununla birlikte, modern kullanım ışığında sınırlayıcı yalnızca virgülle sınırlı değildir ve noktalı virgül, sekme veya boşluk da olabilir. Microsoft Excel gibi uygulamalar, kayıtları bir CSV dosyasından içe aktarmak için sınırlayıcı karakteri belirtme seçeneği sunar.

## Referanslar

* [RFC 4180](https://tools.ietf.org/html/rfc4180)
* [RFC 2048](https://tools.ietf.org/html/rfc2048)
* [CSV - Wikipedia](https://en.wikipedia.org/wiki/Comma-separated_values)

