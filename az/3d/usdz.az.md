{
  "date": "2021-02-01",
  "keywords": [
"usdz",
"usdz faylı",
"usdz fayl formatı",
"fayl formatı",
"3d",
"usdz faylı yükləyin"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "USDZ - Universal Səhnə Təsviri ZIP Format",
  "description": "USDZ fayl formatı və USDZ fayllarını aça və yarada bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "USDZ",
  "menu": {
    "docs": {
      "parent": "3d",
      "identifier": "3d-usd-azz"
}
},
  "lastmod": "2021-02-01"
}

## USDZ faylı nədir?

.usdz faylı arxivə daxil edilmiş və onları işlədən digər formatlı faylları (teksturalar və animasiyalar kimi) ehtiva edən və onların proksilərini ehtiva edən [USD](/3d/usd/) (Universal Səhnə Təsviri) fayl formatı üçün sıxılmamış və şifrələnməmiş ZIP arxividir. heç bir açma ehtiyacı olmadan birbaşa USD iş vaxtı ilə. USDZ faylları dizaynı paketin yeni Ar səviyyəli abstraksiyasına əsaslanan paketlərdir. Usdz IANA-da qeydiyyatdan keçib və modelin media tipli adına və vnd.usd+zip alt tip adına malikdir və onun təfərrüatları [IANA registration page](https://www.iana.org/assignments/media-types/model/vnd.usdz+zip)-də tapıla bilər.

## USDZ Fayl Formatı

USDZ files are based on the ZIP file format that archive individual files in its container. This enables the receiver end to just unzip the contents and use the normal USD scene description files to work with and inspect. Almost all operating systems provide builtin support for the ZIP file formats and choosing this archiving format over any custom method makes it easy for USDZ files to be useful as a simple transport protocol.

### ZIP Məhdudiyyətləri

USDZ fayl formatı heç bir `sıxılma` və `şifrləmə` olmadan ZIP fayl formatından istifadə edir. Bu, dizaynla iki tələbə cavab vermək məqsədi daşıyırdı:

 * Artıq yaddaşa və ya diskdə tək fayl kimi yüklənmiş paket üçün təsvirdə olan məlumatlara daxil olmaq üçün API USD-də mövcuddur.
 * Faylları diskə çıxarmağa və ya daha çox yığın yaddaş ayırmağa ehtiyac yoxdur

USDZ ilə bu tələblərin hər ikisi yerinə yetirilir, çünki şəkil formatlarının əksəriyyəti özləri daxili sıxılma sxemlərinə imkan verir, nəticədə kompakt fayl ölçüsü olur.

### Layout Tələbləri

USDZ paketləri paket daxilində faylların düzülməsini tələb edir ki, hər bir fayl üçün məlumat paketin əvvəlindən 64 baytdan çox olmalıdır. Bununla belə, paketi sadə bir istinadla hədəflədiyi halda, paket yerli [USD](/3d/usd/) faylı ilə başlamalıdır. Belə bir halda, bu ilk USD faylı Defolt Layer adlanır. Axınan məzmun” təqdim etmək istəyən müştərilər digər tərtibat məhdudiyyətlərini də nəzərə almaq istəyə bilər.

## USDZ faylı yükləyin
Usdz faylları digər yüksək keyfiyyətli şəkillər və usd faylları ilə dolu olduğundan, daha çox disk yaddaşı tuta bilər. Burada yükləmək üçün sadə və daha kiçik USDZ nümunə faylı tapa bilərsiniz:

- [Sample.usdz](../sample.usdz)

## İstinadlar

* [USDZ Fayl Formatının Xüsusiyyətləri](https://openusd.org/release/spec_usdz.html)


