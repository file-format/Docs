{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","jar dosyası nedir","jar dosyası nasıl açılır", "uzantı", "dosya", "jar dosyası","jar dosya formatı", ".jar uzantısı "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Java Arşiv Dosya Biçimi",
  "description":"JAR dosyası formatı ve JAR dosyası oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## JAR dosyası nedir?

.jar uzantılı bir dosya, uygulama ile ilgili birçok farklı dosyayı tek bir dosya olarak içeren bir Java Arşiv dosyasıdır. Bu dosya biçimi, birden çok HTTP bağlantısı oluşturmaktan kaçınarak, indirilen bir Java Applet'in HTTP işlemi yoluyla tarayıcıya yüklenme hızını azaltmak için oluşturulmuştur. Tek bir JAR dosyası, Java sınıf dosyalarını ([.class](/tr/programming/class/)) [resimler](/tr/image/) ve [sesler](/tr/audio/) içerebilir. Bir JAR dosyası içindeki ayrı öğeler, uygulama geliştiricisi tarafından kökenlerini doğrulamak için dijital olarak imzalanabilir. JAR dosyaları, bu API ile ilgili belirli işlevleri içeren işlevsel API'ler oluşturmak için düzenli olarak kullanılır.

## JAR Dosya Biçimi

JAR dosyaları, kendi içerik dosyalarını tek bir dosyada arşivleyen popüler [ZIP dosya formatına](/tr/compression/zip/) dayalıdır. JAR dosya formatı sıkıştırmaları destekler, bu da indirme için daha küçük bir dosya boyutuyla sonuçlanır ve dolayısıyla indirme süresini daha da artırır. Oracle'ın [JAR dosyası özellikleri](https://docs.Oracle.com/javase/8/docs/technotes/guides/jar/jar.html) makalesi, JAR dosyalarının dahili özellikleri hakkında eksiksiz ayrıntılar verir.

### Manifest Dosyası

Bir JAR dosyası oluşturulduğunda, JAR dosyasının içeriğiyle ilgili meta veri bilgilerini içeren bir bildirim dosyası otomatik olarak dosyanın içinde oluşturulur. Bu dosya, JAR dosyası içinde paketlenmiş içeriği gösterir. Tipik bir Manifest dosyası, JAR dosyasında bulunan klasörleri ve sınıfları gösteren aşağıdaki gibi görünür.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest Spesifikasyonları

Manifest belirtimleri Oracle tarafından aşağıdaki gibi tanımlanır.

`manifest-file`: ana bölüm yeni satır \*bireysel-bölüm

"ana bölüm": sürüm bilgisi yeni satır \*main-attribute

"sürüm bilgisi": Bildirim Sürümü: sürüm numarası

`sürüm numarası` : digit+{.digit+}*

`main-attribute`: (herhangi bir meşru ana özellik) yeni satır

"bireysel bölüm": Ad : değer yeni satır \*perentry-attribute

`perentry-attribute`: (herhangi bir meşru perentry özelliği) yeni satır

"yeni satır": CR LF | LF | CR (ardından LF gelmez)

`digit`: {0-9}

### Yürütülebilir JAR

JAR dosyaları, Microsoft Windows İşletim Sistemindeki diğer herhangi bir uygulamaya benzer şekilde Java Virtual Machine (JVM) tarafından yürütülebilen bir uygulamadan da oluşabilir. Bu durumda, JVM'nin, uygulamanın giriş noktası olan, genel statik geçersiz ana yöntemi olan herhangi bir sınıf hakkında bilgi sahibi olması gerekir. Manifest dosyası, "Ana Sınıf" başlığına sahip böyle bir sınıfı aşağıdaki biçimde tanımlar:

```
Main-Class: com.example.MyClassName
```



## Referanslar

* [JAR Dosyasına Genel Bakış](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [JAR Dosya Biçimi](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Bunlar,jar%20file%20uzantısı üzerinde%20%20oluşturulmuşlardır%20%20.)

