{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICS - iCalendar Dosya Biçimi",
  "description":"ICS dosya formatı ve ICS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "ICS",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-10"
}

## ICS dosyası nedir?

İnternet Takvimi ve Çizelgeleme Temel Nesne Spesifikasyonu (iCalendar), takvim olaylarını ve zamanlamayı değiş tokuş etmek ve dağıtmak için bir internet standardıdır (RFC 2445). iCalendar formatı birlikte çalışabilir, böylece farklı e-posta uygulamalarına sahip kullanıcılar arasında takvim bilgisi alışverişini sağlar. iCalendar, giriş verilerini Çok Amaçlı İnternet Posta Uzantıları (MIME) olarak biçimlendirir ve farklı aktarım protokolleri yoluyla nesne alışverişini kolaylaştırır. Bu aktarım protokolleri SMTP, HTTP, noktadan noktaya eşzamansız iletişim ve fiziksel ortam tabanlı ağ aktarımı olabilir.

iCalendar, kullanıcıların etkinlikleri, tarihe/zamana bağlı görevleri ve uygun/meşgul bilgilerini e-postalar aracılığıyla yanıt verebilecek diğer kullanıcılara paylaşmasına olanak tanır. iCalendar dosyaları, MIME türü "text/calendar" ile ".ics" ".iCalendar" veya ".ifb" soneklerini kullanarak depolanır. iCalendar, herhangi bir aktarım protokolü bağımlılığı olmadan kendi kendine yetecek şekilde tutulur. Web sunucuları (HTTP protokollü) iCalendar bilgilerini taşıyabilir ve web sayfaları, iCalendar kullanarak gömülü biçimde iCalendar verilerini içerebilir.

## ICS Dosya Formatının Kısa Tarihi

1998'de İnternet Mühendisliği Görev Gücü (IETF), iCalendar'ı bir standart (RFC 2445) olarak tanımladı. Standart, Frank Dawson(Lotus Notes Corporation) ve Derik Stenerson (Microsoft) tarafından belgelenmiştir. 2009'da standart, Bernard Desruisseaux (Oracle) tarafından RFC 5545 olarak yeniden rafine edildi. Bu sefer bazı yeni özellikler eklendi ve bazı eski özellikler kullanımdan kaldırıldı. 2016'da RFC 7986 piyasaya sürüldü ve orijinal iCalendar RFC'ye yükseltildi. RFC 7986, ana VCALENDAR nesnesine yeni özellikler ekledi ve konferans sistemleri için yeni destekleyici özellikler de tanıtıldı.

## ICS Dosya Biçimi ##

iCalendar verileri tarafından kullanılan MIME tipi “text/calendar”dır. iCalendar için varsayılan karakter seti UTF-8'dir, ancak MIME'de parametreler sağlanarak farklı bir karakter seti kullanılabilir. Bir iCalendar dosyası, bu bölümler arasında bölümler içerir "VCALENDAR", diğer tüm bölümleri içine alan genel bölümdür. VEVENT bölümü olayları tanımlar, VTODO tüm yapılacakları listeler, VJOURNAL günlük girişlerini içerir ve VTMEZONE saat dilimi bilgilerini belirtir. benzer kategorideki birden fazla bölüme izin verilir. Çok sayıda etkinlik için, bir iCalendar dosyasında birden çok VEVENT bölümü bulunabilir.

### İçerik Satırları ###

iCalendar nesneleri, farklı metin satırları "içerik satırları" şeklinde düzenlenmiştir. Bu dosya formatında, CRLF dizisi bir satırı sonlandırırken, satır uzunluğu satır sonu hariç 75 sekizli ile sınırlıdır. Uzun bir veri öğesi birçok satıra yayılabilir.

### Liste ve Alan Ayırıcıları ###

Özellikler ve parametreler, bir virgül karakteriyle ayrılan değerlerin listesini belirtir. Alıntılanmış dizeler, URI tabanlı parametre değerleri için kullanılır. Özellik değerine göre parametre listesi oluşturulabilir. Bu listedeki her özellik parametresi, bir NORMALI virgülle ayrılmalıdır.

Bir değer listesinde, bir SEMICOLON ayrı özellik parametreleri ve bir COMMA ayrı özellik değerleri. Örnek aşağıda verilmiştir:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Birden Fazla Değer

Bazı özelliklerin birden fazla değeri olabilir. Yalnızca özellik adıyla yeni bir içerik satırı oluşturmak, çok değerli özellikler için temel kuraldır. Ancak, birden çok dil varyasyonu olan tek bir değer için çok değerli özellikler kullanılmamalıdır.

### İkili İçerik

Bir iCalendar nesnesi içinde, özellik değeri, bir URI kullanılarak harici bir MIME varlığına yerleştirilmiş bir ikili içerik verisine başvurabilir. Satır içi ikili içerik, uygulamanın bir iCalendar nesnesini tek bir varlık olarak ifade etmesi gereken "ENCODING" parametresiyle özel durumlarda kullanılabilir. Aşağıdaki örnek, URI referansı olan bir "ATTACH" özelliğini açıklar:

EK: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Karakter seti

Bir iCalendar için varsayılan karakter kümesi şeması UTF-8 olsa da, bir özellik değerinin karakter kümesini tanımlamak için hiçbir özellik parametresi belirtilmemiştir. MIME transferlerinde "karakter seti" parametresi mevcut karakter seti için KULLANILMALIDIR.

## Referanslar

* [İnternet Takvimi ve Çizelgeleme Temel Nesne Spesifikasyonu](https://www.ietf.org/rfc/rfc5545.txt)
* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)
* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)

