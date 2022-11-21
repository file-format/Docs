{
  "date" : "2021-07-12",
  "keywords" :[ "cmd dosyası", "cmd dosyası nedir", "dosya", "cmd örneği", "cmd dosya uzantısı","uzantı", "biçim" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"CMD dosya formatı ve CMD dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "title" :"CMD - Windows Komut Dosyası Biçimi",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## CMD dosyası nedir?
Bir CMD dosyası, çeşitli görevleri yürütmek için çalıştırılan düz metin biçiminde bir veya birden çok komut içeren bir komut dosyasından oluşur. Bu, genellikle yürütülebilir komutların bir yığınını depolamak için de kullanılan bir [BAT](/tr/executable/bat/) dosyasına benzer. CMD dosyaları, Microsoft Windows işletim sisteminde yaygın olarak kullanılmaktadır. Bu dosyalar neredeyse 90'lı yıllarda tanıtıldı, ancak hala en son Windows işletim sisteminde kullanılıyor. Bu dosyalar genellikle bir sırada birden fazla komutu yürütmek için yazılır.

## CMD dosya biçimi
CMD, CP/M tarzı çalıştırılabilir programlar tarafından kullanılan bir dosya formatıdır. Genellikle CP/M-80'deki [COM](/tr/executable/com/) ve DOS'taki [EXE](/tr/executable/exe/) ile karşılaştırılabilir. Bir CMD dosyası, 1 ila 8 kod veya veri grubu ve 128 baytlık bir başlık içerir. Her grubun boyutu en fazla 1 mb olabilir. CMD dosyaları ayrıca sonraki sürümlerinde yer değiştirme bilgilerini ve Yerleşik Sistem Uzantılarını (RSX'ler) içerebilir. CMD, [BAT](/tr/executable/bat/) dosyasına kıyasla yenidir; Windows MS-DOS'ta piyasaya sürülmeden önce MS-DOS için kullanılır. Bugün hala .bat uzantılı dosyaları kaydedebilseniz de, birçok kişi yürütülebilir komut dosyalarını kaydetmek için .cmd uzantısını kullanır.

### CMD biçimi Spesifikasyonu

Başlığın başlangıcı, türleriyle birlikte dosyada bulunan grupların listesini içerir. Her tip en fazla bir kez kullanılabilir. Bu türler:

- Kod
- Veri
- Ekstra
- Yığın
- Kullanıcı 1
- Kullanıcı 2
- Kullanıcı 3
- Kullanıcı 4
- Paylaşılan Kod

DOS'taki Program Segment Öneki gibi, veri grubunun ilk 256 baytı sıfırdır. Sıfır sayfalı CP/M-86 ile doldurulacaklar. Veri grubu yoksa, bunun yerine kod grubunun ilk 256 baytı kullanılacaktır.
## CMD dosyası örneği
Aşağıda, sistem bilgilerini göstermek için bir CMD betiği örneği verilmiştir.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referanslar

* [CMD Komut Dosyası Nasıl Yazılır](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [CMD dosyası (CP/M) - Wikipedia'dan](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

