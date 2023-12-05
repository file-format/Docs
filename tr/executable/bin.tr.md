{
"tarih":"2023-07-20",
   "keywords":[
"ÇÖP KUTUSU",
"BIN Dosyası",
"dosya",
"BIN dosya uzantısı",
"eklenti",
"dosya"
],
   "author":{
"display_name":"Shakeel Faiz"
},
"draft":"false",
"toc":true,
"title":"BIN Dosya Formatı - Unix Çalıştırılabilir Dosyası",
   "description":"BIN dosyalarını oluşturabilen ve açabilen BIN formatı ve API'ler hakkında bilgi edinin.",
"linktitle" : "BIN",
   "menu":{
      "docs":{
         "identifier":"executable-bin",
         "parent":"executable"
}
},
"lastmod":"2023-07-20"
}

## BIN dosyası nedir?

BIN dosyası, Linux veya FreeBSD gibi Unix tabanlı işletim sistemlerinde çalıştırılabilir bir dosyadır. Kaynak kodundan türetilen ikili koddan oluşan derlenmiş bir programı barındırır ve bu da onu temeldeki sistem mimarisiyle uyumlu hale getirir. Unix Yürütülebilir BIN dosyaları, yürütülebilir formatlar olarak rolleri açısından Windows .EXE dosyaları ve macOS .APP dosyalarıyla karşılaştırılabilir.

Unix sistemleri için yazılım geliştirme alanında, BIN dosyaları geliştiriciler tarafından programları paketlemek ve dağıtmak için yaygın olarak kullanılır. Kolay kurulum ve yürütmeye olanak tanıyarak, kullanıcılara yazılım sunmanın uygun bir yolunu sunarlar. BIN dosyalarının yanı sıra, her biri belirli donanıma veya donanıma göre uyarlanmış [.ELF](/tr/executable/elf/), .X86, [.RUN](/tr/executable/run/) ve .X86_64 dahil olmak üzere diğer yürütülebilir Unix türleri de vardır. sistem gereksinimleri.

Bir BIN dosyasının iç yapısı söz konusu olduğunda, Unix işletim sisteminin ekteki programı tanımlamak, okumak ve yürütmek için kullandığı kodlanmış verilerden oluşur. Sistem, BIN dosyasını yürütülebilir bir dosya olarak tanımak için belirli dosya imzalarına veya başlıklarına ve ardından içerdiği ikili talimatların yorumlanmasına ve yürütülmesine dayanır.

BIN dosyaları genellikle, programın nasıl düzgün şekilde kurulacağı ve ayarlanacağı hakkında ayrıntılı talimatlar sağlayan **INSTALL.TXT** dosyasıyla birlikte gelir. Bu belge, kullanıcıların kurulum sürecinde başarıyla ilerleyebilmelerini ve yazılımı herhangi bir sorunla karşılaşmadan kullanmaya başlayabilmelerini sağlar.

## BIN dosyası nasıl açılır?

BIN dosyaları doğrudan açılıp görüntülenecek şekilde tasarlanmamıştır. Ancak programları çalıştırabilir veya içerdikleri verileri çıkarabilirsiniz. Bir BIN dosyasının içeriğine erişmek için, BIN dosyasının adının "sample.bin" olduğunu varsayarak komut satırında şu adımları izleyin:

1. **Yürütülebilir izinlerden emin olun:**

BIN dosyasını çalıştırmadan önce, yürütülebilir dosya olarak çalıştırılabilmesi için gerekli izinlere sahip olduğundan emin olun. Şu komutu kullanın:

```
$ chmod +x sample.bin
```

Bu komut, dosyaya yürütülebilir ayrıcalıklar verir.

2. **BIN dosyasını yürütün:**

Yürütülebilir izinleri ayarladıktan sonra aşağıdaki komutu girerek BIN dosyasını çalıştırabilirsiniz:

```
$ ./sample.bin
```

**Uyarı**

_İndirilen veya e-postayla gönderilen BIN dosyalarıyla uğraşırken dikkatli olun; çünkü bunlar, siber suçlular tarafından kötü amaçlı yazılım dağıtmak için kullanılabilir. Kötü niyetli yürütülebilir saldırı riskini azaltmak için BIN dosyalarını yalnızca güvenilir kaynaklardan çalıştırın._

## Diğer BIN dosyaları

**.bin** dosya uzantısını kullanan diğer dosya türleri şunlardır.

- [BIN - MacBinary Kodlanmış Dosya](/tr/compression/bin/)
- [BIN - İkili Disk Görüntü Dosyası](/tr/disc-and-media/bin/)
- [BIN - BlackBerry BT Politika Dosyası](/tr/settings/bin/)
- [BIN - Sega Genesis Oyun ROM'u](/tr/game/bin/)
- [BIN - PSX PlayStation BIOS Görüntüsü](/tr/game/bin-pcsx/)

## Referanslar

* [Linux'ta İkili Dosyalar Nasıl Çalıştırılır](https://linuxhint.com/execute-binary-files-in-linux/)


