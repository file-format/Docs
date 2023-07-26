
{
  "date" : "2022-02-06",
  "keywords": [ ".apks file", "extension", "format","APK Set Archive", "how to open .apks file","apks file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APKS Dosyası - APK Set Arşivi",
  "description":"APKS dosyası nedir öğrenin?",
  "linktitle" : "APKS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-02-06"
}

## APKS dosyası nedir?

.apks uzantılı bir dosya, Android paketi **APK** dosyalarından oluşan bir arşiv dosyasıdır. APKS dosyasındaki her bir APK dosyası, cihazların çeşitli yönleri göz önünde bulundurularak oluşturulur. Bunlar mimari, dil, ekran yoğunluğu ve diğer cihaz özelliklerini içerir. APKS dosyaları **bundletool** tarafından oluşturulur. Android App Bundle oluşturmak ve uygulama paketini cihazlarda dağıtım için farklı APK'lara dönüştürmek için kullanılır.

## APKS Dosya Biçimi - Daha Fazla Bilgi

APKS dosyaları, [ZIP](/tr/compression/zip/) dosya biçimi kullanılarak sıkıştırılmış dosyalar olarak kaydedilir.

## APKS dosyası nasıl oluşturulur?

Android App Bundle (AAB) hazır olduğunda, Google Play Store'daki davranışı bir cihaza dağıtım için test edilebilir. APKS dosyaları bu amaçla AAB dosyalarından oluşturulabilir ve Google'ın Android [bundletool](https://developer.android.com/tools/bundletool) kullanılarak test cihazlarına yüklenebilir. Aşağıdaki komutu kullanarak APK'lardan APKS arşiv dosyası oluşturmak için komut satırı araçları sağlar.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
```

APK'ları bir cihaza dağıtmak için, APKS dosyası cihaz imzalama bilgileriyle aşağıdaki gibi imzalanabilir.

```
bundletool build-apks --bundle=/MyApp/my_app.aab --output=/MyApp/my_app.apks
--ks=/MyApp/keystore.jks
--ks-pass=file:/MyApp/keystore.pwd
--ks-key-alias=MyKeyAlias
--key-pass=file:/MyApp/key.pwd
```

## Referanslar

* [paket aracı - komut satırı](https://developer.android.com/tools/bundletool)

