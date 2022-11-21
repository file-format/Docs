{
  "date" : "2019-10-11",
  "keywords" :[ "mht","mht dosyası", "mht dosya biçimi", "mht dosya türü", "dosya", "tür", "mht dosyası nedir" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MHT - MIME HTML Dosya Biçimi",
  "description" :"MHT Dosya Biçimi ve MHT dosyaları oluşturmak ve açmak için API'ler hakkında bilgi edinin.",
  "linktitle" : "MHT",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## .mht dosyası nedir?

.mht uzantılı bir dosya, farklı veri türlerini tek bir dosyada içeren, MIME özellikli bir arşivleme dosyası biçimidir. Metin, resimler, sayfa stili gibi verileri [CSS](/tr/web/css/) biçiminde, JavaScript'te ve diğer kaynaklarda gömülü kaynaklar olarak saklayabilir. MIME tipi mesaj/rfc822'ye sahip olan MHT dosyaları, bir HTML dosyasının tüm içeriğini, depolama aygıtlarında arşivlemede depolamak için tek bir arşiv dosyası olarak kapsüller. Microsoft Word gibi yazılım uygulamaları, WORD belgelerinizi MHT dosyası olarak dışa aktararak MHT'ye dönüştürmenizi sağlar. MHT dosyaları, Microsoft Internet Explorer ve Google Chrome gibi popüler tarayıcılar kullanılarak açılabilir.

## MHT Dosya Biçimi

[MHTML](/tr/web/mhtml/) gibi, MHT de toplu HTML belgelerinin bir MIME kapsüllemesidir. Bir MHT belgesi içindeki satır içi resimler, stil sayfaları, uygulamalar vb. gibi belge içerikleri, URI'ler yoluyla bir kök kaynağa bağlandıklarında MIME kodludur. Microsoft Outlook gibi e-posta istemcileri, e-postaları (genellikle [EML](/tr/email/eml/)) MHT dosya biçiminde depolar. MHT dosya biçiminin tüm özellikleri [RFC 822](https://tools.ietf.org/html/rfc822) içinde mevcuttur ve MHT dosyalarını işleyebilen yazılım uygulaması geliştirme için başvurulabilir.

## MHT ve MHTML arasındaki fark

Çevrimiçi bir sayfayı kaydederken, kullanıcıdan çevrimiçi sayfanın yerel sisteme kaydedilmesi gereken dosya formatı türünü belirlemesi istenir. Çoğu zaman, kullanıcının biçimlendirme dili ile MHTML dosya biçimleri arasında kafası karışır. Bunlar arasında dosya formatının daha sağlıklı olduğunu görmekte sıkıntı çekiyorlar.

Bir kullanıcı çevrimiçi sayfayı biçimlendirme dili olarak israf etmekten kaçınmaya karar verdiğinde, sayfanın çeşitli içerikleri için birden çok dosya içeren bir klasör oluşturulur; yani metin, grafik, küçük uygulamalar vb. için oluşturulmuş tamamen farklı dosyalar alanı birimi. MHTML çevrimiçi sayfanın tamamı için tek bir dosya oluşturur. Grafikler, bağlantılar ve alternatif dosyalar alan birimi ile birlikte sayfanın tüm öğeleri tek bir dosyanın içine gömülüdür.

Doğal olarak, MHT veya MHTML dosyalarını işlemek kolaydır çünkü dosya korunabilir ve yalnızca e-posta yoluyla paylaşılabilir. Bununla birlikte, biçimlendirme dili dosyaları, tek bir dosyanın bile kaybedilmesi veya silinmesi nedeniyle bilgi kaybı şansının altındaki alan birimi, tüm biçimlendirme dili klasörünün kullanıcı için yararsız olmasına neden olabilir.

## Referanslar

* [MHTML - Wikipedia](https://en.wikipedia.org/wiki/MHTML)
* [MHT RFC](https://tools.ietf.org/html/rfc822)

