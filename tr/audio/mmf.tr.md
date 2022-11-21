{
  "date" : "2021-08-09",
  "keywords" :[ "mmf", "dosya", "uzantı", "biçim", "ses", "smaf", "mmf uzantısı", "mmf dosyaları", "mobil müzik dosyası", "yamaha"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MMF dosya formatı ve MMF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MMF - Mobil Müzik Dosyası Formatı",
  "linktitle" : "MMF",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-08-09"
}

## .mf dosyası nedir?

MMF, bir SMAF dosyasıyla ilişkili bir dosya uzantısıdır. MMF, Mobil Müzik Dosyası anlamına gelirken SMAF, sentetik müzik Mobil Uygulama Formatı anlamına gelir. Bir akıllı telefondaki MMF dosyaları sistem zil sesleri, ses içerir ve ayrıca grafik ve metin ekranı içerebilir. MMF ayrıca FM, PCM ve Stream PCM dahil olmak üzere üç tür enstrüman parametresi içerir. Bu dosya biçimleri, Windows sistem platformuyla uyumludur. MMF dosyaları veri dosyaları olarak kategorize edilir. Genellikle, Microsoft Mail MMF dosyalarını destekler. MMF son ekine sahip dosya, herhangi bir mobil cihaza veya sistem platformuna kopyalanabilir.

Ayrıca, bu dosyaların boyutu standart MIDI formatındaki dosyalara kıyasla çok daha küçüktür. [WAV](/tr/audio/wav/) ve [MID](/tr/audio/mid/) dosyaları, daha sonra ses içeriği olarak paylaşılabilen ve dağıtılabilen MMF formatına dönüştürülebilir. Bu dosyalar e-posta yoluyla doğrudan telefonlara ve PC'ye alınabilir.


## MMF Dosya Biçiminin Kısa Tarihi

Yamaha, akıllı telefonların daha fazla sayıda benzersiz zil sesi depolayabilmesi için SMAF araçlarını ses dosyaları olarak geliştirdi. Yamaha, MA-1, MA-2, MA-3, MA-5 ve MA-7 LSI ses yongalarının üretimiyle SMAF'ı tanıttı. Tüm bu biçimler, 2000 yılının başlarında Doğu Asya Pazarındaki cep telefonları arasında oldukça tanıdık hale geldi.

Uluslararası düzeyde, MMF formatı Samsung tarafından onaylanmıştır. MMF formatının yardımıyla Samsung, Samsung akıllı telefonlarında kullanılmak üzere çok çeşitli polifonik zil sesleri tasarlamayı başardı.

Yamaha, formatı daha da popüler hale getirmek istedi ve bu nedenle resmi Yamaha SMAF dosyalarında bu formatla uyumlu daha fazla araç yayınladı. Bununla kullanıcılar artık MMF dosyalarını bilgisayarlarında kolayca oynatabilir.


## MMF Dosya Biçimi Özellikleri ##

MMF dosyaları veri bölümlerine ayrılmıştır. Her segmenti tanımlamak için 8 baytlık bir ön ekli yapı kullanılır.
4 baytlık etiket CNTI, OPDA, MSTR, MTR ve ATR'yi içerir. Veri boyutu artı 8 bayt yığın boyutudur; tüm dosya boyutu, tüm parça boyutları toplanarak hesaplanır. Bir dosya zarar görmemişse, toplanan dosya boyutu birincil başlık boyutuyla aynı olmalıdır.

### Başlık ###

```
struct SMAF_Header
{
    uint32   SignatureMMMD;     // Signature: "MMMD"
    uint32   SizeSMAF;      // 4 byte data size, big-endian order
};
```

İşte bir MMF dosyası örneği:

![](../mmf.png)

## Referanslar

* [MMF - Wikipedia'dan](https://en.wikipedia.org/wiki/Synthetic_music_mobile_application_format)

