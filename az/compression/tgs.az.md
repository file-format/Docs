{
  "date": "2019-10-11",
  "keywords": [
"tgs faylı",
"tgs fayl formatı",
"tgs faylı nədir",
"fayl",
"tgs nümunəsi",
"tgs fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TGS - Telegram Animated Sticker File Format",
  "description": "TGS fayl formatı və TGS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "TGS",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-tg-azs"
}
},
  "lastmod": "2021-04-02"
}

## TGS faylı nədir?

.tgs genişləndirilməsi olan fayl [Telegram](https://core.telegram.org/stickers#animated-stickers) platformalararası mesajlaşma xidməti tərəfindən təqdim edilmiş animasiyalı stiker faylıdır. Animasiyalı stikerlər mesajlaşma proqramları istifadəçiləri tərəfindən sabit şəkillər olan statik qrafiklərdən fərqli olaraq mesajlarda daha təkmil və canlı məzmun göndərmək üçün istifadə olunur. Telegram ilkin olaraq şəkil stikerləri üçün [WEBP](/image/webp/) fayl formatından istifadə edirdi. TGS fayl formatı statik WEBP stikerləri ilə müqayisədə animasiya məlumatlarını daha yüksək qətnamələrdə və daha kiçik fayl ölçüsündə saxlaya bilər. TGS faylları Telegram, 7-zip, Apple Archive Utility və Corel WinZip kimi proqramlardan istifadə etməklə açıla bilər.

## TGS fayl formatı

Telegram Lottie kitabxanası əsasında 2019-cu ilin iyul ayında TGS fayl formatını təqdim etdi. TGS faylı Adobe After Effects proqramında animasiyadan ixrac edilən [JSON](/web/json/) mətndən ibarətdir. Eksport edilmiş JSON mətni faylın ölçüsünü azaldan gzip sıxılması ilə sıxılır. Mətn faylı haqqında JSON məlumatı yüksək sıxılma sürətlərinin əsasını təşkil edən mətn faylında saxlanılır.

### TGS Stickers Spesifikasiyaları

TGS fayl formatı TGS animasiya etiketlərinin yaradılmasına müəyyən məhdudiyyətlər qoyur. TGS animasiya faylı:

 * Stiker/kətanın ölçüsü 512x512 piksel olmalıdır.
 * Etiket obyektləri kətanı tərk etməməlidir.
 * Animasiya uzunluğu 3 saniyədən çox olmamalıdır.
 * Bütün animasiyalar dövrəyə salınmalıdır.
 * Bodymovin-də göstərildikdən sonra stiker ölçüsü 64 KB-dan çox olmamalıdır.
 * Bütün animasiyalar saniyədə 60 kadr sürətlə işləməlidir.

### Nümunə TGS JSON Mətni

Nümunə animasiya stikeri açıldıqda aşağıdakı JSON mətn məzmununu ehtiva edir.
```
$ head -c 200 animated-sticker
{"tgs":1,"v":"5.5.2","fr":60,"ip":0,"op":180,"w":512,"h":512,"nm":"C-07","ddd":0,"assets":[],"comps":[],"layers":[{"ddd":0,"ind":1,"ty":3,"nm":"master","sr":1,"ks":{"o":{"a":0,"k":0},"r":{"a":0,"k":0}
```
## İstinadlar ##

* [TGS](https://core.telegram.org/stickers#animated-stickers)

* [gzip - Wikipedia](https://en.wikipedia.org/wiki/Gzip)


