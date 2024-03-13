{
  "date": "2021-04-22",
  "keywords": [
"msix faylı",
"uzadılması",
"format",
"msix faylını necə açmaq olar",
"msix fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MSIX - MSIX faylı nədir?",
  "description": "Learn about MSIX file and APIs that can create and open MSIX files.",
  "linktitle": "MSIX",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-msi-azx"
}
},
  "lastmod": "2021-12-16"
}

## MSIX faylı nədir?

An MSIX file is a Windows app packaging format that is used to create and distribute applications in Windows 10. Bu [APPX](/programming/appx/) və MSI ilə müqayisədə müasir paket fayl formatıdır və nəhayət bu yeni fayl formatına buraxılacaq. O, Win32, WPF və Windows Forms proqramlarının yerləşdirilməsi üçün istifadə edilə bilər. MSIX faylları etibarlıdır və şəbəkə və disk sahəsinin optimallaşdırılmasını hədəfləyir. Tərtibatçılar bunlardan Microsoft Mağazası (əvvəllər Windows Mağazası kimi tanınır) vasitəsilə proqramları son istifadəçilərə yaymaq üçün istifadə edirlər.

## MSIX Fayl Format - Ətraflı Məlumat

MSIX faylları [ZIP](/compression/zip/)-sıxılmışdır, bütün fayllar paketlənmiş faylın içərisinə daxildir. Tətbiqlə əlaqəli fayllara əlavə olaraq, MSIX faylı proqram quraşdırılması ilə bağlı məlumatları ehtiva edən [.xml](/web/xml/) konfiqurasiya fayllarını ehtiva edir.

## MSIX paketinin içərisində nə var?

MSIX paketi aşağıdakı fayllardan ibarətdir.

 * `AppxBlockMap.xml` - Paket bloku xəritəsi faylı kimi tanınan bu, paketdə saxlanılan hər bir məlumat bloku üçün indeksləri və kriptoqrafik heşləri olan proqram fayllarının siyahısını ehtiva edən XML sənədidir.
 * `AppxManifest.xml` - MSIX proqramının yerləşdirilməsi, göstərilməsi və yenilənməsi üçün tələb olunan məlumatları ehtiva edən XML sənədi. Bu məlumata paket şəxsiyyəti, paketdən asılılıqlar, tələb olunan imkanlar, vizual elementlər və genişlənmə nöqtələri daxildir.
 * `AppxSignature.p7x` - Paket imzalandıqda yaradılan fayl. Bütün MSIX paketləri quraşdırmadan əvvəl imzalanmalıdır. AppxBlockmap.xml ilə platforma paketi quraşdıra və təsdiqlənə bilər.

## İstinadlar

 * [MSIX Baxışı](https://learn.microsoft.com/en-us/windows/msix/overview)
 * [Microsoft Visual Studio istifadə edərək APPX faylları yaradın](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

