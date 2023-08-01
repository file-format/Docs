{
  "date" : "2019-10-11",
  "keywords" :[ "rtf dosyası", "rtf dosya biçimi", "rtf dosyası nedir", "dosya", "rtf örneği", "rtf dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Zengin Metin Biçimi",
  "description":"RTF dosya formatı ve RTF dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## .rtf dosyası nedir?

Microsoft tarafından tanıtılan ve belgelenen Zengin Metin Biçimi (**RTF**), uygulamalarda kullanılmak üzere biçimlendirilmiş metin ve grafikleri kodlama yöntemini temsil eder. Biçim, diğer Microsoft Ürünleri ile platformlar arası belge alışverişini kolaylaştırır ve böylece birlikte çalışabilirlik amacına hizmet eder. Bu yetenek, onu kelime işlem yazılımları arasında bir veri aktarımı standardı haline getirir ve bu nedenle içerikler, belge formatını kaybetmeden bir işletim sisteminden diğerine aktarılabilir. Dosya formatı belirtimleri, Microsoft tarafından genel [indirme](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) için mevcuttur ve geliştiricinin bakış açısından atıfta bulunulabilir.

## RTF Dosya Biçiminin Kısa Tarihi ##

RTF dosya formatı, yayınlanmasından bu yana birkaç revizyondan geçti. Okuma/yazma için resmi sürümü, sürüm 1.0 özellikleriyle Macintosh için Microsoft Word 3.0'ın bir parçası olarak yayınlandı. Spesifikasyonların son sürümü olan 1.9.1, Microsoft tarafından Mart 2008'de yayınlandı. Bundan sonra spesifikasyonlarda başka geliştirme yapılmadı. Şu anda, hemen hemen tüm işletim sistemleri, RTF dosya formatının kullanımını en aza indiren/ortadan kaldıran, daha zengin özelliklere sahip uygulamalara sahiptir.

## RTF Dosya Biçimi Özellikleri ##

RTF, kelime işlemci yazılımı ile içeriğin bir işletim sisteminden diğerine aktarımı arasında bir veri aktarımı standardı olarak hizmet eder. Bu, Microsoft Office Word tarafından 2007'ye kadar tanıtılan kontrol sözcükleri kullanılarak gerçekleştirilir. Standart bir RTF dosyası, zengin metni temsil eden ASCII'den ve uygun kod değerlerine dönüştürülen ASCII olmayan karakterlerden oluşur. Word'ün daha yeni sürümleri, önceki sürümlerle oluşturulan RTF dosyalarını okuyabilirken, eski sürümler anlamadıkları kontrol sözcüklerini ve grupları yok sayar.

### RTF'nin Temellerini Anlamak ###

RTF dosyaları, aşağıdakilerden oluşan 7 bitlik ASCII düz metin kullanır:

* kontrol kelimeleri
* kontrol sembolleri ve
* gruplar.

Bunlar, RTF verilerinin anlaşılır metin ve karakter kodlaması olarak temsil edilmesi için yapı taşları görevi görür.

#### Kontrol Kelimesi ####

Bunlar, karakterleri görüntülemek üzere işaretlemek için kullanılan özel olarak biçimlendirilmiş komutu temsil eder ve 32 harften uzun olamaz. Bir kontrol kelimesi şu şekilde tanımlanır:

\<ASCII Letter Sequence> //<//Delimiter//> //

Her kontrol sözcüğü büyük/küçük harfe duyarlıdır ve ters eğik çizgi ile başlar. ASCII Harf Dizisi, ASCII Alfabelerini (a'dan z'ye ve A'dan Z'ye) içerebilir. bu<Delimite> kontrol kelimesinin adının sonunu işaretler ve aşağıdakilerden biri olabilir:

* Bir boşluk. Bu sadece bir kontrol kelimesini sınırlamaya hizmet eder ve sonraki işlemlerde dikkate alınmaz.
* Sayısal bir parametrenin kontrol sözcüğüyle ilişkilendirildiğini gösteren bir sayısal basamak veya ASCII eksi işareti. Sonraki dijital dizi daha sonra bir ASCII basamağı (genellikle ters eğik çizgi ile başlayan başka bir kontrol sözcüğü) dışında herhangi bir karakterle sınırlandırılır. Parametre, pozitif veya negatif bir ondalık sayı olabilir. Sayı için değer aralığı nominal olarak –32768 ila 32767'dir, yani işaretli 16 bitlik bir tam sayıdır. Az sayıda kontrol kelimesi‌ -2,147,483,648 ila 2,147,483,647 (32 bit işaretli tam sayı) aralığında değerler alır. Bu kontrol kelimeleri **\binN**, **\revdttmN//**, **\rsidN** ile ilgili kontrol kelimelerini ve **\bliptagN** gibi bazı resim özelliklerini içerir. Burada **N**, sayısal parametreyi ifade eder. Bir RTF ayrıştırıcısı, isteğe bağlı olarak önünde bir eksi işareti bulunan en fazla 10 haneye izin vermelidir. Ayırıcı bir boşluksa, atılır, yani sonraki işlemeye dahil edilmez.
* Harf veya rakam dışında herhangi bir karakter. Bu durumda sınırlayıcı karakter, kontrol kelimesini sonlandırır ve kontrol kelimesinin bir parçası değildir. Yeni bir kontrol sözcüğü veya bir kontrol sembolü anlamına gelen ters eğik çizgi "\" gibi.

#### Kontrol Sembolü ####

Bir Kontrol Sembolü, içeriğine bağlı olarak belirli bir anlamı olan özel bir oluşumu temsil eder. Bir ters eğik çizgiden ve ardından özel bir karakterden (alfabetik olmayan karakter) oluşur ve sınırlayıcı içermez.

#### Grup ####

Bir grup, köşeli ayraçlar (**{ }**) içine alınmış metin, kontrol sözcükleri veya kontrol sembollerinden oluşabilir. Açılış ayracı (**{** ) grubun başlangıcını, kapanış ayracı ( **}**) ise grubun sonunu gösterir. Her grup, gruptan etkilenen metni ve o metnin farklı niteliklerini belirtir.

### RTF Dosya Yapısı ###

Bir RTF dosyası aşağıdaki Standart sözdizimine sahiptir:

Microsoft tarafından tanıtılan ve belgelenen Zengin Metin Biçimi (**RTF**), uygulamalarda kullanılmak üzere biçimlendirilmiş metin ve grafikleri kodlama yöntemini temsil eder. Biçim, diğer Microsoft Ürünleri ile platformlar arası belge alışverişini kolaylaştırır ve böylece birlikte çalışabilirlik amacına hizmet eder. Bu yetenek, onu kelime işlem yazılımları arasında bir veri aktarımı standardı haline getirir ve bu nedenle içerikler, belge formatını kaybetmeden bir işletim sisteminden diğerine aktarılabilir. Dosya formatı belirtimleri, Microsoft tarafından genel [indirme](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf) için mevcuttur ve geliştiricinin bakış açısından atıfta bulunulabilir.

#### RTF Başlığı ####

Bir RTF Başlığı aşağıdaki gösterime sahiptir.

|Alan|Açıklama
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

Varsa, başlık tabloları bu sırayla görünmelidir. RTF dosyası, yazı tipleri, stiller, ekran rengi, resimler, dipnotlar, yorumlar (ek açıklamalar), üst bilgiler ve alt bilgiler, özet bilgiler, alanlar, yer imleri, belge, bölüm, paragraf ve karakter biçimlendirme özellikleri, matematik, görüntüler ve nesneler. Yazı tipi, dosya, stil, renk, revizyon işareti ve özet bilgi grupları ve belge biçimlendirme özellikleri dosyaya dahil edilmişse, RTF gövdesinden önce gelen RTF başlığında görünmelidirler. Herhangi bir grubun içeriği kullanılmazsa, grup atlanabilir. Başka bir grupta tanımlanan özellikleri kullanan herhangi bir grup, bu özellikleri tanımlayan gruptan sonra görünmelidir. Örneğin, renk ve yazı tipi özellikleri stil grubundan önce gelmelidir.

#### RTF Sürümü ####

Bir RTF belgesi şu altı karakterle başlamalıdır:

```
{\rtf1
```
1, RTF sürüm numarasını gösterir.

#### Karakter seti ####

{\rtf1'den sonra, belge hangi karakter kümesini kullandığını bildirmelidir. Bir karakter kümesi bildirmenin yolu şu komutlardan biridir:

`\ansi` - Belge, normal MSWindows karakter seti olan Code Page 1252 olarak da bilinen ANSI karakter setindedir.

`\mac` - Belge, Mac OS'nin eski (10 öncesi) sürümleri altındaki normal karakter seti olan MacAscii karakter setindedir.

`\pc` - Belge, MS-DOS için varsayılan karakter seti olan DOS Code Page 437'dedir. Kas hafızası iyi olan daktilocular, bunun "Alt sayısal" kodları yorumlamak için hala kullanılan karakter kümesi olduğunu fark edeceklerdir; örneğin, sayısal tuş takımında Alt tuşunu basılı tutup "130" yazdığınızda, bir é üretir, çünkü karakter CP437'de 130 bir e'dir. Bu, CP437'nin bugünlerde gördüğü tek kullanımla ilgili.

`\pca` - Belge, MS-DOS Çok Dilde Kod Sayfası olarak da bilinen DOS Kod Sayfası 850'dedir.

#### Yazı Tipi Komutu ####

Karakter seti tanımını `\deffN` komutu takip eder. Bu, N yazı tipi numarasının bu belge için varsayılan yazı tipi olduğunu tanımlar. Yazı tipi numarası N, yazı tipi tablosundan belirtilir. `\deffN` komutu teknik olarak isteğe bağlıdır, ancak aşağıdaki gibi yaygın bir prolog varsayılan yazı tipi olarak yazı tipi 0'ı seçtiği için güvenli tarafta olması gerekir.

`{\rtf1\ansi\deff0`

#### Yazı Tipi Tablosu ####

Bir belgede kullanılabilen tüm yazı tipleri, her yazı tipinin bir yazı tipi numarasıyla temsil edildiği bir yazı tipi tablosunda listelenir. Bazı programlar onsuz da çalışsa da, belgede bir yazı tipi tablosu olmalıdır.

Bir yazı tipi tablosunun sözdizimi {\fonttbl //...bildirimler//...} şeklindedir ve burada her bildirim şu temel sözdizimine sahiptir:

`{\fnumber\familycommand Fontname;}`

Dört bildirim içeren bir yazı tipi tablosu aşağıdaki gibidir:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Bu yazı tipi tablosuna sahip bir belgede, `{\f2 stuff}`, Courier New'de "öğeler" yazdırır. Bir yazı tipi, yazı tipi tablosunda listelenmeden bir belgede kullanılamaz.

### Dokümanın sonu ###

Belgedeki ilk karakter olan { tarafından açılan grubu kapatmak için her RTF belgesinin bir } ile bitmesi gerekir. Muhtemelen bir yeni satır dışında hiçbir şey son }'den sonra gelemez.

## Referanslar ##

* [RTF 1.9.1 Spesifikasyonları](https://interoperability.blob.core.windows.net/files/Archive_References/%5bMSFT-RTF%5d.pdf)
* [Zengin Metin Biçimi](https://en.wikipedia.org/wiki/Rich_Text_Format)

