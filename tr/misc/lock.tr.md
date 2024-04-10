{
  "date" : "2022-01-26",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"KİLİT Dosya Biçimi - Kilit dosyası nedir?",
  "description":"LOCK dosya biçimi ve onun hakkında bilgi edinin.",
  "linktitle" : "LOCK",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-26"
}

## .lock dosyası nedir?

**KİLİT** dosyası, uygulamalar ve işletim sistemleri tarafından bir dosyayı veya bazı cihazları kilitli olarak işaretlemek için kullanılan, yeniden adlandırılmış bir dosyadır. Bu, diğer uygulamalara, onu kullanan uygulamadan bağımsız olmadıkça dosyayı kullanmamalarını söyler. Çoğu durumda, bu kilit dosyaları boştur, ancak diğer durumlarda, özellikler ve ayarlar gibi kilitle ilgili bilgiler içerebilirler.

Bazen .lock dosyası, bir veritabanı dosyasının **lockeed** kopyalarını oluşturmak için Microsoft'un .NET Framework tarafından kullanılır. Böyle bir durumda veritabanı dosyasının bir kopyası .lock uzantılı açılacaktır. Bu, başka bir kullanıcı tarafından kullanımdayken kullanıcının dosyada değişiklik yapmasına izin vermez.

## KİLİT Dosya Biçimi - Daha Fazla Bilgi

Her uygulama tarafından bir LOCK dosyası oluşturulur ve dosya formatı uygulamaya özeldir. Bu kilit dosyaları hem metin hem de ikili dosya biçiminde kaydedilebilir.

Kilit dosyalarının varlığı, bir kaynağın o kaynağa erişmeye çalışan birden çok dosyaya aynı anda erişmesini engeller. Orijinal dosyanın bir kopyası, adına .lock uzantısı eklenerek oluşturulur. Bu, diğer uygulamalara dosyaya salt okunur erişime sahip olmalarını söyler. Örneğin, kaynak.dat, kaynak.data.lock olur.

Ruby programlama dili için **gemfile.lock** dosyasına rastlayabilirsiniz. Burası, Bundler'ın kurulu olan sürümlerin kaydını tuttuğu yerdir. Bu nedenle, bir proje/kütüphane başka bir makineye taşındığında, çalışan paket ilgili sürüm için Gemfile'a bakacaktır.

## Linux'ta Dosyayı Kilitle

Linux iki tür dosya kilidini destekler: tavsiye niteliğindeki kilitler ve zorunlu kilitler.

* **Danışma Kilitleri**: Zorunlu olmayan kilitleme türü. Bu durumda, katılan süreçler açıkça kilitler alarak birbirleriyle işbirliği yapar. Bu mümkün değilse, danışma kilitleri dikkate alınmaz.

* **Zorunlu Kilitler**: Zorunlu kilitleme durumunda, işletim sistemi diğer işlemlerin dosyayı okumasını veya yazmasını engelleyerek dosya kilitlemeyi zorunlu kılar. Bu, süreçler arasında herhangi bir işbirliği gerektirmez.

zorunlu kilitleme, katılan süreçler arasında herhangi bir işbirliği gerektirmez. Bir dosya üzerinde zorunlu bir kilit etkinleştirildiğinde, işletim sistemi diğer işlemlerin dosyayı okumasını veya yazmasını engeller.

## Referanslar

* [Ruby'de GemFile ve Gemfile.lock](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-Ruby-65adc918b856)
* [Linux'ta Kilitleme](https://www.baeldung.com/linux/file-locking)

