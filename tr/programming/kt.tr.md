---
date: 2019-10-11
keywords: kt, .kt, kotlin dosya formatı, kotlin dosyaları nasıl açılır, kotlin dosyaları nasıl çalıştırılır, .kt dosya formatı, kt dosyası , kotlin dosya uzantısı, .kt uzantısı, kotlin vs java
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: KT Dosya Biçimi
linktitle: KT
description: "KT dosya formatı ve KT dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-20
---

## .KT dosyası nedir? ##

Kotlin'de yazılmış bir kaynak kodu, genellikle **Kotlin dosya uzantısı** olarak bilinen .kt uzantısıyla kaydedilir. Kotlin, JetBrains tarafından [Java](/tr/programming/java/) ile tamamen birlikte çalışabilecek şekilde geliştirilmiş genel amaçlı bir çapraz platform programlama dilidir. Kotlin ticari markası, Kotlin Vakfı tarafından korunmaktadır.

Kotlin, 7 Mayıs 2019'da Google tarafından Android Uygulama geliştirme için tercih edilen programlama dili olarak ilan edildi. Android Studio 3.0, Ekim 2017'de Android Uygulama geliştirme için bir alternatif olarak Kotlin'i desteklemeye başladı.

## Kotlin KT Dosya Formatının Kısa Tarihi##

Kotlin, JetBrains tarafından Temmuz 2011'de JVM için yeni bir programlama dili olarak tanıtıldı. JetBrains lideri Dmitry Jemerov, Scala dışında çoğu dilin aradıkları özelliklerin eksik olduğunu ancak Scala'nın yavaş derlenmesinin bir dezavantaj olduğunu söyledi. Kotlin'in ana hedeflerinden biri Java kadar hızlı derlemekti. Kotlin projesi, Şubat 2012'de Apache 2 Lisansı altında açık kaynaklı hale getirildi.

Kotlin'in 1.0 sürümü 15 Şubat 2015'te yayınlandı. Android, Google I/O 2017'de Android'de birinci sınıf Kotlin desteğini duyurdu. Kotlin 1.2, JVM ve JavaScript platformları arasında kod paylaşma özelliğiyle 28 Kasım 2017'de yayınlandı. Kotlin 1.3, asenkron programlama desteği ile 29 Ekim 2018'de yayınlandı. Google, 7 Mayıs 2019'da Kotlin'in Android Uygulama geliştirme için tercih edilen programlama dili olduğunu duyurdu. Kotlin 1.4, Swift/Objective-C ile birlikte çalışabilirliği desteklemek için bazı küçük değişikliklerle Ağustos 2020'de piyasaya sürüldü.

## Kotlin Sözdizimi ##

Kotlin, Java'dan daha iyi olacak şekilde tasarlanmıştır, ancak yine de Java'dan Kotlin'e kademeli geçişe izin vermek için Java koduyla birlikte çalışabilir.

* Kotlin'de noktalı virgül isteğe bağlıdır. İfadenin sonunu belirtmek için yeni bir satır yeterlidir.
* Kotlin, *val* anahtar sözcüğüyle tanımlanan salt okunur ve *var* anahtar sözcüğüyle tanımlanan değişken olmak üzere iki tür değişkeni destekler.
* Sınıflar varsayılan olarak özel ve kesindir. Bir sınıftan türetmek için, temel sınıfın *open* anahtar sözcüğü ile bildirilmesi gerekir.
* Kotlin prosedürel programlamayı da destekler.
* Kotlin programına giriş noktası Java, C# vb. benzer "main" fonksiyondur.

### Sözdizimi Örneği ###

Aşağıda Kotlin sözdizimi örneği verilmiştir.

```kotlin
// The example code prints Hello World from Kotlin to the console.
    fun main() {
      val audience = "World"
      println("Hello, $audience!")
}
```

Yukarıdaki kodda **fun** anahtar sözcüğü main adlı işlevi tanımlar. İşlevin içinde, salt okunur bir 'kitle' değişkeni **val** anahtar sözcüğüyle bildirilir. **println** yöntemi kullanılarak konsolda "Kotlin'den Merhaba Dünya" yazdırılır. Seyirci değişkeninin değeri, **$** işaretiyle dizeye eklenir.

## Kotlin ve Java
Kotlin, birçok gelişmiş özellik sunan Android uygulamaları yazmak için resmi bir dildir, ancak birçok uzman Java geliştiricisi hala Kotlin'e geçmek için ilgi göstermemektedir. Sadece Java ile her şeyi yapabileceklerini düşünüyorlar. Java geliştiricilerini geçiş yapmaya ikna edebilecek iki teknoloji arasındaki karşılaştırma aşağıdadır:

| Parametre | Java | Kotlin |
|--------------------|----------|---------------- -|
| Tekil Nesneler | √ | √ |
| Joker Karakter Türleri | √ | Χ |
| Derleme | Bayt kodları | Sanal Makine |
| Lambda İfadesi | Χ | √ |
| Değişmeyen Dizi | Χ | √ |
| Özel Olmayan Alanlar | √ | Χ |
| Akıllı Yayınlar | Χ | √ |
| Boş Güvenlik | Χ | √ |
| Statik Üyeler | √ | Χ |

## Referanslar ##

- [Kotlin (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Kotlin_(programming_language))

