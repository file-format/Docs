{
  "date" : "2021-07-25",
  "keywords":["man","file", "extension", "type", "format", "Unix Manual"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MAN - Unix Kılavuzu",
  "description":"FODT dosya formatı ve MAN dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "MAN",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2021-07-25"
}

## .man dosyası nedir?

.man uzantılı bir dosya, yazılım dokümantasyonu biçiminde bir Unix programlama kullanım kılavuzu olan man sayfası anlamına gelir. Belgeleri görüntülemek için kullanılan Unix'te bulunan 'Man' yardımcı programı tarafından kullanılır. Yazılım belgeleri, Man yardımcı programı kullanılarak komutlar vererek komut terminalinden alınabilen bölümler ve sayfalardaki bilgileri içerir. Dokümantasyonun elektronik kopyası olarak bilgisayarda bulunduğundan, ona erişmek için herhangi bir basılı kopya veya internet bağlantısı gerektirmez.

## Unix Manuel Man Dosya Biçimi - Daha Fazla Bilgi

Kılavuz sayfaları düz metin biçiminde saklanır ve görüntülenmek veya düzenlenmek üzere herhangi bir metin düzenleyicide oluşturulabilir ve açılabilir. UNIX'te, Kılavuz sayfalarından bilgi, kılavuzdan bölüm ve sayfa numaralarına referans içeren terminalden komutlar vererek alınır.

### Bölümler ve Sayfalar

Unix man, komuttaki her sayfa bağımsız değişkeninin bir programın, yardımcı programın veya işlevin adına atıfta bulunduğu sistem kılavuzudur. komut, bölüm bilgisi sağlanmışsa, o belirli bölümdeki sayfayı arayacaktır. Ancak, varsayılan davranış, sayfayı tüm bölümlerde aramak ve birden çok bölümde bulunup bulunmadığına bakılmaksızın ilk sayfayı görüntülemektir.

### Bölüm Numaraları

Aşağıda kılavuzun bölüm numaraları ve içerdikleri sayfa türleri ile ilgili bilgiler yer almaktadır.

|Bölüm Numarası|Sayfa türleri|
---|---|
|1|Yürütülebilir programlar veya kabuk komutları|
|2|Sistem çağrıları (çekirdek tarafından sağlanan işlevler)|
|3|Kütüphane çağrıları (program kitaplıkları içindeki işlevler)|
|4|Özel dosyalar (genellikle /dev'de bulunur)|
|5|Dosya biçimleri ve kuralları, örneğin /etc/passwd|
|6|Oyunlar|
|7|Çeşitli (makro paketleri ve kuralları dahil), örneğin man(7), groff(7)|
|8|Sistem yönetimi komutları (genellikle yalnızca kök için)|
|9|Kernel rutinleri [Standart dışı]|

## Örnek - MAN Sayfaları Nasıl Okunur?

İşte Man komutunu kullanarak MkDir komutu hakkında bilgi almanın bir örneği.

```
% man mkdir

MKDIR(1)    USER COMMANDS       MKDIR(1)

NAME
   mkdir - make a directory

SYNOPSIS
   mkdir [ -p ] dirname...

DESCRIPTION
   mkdir creates directories. Standard entries,`.',for the
   directory itself, and `..' for its parent, are made automat-
   ically.

   The -p flag allows missing parent directories
   to be created as needed.

   With the exception of the set-gid bit, the
   current umask(2V) setting determines the mode in which
   directories are created. The new directory inherits the set-gid
   bit of the parent directory. Modes may be modified after
   creation by using chmod(1V).

   mkdir requires write permission in the parent directory.

SEE ALSO
   chmod(1V), rm(1), mkdir(2v), umask(2V)
```

## Referanslar

* [OpenDocument Teknik Spesifikasyonları - Wikipedia Tarafından](https://en.wikipedia.org/wiki/OpenDocument_technical_specification)
* [man(1) — Linux kılavuz sayfası](https://man7.org/linux/man-pages/man1/man.1.html)

