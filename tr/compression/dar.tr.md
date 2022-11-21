{
  "date" : "2021-04-08",
  "keywords" :[ "dar dosyası", "dar dosyası biçimi", "dar dosyası nedir", "dosya", "dar örneği", "dar dosya uzantısı","uzantı", "biçimi"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Disk Arşivleyici Dosya Biçimi",
  "description":"DAR dosya formatı ve DAR dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## DAR dosyası nedir?

.dar uzantılı bir dosya, DAR Disk arşivi kullanılarak oluşturulan sıkıştırılmış bir arşivdir. Tam disk veya bir dosya grubu için yedekleme/arşiv oluşturabilir. UNIX OS'deki [TAR](/tr/compression/tar/) dosya biçimini değiştirmek için oluşturulmuştur ve çok sayıda dosya için bölünmüş arşiv dosyaları olarak oluşturulabilir. DAR arşivi, arşivdeki ana dosyalara bağlı dosyaları sistemden silme seçeneğini destekler. Diferansiyel, Artımlı ve Azalan yedekleme sağlama yetenekleri, onu TAR dosyalarından üstün kılar.

## DAR Dosya Biçimi

DAR dosyaları, [gzip](/tr/compression/gz/), [bzip2](/tr/compression/bz2/), lzo, xz veya lzma gibi herhangi bir dosya başına sıkıştırmayı kullanabilen sıkıştırılmış arşivlerdir. Bir DAR dosyasının tam dosya biçimi, arşiv içeriğini sıkıştırmak için hangi tür biçimlendirmenin kullanıldığına bağlıdır. Ayrıca isteğe bağlı Blowfish, Twofish, AES, Serpent, Camellia şifrelemesine ve genel anahtar şifrelemesine ve imzasına (OpenPGP) izin verir.

### DAR Özellikleri

DAR dosya formatının bazı özellikleri aşağıdaki gibidir.

* Her türlü inode ile ilgilenir (dizin, düz dosyalar, sembolik bağlantılar, özel cihazlar, adlandırılmış kanallar, soketler, kapılar, ...)
* Sabit bağlantılı düğümlerle ilgilenir (sabit bağlantılı düz dosyalar, char cihazları, blok cihazları, sabit bağlantılı sembolik bağlantılar)
* Seyrek dosyalarla ilgilenir
* Linux dosyasının Genişletilmiş Öznitelikleri ile ilgilenir,
* Linux dosyası ACL ile ilgilenir
* Mac OS X eğe çatallarını halleder
* HFS+ dosya sisteminin Doğum Tarihi ve ext2/3/4 dosya sisteminin immutable, data-journaling, secure-deletion, no-tail-merging, undeletable, noatime öznitelikleri gibi bazı dosya sistemine özel özniteliklerle ilgilenir.
* gzip, bzip2, lzo, xz veya lzma ile dosya başına sıkıştırma (tüm arşivi sıkıştırmanın aksine). Bir kişi, dosya adı son ekine göre zaten sıkıştırılmış dosyaları sıkıştırmamayı seçebilir.
* Arşivdeki herhangi bir yerden dosyaların hızlı ayıklanması
* Arşivdeki dosyaların kataloğunu kaydederek arşiv içeriklerinin hızlı bir şekilde listelenmesi
* Canlı dosya sistemi yedeklemesi: Bir dosya yedekleme için okunurken değiştirildiğinde algılar ve belirli bir maksimum yeniden deneme sayısına kadar kaydetmeyi yeniden deneyebilir
* Her dilim için anında oluşturulan karma dosya (MD5, SHA1 veya SHA-512), elde edilen dosya, her dilimin bütünlüğünü hızlı bir şekilde kontrol edebilmek için md5sum veya sha1sum ile uyumludur.
* Dosya sisteminden bağımsız: bir sistemi farklı boyuttaki bir bölüme ve/veya farklı bir dosya sistemine sahip bir bölüme geri yüklemek için kullanılabilir[5]

## Referanslar

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Arşivleyici](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

