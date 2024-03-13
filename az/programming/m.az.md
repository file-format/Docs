{
  "date": "2019-10-11",
  "keywords": [
"M faylı",
"M",
"uzadılması",
"format",
"M fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "M - Matlab mənbə kodu faylı",
  "description": "MF faylları yarada və aça bilən Matlab .m Mənbə Kodu faylı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "M",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming--azm"
}
},
  "lastmod": "2020-09-10"
}

# M - Matlab mənbə kodu faylları

## M (Matlab) faylı nədir?

.m uzantılı fayl, təhlil, alqoritmlərin işlənməsi və simulyasiya modelləşdirilməsi üçün istifadə edilən proqramlaşdırma və rəqəmsal hesablama platforması olan Matlab tərəfindən istifadə edilən mənbə kodu faylıdır. Digər proqramlaşdırma fayl formatları kimi, M faylı da qrafiklərin qurulması, simulyasiyaların aparılması və digər riyazi əməliyyatlar üçün Matlab əmrlərini yerinə yetirən mənbə kodu ehtiva edir. Tək Matlab simulyasiyası tətbiqi skriptlərdə, siniflərdə, funksiyalarda və ya bəyannamələrdə təsnif edə bilən çoxsaylı belə .m faylları əhatə edə bilər. Matlab M faylları istənilən mətn redaktoru ilə açıla bilər.

## Matlab M Fayl Format - Ətraflı Məlumat

Matlab .m faylları Matlab proqramlaşdırma dilində proqramlaşdırma kodunu ehtiva edən mətn fayllarıdır. Bunlar istənilən mətn redaktorunda açıla və redaktə edilə bilər və Matlab proqramında icra olunmaq üçün yenidən saxlanıla bilər. Matlab-ın özündə kod, çıxış və formatlaşdırılmış mətnin birləşməsindən ibarət skriptlər yaratmaq üçün istifadə olunan Canlı Redaktor var.

### Matlab Funksiya Faylları

Digər proqramlaşdırma dilləri kimi, siz yalnız müəyyən tapşırığı yerinə yetirən funksiyanın tərifini ehtiva edən .m faylı yarada bilərsiniz. Bu cür fayllar da .m genişlənməsi ilə saxlanılır və yalnız həmin funksiyaya aid funksiyaları həyata keçirir.

### .M Fayl Nümunəsi

Aşağıda h hündürlüyündən düşmüş obyekt üçün çəkilən vaxtı hesablayan Matlab funksiya faylı nümunəsidir.

```C++
function t= TimeToGround(h)  
  t=sqrt(h/4.9);
end
```

Bu funksiyanı Matlab redaktorundan və ya başqa .m faylından çağırmaq üçün aşağıdakı koddan istifadə etmək olar.
```C++
TimeToGround(100)
```

## İstinadlar

 * [Matlab - Dəstəklənən Fayl Formatları](https://www.mathworks.com/help/matlab/standard-file-formats.html)
 * [Matlabdan istifadə](https://www.maths.unsw.edu.au/sites/default/files/MatlabSelfPaced/lesson0/MatlabLesson0_Mfiles.html)

# M - Objective-C İcra Faylı

## M (Objective-C) faylı nədir?

M faylına həmçinin OS X və iOS üçün proqram proqramları yazmaq üçün istifadə olunan proqramlaşdırma dili olan Objective-C dilində yazılmış sinifin mənbə kodunu ehtiva edən icra faylı deyilir. Objective-C bu platformalar üçün Apple-ın əsas API-ləri olan Cocoa və Cocoa Touch tərəfindən istifadə edilən əsas proqramlaşdırma dilidir. Bu dildə hazırlanmış tək proqram təminatı proqram siniflərinin həyata keçirilməsini ehtiva edən çoxsaylı .m faylları ehtiva edə bilər. Bunlar Apple XCode, jEdit və digər ümumi mətn redaktorlarından istifadə etməklə açıla bilər.

## Objective-C M Fayl Format - Ətraflı Məlumat

M faylları Objective-C-nin proqramlaşdırma sintaksisindən istifadə edərək düz mətn formatında yazılmışdır. Sinfin hər bir metodu bu icra fayllarında onun bütün lazımi kodu ilə müəyyən edilməlidir. Bu tətbiq M faylları tələblərə uyğun olaraq bir və ya daha çox .h başlıq faylını idxal edə bilər. Import bəyanatı kompilyatora bu icra faylına aid başlıq faylını haradan tapacağını bildirir. İdxal bəyanatı aşağıdakı kimi yazılır.

```C++
#import "network.h"
```

Hər bir M faylının tətbiqi daha sonra `@implementation` direktivi ilə başlayır, ardınca isə tətbiq sinfi fayl adı verilir. Bundan sonra başlıq faylında elan edilən bütün metodların icrası izlənilir.

### M Fayl Formatının Nümunəsi

```C++
UrlConnection.m

#import "UrlConnection.h"

@implementation UrlConnection

(void)connect {
    // In here would be code to attempt a connection to the
    // specified URL, while possibly handling connection errors.
    //
}

 + (BOOL)canHandleRequest:(NSString \*)type
                   forUrl:(NSString \*)url {
    //And in here would be code to see if the given URL passed
    // in is capable of handling the HTTP request type specified
    // by the "type" parameter. It will return YES or NO.
 }

 @end
```

## İstinadlar
 * [Obyektiv C haqqında](https://developer.apple.com/library/archive/documentation/Cocoa/Conceptual/ProgrammingWithObjectiveC/Introduction/Introduction.html#//apple_ref/doc/uid/TP40011210-CH1-SW1)
 * [Obyekt-C Bələdçisi](https://blog.teamtreehouse.com/beginners-guide-objective-c-classes-objects)

