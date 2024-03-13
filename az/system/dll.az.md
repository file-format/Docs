{
  "date": "2021-06-29",
  "keywords": [
"DLL",
"uzadılması",
"fayl",
"format",
"sistemi",
"Dinamik Bağlantı Kitabxanası",
"parametrlər",
"proqramlar",
"kompüter",
"tətbiq"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "DLL - Dinamik Bağlantı Kitabxanası",
  "description": "DLL faylları yarada və aça bilən DLL fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DLL",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-dl-azl"
}
},
  "lastmod": "2021-06-29"
}

## DLL faylı nədir? ##

DLL faylı və ya Dinamik Bağlantı Kitabxanası icra edilə bilən fayl növüdür. Bu, cihazınızda ən çox tapılan genişləndirmə fayllarından biridir və adətən Windows sisteminizdə System32 qovluğunda saxlanılır. DLL uzadılması faylı Microsoft tərəfindən hazırlanmışdır və onlar tərəfindən populyar olaraq istifadə olunur. Yüksək populyarlıq istifadəçi reytinqinə malikdir. DLL, Windows serveri tərəfindən proqram/tətbiq üçün nəzərdə tutulmuş və tətbiq edilən *sürücülər/prosedurlar/funksiyalar/xüsusiyyətləri* ehtiva edən rəf kimi işləyir. Tək bir DLL faylı müxtəlif Windows proqramları arasında da paylaşıla bilər. Bu genişləndirmə faylları cihazınızda Windows proqramlarının düzgün işləməsi üçün çox vacibdir, çünki onlar proqramda faylların yazılması və oxunması, quraşdırmanıza kənar olan digər cihazlarla əlaqə kimi müxtəlif funksiyaların işə salınmasına və işə salınmasına cavabdehdirlər.
Lakin bu Fayllar yalnız Windows-un istənilən versiyasını (windows 7/windows 10/s.) dəstəkləyən cihazda açıla bilər və buna görə də birbaşa Mac OS-ni dəstəkləyən cihazda açıla bilməz. (Mac OS-də DLL faylı açmaq istəyirsinizsə, müxtəlif xarici proqramlar onları açmağa kömək edə bilər.)


## DLL fayl formatı ##

DLL faylı Microsoft tərəfindən hazırlanmışdır və növü təmsil edən .dll uzantısına malikdir. O, Windows 1.0 serverinin və ondan kənarda ayrılmaz hissəsi olmuşdur. Bu, ikili fayl növüdür və Microsoft Windows-un bütün versiyaları tərəfindən dəstəklənir. Bu fayl növü Windows proqramları daxilində ortaq kitabxana sistemi yaratmaq, proqramların yenidən əlaqələndirilməsinə ehtiyac olmadan proqram kitabxanalarında ayrıca və müstəqil redaktə və ya dəyişikliklərə icazə vermək üçün yaradılmışdır.


## DLL Nümunəsi ##

DLL giriş nöqtəsi üçün nümunə kodu aşağıda tapa bilərsiniz:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## İstinad ##

* [DLL - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
