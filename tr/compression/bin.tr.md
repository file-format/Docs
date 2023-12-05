{
"tarih":"2023-07-20",
   "keywords":[
"ÇÖP KUTUSU",
"BIN Dosyası",
"dosya",
"BIN dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"BIN Dosya Formatı - MacBinary Kodlanmış Dosya",
   "description":"BIN dosyalarını oluşturabilen ve açabilen BIN formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin",
         "parent":"compression"
}
},
"lastmod":"2023-07-20"
}

## BIN dosyası nedir?

Macintosh bilgisayarları bağlamında bir BIN dosyası, MacBinary formatında kaydedilen bir dosyaya atıfta bulunabilir. MacBinary, Macintosh dosyalarını internet, e-posta, FTP veya taşınabilir medya üzerinden aktarmak için özel olarak tasarlanmış bir dosya formatıdır. MacBinary'nin amacı, hem veri çatalı hem de kaynak çatalı dahil olmak üzere Macintosh dosyalarının tüm dosya yapısını ve niteliklerini tek bir dosyada korumaktır.

MacBinary formatı bunu, Macintosh Hiyerarşik Dosya Sistemi (HFS) kaynak çatalını ve veri çatalını sıkıştırılmış bir dosyaya yerleştirerek başarır. Ayrıca dosyayla ilgili önemli meta verileri içeren bir bulucu başlığı da içerir. MacBinary, tüm bu bileşenleri tek bir dosyada birleştirerek dosyanın bütünlüğünü korumasını ve farklı platformlar arasında kolayca aktarılıp paylaşılabilmesini sağlar.

Apple'ın dosya sistemleri ve dosya aktarım protokollerindeki gelişmelerle birlikte BIN dosyalarının ve MacBinary formatının kullanımı daha az yaygın hale geldi. ZIP gibi dosya formatlarının kullanıma sunulması ve HFS+ ve APFS gibi daha modern dosya sistemlerine geçiş, MacBinary kodlu dosyalara olan ihtiyacı azalttı. Bu daha yeni dosya sistemleri, dosya özniteliklerini, kaynak çatallarını ve veri çatallarını işlemek için daha verimli yollar sağlayarak MacBinary formatını günümüzün bilgi işlem ortamında daha az gerekli hale getirir.

## BIN Dosya Formatı - Daha Fazla Bilgi

Macintosh bilgisayarların ilk günlerinde, veri sınırlamaları nedeniyle dosyalar iki ayrı "çatal"da saklanıyordu. "Kaynak çatalı" yapılandırılmış verileri içerirken, "veri çatalı" yapılandırılmamış verileri barındırıyordu. Klasik Mac OS bu çatalları tek bir dosya olarak ele alırken, dosyaları Mac olmayan sistemlere aktarmak, çatalları tek bir varlık olarak tanımadıkları için veri kaybına neden oluyordu. Bu sorunu çözmek için MacBinary formatı Dennis Brothers, Harry Chesley ve Yves Lempereur gibi kişiler tarafından oluşturuldu. MacBinary, Mac dışındaki sistemlere aktarım için çatalları sıkıştırıp BIN dosyası olarak bilinen tek bir dosyada birleştirdi. Mac OS'a döndükten sonra çatallar tekrar ayrılacaktı. 2000'li yıllarda çatal tabanlı HFS'den uzaklaşmayla birlikte MacBinary formatının kullanımı önemli ölçüde azaldı. Bugün, Mac olmayan bir sistemde eski bir dosyayla karşılaşmadığınız veya internetten bir dosya indirmediğiniz sürece, MacBinary kodlu bir BIN dosyasıyla karşılaşmak nadirdir.

MacBinary formatı, Macintosh sistemlerindeki ve dosya işlemedeki değişikliklere uyum sağlamak için zaman içinde çeşitli sürümlerden geçmiştir. MacBinary formatının farklı versiyonlarından bazıları şunlardır:

- **MacBinary I:** MacBinary'nin 1980'lerin sonunda tanıtılan ilk sürümü. Kaynak çatalını ve veri çatalını tek bir ikili dosyada birleştirerek Macintosh dosyalarının platformlar arası aktarımına olanak sağladı.

- **MacBinary II:** 1990'ların başında piyasaya sürülen bu sürüm, ikili dosyanın başlığına dosya türü ve oluşturucu kodları gibi ek bilgiler ekleyerek orijinal MacBinary formatını geliştirdi. Bu kodlar, aktarım sırasında Macintosh dosyalarının bütünlüğünün ve kimliğinin korunmasına yardımcı oldu.

- **MacBinary III:** 1990'ların ortalarında piyasaya sürülen MacBinary III formatı, ikili dosyanın başlığına dosya adı ve dosya oluşturma ve değiştirme tarihleri gibi ek meta veriler ekleyerek önceki sürümleri daha da geliştirdi. Bu, aktarım sırasında Macintosh dosya özniteliklerinin daha kapsamlı korunmasına olanak sağladı.

- **MacBinary IV:** MacBinary IV, 2000'li yılların başında ortaya çıkan Mac OS X işletim sistemindeki uyumluluk sorunlarını gidermek için geliştirildi. Yeni dosya sistemi yapısına ve Mac OS X'te tanıtılan niteliklere uyum sağlayacak değişiklikler içeriyordu.

## BIN dosyası nasıl açılır?

MacBinary Encoded BIN dosyaları çeşitli sıkıştırma yardımcı programları kullanılarak açılabilir. macOS kullanıcıları için **Apple Arşiv Yardımcı Programı** uygun bir seçenektir. Windows kullanıcıları, MacBinary Encoded BIN dosyasının içeriğini çıkarmak için **Smith Micro StuffIt Deluxe** gibi yazılımlardan yararlanabilir. MacOS kullanıcıları için başka bir seçenek de MacBinary de dahil olmak üzere birden fazla dosya biçimini işleyebilen çok yönlü bir araç olan **Unarchiver**'dır.

.bin dosya uzantısının yalnızca MacBinary tarafından değil, çeşitli dosya formatları tarafından kullanıldığına dikkat etmek önemlidir. Bu nedenle yukarıda belirtilen yardımcı programlarla açılamayan bir BIN dosyasıyla karşılaşırsanız, dosya farklı bir formatta kaydedilebilir. Bu gibi durumlarda, dosya içeriğine erişmek için belirli dosya formatını tanımlamanız ve o format için tasarlanmış uygun yazılımı veya yardımcı programı kullanmanız gerekebilir.

## Diğer BIN dosyaları

**.bin** dosya uzantısını kullanan diğer dosya türleri şunlardır.

- [BIN - İkili Disk Görüntü Dosyası](/tr/disc-and-media/bin/)
- [BIN - Unix Yürütülebilir Dosyası](/tr/executable/bin/)
- [BIN - BlackBerry BT Politika Dosyası](/tr/settings/bin/)
- [BIN - Sega Genesis Oyun ROM'u](/tr/game/bin/)
- [BIN - PSX PlayStation BIOS Görüntüsü](/tr/game/bin-pcsx/)

## Referanslar

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)

