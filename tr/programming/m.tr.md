{
  "date" : "2019-10-11",
  "keywords": [ "M file", "M", "extension", "format", "M file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"M - Matlab Kaynak Kod Dosyası",
  "description":"Matlab .m Kaynak Kodu dosyası ve MF dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "M",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

# M - Matlab Kaynak Kod Dosyaları

## M (Matlab) dosyası nedir?

.m uzantılı bir dosya, analiz, algoritma geliştirme ve simülasyon modelleme için kullanılan bir programlama ve sayısal hesaplama platformu olan Matlab tarafından kullanılan bir kaynak kod dosyasıdır. Diğer programlama dosyası biçimleri gibi, bir M dosyası da grafikleri çizmek, simülasyonları çalıştırmak ve diğer matematiksel işlemleri yapmak için Matlab komutlarını yürüten kaynak kodunu içerir. Tek bir Matlab simülasyonu, uygulamayı betiklerde, sınıflarda, işlevlerde veya bildirimlerde sınıflandırabilen bu tür birden çok .m dosyasına yayılabilir. Matlab M dosyaları herhangi bir metin düzenleyici ile açılabilir.

## Matlab M Dosya Biçimi - Daha Fazla Bilgi

Matlab .m dosyaları, Matlab programlama dilinde programlama kodu içeren metin dosyalarıdır. Bunlar herhangi bir metin düzenleyicide açılıp düzenlenebilir ve Matlab yazılımında yürütülmek üzere tekrar kaydedilebilir. Matlab'ın kendisi, kod, çıktı ve biçimlendirilmiş metnin birleşimi olan betikler oluşturmak için kullanılan bir Canlı Düzenleyici içerir.

### Matlab Fonksiyon Dosyaları

Diğer programlama dilleri gibi, yalnızca belirli bir görevi gerçekleştiren bir işlevin tanımını içeren bir .m dosyası oluşturabilirsiniz. Bu tür dosyalar da .m uzantısıyla kaydedilir ve yalnızca o işlevle ilgili işlevselliği uygular.

### .M Dosya Örneği

Aşağıda, h yüksekliğinden bırakılan bir nesne için geçen süreyi hesaplayan bir Matlab işlev dosyası örneği verilmiştir.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Bu fonksiyonu Matlab editöründen veya başka bir .m dosyasından çağırmak için aşağıdaki kod kullanılabilir.
```C++
TimeToGround(100)
```

## Referanslar

* [Matlab - Desteklenen Dosya Biçimleri](https://www.mathworks.com/help/matlab/standard-file-formats.html)
* [Matlab kullanarak](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C Uygulama Dosyası

## M (Objective-C) dosyası nedir?

Bir M dosyası, OS X ve iOS için yazılım uygulamaları yazmak için kullanılan bir programlama dili olan Objective-C dilinde yazılmış bir sınıfın kaynak kodunu içeren uygulama dosyası olarak da adlandırılır. Objective-C, Apple'ın ana API'leri Cocoa ve Cocoa Touch tarafından bu platformlar için kullanılan ana programlama dilidir. Bu dilde geliştirilen tek bir yazılım uygulaması, program sınıflarının uygulanmasını içeren birden çok .m dosyası içerebilir. Bunlar, Apple XCode, jEdit ve diğer yaygın metin editörleri kullanılarak açılabilir.

## Objective-C M Dosya Biçimi - Daha Fazla Bilgi

M dosyaları, Objective-C'nin programlama söz dizimi kullanılarak düz metin biçiminde yazılır. Bir sınıfın her yöntemi, bu uygulama dosyalarında gerekli tüm kodlarıyla tanımlanmalıdır. Bu uygulama M dosyaları, gereksinimlere göre bir veya daha fazla .h başlık dosyasını içe aktarabilir. import deyimi, derleyiciye bu uygulama dosyasına ait olan başlık dosyasını nerede bulacağını söyler. import ifadesi aşağıdaki gibi yazılır.

```C++
#import "network.h"
```

Her M dosyası uygulaması daha sonra `@implementation` yönergesiyle başlar ve ardından uygulama sınıfı dosya adı gelir. Bunu daha sonra başlık dosyasında bildirilen tüm yöntem uygulamaları izler.

### M Dosya Biçimi Örneği

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## Referanslar
* [Amaç C Hakkında](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
* [Object-C Kılavuzu](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

