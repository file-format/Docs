{
  "date" : "2021-09-16", 
  "keywords" :[ "hta", "dosya", "uzantı", "dosya biçimi", "hta uygulaması", "Programlama Kılavuzu", "hta örneği", "HTML Uygulaması", "Köprü Metni Biçimlendirme Dili Uygulaması", "HTA dosyaları", "Microsoft HTML Uygulaması"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HTA - HTML Uygulama Dosyaları",
  "description":"HTA dosya formatı ve HTA dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "HTA",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-16"
}

## HTA dosyası nedir?

**Köprü Metni İşaretleme Dili Uygulaması** anlamına gelen HTMLA, Microsoft Windows ile uyumlu bir programdır. Bu programın kaynak kodu, [HTML](/tr/web/html/) ve [JavaScript](/tr/web/js/) gibi birden fazla betik dili içermektedir. Kullanıcı arayüzü için HTML Uygulaması tercih edilirken, program mantığının gereğini yerine getirmek için herhangi bir betik dili kullanılmaktadır.

Bir HTML Uygulaması, internet tarayıcısının güvenlik modelinden bağımsızdır ve tamamen güvenilir bir uygulama olarak çalışır. Bu uygulamalarla ilgili dosyalar için kullanılan uzantı HTA'dır. Bu uygulamalar, diğer betik dillerinin özellikleriyle birlikte HTML'nin özelliklerini içerir.


## Kısa Tarih ##

HTA ilk olarak 1999 yılında Microsoft tarafından Internet Explorer 5'in piyasaya sürülmesiyle birlikte tanıtıldı. Internet Explorer ile uyumluydu ve bu nedenle yalnızca Windows işletim sisteminde çalıştırılabiliyordu. Bu teknolojinin patenti 2003 yılında alınmıştır. HTA dosyaları diğer tüm .exe dosyalarına benzer şekilde yürütülür. HTA dosyaları, Windows 11'in günümüzün güncellenmiş sürümüyle de uyumludur.


## Teknik Şartname ##

HTA'lar, diğer herhangi bir HTML sayfasının içerdiği formatla aynı formata sahipken, bazı nitelikler programların kenarlık stillerini veya simgelerini kontrol etmek için kullanılır. Ayrıca, HTA'nın başlatılması için argümanlar sağlanmıştır. Bu uygulamalar, mshta.exe adlı bir program kullanılarak yürütülebilir. Dosyaya çift tıklayarak kolayca erişilebilir. Bu programlar otomatik olarak Internet explorer ile birlikte çalışır. Diğer spesifikasyonların yanı sıra, bunlar Trident motor tarayıcısından bağımsız değil, Internet Explorer'dan bağımsızdır. Bu, bunların Internet Explorer kullanılmadan yürütülebileceği anlamına gelir.

Etiketler, bu uygulamaların görünümünün özelleştirilmesi amacıyla kullanılmaktadır. Microsoft HTML uygulamasından HTA biçimine dönüştürme daha kolaydır, yani yalnızca uzantıyı değiştirmeniz gerekir. Bu uygulamaların tamamen güvenilir olduğunu bildiğimiz için bunlar, basit HTML dosyalarına kıyasla daha fazla özellik ve avantaj içerir. HTA oluşturmak için metin editörleri kullanılabilir. Bu düzenleyiciler, Microsoft veya başka herhangi bir güvenilir kaynak tarafından edinilebilir.


## HTA Dosya Biçimi Örneği ##

```
<HTML>
<HEAD>
<HTA:APPLICATION ID="HelloExample" 
   BORDER="bold" 
   BORDERSTYLE="complex"/>
<TITLE>HTA - Hello World</TITLE>
</HEAD>
<BODY>
<H2>HTA - Hello World</H2>
</BODY>
</HTML>

```

## Referans ##

* [HTA - Wikipedia'dan](https://en.wikipedia.org/wiki/HTML_Application)



