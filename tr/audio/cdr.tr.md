{
"tarih":"2023-10-18",
   "keywords":[
"cdr",
"cdr dosyası",
"cdr raw cd ses veri dosyası",
"cdr dosyası nasıl açılır",
"dosya",
"cdr dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc": true,
"title":"CDR Dosya Formatı - Ham CD Ses Verileri",
   "description":"CDR Ham CD Ses Verileri dosya formatı ve CDR dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
"linktitle" : "CDR",
   "menu":{
      "docs":{
         "identifier":"audio-cdr",
         "parent":"audio"
}
},
"lastmod":"2023-10-18"
}

## .CDR dosyası nedir?

**"Ham CD Ses Verileri"** içeren bir **.CDR** dosyası, genellikle müzik parçaları gibi doğrudan bir ses CD'sinden çıkarılan ses bilgilerini içeren dosyayı ifade eder. "Ham CD Ses Verileri", genellikle ikili formatta saklanan, CD'deki işlenmemiş dijital ses verilerini ifade eder. Bu ham veriler, hem ses hem de alt kod bilgileri dahil olmak üzere, tam olarak CD'deki gibi ses örneklerini içerir.

Bu dosyalar genellikle doğrudan oynatılmak üzere tasarlanmamıştır; bunun yerine CD mastering, ses düzenleme ve CD yazma gibi çeşitli amaçlar için kullanılır. Ses düzenleme ve CD yazmaya yönelik yazılım uygulamaları genellikle bu ham verileri ses CD'leri oluşturmak veya bunları WAV veya MP3 gibi diğer ses dosyası formatlarına dönüştürmek için kullanır.

"Ham CD Ses Verileri" içeren .cdr dosyalarıyla çalışmanız gerekiyorsa, çoğu medya oynatıcısında oynatılabilen standart ses dosyaları olmadıklarından bunları işlemek veya dönüştürmek için genellikle özel ses yazılımı kullanırsınız.

## CDR dosyası nasıl dönüştürülür?

"Ham CD Ses Verileri" içeren .cdr dosyasını WAV veya MP3 gibi daha yaygın ses formatına dönüştürmek için özel yazılıma ihtiyacınız olacaktır. .cdr dosyanızı VideoLAN VLC medya oynatıcısında oynatabiliyorsanız, onu farklı ses formatlarına dönüştürmek için VLC'yi de kullanabilirsiniz;

- [.MP3](/tr/audio/mp3/) - MP3 Ses
- [.FLAC](/tr/audio/flac/) - Ücretsiz Kayıpsız Ses Codec Bileşeni
- [.WAV](/tr/audio/wav/) - WAVE Sesi
- [.OGG](/tr/audio/ogg/) - Ogg Vorbis Ses

## CDR dosyası nasıl açılır?

.cdr dosyasını, özellikle de "Ham CD Ses Verileri"ni içeren dosyayı açmak, standart ses dosyası formatı olmadığı için biraz yanıltıcı olabilir. Bu tür dosyaları açmak ve bunlarla çalışmak için ham CD ses verilerini işleyebilen özel bir yazılım kullanabilirsiniz. Bunu nasıl yapacağınız ve bazı yazılım seçenekleri aşağıda açıklanmıştır:

**.cdr Dosyalarını Açma ve Çalışma Yazılımı:**

1. **Tam Ses Kopyası (EAC)**:
    





- Ses CD'leriyle çalışmak ve "Ham CD Ses Verilerini" çıkarmak için popüler ve güçlü bir araç olan Exact Audio Copy'yi indirip yükleyin.
- .cdr dosyasını içeren CD'yi bilgisayarınızın CD/DVD sürücüsüne yerleştirin.
- EAC'yi açın ve çıktı formatı (örn. WAV veya MP3) dahil olmak üzere tercihlerinize göre yapılandırın.
- CD'den ses parçalarını çıkarmak ve istediğiniz formatta kaydetmek için EAC'yi kullanın.
2. **Cesaret**:
    





- Audacity, "Ham CD Ses Verileri" ile de çalışabilen ücretsiz, açık kaynaklı bir ses düzenleme yazılımıdır.
- CD'yi takın.
- Audacity'yi açın ve CD sürücünüzden ses kaydedecek şekilde yapılandırın.
- CD'den ses kaydedin ve ardından daha yaygın ses formatında kaydedin.
3. **VLC Medya Oynatıcı**:
    





- VLC, "Ham CD Ses Verisi"ne sahip olanlar da dahil olmak üzere CD'lerden doğrudan ses çalabilir.
- CD'yi bilgisayarınıza takın.
- VLC'yi açın, "Medya" menüsüne gidin ve "Diski Aç"ı seçin.
- CD sürücüsünü seçin ve ses parçalarını doğrudan oynatın.
4. **CD Ripper Yazılımı**:
    





- Windows Media Player (Windows için), iTunes (Mac için) ve diğerleri gibi çeşitli CD kopyalama yazılımı seçenekleri mevcuttur.
- CD'yi bilgisayarınıza takın.
- Tercih ettiğiniz CD kopyalama yazılımını açın ve bunu ses parçalarını çıkarmak ve bunları ortak ses formatında kaydetmek için kullanın.
5. **DAEMON Tools** (.cdr görüntü dosyaları için):
    





- Eğer .cdr dosyası DAEMON Tools gibi bir yazılım tarafından oluşturulmuş bir imaj dosyası ise, DAEMON Tools veya benzeri bir yazılımı kullanarak imajı bağlayabilirsiniz.
- Görüntü bağlandıktan sonra içeriğine sanki fiziksel bir CDymiş gibi erişebilir ve gerektiği gibi ses çalabilir veya çıkartabilirsiniz.

## Diğer CDR dosyaları

**.cdr** dosya uzantısını kullanan diğer dosya türleri şunlardır.

**Ses, Disk ve Medya**
- [CDR - Ham CD Ses Verileri](/tr/audio/cdr/)
- [CDR - Macintosh DVD/CD Master](/tr/disc-and-media/cdr/)

**Veri Dosyaları ve Görüntüsü**
- [CDR - Kilitlenme Verisi Alma Veri Dosyası](/tr/data/cdr-crash/)
- [CDR - Vektör Çizim Görüntü Dosyası](/tr/image/cdr/)

## Referanslar
* [Tam Ses Kopyası](https://en.wikipedia.org/wiki/Exact_Audio_Copy)

