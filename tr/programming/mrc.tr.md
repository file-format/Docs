{
  "date" : "2021-09-14", 
  "keywords" :[ "mrc", "dosya", "uzantı", "dosya biçimi", "mrc uygulaması", "Programlama Kılavuzu", "mrc örneği", "mIRC", "mIRC betik dili", "INI dosyaları", " mSL betik dili", "mIRC dili", "mIRC betikleri", "komut dosyası dili"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MRC - mIRC Komut Dosyası Dil Dosyası",
  "description":"MRC dosya formatı ve MRC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MRC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-14"
}

## Bir MRC dosyası nedir?

mIRC, Windows işletim sisteminde bir IRC istemcisi (Internet Relay Chat) olarak katıştırılmış bir betik dilidir. Kişisel ve kanal kullanımı için istenmeyen e-postalara karşı bir koruma tesisi sağlar. Daha iyi bir kullanıcı uyumluluğu deneyimi sağlamak için bu mIRC betik dili, diyalog pencerelerinin oluşturulmasına izin verir. Çoğunluğu düz metin biçiminde olan komut dosyaları içeren dosyalar, MRC uzantısıyla veya [INI](/tr/system/ini/) dosyaları olarak depolanır. Bu dilin işlevleri, komutlar ve tanımlayıcılar (değer döndürdüklerinde) olarak bilinir.

mIRC dili, aynı anda birden çok betik dosyasının yüklenmesini sağlar. Öte yandan, bir dosya aynı anda yüklendiğinde diğerinin artık kullanılmamasına neden olabilir. Komutlar kaydedilir ve otomatik olarak IRC'de bulunabilirler. Bu dilde kullanılan komutlar ve takma adlar, herhangi bir karakterin önceliğini içermez.

mIRC, botların bir kanalı otomatik olarak yönetmesini sağlamak için yaygın olarak kullanılır, ancak mSL betik dili tarafından da değiştirilebilir. Makrolar, müzik çalma yeteneği, küçük makrolar ve işlevler, temel oyunlar veya küçük uygulamaları çalıştırma gibi birçok yeni özelliği tanıtabilir.


## Kısa Tarih ##

Bu betik dili ilk olarak 1995 yılında Khaled Adam Bey tarafından geliştirilmiştir. Betik dilinin tasarımı da Khalid tarafından yapılmıştır. Bu dilin hedefi olay güdümlü programlamaydı. Başlangıçta, bu programlama dilinin dosyaları için kullanılan dosya uzantısı .mrc ve .ini idi. Ayrıca, tescilli yazılım lisansı altında geliştirilmiştir.

## Teknik Şartname ##

Bazı işlevler, bu mIRC dili aracılığıyla özel olarak yazılır ve takma adlar olarak bilinir. Bu takma adlar değer döndürdüğünde, özel tanımlayıcılar olarak bilinirler. Bu mIRC dilinde yer alan tüm değişkenler dinamik olarak yazılır. İşaretler, mIRC betikleri tarafından kullanılır. Bu betik dilinin bir diğer özelliği de pop-up'lardır. Kullanıcılar pop-up'ları basitçe seçerek çağırabilir. Uzaktan kumandalar belirli olaylar için belirtilir. Uzaktan kumandalar, ilgili olay meydana geldiğinde çağrılır.

Boşlukla ayrılmış belirteçler, bu dilin her bir kod satırını kırmak için kullanılır. MDX (mIRC Dialog Extension) ve DCX (Dialog Control Extension) gibi mIRC dosyaları için kullanılan başka popüler uzantılar da vardır. Bunların her ikisi de diyalog uzantılarıdır ve nispeten daha popülerdir. Dil yapıları, bu betik dilinin terminolojisi ile anılır. mIRC dili, bir betik dilinin yerel ve genel değişkenler, ikili değişkenler, karma tablolar ve dosya işleme gibi farklı yönlerini içerir.


## MRC Dosya Biçimi Örneği ##

```

;Defines the alias 'hello' in the remote script

;Note: if this is placed in an alias script,
;the 'alias' part must be removed (result: hello {)
;Usage: /hello

alias hello {

  ;Displays(/tr/echo) 'Hello World!' into the active window(-a)
  echo -a Hello World!

}

```

```
;Placed in a remote script

;When a user types Hello! in a channel,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:#:{ msg $chan Hello, $nick $+ ! }

;When a user types Hello! in a private message,
;you answer back: Hello, [nickname]!

on *:TEXT:Hello!:?: { msg $nick Hello, $nick $+ ! }

;Here is a script which automatically gives voice to a user
;who joins a particular channel (The Bot or user should have HOP)

on *:JOIN:#?: { mode $chan +v $nick }

;A bad word script

on *:Text:die*:#: { .mode $chan +b $nick | kick $chan $nick Dont say that again }

```

## Referans ##

* [MIRC - Wikipedia'dan](https://en.wikipedia.org/wiki/MIRC_scripting_language)



