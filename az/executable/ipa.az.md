{
  "date": "2021-08-30",
  "keywords": [
"ipa faylı",
"ipa fayl formatı",
"ipa faylı nədir",
"fayl",
"ipa nümunəsi",
"ipa fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "IPA fayl formatı və IPA faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "IPA - iOS Tətbiq Paketi Faylı",
  "linktitle": "IPA",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ip-aza"
}
},
  "lastmod": "2021-08-30"
}

## IPA faylı nədir?
.ipa uzantılı fayl iOS-a aiddir və proqram paketi faylı kimi tanınır. Bu, iOS tətbiqini saxlayan arxivdir ([ZIP](/compression/zip/) sıxılma ilə sıxılmışdır), lakin həmin proqram yalnız iPad, iPhone və ya iPod Touch kimi iOS və ya ARM əsaslı MacOS cihazlarında quraşdırıla bilər. Əsasən, iTunes, Apple Configurator 2 və ya hər hansı üçüncü tərəf proqramları IPA fayllarını quraşdırmaq üçün istifadə edilə bilər.

## IPA fayl formatı
Apple Xcode istifadə edərək tətbiqləri inkişaf etdirən IOS tərtibatçıları IPA faylları ilə yaxşı tanışdırlar, çünki onlar hazırlanmış tətbiqləri ya tətbiq mağazasının yerləşdirilməsi məqsədləri üçün sınaqdan keçirmək üçün IPA faylları kimi paketləməlidirlər. Baxmayaraq ki, IPA faylları iOS tətbiqləri kimi quraşdırılmışdır, lakin siz həmçinin proqram məlumatlarına baxmaq üçün onları aça bilərsiniz. IPA faylı mobil telefonların ARM arxitekturası üçün yalnız bir binar ehtiva etdiyinə və x86 arxitekturası üçün binar olmadığına görə, bir çox .ipa faylları iPhone Simulyatorunda quraşdırıla bilməz.
### .ipa faylının strukturu
Aşağıdakı nümunə IPA-nın strukturunu göstərir:

```
/Payload/
/Payload/Application.app/
/iTunesArtwork
/iTunesArtwork@2x
/iTunesMetadata.plist
/WatchKitSupport/WK
/META-INF
```
Yuxarıda iTunes və App Store-un tanıması üçün daxili strukturdur. Bu quruluşa görə:
- Payload kataloqu bütün proqram məlumatlarını ehtiva edir.
- iTunes Artwork faylı 512×512 piksel ölçülü PNG şəklidir, içərisində iTunes-da və iPad-də App Store proqramında göstərmək üçün proqramın simvolu var.
- iTunesMetadata.plist-də tərtibatçının adı və ID-si, müəllif hüququ məlumatı, paket identifikatoru, proqramın adı, janr, buraxılış tarixi, satınalma tarixi və s. kimi müxtəlif məlumatlar var.
- META-INF qovluğunda yalnız IPA yaratmaq üçün hansı proqramdan istifadə edildiyi barədə metadata var.


## İstinadlar 

* [.ipa - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/.ipa)



