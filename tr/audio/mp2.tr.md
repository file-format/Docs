{
  "date" : "2021-06-11",
  "keywords" :[ "mp2", "mp2 dosyası", "uzantı", "format", "mp2 dosyası nedir", "müzik", "mp2 dosya biçimi"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"MP2 dosya formatı ve MP2 dosyalarını oluşturabilen, dönüştürebilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"MP2 - MPEG Katman 2 Ses Dosyası Formatı",
  "linktitle" : "MP2",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-11"
}

## MP2 dosyası nedir?

MPA dosyası olarak da adlandırılan bir MP2 dosyası, MPEG-1 veya MPEG-2'nin II. Katmanı ile sıkıştırılmış bir Ses dosyasıdır; ses dosyası boyutunu azaltmak için MPEG-1 Audio Layer I ve MPEG-1 Audio Layer III ([MP3](/tr/audio/mp3/)) ile birlikte ISO/IEC 11172-3 tarafından tanımlanan kayıplı bir ses sıkıştırma formatı. Oysa MP3, daha küçük boyutu ve internet üzerinden kullanılabilirliği nedeniyle MP2'den daha popülerdir. Bu nedenle MP2, ses yayını için hala hayati bir standarttır.

## MP2 Dosya Biçimi

MPEG Audio Layer II (MP2), MP3 standartlarının temel algoritmasıdır. MPEG-1 Ses Katmanı 2 kodlaması, MUSICAM ses codec'inden elde edildi. EUREKA araştırma programının bir parçası olarak Almanya'da Digital Audio Broadcast (DAB) projesi olarak başlamıştır. Eureka 147 üç ana unsur içeriyordu: İletim Kodlama ve Çoğullama, COFDM Modülasyonu ve MUSICAM Ses Kodlama (Maskeleme modeli Evrensel Alt-bant Tümleşik Kodlama ve Çoğullama). MUSICAM, monofonik kanal başına 64 ila 192 kbit/s aralığındaki bit hızlarında yüksek ses kalitesi elde edebilen birkaç kodlamadan biriydi. Amaç, düşük gecikme, düşük karmaşıklık, hata sağlamlığı, kısa erişim birimleri sağlamak ve dijital depolama ortamlarında yayın, telekomünikasyon ve kayıt teknik gereksinimlerini karşılamaktı.

MP2, 32 frekans alanı bileşeni üreten düşük gecikmeli bir filtre bankası ile zaman alanında sıkıştırılabilen bir alt bant ses kodlayıcıdır. Karşılaştırıldığında, MP3, hibrit filtre bankasına sahip bir dönüşüm ses kodlayıcıdır; bu, sıkıştırmanın, zaman alanından bir hibrit dönüşümün ardından frekans alanında uygulandığı anlamına gelir. MP2 kodlayıcı, isteğe bağlı "ortak stereo" yoğunluk kodlaması kullanarak kanallar arası fazlalıklardan yararlanabilir.

### MP2 Dosya Biçimi Özellikleri

MP2 dosya formatı, dört olası formatla 1152 örnekleme aralığından oluşan ardışık dijital çerçevelere dayanır:

- mono biçim
- stereo formatı
- yoğunluk kodlu ortak stereo formatı (stereo alakasız)
- çift kanallı (ilişkisiz) format
MP2'nin bazı önemli teknik özellikleri aşağıdaki tabloda verilmiştir:

|Şartname| Açıklama|
---|---|
|**Örnekleme oranları**| 32, 44.1 ve 48 kHz|
|**Bit hızları**|32, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 ve 384 kbit/sn|
|**Ek örnekleme hızları**|16, 22.05 ve 24 kHz|
|**Ek bit hızları**|8, 16, 24, 40 ve 144 kbit/sn|
|**Çok kanallı destek**|5 adede kadar tam aralıklı ses kanalı ve bir LFE kanalı (Düşük Frekans Geliştirme kanalı)|

## Referanslar ##

* [MPEG-1 Ses Katmanı II - Wikipedia'dan](https://en.wikipedia.org/wiki/MPEG-1_Audio_Layer_II)

