{
  "date": "2019-10-11",
  "keywords": [
"BANKA",
".banka",
"jar faylı nədir",
"jar faylını necə açmaq olar",
"uzadılması",
"fayl",
"jar faylı",
"jar fayl formatı",
".jar uzadılması"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JAR - Java Arxiv Fayl Format",
  "description": "JAR faylı yarada və aça bilən JAR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "JAR",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-ja-azr"
}
},
  "lastmod": "2020-09-10"
}

## JAR faylı nədir?

.jar uzantısı olan fayl, tək bir fayl kimi çoxlu müxtəlif proqramla əlaqəli faylları ehtiva edən Java Arxiv faylıdır. Bu fayl formatı birdən çox HTTP bağlantısı yaratmaqdan qaçaraq HTTP əməliyyatı vasitəsilə brauzerə yüklənmiş Java Applet yükləmə sürətini azaltmaq üçün yaradılmışdır. Tək JAR faylında Java sinif faylları ([.class](/programming/class/)), [images](/image/) və [sounds](/audio/) ola bilər. JAR faylı daxilindəki fərdi elementlər onların mənşəyini təsdiqləmək üçün proqram tərtibatçısı tərəfindən rəqəmsal imzalana bilər. JAR faylları mütəmadi olaraq həmin API ilə əlaqəli xüsusi funksiyaları ehtiva edən funksional API yaratmaq üçün istifadə olunur.

## JAR fayl formatı

JAR files are based on the popular [ZIP file format](/compression/zip/) that archives its individual content files in a single file. JAR file format supports compressions, resulting in a smaller file size for downloading and hence further improves the download time. The [JAR file specifications](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) artilce by Oracle gives complete details about the internal specifications of JAR files.

### Manifest Faylı

JAR faylı yaradıldıqda onun daxilində avtomatik olaraq JAR faylının məzmunu haqqında metadata məlumatı olan manifest faylı yaradılır. Bu fayl JAR faylı daxilində paketlənmiş məzmunu göstərir. Tipik bir Manifest faylı JAR faylına daxil olan qovluqları və sinifləri göstərən aşağıdakı kimi görünür.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Manifest Xüsusiyyətləri

Manifest spesifikasiyaları Oracle tərəfindən aşağıdakı kimi müəyyən edilir.

`manifest-fayl`: əsas bölmə yeni sətir \*fərdi-bölmə

`əsas bölmə`: versiya-məlumat yeni sətir \*əsas atribut

`versiya məlumatı`: Manifest-Versiya: versiya nömrəsi

`versiya nömrəsi` : rəqəm+{.rəqəmli+}*

`əsas atribut`: (hər hansı qanuni əsas atribut) yeni sətir

`fərdi-bölmə`: Ad : dəyər yeni sətir \*perentry-atribut

`perentry-atribut`: (hər hansı qanuni daimi atribut) yeni sətir

`yeni xətt` : CR LF | LF | CR (ardınca LF deyil)

`rəqəm`: {0-9}

### İcra edilə bilən JAR

JAR faylları həmçinin Microsoft Windows Əməliyyat Sistemindəki hər hansı digər proqrama bənzər Java Virtual Maşın (JVM) tərəfindən icra edilə bilən proqramdan ibarət ola bilər. Bu halda, JVM ictimai statik boşluq əsas metodu olan istənilən sinif olan tətbiqin giriş nöqtəsi haqqında bilməlidir. Manifest faylı belə bir sinfi `Əsas-Class` başlığı ilə aşağıdakı formatda müəyyən edir:

```
Main-Class: com.example.MyClassName
```



## İstinadlar

 * [JAR File Overview](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
 * [JAR Fayl Formatı](https://en.wikipedia.org/wiki/JAR_(fayl_formatı))

