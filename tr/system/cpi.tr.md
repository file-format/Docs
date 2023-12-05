{
"tarih":"2023-10-18",
   "keywords":[
"TÜFE",
"cpi dosyası",
"cpi kod sayfası bilgi dosyası",
"cpi dosyası nasıl açılır",
"dosya",
"cpi dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"CPI Dosya Formatı - Kod Sayfası Bilgi Dosyası",
   "description":"CPI Kod Sayfası Bilgileri dosya formatı ve CPI dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi",
         "parent":"system"
}
},
"lastmod":"2023-10-18"
}

## .CPI dosyası nedir?

Microsoft Windows ve DOS işletim sistemleri bağlamında bir `.cpi` dosyası genellikle **"Kod Sayfası Bilgi Dosyası"dır.** Bu dosyalar, metin kodlama ve karakter kümesi eşlemeleri için kullanılan kod sayfaları hakkında bilgi içerir. Kod sayfaları, çeşitli dillerdeki ve karakter kümelerindeki metinlerin görüntülenmesi ve işlenmesi için gereklidir.

Windows ve DOS bağlamında kod sayfaları, karakterlerin farklı dillerde ve bölgelerde nasıl temsil edildiğini ve kodlandığını tanımlamak için kullanılır. Bu kod sayfaları, karakterlerin bellekte nasıl saklanacağını ve ekranda nasıl görüntüleneceğini belirler. Her kod sayfasının benzersiz bir tanımlayıcısı vardır ve ".cpi" dosyaları, karakter eşlemeleri ve yazı tipi bilgileri gibi ayrıntılar da dahil olmak üzere bu kod sayfalarıyla ilgili bilgileri depolar.

`.cpi` dosyaları genellikle Windows veya DOS sistem dizinlerinde bulunur ve işletim sisteminin metni farklı yerel ayarlar ve karakter kümeleri için doğru şekilde görüntülemesini sağlamada çok önemli bir rol oynarlar. Sistemin farklı dil ve kodlamalardaki karakterleri nasıl yorumlayacağını ve oluşturacağını anlamasına yardımcı olurlar.

## Kod Sayfası Bilgi Dosyaları

Kod Sayfası Bilgi Dosyalarına (.cpi) ve bunların MS-DOS ve Microsoft Windows'un önceki sürümleri çerçevesinde nasıl çalıştıklarına daha yakından bakalım:

1. **Karakter Kodlama ve Kod Sayfaları**: Kod sayfaları, metnin bilgisayarda nasıl kodlandığı ve görüntülendiği konusunda kritik bir bileşendir. Belirli bir dil veya karakter kümesi için karakter kodlamasını tanımlarlar. Her kod sayfası karakterlere sayısal değerler (kod noktaları) atayarak bilgisayarın bunları temsil etmesine ve görüntülemesine olanak tanır. Örneğin, Amerika Birleşik Devletleri ve Batı Avrupa'da yaygın olarak kod sayfası 437 kullanılırken, Latin-1 kodlaması için kod sayfası 850 kullanılır.
    







2. **Sistemin Başlatılması**: Sistemin başlatılması sırasında (bilgisayar önyüklendiğinde), MS-DOS ve Windows'un eski sürümleri, hangi kod sayfalarının destekleneceğini belirlemek için `.cpi' dosyalarını okurdu. Bu bilgi metin oluşturma, klavye girişi ve karakter seti dönüşümleri için çok önemliydi.
    







3. **Ekran ve Klavye Desteği**: Bu dosyalar, karakterlerin ekranda nasıl görüntülenmesi gerektiği ve klavye girişi için hangi karakter kümelerinin veya kod sayfalarının desteklenmesi gerektiği hakkında bilgi sağlar. Farklı kod sayfaları farklı karakter kümelerini tanımlar; dolayısıyla bu dosyalar, işletim sisteminin kullanıcı girişini nasıl işleyeceğini ve metni doğru şekilde nasıl görüntüleyeceğini bilmesine yardımcı olur.
    







4. **Yerelleştirme**: `.cpi` dosyaları işletim sisteminin yerelleştirilmesi için gereklidir. Sistemin farklı dillere, bölgelere ve karakter kümelerine uyum sağlamasına olanak tanıyarak dünya çapındaki kullanıcıların MS-DOS veya Windows'u tercih ettikleri dillerde kullanmalarına olanak tanır.
    







5. **Birden Çok ".cpi" Dosyası**: Çok dil desteği olan bilgisayarda, farklı kod sayfalarına karşılık gelen birkaç ".cpi" dosyası bulabilirsiniz. Örneğin, sistem Amerika Birleşik Devletleri için '437.cpi', Latin-1 için '850.cpi', Orta Avrupa için '852.cpi' vb. olabilir. Uygun dosya, kullanıcının yerel ayarına veya seçilen kod sayfasına göre yüklenir.
    







6. **Yazı Tipi Bilgileri**: Karakter eşlemelerine ek olarak, bu dosyalar her kod sayfası için hangi yazı tiplerinin kullanılacağını belirten yazı tipi bilgilerini içerebilir. Bu, metni uygun stilde ve boyutta oluşturmak için önemlidir.
    







7. **Eski Sistemler**: `.cpi' dosyaları MS-DOS ve Windows'un eski sürümlerinde daha yaygındı. Modern Windows sürümleri (Windows 10 ve üzeri gibi), metin kodlama için genellikle çok çeşitli karakterleri ve dilleri destekleyen Unicode'u kullanır. Unicode, çok dilli ortamlar için metin işlemeyi basitleştirir ve modern yazılımlar için standarttır.

## CPI dosyası nasıl açılır?

.CPI (Kod Sayfası Bilgileri) dosyasını açmak tipik bir kullanıcı eylemi değildir ve bu dosyaların genellikle manuel olarak açılması amaçlanmamıştır. İşletim sistemi tarafından metin kodlamayı ve karakter setlerini yönetmek için kullanılırlar ve içeriklerine sistem tarafından otomatik olarak erişilir ve kullanılır.

Ancak .CPI dosyasının içeriğini bilgilendirme amacıyla görüntülemek istiyorsanız, dosyayı metin düzenleyici veya onaltılık görüntüleyici ile açmayı deneyebilirsiniz. .CPI dosyasını şu şekilde açmayı deneyebilirsiniz:

1. **Metin Düzenleyici**: .CPI dosyasını açmak ve görüntülemek için Not Defteri (Windows'ta) gibi bir metin düzenleyiciyi veya diğer işletim sistemlerindeki herhangi bir düz metin düzenleyiciyi kullanabilirsiniz. .CPI dosyalarının içeriğinin insanlar tarafından okunabilir nitelikte olmadığını ve yorumlanması zor karakter dizileri görebileceğinizi unutmayın.
    







2. **Onaltılık Görüntüleyici**: Onaltılık bir görüntüleyici veya onaltılık düzenleyici, .CPI dosyasının içeriğini ham ikili biçiminde açmak ve incelemek için kullanılabilir. Hex düzenleyicileri, dosyanın verilerinin daha ayrıntılı bir görünümünü sağlar; bu, eğer dosyanın yapısını anlamaya çalışıyorsanız yararlı olabilir. Bu tür yazılımlara örnek olarak HxD, Hex Fiend (macOS için) ve 010 Editor verilebilir.

## Diğer CPI dosyaları

**.cpi** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Video sistemi**
- [CPI - AVCHD Video Klip Bilgisi](/tr/video/cpi/)
- [CPI - Kod Sayfası Bilgi Dosyası](/tr/system/cpi/)

## Referanslar
* [Kod sayfası](https://en.wikipedia.org/wiki/Code_page)

