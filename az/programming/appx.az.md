{
  "date": "2021-04-22",
  "keywords": [
"appx file",
"uzadılması",
"format",
"appx faylını necə açmaq olar",
"appx fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "APPX - APPX faylı nədir?",
  "description": "APPX faylları yarada və aça bilən APPX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "APPX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-app-azx"
}
},
  "lastmod": "2021-12-16"
}

## APPX faylı nədir?

APPX faylı proqramın yayılması və quraşdırılması üçün istifadə olunan paylana bilən paket fayl formatıdır. O, Microsoft Windows Mağazasında dərc olunacaq Windows 8 ilə təqdim edilib. Bu, Windows proqramını quraşdırmaq üçün lazım olan bütün faylları ehtiva edir. Bunlara metadata, fayllar və etimadnamə məlumatları daxildir. Daha müasir qablaşdırma fayl formatı APPX ilə müqayisədə hazırda daha çox istifadə olunan MSIX-dir.

## APPX Fayl Formatı - Ətraflı Məlumat

APPX faylları [ZIP](/compression/zip/) fayl formatında sıxılmış fayllar kimi saxlanılır. Bu, bütün paketi Microsoft Mağazasına yükləmək asan olan kiçildilmiş fayl ölçüsü ilə arxiv faylı halına gətirir.

## APPX faylında faylları necə görmək olar?

APPX faylının içindəki məzmunu və ya faylları görmək üçün aşağıdakı addımlar yerinə yetirilməlidir.

 1. APPX faylları sıxılmış ZIP faylları kimi saxlandığından, faylın adını .zip uzantısı ilə dəyişdirin
 1. APPX faylında olan faylları çıxarmaq üçün 7-Zip, WinZip və ya WinRAR kimi hər hansı dekompressiya alətindən istifadə edin.

## APPX faylını necə yaratmaq olar?

APPX faylları yaratmaq üçün istifadə edilə bilən iki üsul var.

 1. MakeApp.exe-dən istifadə - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) həm proqram paketləri (.msix və ya .appx) və həm də proqram paket paketi faylları .msixbundle və ya .appxbundle yaratmaq üçün istifadə olunur. Bundan əlavə, o, proqram paketindən faylları çıxara bilər. MakeApp.exe Windows 10 SDK ilə mövcuddur və əmr sorğusundan istifadə edilə bilər.
 1. Microsoft Visual Studio istifadə - Tərtibatçılar adətən Microsoft Visual Studio istifadə edərək [create APPX files](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview). Tətbiqin hazırlanması tamamlandıqdan və proqram dərc olunmağa hazır olduqdan sonra APPX paket faylı onu Visual Studio daxilində dərc etməklə yaradıla bilər.

## İstinadlar

 * [MakeAppx.exe ilə MSIX paketi və ya paketi yaradın](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
 * [Microsoft Visual Studio istifadə edərək APPX faylları yaradın](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

