{
  "date" : "2022-11-17",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "BIF Dosyası - Ventana Tam Slayt Görüntü Formatı",
  "description":"BIF dosya formatı ve BIF dosyalarını oluşturup açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "BIF",
  "menu" : {
    "docs" : {
      "identifier":"image-bif-tr",
      "parent" : "image"
}
},
  "lastmod" : "2022-11-17"
}

## BIF dosyası nedir?

BIF dosyası, slayt örneği görüntüsünü içeren bir raster görüntü dosyasıdır. Slayt görüntüleme uygulamalarıyla tek bir kompozit görüntüde birleştirilen birden fazla TIFF görüntüsünden oluşur. BIF dosyaları Ventana Medical Systems dijital slayt tarayıcısı tarafından oluşturulmuştur ve [TIFF](/image/tiff/) v 6.0 tanımının BigTIFF varyantıyla tamamen uyumludur.

## BIF Dosya Formatı

Bir BIF dosyası ikili görüntü dosyası olarak kaydedilir ve 200.000 x 200.000 piksele kadar oluşur. Bu, TIF standardı tarafından tanımlanan 32 bitlik dosya işaretçilerinin dayattığı 4 GB boyut sınırını aşarak büyük dosya boyutlarına yol açabilir. Ancak 64 bitlik dosya işaretçileriyle bu dosya boyutu engeli, TIFF standardının BigTIFF varyantı tarafından aşılır.

### BIF Dosyasını kimler kullanır?

BIF dosyaları, dijital slayt tarayıcıları tarafından slayt örneklerini taramak ve dijital kopyalarını oluşturmak için kullanılır. Patolog iseniz bu BIF dosyalarını slayt görüntüleme uygulamalarında açabilirsiniz. Mükemmel düzeyde ayrıntı ve yüksek çözünürlüklü verilerle, örnek bölümlerini daha fazla veya daha az ayrıntıyla görüntülemek için slayt görüntüsünü yakınlaştırıp uzaklaştırabilirsiniz. Bu dosyalarda bulunan [XML](/web/xml/) meta veri dosyası, görsellerin nasıl birleştirilmesi gerektiğini ve dosyanın küçük resmi olarak kullanılması gereken görseli tanımlar.

## BIF Dosyası Nasıl Açılır?

BIF dosyalarını şununla açabilirsiniz:

 * OpenSlide (platformlar arası)
 * ImageJ (platformlar arası)
 * NetScope Görüntüleyici (Windows)

## Referanslar ##

 * [Roche Dijital Patoloji BIF Teknik Raporu](https://diagnostics.roche.com/content/dam/diagnostics/Blueprint/en/pdf/rmd/Roche-Digital-Pathology-BIF-Whitepaper.pdf)

