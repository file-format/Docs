{
  "date" : "2021-06-29",
  "keywords" :[ "CFG", "uzantı", "dosya", "biçim", "sistem", "konfigürasyon", "ayarlar", "programlar", "bilgisayar", "uygulama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CFG - Dosya Biçimi",
  "description":"CFG dosya formatı ve CFG dosyaları oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "CFG",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## .cfg dosyası nedir? ##

.cfg uzantılı bir dosya, bir tür "ayarlar" dosyasıdır. Yaygın olarak kullanılan bir dosya türüdür ve bilgisayar programları için yapılandırma ve ayarlarla ilgili bilgileri depolamak için kullanılır. Çoğu CFG dosyası türü metin biçiminde saklanır ve manuel olarak açılmamalı, bunun yerine bir metin düzenleyici kullanılarak açılmalıdır. Ancak, bilgilerin saklanma biçimine göre farklılık gösteren farklı CFG dosyası türleri vardır. CFG dosyalarının sunduğu özellikler uygulamadan uygulamaya değişir. Bazı bilgisayar uygulamaları, kullanıcıların yapılandırma dosyalarının sözdizimini grafik müdahaleler kullanarak değiştirmesine veya geliştirmesine olanak tanırken, diğerleri yalnızca bir metin düzenleyici kullanarak değişikliklere izin verir. Bu dosyaları değiştirdikten sonra, kullanıcılar uygulamaya bu dosyaları tekrar okuması ve değişiklikleri sisteme uygulaması talimatını verebilir.


## CFG Dosya Biçimi ##

CFG dosyaları, Unix ve Unix benzeri işletim sistemleri, MS-DOS, macOS, Microsoft Windows ve IBM OS/2 gibi çeşitli işletim sistemleri tarafından desteklenir. Bu dosyaların saklandığı ve bu işletim sistemlerinin her birinde kullanıldığı biçim değişiklik gösterir. Çoğu sistem bu dosyaları insanlar tarafından okunabilir ve düzenlenebilir bir düz metin biçiminde kullanır ve depolar, diğerleri ise dosyaların kullanımına ve işletim sisteminin gereksinimlerine bağlı olarak daha karmaşık bir biçimde depolar.

Unix ve Unix benzeri işletim sistemlerinde, çoğu CFG dosyası, CFG dosyaları için birkaç farklı biçim stili kullanılır, ancak en yaygın biçim, kolayca okunabilen bir düz metin biçimidir ve hemen hemen tüm biçimler, yorumların yapılmasına ve düzenlenmesine izin verir. Bu işletim sistemlerinde CFG dosyaları için en yaygın dosya uzantıları CNF, CONF, CF ve INI'dir.

MS-DOS işletim sisteminde başlangıçta yalnızca bir yapılandırma dosyası formatı, yani düz metin vardı, ancak MS-DOS 6, beraberinde bir INI konfigürasyon dosyası formatını getirdi.

macOS, standart bir özellik listesi biçim stili yapılandırma dosyası kullanır.

Microsoft Windows'ta, Düz metin INI tarzı yapılandırma dosyaları, bilgileri depolamak ve düzenlemek için önemli bir kaynaktı, ancak 1993'te yeni bir veritabanı sistemi tanıtıldı ve 1993'ten sonra Microsoft Windows'ta yapılandırma dosyalarının kullanımında bir azalmaya yol açtı.


## CFG Örneği ##

Örnek bir CFG dosyası aşağıda görülebilir:

```
#########################
## Settings
##

genome_dir = ~/genome/hg18/

> reads_list1
fastq_100k_1_1.txt
fastq_100k_3_1.txt
<

> reads_list2
fastq_100k_1_2.txt
fastq_100k_3_2.txt
<

read_format = FASTQ
quality_format = phred-33
mapper = bowtie
annotations = all.gene.refFlat.txt
out_path = output
max_intron = 400000
max_multi_hit = 10

```
