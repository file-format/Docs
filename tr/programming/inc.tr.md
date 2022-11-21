{
  "date" : "2022-07-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INC Dosya Uzantısı - INC dosyası nedir?",
  "description":"INC Include dosya formatı ve INC dosyalarını oluşturabilen ve açabilen API'ler hakkında bilgi edinin.",
  "linktitle" : "INC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-07-14"
}

## .inc dosyası nedir?

Bir INC dosyası, yazılım programının kaynak kodu tarafından başlık bilgilerine başvurmak için kullanılan bir içerme dosyasıdır. [.h dosya biçimine](/tr/programming/h/) benzer ve C++ gibi kaynak kod dosyaları tarafından yeniden kullanılabilen bildirimler, işlevler, başlıklar veya makrolar içerir. INC dosyaları, C, [C++](/tr/programming/cpp/), Pascal, [PHP](/tr/programming/php/) ve [Java](/tr/programming/java/) gibi çeşitli programlama dilleri tarafından kullanılır. INC dosyalarını açmak için Microsoft Notepad, Notepad++ ve TextEdit gibi metin editörleri kullanılabilir.

## INC Dosya Biçimi - Daha Fazla Bilgi

Bir INC dosyası, beyan sözdizimine göre dahil edilen tüm beyannamelerle birlikte düz metin dosyası olarak kaydedilir. Bir INC dosyası, diğer INC dosyalarına da başvurabilir. INC dosyası oluşturulduktan sonra projenin bir parçası haline gelir ve C++ gibi kaynak dosyalardan başvurulabilir. Herhangi bir yinelemeyi önlemek için birden fazla kaynak dosya tarafından referans alınabilir.

## INC Dosya İçeriği

INC dosyaları aşağıdaki bilgileri içerebilir.

**`Değişkenler`** - Nesne Yönelimli Programlama (OOP) durumunda, bir sınıf başlık dosyası, uygulama kaynak kodu dosyalarından erişilebilen tüm sınıf düzeyindeki değişkenlerin tanımlarını içerir

**`Metot Bildirimi`** - Tüm yöntem bildirimleri, birden çok uygulama dosyasında erişilebilmesi için .h başlık dosyalarına dahil edilmiştir.

**`Satır İçi Olmayan İşlev Tanımları`** - Başlık dosyaları, satır içi olmayan yöntemlerin tanımlarını da içerebilir.

## PHP'de INC dosyasını kullanmanın dezavantajı

PHP, sunucu üzerinde çalışan ve sonuçları çağıran web sayfalarına döndüren sunucu tarafı betikleridir. Bir PHP dosyası bir INC dosyasına başvuruyorsa ve sunucu .inc dosyalarını ayrıştıracak şekilde yapılandırılmamışsa (ki bu çok yaygındır), bir kullanıcı URL dizinini ziyaret ederek .inc dosyasındaki php kaynak kodunu görüntüleyebilir. Bu nedenle, INC dosyalarını PHP'de include dosyaları olarak kullanırken dikkatli olunmalıdır.

## Referanslar

* [PHP'de INC kullanımı](https://stackoverflow.com/questions/7129842/what-is-an-inc-and-why-use-it)

