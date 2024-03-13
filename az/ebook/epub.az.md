{
  "date": "2019-12-12",
  "keywords": [
"EPUB",
"fayl",
"uzadılması",
"format",
"Elektron kitab",
"Rəqəmsal kitab"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "EPUB fayl formatı və EPUB faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "EPUB faylı nədir?",
  "linktitle": "EPUB",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-epu-azb"
}
},
  "lastmod": "2019-12-12"
}

## EPUB faylı nədir?

.epub genişləndirilməsi olan fayllar naşirlər və istehlakçılar üçün standart rəqəmsal nəşr formatını təmin edən e-kitab fayl formatıdır. Bu format indiyə qədər o qədər geniş yayılmışdır ki, bir çox e-oxucular və proqram proqramları tərəfindən dəstəklənir. Məsələn, Mac OS-də əvvəlcədən quraşdırılmış **Kitablar** proqram təminatı belə faylların açılması üçün dəstəyi təmin edir. Bundan əlavə, smartfonlar, planşetlər və kompüterlər üçün çoxlu uyğun proqramlar mövcuddur. EPUB fayl standartları [International Digital Publishing Forum](https://idpf.org/epub/30/spec/epub30-publications.html)(IDPF) tərəfindən qorunur. EPUB 3 versiyası həmçinin məzmunun qablaşdırılması üçün standartlaşdırılmış ən yaxşı təcrübələr, tədqiqatlar, məlumat və tədbirlər üçün aparıcı kitab ticarəti assosiasiyası olan Kitab Sənayesi Tədqiqat Qrupu (BISG) tərəfindən təsdiq edilmişdir.

## EPUB Fayl Formatının Qısa Tarixi

* **Oktyabr 2007** - EPUB 2.0 təsdiq edilib

* **Sentyabr 2010** - Baxım yeniləməsi buraxıldı

* **Oktyabr 2011** - EPUB 3.0 spesifikasiyası qüvvəyə minib

* **İyun 2014** - 3.0 versiyasını əvəz etmək üçün kiçik texniki yeniləmə buraxıldı

* **Yanvar 2017** - EPUB 3.1 qüvvəyə minib


## EPUB fayl formatı

EPUB fayl formatı [ZIP](/compression/zip/) uzantısına dəyişdirilə bilən arxivdir və onun məzmununa arxivi istənilən arxiv çıxarıcı ilə çıxarmaqla baxmaq olar. O, açıq XML əsaslı formatdır və HTML faylları, şəkillər, CSS üslub cədvəlləri və digər elementlərdən ibarətdir. O, həmçinin bir sıra proqram proqramları və API-lər vasitəsilə PDF, Mobi və bir sıra digər fayl formatlarına çevrilə bilər.

{{< figure src="../epub.png" alt="EPUB fayl formatı" >}}

**EPUB E-Kitab Mac OS Kitablar Tətbiqi ilə açıldı**

EPUB fayl formatı aşağıdakı üç açıq standarta əsaslanır.

### Açıq İctimai Struktur (OPS) ###

EPUB 2.0 faylı nəşrin məzmununu qurmaq üçün XHTML 1.1-dən istifadə edir. Əslində bu o deməkdir ki, EPUB faylı bir və ya bir neçə veb səhifədən ibarətdir. Kitabın və ya qəzetin bütün məzmununu bir səhifəyə daxil edə bilsəniz də, həm performans, həm də uyğunluq baxımından belə bir faylın 300K-dan çox olmaması daha yaxşıdır. Adi veb səhifələrdə olduğu kimi, üslub və tərtibat kaskad stil cədvəllərindən (CSS) istifadə etməklə müəyyən edilir. EPUB fayllarında CSS2 alt çoxluğundan (məhdud əmrlər seriyası) istifadə edilməlidir. CSS3-ün dairəvi qutular və ya kölgələr kimi bir çox yeni funksiyaları hələ mövcud deyil. Geriyə doğru uyğunluq üçün yaradıcı məzmunu kodlaşdırmaq üçün XHTML əvəzinə DTBook-dan da istifadə edə bilər.

### Açıq Qablaşdırma Formatı (OPF) ###

Xüsusiyyətlərin bu hissəsi metadata (müəllif və naşir kimdir, başlıq nədir, ..), manifest (epub faylının içindəki bütün faylların siyahısı) və məzmun cədvəli kimi struktur məlumatlarla məşğul olur. Bu məlumatların hamısı XML istifadə edərək daxil edilir.

### Açıq Konteyner Format (OCF) ###

As the above descriptions should have made it clear an EPUB document consists of a series of files. The OCF specs define how all those files end up being packaged in one single container file. ZIP compression is used for this.

## Dəstəklənən Şəkil Fayl Formatları ##

EPUB fayl formatı aşağıdakı şəkil fayl formatlarını dəstəkləyir.

* [GIF](/şəkil/gif/)

* [JPG](/şəkil/jpeg/)

* [PNG](/şəkil/png/)

* [SVG](/page-description-language/svg/)

## İstinadlar ##

* [EPUB - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/EPUB)


