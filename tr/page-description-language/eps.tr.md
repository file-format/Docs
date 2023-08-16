{
  "date" : "2019-12-12",
  "keywords" :[ "EPS", "dosya", "uzantı", "dosya formatı", "Sayfa Düzeni", "Encapsulated PostScript"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"EPS dosya formatı ve EPS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"EPS Dosya Biçimi - Encapsulated PostScript Dosyası",
  "linktitle" : "EPS",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## EPS dosyası nedir?

.eps dosyası, Encapsulated Postscript dosya biçiminde diske kaydedilen bir görüntü dosyasıdır. Metin, grafik ve resimlerin herhangi bir kombinasyonunu içerebilir. EPS dosyaları, bu tür dosyaları açabilen uygulamalar tarafından görüntülenmek üzere içine kapsüllenmiş bir bitmap önizleme görüntüsü de içerebilir.

## EPS Dosya Formatının Kısa Tarihi

Geçmiş perspektifinden EPS dosya biçimine hızlı bir bakış, aşağıdaki bilgileri ortaya çıkarır:

* EPS'nin ilk sürümü Adobe tarafından 1985 ile 1988 yılları arasında yayınlandı.
* EPS belirtiminin 2.0 sürümü Ocak 1989'da yayınlandı
* EPS'nin 3.0 sürümünün özellikleri 1992'de ayrı bir belge olarak yayınlandı; bu en son yayınlanan sürümdür.

EPS, Adobe'nin PostScript Dil Belgesi Yapılandırma Kuralları Belirtimi'nin 9. maddesinde açıklanan Open Structuring Conventions uzatma mekanizmasıyla birlikte, Adobe Illustrator Artwork dosya biçiminin ilk sürümlerinin temelini oluşturdu.

## EPS Dosya Biçimi

EPS, tescilli ancak herkes tarafından belgelenmiş bir biçimdir ve EPS dosya biçimi belirtimleri, geliştiricinin referansı için herkese açıktır. EPS, bir [DSC](https://en.wikipedia.org/wiki/Document_Structuring_Conventions) (Belge Yapılandırma Sözleşmesi) uyumlu dosya biçimidir ve DSC tarafından belirlenen tüm kurallara uyar. DSC, Adobe tarafından PostScript belgeleri için özel bir dosya formatıdır. EPS dosyalarını okuyabildiğini iddia eden herhangi bir uygulamanın DSC uyumlu olması gerekir.

Bir EPS dosyası, aşağıda açıklandığı gibi iki ana bölümden oluşur.

### Önizleme resmi ###

Tipik bir EPS dosyası, birkaç sistemi veya uygulamayı içeren bir iş akışında uygun kullanım için tasarlanmış bir biçimde bir önizleme görüntüsü içerir. Ön izlemenin amacı, çoğu grafik uygulamasının işleyebileceği biçimde bir görüntüye sahip olmaktır; bir önizleme genellikle daha düşük çözünürlükte, piksel boyutlarında ve/veya bit derinliğindedir. Önizleme dosyası birkaç formattan birinde olabilir. EPS_3 belirtimi, üç "cihaza özgü" önizleme formatını listeler:

* Apple Macintosh için, QuickDraw uygulaması tarafından kullanılan bir PICT görüntüsü
* DOS bilgisayarları için bir TIFF bit eşlemi
* Windows Meta Dosyası.

PICT ve Windows Meta Dosyası, hem bitmap verilerini hem de vektör grafiklerini içerebilir. Ek olarak, belirtim, gömülü bir bit eşlemli ön izleme görüntüsü için cihazdan bağımsız çok basit bir gösterimi tanımlar. Bu temsil, Encapsulated PostScript Değişim Formatı (EPSI) olarak bilinir.

EPSI önizlemesi, ASCII onaltılık olarak temsil edilen, tanımlama için birkaç PostScript yorumu arasına sarılmış ve basit ve kolayca taşınabilir olması amaçlanan bir bit eşlemdir. EPS spesifikasyonunda, farklı önizleme formatlarına sahip EPS dosyalarını ayırt etmek için farklı DOS dosya uzantıları ve Macintosh dosya türleri önerilmiştir.

### PostScript Kodu

EPS dosya formatı en azından aşağıdakileri içermelidir:

* bir başlık yorumu, %!PS-Adobe-3.0 EPSF-3.0
* ve çizimin sınırlarını açıklayan bir sınırlayıcı kutu açıklaması, %%BoundingBox: llx lly urx ury. Bu dört bağımsız değişken, sınırlayıcı kutunun sol alt (llx, lly) ve sağ üst (urx, ury) köşelerine karşılık gelir.

Bir EPS dosyası aşağıdaki işleçlerden herhangi birini kullanamaz:

* bant cihazı,
* cleardictstack
* kopya sayfa
* silme
* çıkış sunucusu
* çerçeve cihazı
* grestoreall
* initclip
* başlangıç grafikleri
* sıfır matris
* çıkış yapmak
* oluşturma bantları
* küresel ayarla
* ayar cihazı
* set paylaşımı
* İşe başla.

## EPS'nin Diğer Dosya biçimlerine dönüştürülmesi

EPS dosyaları, [JPG](/tr/image/jpeg/), [PNG](/tr/image/png/), [TIFF](/tr/image/tiff/) ve [PDF](/tr/pdf) gibi standart görüntü formatlarına dönüştürülebilir. /) Adobe Illustrator, Photoshop ve PaintShop Pro gibi farklı uygulamalar kullanarak.

[Güvenlik açığı](https://support.microsoft.com/en-us/office/support-for-eps-images-has-been-turned-off-in-office-a069d664-4bcf-415e-a1b5-cbb0c334a840) a1b5-cbb0c334a840) EPS dosyalarında, Office 2016, Office 2013, Office 2010 ve Office 365, EPS dosyalarını Office belgelerine ekleme özelliğini kapatmıştır.

## Referanslar

* [Encapsulated PostScript - Wikipedia Tarafından](https://en.wikipedia.org/wiki/Encapsulated_PostScript)

