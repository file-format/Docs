{
  "date" : "2021-04-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ISO - Disk Görüntüsü Dosya Biçimi",
  "description":"ISO dosyası ve ISO dosyalarını oluşturabilen ve açabilen API'ler nedir?",
  "linktitle" : "ISO",
  "menu" : {
    "docs" : {
     "identifier": "compression-iso",
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## ISO dosyası nedir?

.iso uzantılı bir dosya, CD veya DVD gibi bir optik diskteki tüm verilerin içeriğini temsil eden sıkıştırılmamış bir arşiv disk görüntü dosyasıdır. [ISO-9660](https://www.iso.org/standard/17505.html) standardına dayalı olarak, ISO görüntü dosyası formatı, içinde saklanan dosya sistemi bilgileriyle birlikte disk verilerini içerir. ISO dosyalarının içeriğin tam bir kopyasını içerme yeteneği, onu CD/DVD'lerin kopyalarını oluşturmak için mükemmel bir dosya türü yapar ve çoğunlukla kurulum için önyüklenebilir verileri depolamak için kullanılır. Çoğu zaman ISO dosyaları, kurulum için makineyi başlatmak üzere önyüklenebilir içerik olarak USB/CD/DVD'ye yazılır. ISO dosyalarında MIME tipi application/x-iso9660-image bulunur.

## ISO Dosya Biçimi

ISO dosya formatı, belirtilen veri içeriklerini arşivlese de diğer kapsayıcı dosya formatları gibi değildir. Arşiv, içeriğin tam yapısına ve dosya sistemi bilgilerine sahip bir ikili dosya olarak oluşturulur. ISO dosya formatı [ISO-9660](https://en.wikipedia.org/wiki/ISO_9660) tarafından aşağıdaki şekilde açıklanmıştır.

### ISO Dosyasının Üst Düzey Yapısı

Dosyanın genel yapısı şunlardan oluşur:

* "Sistem Alanı" - 32.768 bayt ve ISO_9660 tarafından kullanılmıyor
* `Veri Alanı` - Birim tanımlayıcı seti ve Yol tabloları, dizinler ve dosyalardan oluşur

### Hacim Tanımlayıcı Seti

Veri alanı, bir hacim tanımlayıcı seti sonlandırıcı ile sonlanan bir veya daha fazla hacim tanımlayıcı seti olan hacim tanımlayıcı seti ile başlar. Bunlar toplu olarak veri alanı için bir başlık görevi görür ve içeriğini tanımlar (FAT, HPFS ve NTFS biçimli diskler tarafından kullanılan BIOS parametre bloğuna benzer).

Bir hacim tanımlayıcı seti aşağıda gösterildiği gibidir.

|Hacim Tanımlayıcı Seti|
---|
|Hacim tanımlayıcısı #1|
|...|
|Hacim tanımlayıcısı #N|
|Hacim tanımlayıcı küme sonlandırıcı|

#### Cilt Tanımlayıcı

Her cilt tanımlayıcısı 2048 bayt boyutundadır ve aşağıdaki yapıya sahiptir:

|Parça |Tür |Tanımlayıcı |Sürüm |Veri|
---|---|---|---|---|
|Boyut |1 bayt |5 bayt (her zaman 'CD001') |1 bayt (her zaman 0x01) |2.041 bayt|

## Referanslar

* [Optik Disk Görüntüsü - Wikipedia](https://en.wikipedia.org/wiki/Optical_disc_image)
* [Dosya İmzaları](https://www.garykessler.net/library/file_sigs.html)
* [ISO 9660 - Wikipedia](https://en.wikipedia.org/wiki/ISO_9660)

