{
  "date": "2019-10-11",
  "keywords": [
"mf faylı",
"mf",
"uzadılması",
"format",
"mf fayl formatı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MF - Java Manifest Fayl Formatı",
  "description": "MF fayl formatı və MF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MF",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-m-azf"
}
},
  "lastmod": "2020-09-10"
}

## MF faylı nədir?

.mf uzantılı fayl fərdi [JAR](/programming/jar/) fayl girişləri haqqında məlumatı ehtiva edən Java Manifest faylıdır. MF faylının özü JAR faylının içərisindədir və bütün genişləndirmə və paketlə bağlı tərifləri təmin edir. JAR faylları icra edilə bilən fayl kimi istifadə oluna bilər. Belə halda mainfest faylı **`public static void main`** ifadəsini ehtiva edən tətbiqin əsas sinifini təyin edir. Manifest faylları MANIFEST.MF adlanır və Windows, MacOS və Linux Əməliyyat Sistemlərində istənilən mətn redaktoru ilə açıla bilər.

## Manifest Fayl Formatının Xüsusiyyətləri

[Manifest file format specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) are available by Oracle in their guide for JAR file format. A Manifest file comprises of main sections that are followed by a list of sections for individual JAR file entries. Each section follows some rules and restrictions.

### Əsas bölmələr

Əsas bölmə:

* JAR faylı haqqında təhlükəsizlik və konfiqurasiya haqqında məlumat ehtiva edir

* JAR faylının bir hissəsi olduğu proqram və ya genişləndirmə haqqında məlumat ehtiva edir

* hər bir fərdi manifest elementi üçün əsas atributları müəyyənləşdirir


**Qeyd**: Bu bölmədə heç bir atribut Ad adlandırıla bilməz.

### Fərdi Bölmələr

Fərdi bölmə JAR faylının paketləri və ya faylları üçün müxtəlif atributları müəyyən edir. Hər bölmə Ad adlı atributla başlamalıdır, onun dəyəri faylın nisbi yolu və ya arxivdən kənar verilənlərə istinad edən mütləq URL olmalıdır.

### Manifest Spesifikasiyaları

|Atibutlar|Təsvir|
---|---|
|manifest-fayl|əsas bölmə yeni sətir *fərdi-bölmə|
|əsas bölmə|versiya məlumatı yeni sətir *əsas atribut|
|versiya-info|Manifest-Versiya : versiya nömrəsi|
|versiya-nömrə|rəqəm+{.rəqəmli+}*|
|main-atribut|(hər hansı qanuni əsas atribut) yeni sətir|
|individual-section|Ad : dəyər yeni sətir *perentry-atribut|
|perentry-atribut|(hər hansı qanuni daimi atribut) yeni sətir|
|yeni sətir|CR LF | LF | CR (ardınca LF deyil)|
|rəqəm|{0-9}|

## İstinadlar

 * [Oracle - JAR File Format](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html)
 * [JAR Fayl Formatı](https://en.wikipedia.org/wiki/JAR_(fayl_formatı))

