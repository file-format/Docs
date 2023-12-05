{
"tarih": "2023-02-02",
  "keywords": [
"uygulama dosyası",
"uygulama dosyası nedir",
"dosya",
"uygulama dosyası nasıl açılır",
"uygulama dosya uzantısı",
"eklenti"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"APP dosyalarını oluşturabilen ve açabilen APP dosya formatı ve API'ler hakkında bilgi edinin.",
"title": "APP Dosya Formatı - macOS Uygulama Paketi",
"linktitle" : "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app",
      "parent": "executable"
}
},
"sonmod": "2023-02-02"
}

## APP dosyası nedir?

MacOS'taki bir .app dosyası, yürütülebilir kod, kaynaklar ve meta veriler de dahil olmak üzere belirli bir uygulamayı çalıştırmak için gereken tüm dosyaları içeren özel bir dizin türüdür. .app uzantısı, işletim sistemine bu dizinin ayrı dosyalardan oluşan bir koleksiyon yerine tek bir birim olarak ele alınması gerektiğini ve doğrudan Finder veya Dock'tan başlatılabileceğini bildirir.

Finder, macOS'taki varsayılan dosya yöneticisi uygulamasıdır. Bilgisayarınızdaki dosyalara ve dizinlere göz atmanıza ve bunları düzenlemenize olanak tanır. Dock, sık kullanılan uygulama ve belgelere hızlı erişim sağlayan bir macOS özelliğidir. Hem Finder hem de Dock, ilgili uygulama paketini açacak olan .app dosyalarına tıklayarak uygulamaları başlatmanıza olanak tanır. Bir uygulamayı başlattığınızda, .app paketindeki yürütülebilir kod çalıştırılarak uygulama kullanıma hazır hale gelir. .app dosyası, uygulamanın dosya sistemindeki temsilidir ve kullanıcının uygulamaya erişmesi ve uygulamayı başlatması için bir yol sağlar.

MacOS sisteminde Finder'da bir .app dosyasına sağ tıklayıp "Paket İçeriğini Göster"i seçtiğinizde uygulama paketinin iç yapısını görebileceksiniz. Uygulama tarafından kullanılan kaynaklara veya dosyalara erişmek istiyorsanız ya da sorun giderme amacıyla uygulamanın içeriğini incelemek istiyorsanız bu kullanışlıdır. Bir .app dosyasının paket içeriği genellikle uygulamanın yürütülebilir kodunun yanı sıra görüntüler ve sesler gibi kaynaklara yönelik dizinleri de içerir. Bir .app dosyasının içeriğini keşfederek uygulamanın nasıl bir araya getirildiğine ve ne yaptığına ilişkin daha derin bilgiler edinebilirsiniz.

## APP dosyası nasıl açılır?

MacOS'ta bir .app dosyasını açmak için dosyayı Finder'da çift tıklamanız yeterlidir. Bu, .app paketinde bulunan uygulamayı başlatacaktır. Uygulama sisteminizde yüklüyse ve .app dosya türüyle ilişkilendirilmişse, dosyaya çift tıklandığında uygulamanın otomatik olarak başlatılması gerekir. Uygulama .app dosya türüyle ilişkili değilse, dosyayı sağ tıklayıp "Birlikte Aç"ı seçerek dosyayı açmak için uygun uygulamayı seçmeniz gerekebilir.

MacOS'ta Terminal üzerinde bir .app dosyasını "open" komutunu kullanarak açabilirsiniz. Bunu yapmak için "cd" komutunu kullanarak .app dosyasının bulunduğu dizine gidin ve ardından aşağıdaki komutu çalıştırın:

```
open <AppName>.app 
```

Neresi<AppName> başlatmak istediğiniz uygulamanın adıdır. Bu, uygulamayı Finder'da çift tıklamışsınız gibi başlatacaktır. "Aç" komutu, uygulamalar, belgeler ve dizinler de dahil olmak üzere birçok farklı dosya türünü açmak için kullanılabilen genel amaçlı bir yardımcı programdır. Bir .app dosyasında "aç" komutunu kullandığınızda, pakette yer alan uygulama başlatılır.

## Referanslar
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
