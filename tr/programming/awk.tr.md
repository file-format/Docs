{
  "date" : "2022-04-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AWK Dosya Biçimi - AWK Komut Dosyası",
  "description":"AWK dosya formatı ve AWK dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "AWK",
  "menu" : {
    "docs" : {
      "identifier" : "programming-awk",
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-03"
}

## AWK dosyası nedir?

Bir AWK dosyası, Unix ve Linux işletim sistemleriyle birlikte gelen metin işleme uygulaması **AWK** için oluşturulmuş bir komut dosyasıdır. Metin veya bir dosyanın içeriği üzerinde, metni eşleştirme, değiştirme ve yazdırma gibi eylemleri gerçekleştirmek için mantıksal talimatlar içerir. Bu, girdi dosyasından raporların ve biçimlendirilmiş metnin oluşturulmasına yardımcı olur. awk yardımcı programı çoğu linux/unix dağıtımında genellikle /usr/bin/awk konumunda bulunur.

## AWK Komut Dosyası Nasıl Oluşturulur?

Bir AWK dosyası, Linux/Unix OS üzerindeki herhangi bir metin düzenleyicide oluşturulabilir veya açılabilir. Aşağıdaki gibi yeni bir AWK betik dosyası oluşturulabilir.

```
$ vi script.awk
```

Bu, AWK dosyasını metin düzenleyicide açacaktır. Metin düzenleyicide aşağıdaki gibi bazı ifadeler girin.

```
#!/usr/bin/awk -f
BEGIN { printf "%s\n","Writing my first Awk executable script!" }
```
Bu metin içeriğinin ilk satırı aşağıdaki şekilde açıklanmaktadır.

* \#! – bir komut dosyasındaki talimatlar için bir tercüman belirten 'Shebang' olarak anılır
* /usr/bin/awk – yorumlayıcıdır
* -f – yorumlayıcı seçeneği, bir program dosyasını okumak için kullanılır

## AWK Komut Dosyası Nasıl Yürütülür?

Dosyayı kaydedin ve aşağıdaki komutu vererek betiği çalıştırılabilir yapın:
```
$ chmod +x script.awk
```

Komut dosyası daha sonra aşağıdaki gibi çalıştırılabilir.

```
$ ./script.awk
```

bu, aşağıdaki çıktıyla sonuçlanır.

```
Writing my first Awk executable script!
```

## Referans ##

* [Awk Programlama Dilini Kullanarak Komut Dosyaları Yazın](https://www.tecmint.com/write-shell-scripts-in-awk-programming/)

