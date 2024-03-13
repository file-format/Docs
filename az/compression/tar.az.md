{
  "date": "2019-10-11",
  "keywords": [
"tar faylı",
"tar fayl formatı",
"tar faylı nədir",
"fayl",
"tar nümunəsi",
"tar fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TAR - Unix Arxiv Fayl Formatı",
  "description": "TAR faylı və TAR faylları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "TAR",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-ta-azr"
}
},
  "lastmod": "2019-09-10"
}

## TAR faylı nədir?

.tar uzantılı fayllar bir və ya bir neçə faylı toplamaq üçün Unix əsaslı yardım proqramı ilə yaradılmış arxivlərdir. Arxivə faylların və qovluqların əlavə edilməsi dəstəyi ilə bir neçə fayl sıxılmamış formatda saxlanılır. Unix-də TAR yardım proqramı Əmr əsaslıdır, lakin beləliklə yaradılmış fayllar demək olar ki, bütün əməliyyat sistemlərində əksər fayl arxivləşdirmə sistemləri tərəfindən dəstəklənir. İlk dəfə 1979-cu ildə AT&T Bell Laboratories tərəfindən yaradılmış və sonrakı versiyaları zaman keçdikcə nəşr edilmişdir.

## TAR fayl formatı

TAR is an open file format with full specifications available for developer's reference. Its file structure was standardized in POSIX.1-1988 and later in POSIX.1-2001. Tar tərəfindən yaradılan məlumat dəstləri fayl sistemi parametrləri haqqında məlumatları saxlayır, məsələn:

* Ad

* Vaxt möhürləri

* Mülkiyyət

* Fayl giriş icazələri

* Kataloq təşkilatı


TAR faylının sehrli nömrəsi yoxdur. O, hər blokun BLOCKSIZE baytdan ibarət olduğu bir sıra bloklardan ibarətdir.

Arxivləşdirilmiş hər bir fayl faylı təsvir edən başlıq bloku, sonra isə faylın məzmununu verən sıfır və ya daha çox blokla təmsil olunur. Arxiv faylının sonunda faylın sonu markeri kimi ikili sıfırlarla doldurulmuş iki 512 baytlıq blok var. Ağlabatan sistem arxivin sonunda belə fayl sonu markerini yazmalıdır, lakin arxivi oxuyarkən belə blokun mövcud olduğunu güman etməməlidir. Xüsusilə GNU tar qarşılaşmadığı təqdirdə həmişə xəbərdarlıq edir.

Bloklar fiziki giriş/çıxış əməliyyatları üçün bloklana bilər. n blokdan ibarət hər bir qeyd (burada n bloklama faktoru = tar üçün 512 ölçülü seçim tərəfindən təyin olunur) tək yazma () əməliyyatı ilə yazılır. Maqnit lentlərdə belə bir yazının nəticəsi tək bir qeyddir. Arxiv yazarkən blokların son qeydi tam ölçüdə yazılmalı, sıfır blokdan sonrakı bloklar bütün sıfırları ehtiva etməlidir. Arxivi oxuyarkən ağlabatan sistem son qeydi qalanlarından daha qısa olan və ya sıfır blokdan sonra zibil qeydləri olan arxivi düzgün idarə etməlidir.

### TAR Fayl Başlığı

Hər hansı digər fayl başlıqları kimi, tar faylının başlıq qeydi fayl haqqında metadata ehtiva edir və aşağıdakı cədvəldə göstərilir.

|Sahənin ofseti|Sahənin ölçüsü (bayt)|Sahə
---|---|---|
|0|100|Fayl adı
|100|8|Fayl rejimi
|108|8|Sahibinin rəqəmli istifadəçi ID-si
|116|8|Qrupun rəqəmli istifadəçi ID-si
|124|12|Fayl ölçüsü baytla (səkkizlik baza)
|136|12|Rəqəmsal Unix vaxt formatında son dəyişiklik vaxtı (səkkizlik)
|148|8|Başlıq qeydi üçün yoxlama məbləği
|156|1|Bağlantı göstəricisi (fayl növü)
|157|100|Əlaqələndirilmiş faylın adı

İstifadə olunmayan sahələr NUL baytları ilə doldurulur. Başlıq 512 baytlıq qeydi doldurmaq üçün NUL baytlarla doldurulmuş 257 baytdan ibarətdir.

## TAR faylını necə yaratmaq olar

### Windows-da TAR faylı yaradın

Windows-da TAR faylları yaratmaq üçün Linux üçün Windows Alt Sistemindən (WSL) və ya 7-Zip kimi üçüncü tərəf alətlərindən istifadə edə bilərsiniz. WSL istifadə edərək bunu necə etmək olar:

 1. Əgər hələ də quraşdırmamısınızsa, WSL quraşdırın. Siz onu Windows Xüsusiyyətləri parametrləri vasitəsilə quraşdıra bilərsiniz.

 1. WSL terminalını açın və TAR faylı yaratmaq üçün Linux və ya Unix sistemlərində olduğu kimi eyni tar əmrindən istifadə edin.

### Komanda xəttindən Linux-da TAF faylı yaradın

Linux və ya Unix əsaslı sistemlərdə komanda xəttindən istifadə edərək TAR faylı yaratmaq üçün terminalı açın və tar əmrindən istifadə edin. Siz müxtəlif sıxılma formatlarında TAR faylı yarada bilərsiniz (məsələn, .tar.gz, .tar.bz2, .tar.xz), lakin burada biz sadə .tar faylı yaradacağıq:

Tək bir fayl və ya qovluqdan TAR faylı yaratmaq üçün aşağıdakı əmrdən istifadə edin:

```
tar -cvf archive.tar file_or_directory
```

## TAR faylını necə açmaq olar

### Windows-da TAR faylını açın

Siz Windows OS-də 7-Zip kimi bir dekompressiya proqramı olmalıdır. Bu, müxtəlif sıxılmış fayl formatlarını yaratmaq və çıxarmaq üçün istifadə edilə bilən pulsuz arxivləşdirmə proqramıdır. TAR faylınıza sağ vurun və **Çıxarış** seçimini seçin.

### Mac-da TAR faylını açın

Mac-da TAR, TGZ və ya TAR.GZ faylını paketdən çıxarmaq üçün üzərinə iki dəfə klikləyin.

### Linux-da TAR faylını açın

Əgər siz Linux və ya Mac Terminal proqramından istifadə edirsinizsə, TAR faylları üçün tar -xvf və ya TGZ və ya TAR.GZ ilə bitən fayllar üçün tar -xvzf istifadə edin.

## İstinadlar ##

* [TAR - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Tar_(computing))

* [TAR Basic Format](https://www.gnu.org/software/tar/manual/html_node/Standard.html)


