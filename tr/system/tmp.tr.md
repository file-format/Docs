{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "uzantı", "dosya", "format", "sistem", "TMP dosyası", "TMP belgeleri", "TMP dosyaları", "Geçici dosya", "uygulama", "programlar" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Geçici Dosya Biçimi",
  "description":"TMP dosya formatı ve TMP dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## TMP dosyası nedir? ##

Bir TMP dosyası, bir yazılım programı tarafından oluşturulan geçici bir yedekleme, depolama veya başka bir dosya sistemini ifade eder. Bazen görünmez bir dosya olarak oluşturulur ve program kapatıldığında sıklıkla yok edilir. TMP dosyaları, yeni bir dosya oluşturulurken bilgileri geçici olarak depolamak için de kullanılabilir.

## TMP Dosya Biçimi ##

Bir TMP dosyası tipik olarak, malzemenin bir stilden diğerine dönüştürülme sürecinde bir aşama olarak kullanılan ham verilerden oluşur. Microsoft Word ve Apple Safari, TMP dosya biçimini üretebilen ve kullanabilen iki uygulamadır.

Üretilen TMP belgeleri, teoride, program kapatıldığında veya makine kapatıldığında otomatik olarak kaldırılmalıdır. Uygulamada, bu her zaman böyle değildir. Sonuç olarak, programınızın belgeleri arasında gezinirken, sistem veya başka bir yazılım tarafından aktif olarak kullanılmayan geçici dosyalarla karşılaşabilirsiniz.

### Yardımcı bellek ###

İşletim sistemlerinde sanal bellek kullanılır, ancak büyük miktarda bilgi kullanan programların geçici belgeler oluşturması gerekebilir.

### Arası iletişim ###

Çoğu işletim sistemi, programlar arasında veri aktarımı için kanallar, soketler veya ana bellek gibi ilkel öğeler sağlar, ancak en basit yöntem, dosyaları geçici bir dosyaya aktarmak ve alıcı uygulamaya geçici dosyanın konumunu tavsiye etmektir.


## Teknik Şartname ##

Ayırt edici geçici belge adlarının elde edilmesi genellikle işletim sistemleri ve yazılım programları tarafından sağlanır.
Geçici dosyalar, mkstemp veya tmpfile kitaplık işlevleri kullanılarak POSIX sistemlerinde güvenle oluşturulabilir. Bazı sistemler önceki POSIX (gittiğinden beri) mktemp uygulamasını içerir. Bu dosyalar genellikle /TMP'deki Unix platformlarındaki normal geçici dizinde veya Windows makinelerinde %TEMP%'de (oturum açmaya özeldir) bulunur.

Program durduğunda veya belge kapatıldığında, tmpfile ile oluşturulan geçici dosya otomatik olarak kaldırılır. GetTempFileName (Windows) veya tmpnam (POSIX), onu oluşturan programdan daha uzun sürecek geçici bir dosya adı oluşturmak için kullanılabilir.

## Referans ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
