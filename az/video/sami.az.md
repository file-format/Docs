{
  "date": "2023-05-16",
  "keywords": [
"sami faylı",
"sami faylı nədir",
"sami faylının nümunəsi",
"fayl",
"sami fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "SAMI Fayl Format - Altyazılar və Metadata Mübadilə Faylı",
  "description": "SAMI faylları yarada və aça bilən SAMI formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami-az",
      "parent": "video"
}
},
  "lastmod": "2023-05-16"
}

## SAMI faylı nədir?

.sami uzantılı fayl adətən Altyazılar və Metadata Mübadiləsi (SAMI) faylına istinad edir. SAMI videolarda subtitrləri və ya qapalı yazıları göstərmək üçün istifadə edilən başlıq formatıdır. Əvvəlcə Microsoft tərəfindən Windows Media Player üçün hazırlanmışdır.

SAMI faylları altyazılar və ya qapalı başlıqlar üçün vaxt məlumatı və mətn məzmununu ehtiva edir ki, bu da onları video oxutma ilə sinxronizasiya etməyə imkan verir. Format şrift üslubu, rəng və ekranda altyazıların yerləşdirilməsi kimi əsas formatlaşdırma seçimlərini dəstəkləyir.

SAMI faylları adətən düz mətn fayllarıdır və mətn redaktoru vasitəsilə açıla və redaktə edilə bilər. SAMI faylının məzmunu adətən fayl haqqında məlumat verən başlıq bölməsini, ardınca müvafiq vaxt və mətni olan fərdi altyazı qeydlərini ehtiva edir.

SAMI faylının necə görünə biləcəyinə dair bir nümunə:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

SAMI faylları adətən Windows Media Player və ya VLC Media Player kimi altyazı ekranını dəstəkləyən video pleyerlər və ya media pleyerləri ilə birlikdə istifadə olunur. Pleyer SAMI faylını oxuyur və altyazıları video məzmunu ilə sinxronlaşdırır, izləyicilərə videoya baxarkən başlıqları oxumağa imkan verir.

## Dəstəklənən HTML teqləri

SAMI (Subtitles And Metadata Interchange) files support a limited set of HTML-like tags for formatting and styling the subtitles. Here are some of the commonly used tags supported by SAMI:

- ``<SAMI> :`` Bütün SAMI faylını əhatə edən kök element.
- ``<HEAD> :`` SAMI faylı üçün başlıq məlumatını ehtiva edir.
- ``<TITLE>:`` Specifies the title of the SAMI file.
- ``<BODY>:`` Encloses the subtitle entries and their timing information.
- ``<SYNC>:`` Represents a synchronization point for a subtitle entry. It specifies the timing at which the subtitle should be displayed.
- ``<P>:`` Encloses the actual text content of a subtitle. It is typically used within a <SYNC> block.
- `` <FONT>:`` Əlavə edilmiş mətn üçün şrift xüsusiyyətlərini müəyyənləşdirir. Rəng, Üz, Ölçü və Üslub kimi atributlar şriftin görünüşünü dəyişdirmək üçün istifadə edilə bilər.</font>
- ``<BR>:`` Inserts a line break within a subtitle.
- `` <B>:`` Əlavə edilmiş mətni qalın şriftlə göstərir.</b>
- `` <I>:`` Əlavə edilmiş mətni kursivlə göstərir.</i>
- `` <U>:`` Altı xətt çəkilmiş əlavə mətni göstərir.</u>
- ``<C>:`` Specifies the position or alignment of the subtitle text on the screen. It supports attributes like Center, Middle, Left, Right, Top, Bottom, and their combinations.
- ``<LANG>:`` Specifies the language code for the subtitle text. It helps in identifying the language of the subtitles.

Bunlar SAMI faylları tərəfindən dəstəklənən bəzi əsas teqlərdir. Qeyd etmək vacibdir ki, SAMI bütün HTML teqləri və atributlarını dəstəkləmir. Dəstəklənən teqlər geniş sənəd strukturu və ya interaktivlik təmin etməkdənsə, ilk növbədə altyazıların üslubuna və yerləşdirilməsinə yönəlib.

## İstinadlar
* [SAMI](https://en.wikipedia.org/wiki/SAMI)


