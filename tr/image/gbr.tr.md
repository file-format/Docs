{
  "date" : "2019-10-11",
  "keywords" :[ "gbr dosyası", "gbr dosya biçimi", "gbr dosyası nedir", "dosya", "gbr örneği", "gbr dosya uzantısı","uzantı", "biçim"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"GBR Dosya Formatı - PCB için Gerber Dosya Formatı",
  "description":"GBR dosya formatı ve GBR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "GBR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## .gbr dosyası nedir?

.gbr uzantılı bir dosya, baskılı devre kartı (PCB) tasarım veri aktarımının değiş tokuşu için bir Gerber görüntü dosyası formatıdır. Ucamco tarafından geliştirilmiştir. PCB tasarım verileri, imalat endüstrisinin işleme için ihtiyaç duyduğu ana bileşendir. Bir GRB dosyası, bakır katmanlar, lehim maskesi, açıklama ve delme ve rota verileri gibi PCB verilerini içerir. Kalınlık veya bitiş dahil olmak üzere PCB üretim özellikleri gibi verileri standart bir formatta aktarmak için kullanılabilir. Tüm PCB tasarım sistemleri, PCB fabrikasyon sistemleri tarafından işlenebilen Gerber dosyalarını çıkarır. GBR dosyaları artık baskılı devre kartı (PCB) tasarım veri aktarımı için fiili standart haline geldi. Ucamco, GBR dosya biçimlerini açmak ve görüntülemek için [ücretsiz çevrimiçi görüntüleyici](https://gerber-viewer.ucamco.com/) sağlamıştır.

## GBR Dosya Biçimi

GBR, yalnızca 27 komuttan oluşan, insanlar tarafından okunabilen bir UTF-8 biçimidir. Bu kısa komut listesi ve kompaktlığı nedeniyle, GBR'de hata ayıklamak kolaydır. Gerber özünde 2D ikili görüntüler için açık bir vektör formatıdır. Meta-bilgiler, Nitelikler aracılığıyla görüntülerle birlikte aktarılır. Tek bir GRB dosyası, tek bir görüntüyü belirtir ve yorumlanacak herhangi bir eşlik eden dosya veya harici parametre gerektirmez. Bir görüntünün yalnızca bir dosyaya ihtiyacı vardır. Yazdırılabilir özellikte tanımlanan tüm komutlar ve adlar için 7 bitlik ASCII karakterleri kullanır. Bu tamamen eksiksiz görüntü oluşturmayı kapsar.

### Örnek GBR Dosyası

Aşağıda, orijinde merkezli 1,5 mm çapında bir daire oluşturan örnek bir Gerber dosyası bulunmaktadır. Her satırda bir komut vardır.

```
%FSLAX26Y26*%
%MOMM*%
%ADD   100C,1.5*%
D100* X0Y0D03*
M02*
```

## Referanslar

* [Gerber Formatı](https://www.ucamco.com/en/gerber)

