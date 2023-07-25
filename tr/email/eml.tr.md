{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EML - E-posta Mesajı",
  "description":"EML dosya formatı ve EML dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "EML",
  "menu" : {
    "docs" : {
      "parent" : "email"
}
},
  "lastmod" : "2019-09-16"
}

## EML dosyası nedir?

EML dosya biçimi, Outlook ve diğer ilgili uygulamalar kullanılarak kaydedilen e-posta mesajlarını temsil eder. Hemen hemen tüm e-posta istemcileri, RFC-822 İnternet İleti Biçimi Standardı ile uyumluluğu nedeniyle bu dosya biçimini destekler. Microsoft Outlook, EML mesaj türlerini açmak için varsayılan yazılımdır. EML dosyaları, diske kaydetmek ve iletişim protokollerini kullanarak alıcılara göndermek için kullanılabilir.

## EML'nin Kısa Tarihi

EML dosya formatı özellikleri, [RFC 822](https://www.ietf.org/rfc/rfc0822.txt) Standart Format uyarınca mevcuttur. RFC-822'den önce, RFC-733, 1982'ye kadar ağ mesaj alışverişi kurallarını yönetiyordu, RFC-733, ARPA standartlarını oluşturarak yanal bir gelişme olarak oluşturuldu. Aynı zamanda Microsoft, kendi e-posta istemcisinin, yani Outlook Express'in geliştirilmesi için kendi COM modüllerini yarattı. RFC-822, Microsoft açık standarttan sapıp e-postaların oldukça yapılandırılmış bir veritabanı biçiminde kaydedildiği [PST](/tr/email/pst/) dosya biçimini oluşturduğunda özel bir biçim olarak kurulma yolunu tuttu. Bu, e-postalar Microsoft Outlook'tan iletildiğinde Microsoft dışı e-posta istemcilerinin kullanıcıları için sorunlara neden oldu.

2001 yılında 822 standardı, şu anda MIME RFC-822 formatında EML mesajları oluşturmak, okumak ve göndermek için kullanılan İnternet Mesaj Formatı olan 2822'ye yükseltildi.

## EML Dosya Biçimi Özellikleri

EML dosyaları iki farklı bölümden oluşur:

* Başlıklar - Mesaj başlığı hakkında bilgi içerir
* İleti Gövdesi - İleti içeriğini, katıştırılmış görüntüleri ve ekleri içerebilen bir dizi bilgi içerir

### Başlık Bilgileri ###

Bir EML dosyası, Başlık bilgilerinden ve isteğe bağlı olarak mesaj gövdesinden oluşur. EML'deki her başlık satırı, iki nokta üst üste ":" ile ayrılmış iki bölüme sahiptir. İlki Başlık Adı olarak adlandırılır ve iki nokta üst üste işaretinden sonraki başlık gövdesidir. Örneğin, bu tür başlıklar şunları içerir:

* Gönderenin e-posta adresi
* Alıcı e.posta adresi
* E-postanın Konusu
* Mesajın saat ve tarih damgası

**Örnek Başlık**

İtibaren:<John@bmw.eml.light.com>

İle:<Andy@fileformat.com>

Tarih: Per, 8 Mart 2018 10:43:37 +0100

Konu: bmw eml ışık

### Mesaj Gövdesi ###

EML mesaj gövdesi, metin, köprüler ve ekler biçiminde e-postanın birincil bilgilerini içerir. E-posta gövdesi düz okunabilir metin içerebilir ancak bu gerekli değildir. Bu durumda, mesaj gövdesi boş olabilir veya kodlanmış ek verileri içerebilir.

Mesaj gövdesinin içeriği, okuma uygulamalarının bilgileri ilgili formatlarda okumasını sağlayan İçerik Tipi ile tanımlanır. Aslında bir belgenin doğasını ve biçimini temsil eder. Bir MIME türünün veya içerik türünün yapısı çok basittir; bir tür ve bir alt tür, '/' ile ayrılmış iki diziden oluşur. Boşluğa izin verilmez. "Tür", kategoriyi temsil eder ve ayrık veya çok parçalı bir tür olabilir. "Alt tür" her türe özeldir. İçerik-Türü kategorisine giren türlerin listesi uzundur ancak bazı önemli içerik türleri şunlardır:


|**Tür**|**Açıklama**|**Alt Tür Örneği**
---|---|---|
|text|İnsanlar tarafından okunabilen formatı temsil eder|text/flat, text/html, text/css, text/javascript
|resim|Videolar hariç her türlü resmi temsil eder|resim/bmp, resim/png, resim/jpg, resim/gif
|ses|Herhangi bir ses dosyası formatını temsil eder|audio/mdi, audio/wav
|application|Her türlü ikili veriyi temsil eder|application/octet-stream, application/vnd.mspowerpoint, application/xhtml+xml, application/xml, application/pdf

### EML Gövdesinde Ekin Temsili ###

EML gövdesi, içerdiği her içerik türü için sınırlar içerir. İleti gövdesindeki ek, aşağıdaki örnekte gösterildiği gibi İçerik Türü ve İçerik Yönlendirmesi ile tanımlanır:

İçerik Türü: metin/düz; karakter kümesi#"windows-1252"; name#"apple uygulama mağazası.txt"
İçerik Eğilimi: ek; dosyaadı#"elma uygulama mağazası.txt"
İçerik-Transfer-Kodlama: base64
X-Ek-Kimliği: f_jkhztmd02

Görüldüğü gibi, ek olarak ayarlanan Content-Disposition, okuma uygulamalarının ek dosya adı ve aktarım kodlaması gibi ek bilgilerini almasına olanak tanır. Ek başlık bilgisini, okunacak kodlanmış ek içerikleri takip eder.

#### Ek Olarak Hesap Tablosu Örneği ####

İçerik Türü: application/vnd.openxmlformats-officedocument.spreadsheetml.sheet; name#"english_spodr.xlsx"
İçerik Eğilimi: ek; dosyaadı#"english_spodr.xlsx"
İçerik-Transfer-Kodlama: base64
X-Ek-Kimliği: f_jkhztmd43

## Referanslar

* [RFC 822](https://www.ietf.org/rfc/rfc0822.txt)

