{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ICS - iCalendar Fayl Formatı",
  "description": "ICS fayl formatı və ICS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "ICS",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-ic-azs"
}
},
  "lastmod": "2019-09-10"
}

## ICS faylı nədir?

İnternet Təqvim və Planlaşdırma Əsas Obyekt Spesifikasiyası (iCalendar) təqvim hadisələri və planlaşdırma mübadiləsi və yerləşdirilməsi üçün internet standartıdır (RFC 2445). iCalendar formatı qarşılıqlı fəaliyyət göstərir və bununla da müxtəlif e-poçt proqramları olan istifadəçilər arasında təqvim məlumatlarının mübadiləsini təmin edir. iCalendar giriş məlumatlarını Çoxməqsədli İnternet Poçt Genişləndirmələri (MIME) kimi formatlaşdırır və müxtəlif nəqliyyat protokolları vasitəsilə obyektin mübadiləsini asanlaşdırır. Bu nəqliyyat protokolları SMTP, HTTP, nöqtədən nöqtəyə asinxron rabitə və fiziki media əsaslı şəbəkə nəqliyyatı ola bilər.

iCalendar istifadəçilərə hadisələri, tarix/saatdan asılı tapşırıqları və pulsuz/məşğul məlumatlarını e-poçt vasitəsilə cavab verə biləcək digər istifadəçilərlə paylaşmağa imkan verir. iCalendar faylları MIME tipli mətn/təqvim ilə .ics .iCalendar və ya .ifb şəkilçilərindən istifadə edərək saxlayır. iCalendar heç bir nəqliyyat protokolundan asılı olmadan özünə güvənən şəkildə saxlanılır. Veb serverlər (HTTP protokolu ilə) iCalendar məlumatını nəql edə bilər və veb səhifələr iCalendar-dan istifadə edərək daxili formada iCalendar məlumatlarını ehtiva edə bilər.

## ICS Fayl Formatının Qısa Tarixi

In 1998, the Internet Engineering Task Force (IETF) defined iCalendar as a standard (RFC 2445). The standard was documented by Frank Dawson(Lotus Notes Corporation) and Derik Stenerson ( Microsoft). In 2009, the standard was again refined by Bernard Desruisseaux (Oracle) as RFC 5545. Bu dəfə bəzi yeni funksiyalar əlavə edildi və bəzi köhnəlmiş funksiyalar köhnəldi. 2016-cı ildə RFC 7986 buraxıldı və orijinal iCalendar RFC-ə əlavə edildi. RFC 7986 əsas VCALENDAR obyektinə yeni xüsusiyyətlər əlavə etdi və konfrans sistemləri üçün yeni dəstəkləyici xüsusiyyətlər də təqdim edildi.

## ICS fayl formatı ##

iCalendar məlumatlarının istifadə etdiyi MIME növü mətn/təqvim”dir. iCalendar üçün defolt simvol dəsti UTF-8-dir, lakin MIME-də parametrləri təmin etməklə fərqli simvol dəsti istifadə edilə bilər. iCalendar faylında bölmələr var, bu bölmələr arasında VCALENDAR bütün digər bölmələri əhatə edən qlobal bölmədir. VEVENT bölməsi hadisələri müəyyənləşdirir, VTODO bütün görüləcək işləri siyahıya alır, VJOURNAL jurnal qeydlərini ehtiva edir və VTIMEZONE saat qurşağı haqqında məlumatı müəyyənləşdirir. oxşar kateqoriyadan bir neçə bölməyə icazə verilir. Çoxsaylı hadisələr üçün çoxlu VEVENT bölmələri iCalendar faylında mövcud ola bilər.

### Məzmun Xətləri ###

iCalendar obyektləri fərqli mətn sətirlərində məzmun xətləri şəklində düzülür. Bu fayl formatında CRLF ardıcıllığı xətti bitirir, xəttin uzunluğu isə sətir kəsilməsi istisna olmaqla 75 oktetlə məhdudlaşır. Uzun məlumat elementi bir çox sətirə yayıla bilər.

