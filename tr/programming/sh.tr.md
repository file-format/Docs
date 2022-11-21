{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Bash Shell Komut Dosyası",
  "description":"SH dosya formatı ve SH dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## .sh dosyası nedir?

.sh uzantılı bir dosya, Unix kabuğu tarafından çalıştırılacak bilgisayar programını içeren bir betik dili komut dosyasıdır. Dosya işleme, programların yürütülmesi ve benzeri diğer görevler gibi işlemleri gerçekleştirmek için sırayla çalışan bir dizi komut içerebilir. Bunlar, kullanıcı tarafından komut satırı arayüzünden veya aynı anda birden fazla işlemi gerçekleştirmek için toplu olarak yürütülür. Komut dosyası dosyaları Notepad, Notepad++, Vim, Apple Terminal gibi metin editörlerinde ve Windows, MacOS ve Linux OS'deki diğer benzer uygulamalarda açılabilir.

## SH Dosya Biçimi

SH dosyaları, tanımlanan sözdizimine göre düz metin olarak yazılır. Bu betik dosyaları şunları destekler:

* `Yorumlar` - Yorumlar # ile başlar ve kabuk tarafından dikkate alınmaz.
* `Kısayollar` - Bunlar, kısa ve kolay yürütme için bir komutu yeniden adlandırmak için kullanılabilir.
* `Toplu İşler` - Aksi takdirde manuel olarak girilmesi gereken çeşitli komutlar otomatik olarak yürütülebilir. Bu, bir kullanıcının dizinin her aşamasını tetiklemesini bekleme ihtiyacını ortadan kaldırır.
* `Genelleme` - Basit döngüler kullanılarak, görüntülerin bir kaynaktan diğerine dönüştürülmesi gibi işlemler için çok daha fazla genelleme elde edilir.

## SH dosyası örneği

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## SH dosyası nasıl çalıştırılır?
SH dosyaları genellikle Linux'ta çalışır, Windows'ta bile sh dosyalarını çalıştırmak için Putty gibi yazılımları kullanarak bir Linux terminaline bağlanmanız gerekir. Bir Linux terminalinde bir SH dosyasını çalıştırma adımları aşağıdadır.

1. Linux terminalini açın ve SH dosyasının bulunduğu dizine gidin.
2. "chmod" komutunu kullanarak betiğinizde çalıştırma iznini ayarlayın (henüz ayarlanmamışsa).
3. Aşağıdakilerden birini kullanarak betiği çalıştırın
1. `./filename.sh`
2. `sh dosyaadı.sh`
3. "bash betiği-adı-here.sh"

## Referanslar

* [Yeni Başlayanlar İçin BashScript Oluşturma](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Kabuk yazısı](https://www.shellscript.sh/)

