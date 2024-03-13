{
  "date": "2019-10-11",
  "keywords": [
"rar faylı",
"rar fayl formatı",
"rar faylı nədir",
"fayl",
"rar nümunəsi",
"rar fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "RAR",
  "description": "RAR faylları yarada və aça bilən RAR fayl uzantısı və API nədir.",
  "linktitle": "RAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ra-azr"
}
},
  "lastmod": "2019-09-10"
}

## RAR faylı nədir?

.rar uzantılı fayllar məlumatı sıxılmış və ya normal formada saxlamaq üçün yaradılan arxiv fayllarıdır. Roshal ARchive fayl formatı mənasını verən RAR, 1995-ci ildə rus proqram mühəndisi olan Eugene Roshal tərəfindən yaradılmış xüsusi fayl formatıdır. Format, müxtəlif sıxılma üsulları daxil olmaqla, müxtəlif üsullarla faylları arxivləşdirmək üçün istifadə olunur. RAR fayllarının çıxarılması üçün Windows, Linux və MacOS üçün bir neçə proqram proqramı mövcuddur. RARLab tərəfindən WinRAR proqramı Microsoft Windows platforması üçün paylaşılan fayl arxivləşdirmə proqramıdır (40 gün ərzində pulsuzdur); proqram eyni Müəllif Eugene Roshal tərəfindən Linux-a köçürüldü (yalnız ekstraktor kimi).

## RAR Fayl Formatının Versiya Tarixi

* v1.3 (orijinalda "Rar!" imzası yoxdur)

* v1.5

* v2.0 - MS-DOS 2.0 üçün WinRAR 2.0 və Rar ilə buraxılmışdır

* v2.9 - WinRAR 3.00 versiyasında buraxılmışdır

* v5.0 - WinRAR 5.0 və sonrakı versiyalar tərəfindən dəstəklənir


## RAR formatının əsas xüsusiyyətləri

RAR bu sahədə kifayət qədər uzun müddətdir və sevimli arxiv fayl formatlarından biri olmuşdur. RAR formatının əsas xüsusiyyətləri bunlardır:

**`Yüksək sıxılma nisbəti:`** [ZIP](/compression/zip/) ilə müqayisədə üstündür, 7z və zipx formatı ilə müqayisə edilə bilər.

**`Dizayn üzrə güclü fayl şifrələməsi:`** Şifrələnmiş RAR4 arxivləri AES-128 əsaslı şifrələməyə, şifrələnmiş RAR5 arxivləri isə təkmilləşdirilmiş açar planlaşdırma ilə AES-256 şifrələməsinə əsaslanır.

**` Qabaqcıl xətaların düzəldilməsi və məlumatların bərpası imkanları:`** arxiv yaradılması zamanı isteğe bağlı bərpa qeydləri

**`Fayl Ölçüsü:`** Ölçüdə minimum 20 bayt və maksimum 2^63 bayt (arxivin ümumi ölçüsündən 8 eksabayt)

**`Çoxhəcmli RAR Arxivləri:`** Şəbəkə üzərindən köçürməni asanlaşdırmaq üçün böyük arxivləri bir neçə kiçik fayla bölmək imkanı. Bu halda, bölünmüş həcmləri təmsil etmək üçün fayl uzantıları 1 artırılır

## RAR fayl formatı

RAR formatının tam spesifikasiyası ictimaiyyətə açıq deyil və buna görə də format haqqında təfərrüatları qısa şəkildə tərtib etmək mümkün deyil.

### Ümumi Arxiv Planı

5.0 versiyasında təqdim edilmiş RAR fayl formatının ümumi sxemi aşağıdakı kimidir:

|Fayl Format
---|
|Özünü çıxaran modul (isteğe bağlı)
|RAR 5.0 İmza
|Arxiv Şifrələmə Başlığı (isteğe bağlı)
|Əsas arxiv başlığı
|Arxiv şərh xidmətinin başlığı (isteğe bağlı)
Fayl başlığı 1
|Əvvəlki fayl üçün xidmət başlıqları (NTFS ACL, axınlar və s.) (isteğe bağlı)
|...
|Fayl başlığı N
|Əvvəlki fayl üçün xidmət başlıqları (NTFS ACL, axınlar və s.) (isteğe bağlı)
|Bərpa qeydi (isteğe bağlı)
|Arxiv başlığının sonu

Yuxarıda göstərilən RAR faylının hər bir bölməsi haqqında məlumatı [RAR 5.0 File Format specifications](https://www.rarlab.com/technote.htm#arcstruct) sənədində tapa bilərsiniz.

#### Öz-özünə çıxarılan RAR Arxivləri

Əgər RAR faylı özü çıxarırsa, özü çıxaran məlumat arxiv imzasından əvvəlki faylın başlanğıcında yerləşir. Onun ölçüsü və məzmunu müəyyən edilməyib.

#### RAR 5.0 İmza

RAR imzası aşağıdakı sehrli nömrədən ibarət 8 baytlıq başlıqdır:

0x 52 61 72 21 1A 07 00

harada

0x6152 - HEAD_CRC

0x72 - HEAD_TYPE

0x1A21 - HEAD_FLAGS

0x0007 - HEAD_SIZE

## İstinadlar

* [RAR 5.0 Arxiv Format](https://www.rarlab.com/technote.htm)

* [RAR - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/RAR_(file_format))