### Siyahı və Sahə Ayırıcıları ###

Xüsusiyyətlər və parametrlər VERGİL simvolu ilə ayrılan dəyərlərin siyahısını müəyyənləşdirir. Sitatlanmış sətirlər URI əsaslı parametr dəyərləri üçün istifadə olunur. Parametrlərin siyahısı əmlak dəyərinə görə qurula bilər. Bu siyahıdakı hər bir xüsusiyyət parametri NARIMALI VƏRGİL ilə ayrılmalıdır.

Dəyər siyahısında SEMICOLON xassə parametrlərini və VERGİL ilə ayrıca xüsusiyyət dəyərlərini təcrid edir. Nümunə aşağıda verilmişdir:

```
ATTENDEE;RSVP#TRUE;ROLE#REQ- contestant:mailto:
name@example.com
DATE;VALUE#DATE:20170304,20180504,2015704,201270904
```

### Çoxsaylı Dəyərlər

Bəzi xassələrin bir neçə dəyəri ola bilər. Sadəcə olaraq mülkiyyət adı ilə yeni məzmun xətti yaratmaq çox dəyərli xüsusiyyətlər üçün əsas qaydadır. Bununla belə, birdən çox dil dəyişikliyi olan bir dəyər üçün çox dəyərli xüsusiyyətlərdən istifadə edilməməlidir.

### İkili Məzmun

ICalendar obyekti daxilində mülkiyyət dəyəri URI istifadə edərək xarici MIME obyektində yerləşdirilmiş ikili məzmun məlumatına istinad edə bilər. Daxili ikili məzmun tətbiqin iCalendar obyektini tək obyekt kimi ifadə etməli olduğu KODLAMA parametri ilə xüsusi hallarda istifadə edilə bilər. Aşağıdakı nümunə URI istinadı ilə ATTACH xassəsini izah edir:

ATTACH: https://products.conholdate.app/viewer/view/KDDURXKkLk/fileformat.doc

### Simvol dəsti

iCalendar üçün defolt charset sxemi UTF-8 olsa da, mülkiyyət dəyərinin simvol dəstini təyin etmək üçün heç bir xüsusiyyət parametri göstərilməyib. MIME köçürmələrində charset parametri MÜTLƏQ Mövcud charset üçün istifadə olunmalıdır.

## ICS faylını necə açmaq olar?

ICS faylını açmağın bir çox yolu var. Bunlar aşağıda ətraflı təsvir edilmişdir.

1. Təqvim Tətbiqlərindən istifadə edərək ICS-i açın

Siz Microsoft Outlook, Google Calendar və ya Apple Calendar kimi Təqvim proqramlarından istifadə edərək ICS fayllarını aça bilərsiniz. Cihazınızda bu proqramlar quraşdırılıbsa, sadəcə iki dəfə klikləməklə ICS faylını bu proqramlarla aça bilərsiniz. Bu, ICS faylının hadisələrini təqviminizə idxal edəcək.

1. Mətn redaktorunda ICS faylını açın

Siz həmçinin Microsoft Notepad və ya Apple TextEdit kimi istənilən mətn redaktorunda ICS faylını aça bilərsiniz. Açıldıqdan sonra tədbirin başlanğıc və bitmə vaxtlarını əks etdirən DTSTART və DTEND sətirlərini görəcəksiniz.

1. Təqvim Tətbiqində ICS faylını əl ilə idxal edin

Siz həmçinin bu təqvim proqramlarının İmiprot və ixrac seçimlərindən istifadə etməklə ICS faylını təqvim tətbiqinizə əl ilə idxal edə bilərsiniz. Bu, ICS fayl hadisələrini təqviminizə əlavə edəcək.

## İstinadlar

* [İnternet Təqvim və Planlaşdırma Əsas Obyekt Spesifikasiyası](https://www.ietf.org/rfc/rfc5545.txt)

* [iCalendar (RFC 5545)](https://icalendar.org/RFC-Specifications/iCalendar-RFC-5545/)

* [iCalendar](https://en.wikipedia.org/wiki/ICalendar#History_and_design)


