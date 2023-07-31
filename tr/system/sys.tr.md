{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "uzantı", "dosya", "biçim", "sistem", "Sürücü", "Sistem Dosyası", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Sistem Dosyası Biçimi",
  "description":"SYS dosya formatı ve SYS dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## SYS dosyası nedir? ##

SYS dosyaları, Windows işletim sistemi ve MS-DOS uygulamalarında kullanılan "Sistem dosyalarıdır". Bu dosyalar doğrudan açılamaz ve cihazın sürücüsünden ve yapılandırmasından oluşur. SYS dosyaları, işletim sisteminin temel işlevlerinin dosyalarını içermekten sorumludur. Bunlar, aygıt sürücüsünün kritik dosyaları olarak kabul edilir ve yarış sürücüsünün herhangi bir sorunu çözüleceği zaman da kullanılabilir. Bunlar, bir bilgisayar sisteminin düzgün çalışmasından sorumludur ve .sys dosyalarının doğru ve eksiksiz olması gerekir.


## Teknik Şartname ##

.sys dosyaları, yalnızca belirli birleşimlere izin verdiği için aslında [BMP](/tr/image/bmp/) biçiminin alt kümesidir. Bu dosyaların genel biçimi LOGOS.SYS, LOGOW.SYS ve LOGO.SYS gibidir. Diğer dosyalarda bu biçim yoktur.

Bu dosyalar, kurulum sırasında çoğunlukla Windows'un *C* dizininde kullanılır. Aygıt sürücüleriyle ilgili sorunların çoğu, Windows işletim sistemi güncelleştirilerek çözülür. Bu dosyaların ayrıntıları ve bilgileri, Windows işletim sisteminin yerleşik programları kullanılarak görüntülenebilir. Bunlar ayrıca bir işletim sistemindeki farklı modüllere yapılan referansları içerir.
Sistem dosyalarının bazı örnekleri şunlardır:

* IO.SYS (Bunlar, disk işletim sisteminin aygıt sürücülerini depolar)
* MSDOS.SYS (Bunlar çekirdek veya işletim sisteminin çekirdek kodunu içerir)
* CONFIG.SYS (Bunlar çeşitli yapılandırma seçeneklerini içerir)
* KEYBOARD.SYS (Bunlar klavye düzeni ile ilgili bilgileri içerir)
* COUNTRY.SYS (Bunlar ülke ve kod sayfası ile ilgili bilgileri içerir)

## SYS Dosya Biçimi ##

Microsoft, dosyaları .sys uzantılı olarak geliştirmiştir. Değişkenler ve işlevler SYS dosyalarına dahildir. Bunlar çoğunlukla Microsoft işletim sistemi tarafından kullanılır. Bu dosyalar esas olarak diskin kök dizininde bulunur:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

SYS dosyalarıyla ilgili bazı yaygın uyarılar aşağıdaki gibidir:

* Bu dosyalar işletim sisteminin temel işlevlerinden ve değişkenlerinden sorumlu olduklarından bu dosyaların adları değiştirilmemelidir.
* Bu dosyaların olmaması hatalara neden olabileceğinden bu dosyalar silinmemelidir.
* .sys dosyaları, kaynağın doğruluğundan emin olana kadar internetten indirilmemelidir.
* Bu dosyaların değiştirilmesi veya karıştırılması ciddi sistem hatalarına yol açacağından bu dosyaları kurcalamamak gerekir.
* Bu dosyalar bazı virüsler veya kötü amaçlı yazılımlar tarafından bozulursa yeniden kurulmaları gerekir

## SYS Örneği ##

Aşağıda basit bir SYS sistem yapılandırma dosyası örneği verilmiştir:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
