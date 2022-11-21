---
date: 2019-10-11
keywords: java, .java, java dosya formatı, java dosyaları nasıl açılır, java dosyaları nasıl çalıştırılır, java dosyası, java örnek kodu
yazar:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Java Dosya Biçimi
linktitle: Java
description: "Java dosya formatı ve Java dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin."
menu:
  docs:
    parent: "programming"
lastmod: 2021-05-07
---

## Java dosyası nedir? ##
Java kaynak kodunu içeren ve .java dosya uzantısıyla kaydedilen bir dosya Java dosyası olarak bilinir. Java, oyunların, mobil, web ve masaüstü uygulamalarının geliştirilmesi için en yaygın kullanılan teknolojilerden biridir. Java platformdan bağımsız olduğu için Windows, Mac, Linux, Raspberry Pi, vb. üzerinde kusursuz çalışır. Java, C# ve C++'a çok benzer, dolayısıyla bu diller arasında geçiş yapmak daha kolaydır.

## Kısa Tarih ##

Java projesi, Haziran 1991'de James Gosling, Mike Sheridan ve Patrick Naughton tarafından başlatıldı. Java başlangıçta Oak olarak adlandırıldı. Daha sonra Green ve son olarak Java olarak yeniden adlandırıldı. James Gosling, Java'yı C/C++'a benzer bir söz dizimi ile tasarladı. Java'nın ilk genel sürümü 1996'da Sun Microsystems tarafından piyasaya sürüldü. Java'nın hızla popüler olmasına neden olan tüm popüler sistemlerde çalışabilir. Java 2'nin Aralık 1998'de piyasaya sürülmesiyle, farklı platform türleri için birden çok yapılandırma oluşturuldu. Versiyonlar şu şekildeydi

- J2EE (Java EE): Kurumsal çözümler için
- J2ME (Java ME): Mobil uygulamalar için
- J2SE (Java SE): Masaüstü uygulamaları için

19 Kasım 2006'da Java Virtual Machine (JVM), Sun tarafından ücretsiz ve açık kaynaklı bir yazılım olarak piyasaya sürüldü. Oracle Corporation, 2009–2010'da Sun Microsystems'i satın aldıktan sonra, James Gosling 2 Nisan 2010'da Oracle'dan istifa etti.

## Java kodunu çalıştırma/yürütme ##

Java kodunu çalıştırmak için önce derlenmesi gerekir. Bunun için Java SDK gereklidir. Java SDK, Java kodunu bir bytecode sınıf dosyasına derler. Java kodunu derlemek ve yürütmek için kod tamamlama ve kullanımı kolay arabirim sağlayarak Java dosyalarıyla çalışmayı kolaylaştıran Eclipse ve IntelliJ Idea gibi IDE'ler vardır.

## Java Dosya Biçimi ##

Java'nın sözdizimi, C ve C++'dan büyük ölçüde etkilenmiştir, ancak C++'dan farklı olarak, Java neredeyse yalnızca nesne yönelimli bir dil olarak oluşturulmuştur. Java'da, tüm kod sınıfların içinde yazılır ve her veri öğesi bir nesnedir. C++'ın aksine Java, operatör aşırı yüklemesini veya çoklu kalıtımı desteklemez.

### Java örnek kodu ###

Aşağıda bir Java sözdizimi örneği verilmiştir.

```java
/*
The example code prints
Hello World from Java to the console.
*/
    public class ExampleApp {
        public static void main(String[] args) {
            System.out.println("Hello World from Java"); // Prints the string to the console.
        }
    }
```
Yukarıdaki kodda, **public** anahtar sözcüğü erişim değiştiriciyi belirtir. Bu sınıfa, sınıf hiyerarşisi dışındaki sınıflar tarafından erişilebileceğini belirtir. Erişim değiştirici ayrıca **korumalı** (aynı pakette erişilebilir) veya **özel** (yöntemlere yalnızca aynı sınıf tarafından erişilebilir) olabilir. Yöntemin önündeki **statik**, yöntemin sınıfın belirli bir örneği olmadan çağrılabileceğini belirtir. **void**, yöntemin hiçbir şey döndürmeyeceğini belirtir. Dizeyi konsola yazdırmak için. System.out.println komutu kullanılır. Bu komutta *System* sınıfı, *println* yöntemini içeren *PrintStream* sınıfının bir örneği olan *out* statik alanına sahiptir.

Java dosyalarının dosya adı, sınıf adıyla aynı olmalıdır. Bu nedenle, örnek kod için Java dosyasının adı *ExampleApp.java* olacaktır.

## Referanslar ##

- [Java (programlama dili) - Wikipedia](https://en.wikipedia.org/wiki/Java_(programming_language))

