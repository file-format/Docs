{
  "date" : "2019-10-11",
  "keywords" :[ "md dosyası", "md dosya biçimi", "md dosyası nedir", "dosya", "md örneği", "md dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MD - MarkDown Dil Dosyası",
  "description":"MD dosya formatı ve MD dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MD",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## MD dosyası nedir?

Markdown dil lehçeleriyle oluşturulan metin dosyaları **.md** veya **.MARKDOWN** dosya uzantısıyla kaydedilir. MD dosyaları, girintiler, tablo biçimlendirme, yazı tipleri ve başlıklar gibi bir metnin nasıl biçimlendirilebileceğini tanımlayan satır içi metin sembollerini de içeren Markdown dilini kullanan düz metin biçiminde kaydedilir. MD dosyaları, Markdown adlı bir programla HTML'ye dönüştürülebilir. Markdown dili, John Gruber tarafından yayınlandı.

MD dosyaları, kullanıcıların okuması ve yazması kolay dosyalar oluşturabilmesi için metin dosyalarını HTML sürümlerine dönüştürmek için çoğunlukla Markdown tarafından kullanılan geliştirici dosyaları olarak da kategorize edilebilir. Bir .md dosyasını açabilen uygulamalar şunlardır:

* Microsoft Not Defteri
* Not Defteri2
* Apple MetinDüzenle
* Microsoft WordPad'i

.md dosyalarının uzantısını yeniden adlandırmayın. Böyleyse, bir dosyayı bir türden diğerine değiştirmek için kullanılabilen özel dönüştürme yazılımları olduğundan, bu dosya türünü değiştirmeyecektir. Yukarıda tartışıldığı gibi .MD dosyaları, Markdown dil yazılımı tarafından oluşturulan dosyaların uzantılarıdır. **Markdown**, web'deki metni düz metin biçimlendirme sözdizimiyle biçimlendirmek için tek bir amaca yönelik [hafif bir biçimlendirme dilidir](https://en.wikipedia.org/wiki/Lightweight_markup_language). Markdown'ın HTML'nin yerine geçmediğini açıklığa kavuşturalım, çünkü sözdizimi çok küçüktür ve çok küçük bir HTML etiketi alt kümesi içerir. Markdown'ın arkasındaki sebep, düzyazı okumayı, yazmayı ve düzenlemeyi kolaylaştırmaktır. Yani HTML bir yayın formatı, Markdown ise bir yazı formatı diyebiliriz.

Markdown artık dünyanın en popüler biçimlendirme dillerinden biridir. Microsoft Word'ü kullanırken, sözcükleri ve tümceleri biçimlendirme düğmeleri tıklatarak yapılır ve değişiklikler hemen görünür. Ancak Markdown öyle değil. Markdown formatlı dosya oluşturulduğunda, hangi kelimelerin ve kelime öbeklerinin farklı görünebileceğini belirtmek için metne Markdown sözdizimi eklenir. Örneğin, bir başlığı göstermek için önüne bir sayı işareti eklenir (örn. # Heading One). Kalın bir cümle oluşturmak için önüne ve arkasına iki yıldız eklenir (örneğin, **bu metin kalındır**). Markdown sözdizimi metinden sonra görülebilir.

## Kısa Tarihçe

John Gruber ve Aaron Swartz, 2004 yılında Markdown dilini, insanların "okuması ve yazması kolay düz metin biçimini kullanarak ve onu XHTML veya HTML'ye dönüştürme seçeneğiyle yazmasını" sağlama fikriyle yarattı. Tasarımının arkasındaki amaç okunabilirliktir - dil, etiketlerin ve biçimlendirme talimatlarının açık olduğu RTF veya HTML gibi biçimlendirme dillerinde yapıldığı gibi biçimlendirme yönergeleriyle etiketlenmiş veya eklenmiş gibi görünmeden olduğu gibi okunabilir. Temel ilham, e-postadaki düz metni işaretlemek için mevcut kuralları kullanmaktır.

O zamandan beri Markdown, [CPAN](https://en.wikipedia.org/) üzerinde bulunan bir Perl [modülünde](https://en.wikipedia.org/wiki/Modular_programming) olduğu gibi başkaları tarafından da yeniden uygulandı. wiki/CPAN) ve diğer çeşitli programlama dillerinde. [BSD tarzı bir lisans](https://en.wikipedia.org/wiki/BSD_license) altında dağıtılır ve birkaç [içerik yönetim sistemi](https://en.wikipedia.org/wiki/Content_management_system) ile birlikte gelir veya bunlar için bir eklenti olarak kullanılabilir.

## Teknik özellikler

Markdown'da bir şey yazıldığında, metin önce .md veya .markdown uzantılı düz metin dosyasında depolanır, ardından Markdown formatlı metni web'de görüntülemek için HTML'ye dönüştürmek üzere Markdown dosyasının işlenmesi için Dillinger gibi bir markdown uygulaması kullanılır. tarayıcılar. Markdown uygulamaları, Markdown formatlı metni almak ve HTML formatına çıkarmak için bir //Markdown işlemcisi// (genellikle "ayrıştırıcı" veya "uygulama" olarak da adlandırılır) kullanır. Sürecin akış şeması aşağıdaki gibidir:

Kısacası, aşağıdaki gibi dört aşamalı bir süreçtir:

1. İlk olarak, bir metin düzenleyiciyle veya .md veya .markdown uzantılı Markdown uygulamasıyla Markdown dosyalarının oluşturulması.
1. Markdown dosyası daha sonra bir Markdown uygulamasında açılır.
1. Markdown uygulaması, Markdown dosyasını bir HTML belgesine dönüştürmek için kullanılır.
1. HTML dosyası daha sonra bir web tarayıcısında görüntülenir veya PDF gibi başka bir dosya formatına dönüştürmek için Markdown uygulaması kullanılır.

Markdown, not almak, web sitesi için içerik yazmak, baskıya hazır belgeler üretmek, kitap yayınlamak, sunumlar oluşturmak ve belgeler oluşturmak için hızlı ve kolaydır.

İşaretlemedeki bazı sürümlerin diğer sürümler üzerinde o kadar önemli bir etkisi oldu ki, genellikle diğer sürümlerin bir parçası olarak alıntılandığını göreceksiniz. Örneğin, kütüphaneler CommonMark (GFM) desteğinden bahseder. Bunlara kısaca bir göz atalım.

###
Markdown, geliştiriciler arasında çok popüler çünkü açık kaynak paylaşım platformu Github dili kabul etti ve çitle çevrili kod blokları, URL aultlinking, üstü çizili, tablolar ve yapılacak işler içeren Github Flavored Markup (GFM) adlı bir sürümle genişletti.

### Ortak Marka
Markdown geliştiricileri son zamanlarda markdown'u standartlaştırmaya çalıştılar, daha sağlam olan ve CommonMark olarak adlandırılan dil için bir sürüm, testler ve belgeler oluşturmak için bir araya geldiler. Bu format biraz yeni ve pek çok özelliği desteklemiyor, ancak yakında birçok MultiMarkdown özelliği eklenecek.

### Çoklu İşaretleme
Multi-Markdown, dile diğer sürümler tarafından desteklenen çeşitli özellikler ekledi. Başlangıçta Perl'de yazılmıştır, ancak daha sonra C'ye taşınmıştır. Çitlerle çevrili kod bloklarını, sözdizimi vurgulamayı, tabloları, meta verileri, parça/çapraz referans bağlantılarını, dipnotları, üstü çizili, tanım listelerini, matematiği destekler.

## Referanslar

* [MarkDown'da Ustalaşma](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

