{
  "date": "2022-01-26",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "LOCK Fayl Format - Kilid faylı nədir?",
  "description": "LOCK fayl formatı və onun .",
  "linktitle": "LOCK",
  "menu": {
    "docs": {
      "parent": "misc",
      "identifier": "misc-loc-azk"
}
},
  "lastmod": "2022-01-26"
}

## LOCK faylı nədir?

**LOCK** faylı faylı və ya bəzi cihazı kilidli kimi qeyd etmək üçün proqramlar və əməliyyat sistemləri tərəfindən istifadə edilən adı dəyişdirilmiş fayldır. Bu, digər proqramlara faylı istifadə edən proqramdan azad olmadıqda istifadə etməməyi bildirir. Əksər hallarda bu kilid faylları boşdur, lakin digər hallarda onlar xassələr və parametrlər kimi kilidlə bağlı məlumatları ehtiva edə bilər.

Bəzən, .lock faylı verilənlər bazası faylının **lockeed** nüsxələrini yaratmaq üçün Microsoft-un .NET Framework tərəfindən istifadə olunur. Belə olan halda verilənlər bazası faylının surəti .lock uzantısı ilə açılacaq. Bu, istifadəçiyə fayl başqa istifadəçi tərəfindən istifadə edilərkən ona dəyişiklik etməyə icazə vermir.

## LOCK Fayl Format - Ətraflı Məlumat

LOCK faylı hər bir proqram tərəfindən yaradılır və onun fayl formatı proqrama xasdır. Bu kilid faylları həm mətn, həm də ikili fayl formatında saxlanıla bilər.

Kilid fayllarının olması resursun həmin resursa daxil olmağa çalışan birdən çox fayla eyni vaxtda daxil olmasına mane olur. Orijinal faylın surəti adına əlavə edilmiş .lock uzantısı ilə yaradılmışdır. Bu, digər proqramlara fayla yalnız oxumaq üçün giriş imkanı verir. Məsələn, resource.dat resource.data.lock olacaq.

Ruby proqramlaşdırma dili üçün siz **gemfile.lock** faylına rast gələ bilərsiniz. Bundler quraşdırılmış dəqiq versiyaların qeydini saxladığı yerdir. Beləliklə, bir layihə/kitabxana başqa maşına köçürüldükdə, işləyən paket dəqiq müvafiq versiya üçün Gemfile-ə baxacaq.

## Linux-da faylı kilidləyin

Linux iki növ fayl kilidini dəstəkləyir: məsləhət kilidləri və məcburi kilidlər.

 * **Məsləhət Kilidləri**: Tətbiq edilməyən kilidləmə növü. Bu halda, iştirak edən proseslər bir-biri ilə açıq şəkildə əməkdaşlıq edərək kilidlər əldə edir. Bu mümkün deyilsə, məsləhət kilidləri nəzərə alınmır.

 * **Məcburi Kilidlər**: Məcburi kilidləmə halında, əməliyyat sistemi digər proseslərin faylı oxumasına və ya yazmasına mane olmaqla faylın kilidlənməsini tətbiq edir. Bu, proseslər arasında hər hansı əməkdaşlıq tələb etmir.

məcburi kilidləmə iştirakçı proseslər arasında hər hansı əməkdaşlıq tələb etmir. Faylda məcburi kilid aktivləşdirildikdən sonra əməliyyat sistemi digər proseslərin faylı oxumasına və ya yazmasına mane olur.

## İstinadlar

* [Ruby-də GemFile və Gemfile.lock](https://medium.com/never-hop-on-the-bandwagon/gemfile-and-gemfile-lock-in-ruby-65adc918b856)

* [Linux-da kilidləmə](https://www.baeldung.com/linux/file-locking)


