{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "dosya", "uzantı", "biçim", "Perl", "Perl dili", "PL dosyaları", "programlama"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"PL dosyaları oluşturabilen ve açabilen PL dosya formatı ve API'ler hakkında bilgi edinin.",
  "title" :"PL Dosyası - Perl Komut Dosyası Dosya Biçimi",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## PL dosyası nedir?

.pl uzantılı bir dosya, betik dili olan bir Perl Betik dosyasıdır. Bunlar Perl Interpreter yazılımı kullanılarak derlenir ve çalıştırılır. Bir PL betik dosyası kod satırları, değişkenler ve yorumlar içerir. Komut dosyası dilleri nispeten zordur
[PHP](/tr/programming/php/) gibi diğer programlama dosyası formatlarını anlayın. PL dosyaları oluşturulabilir ve Windows, macOS ve Linux ile uyumludur.

## Perl Betik Dilinin Kısa Tarihi

Bu dil ilk olarak 1987'de kullanılmaya başlandı, bu nedenle bu dosyalar o yıl ortaya çıktı. 1989'da Perl 2 piyasaya sürüldü. Daha sonra güncellenerek 5.35 versiyonuna kadar modifiye edilmiş olup bir sonraki versiyonun seneye çıkması hedeflenmektedir.

Her güncellemede, dilin ve dosyaların işlevselliği, performansı ve görünümü ile ilgili araçlar eklenmiştir. Bu yıllarda sürümler hakkında birçok revizyon yapılmıştır. Başlangıçta temel bir betik diliydi, ancak şimdi birçok başka modülü de içeriyor. Başlangıçta çok basit bir dildi, ancak bu dilin yazıları kompakt oldukları için anlaşılması oldukça zordu.

## Perl Dosya Biçimi Uzantısı Özellikleri

Bu programlama dosyalarının bazı özellikleri veya spesifikasyonları vardır, bunlardan bazıları aşağıdaki gibidir:

* Bu dosyalarda bulunan kodlar düz metin biçimindedir ve komut dosyası geliştirme amacıyla kullanılmaktadır.
* Sunucu komut dosyası oluşturma, metnin ayrıştırılması ve sunucu yönetimi, bu dilin komut dosyasının kapsadığı ana unsurlardır.
* Bu dille ilişkili birçok popüler program, Active state Active Perl ve Bare Bones BBEdit'tir (Mac OS ile uyumlu)
* Bu dil üst düzey bir dil olarak kabul edilir
* Win32 için, kullanıcının dilin yerel ikili dağıtımını kurması gerekebilir
* Çeşitli Windows Kaynak Kitlerinde çalıştırılabilir hale gelmek için bazı komut dosyası araçları gerektirir
* Visual Studio .NET, programlama dillerinin geliştirilmesi için ünlü bir çerçevedir. Visual Perl olarak bilinen Aktif Durum aracı, Perl'i Visual Studio'ya eklemek için kullanılır.
* Dosyalarda kaynak kodun ilk satırı kullanılan tercümanın bilgilerini anlatır. PL dosyaları genellikle **#!/usr/bin/Perl** satırıyla başlar ve bilgisayarınıza bu betiği bilgisayarda kurulu bir Perl yorumlayıcısı kullanarak çalıştırmasını söyler.


## PL Komut Dosyası Örnekleri

```
#!/usr/bin/perl
print "Hello, world\n";
```

Bu yazdırılacak

```
Hello, World
```

### Tek satırlık yorum ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Çok satırlı yorum ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Değişken atama ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Skaler değişken ataması ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Basit skaler işlemler ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referanslar ##

- [Python (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

