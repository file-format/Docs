{
  "date": "2023-02-02",
  "keywords": [
"proqram faylı",
"proqram faylı nədir",
"fayl",
"proqram faylını necə açmaq olar",
"proqram fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "description": "APP faylları yarada və aça bilən APP fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "APP Fayl Format - macOS Tətbiq Paketi",
  "linktitle": "APP",
  "menu": {
    "docs": {
      "identifier": "executable-app-az",
      "parent": "executable"
}
},
  "lastmod": "2023-02-02"
}

## APP faylı nədir?

macOS-da .app faylı icra edilə bilən kod, resurslar və metadata daxil olmaqla, xüsusi proqramı işə salmaq üçün lazım olan bütün faylları ehtiva edən xüsusi qovluq növüdür. .app genişləndirilməsi əməliyyat sisteminə siqnal verir ki, bu kataloq ayrı-ayrı fayllar toplusu deyil, vahid vahid kimi qəbul edilməlidir və o, Finder və ya Dock-dan birbaşa işə salına bilər.

Finder, macOS-da standart fayl meneceri proqramıdır. Bu, kompüterinizdəki faylları və qovluqları nəzərdən keçirməyə və təşkil etməyə imkan verir. Dock tez-tez istifadə olunan proqramlara və sənədlərə sürətli çıxışı təmin edən macOS-un xüsusiyyətidir. Həm Finder, həm də Dock sizə müvafiq proqram paketini açacaq onların .app fayllarına klikləməklə proqramları işə salmağa imkan verir. Tətbiqi işə saldığınız zaman .app paketi daxilində icra edilə bilən kod işlədilir və tətbiqi istifadə üçün əlçatan edir. .app faylı proqramın fayl sistemindəki təmsilidir və istifadəçiyə proqrama daxil olmaq və işə salmaq üçün bir yol təqdim edir.

MacOS sistemində Finder-də .app faylına sağ kliklədikdə və Paket Məzmunu Göstəri seçdiyiniz zaman proqram paketinin daxili strukturunu görə biləcəksiniz. Tətbiq tərəfindən istifadə olunan resurslara və ya fayllara daxil olmaq istəyirsinizsə və ya problemlərin həlli üçün proqramın məzmununu yoxlamaq istəyirsinizsə, bu faydalıdır. .app faylının paket məzmununa adətən şəkillər və səslər kimi resurslar üçün kataloqlar, həmçinin proqram üçün icra olunan kod daxildir. .app faylının məzmununu tədqiq etməklə siz proqramın necə bir araya gətirildiyi və onun nə etdiyi barədə daha dərin fikirlər əldə edə bilərsiniz.

## APP faylını necə açmaq olar?

MacOS-da .app faylını açmaq üçün sadəcə Finder-də fayla iki dəfə klikləyin. Bu, .app paketində olan tətbiqi işə salacaq. Tətbiq sisteminizdə quraşdırılıbsa və .app fayl növü ilə əlaqələndirilibsə, fayla iki dəfə klikləməklə proqram avtomatik başlamalıdır. Tətbiq .app fayl növü ilə əlaqəli deyilsə, onu açmaq üçün müvafiq proqram seçmək üçün faylı sağ klikləməlisiniz və Birlikdə aç seçimini etməlisiniz.

Siz açıq əmrindən istifadə edərək macOS-da Terminalda .app faylını aça bilərsiniz. Bunu etmək üçün cd əmrindən istifadə edərək .app faylının yerləşdiyi qovluğa gedin və sonra aşağıdakı əmri yerinə yetirin:

```
open <AppName>.app 
```

harada<AppName> başlamaq istədiyiniz proqramın adıdır. Bu, proqramı Finder-də iki dəfə klikləmiş kimi işə salacaq. Açıq əmri proqramlar, sənədlər və qovluqlar da daxil olmaqla bir çox müxtəlif növ faylları açmaq üçün istifadə edilə bilən ümumi təyinatlı bir yardım proqramıdır. .app faylında açıq əmrindən istifadə etdiyiniz zaman o, paketdə olan proqramı işə salır.

## İstinadlar
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
