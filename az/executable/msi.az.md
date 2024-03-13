{
  "date": "2021-06-30",
  "keywords": [
"msi faylı",
"MSI fayl formatı",
"msi faylı nədir",
"fayl",
"msi nümunəsi",
"msi fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "MSI faylları yarada və aça bilən MSI fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "MSI - Windows Quraşdırıcı Paket Faylı",
  "linktitle": "MSI",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-azi"
}
},
  "lastmod": "2021-06-30"
}

## MSI faylı nədir?
Windows proqramlarını quraşdırmaq və işə salmaq üçün istifadə olunan MSI faylı; quraşdırılacaq əsas fayllar və quraşdırma yeri haqqında məlumat daxil olmaqla, tipik proqram proqramı üçün quraşdırma məlumatlarını ehtiva edən Microsoft Windows üçün tam paket. MSI faylları proqram yeniləmələri paketini də ehtiva edə bilər. MSI faylları [EXE](/executable/exe/) faylına bənzəyir, lakin EXE bəzən quraşdırıcı məlumatını ehtiva etməyə bilər və proqram proqramı EXE faylını icra edərkən birbaşa işləyə bilər.

## MSI fayl formatı
Windows Quraşdırıcısı əslində bir API (Tətbiq Proqramlaşdırma İnterfeysi) və proqram proqramının quraşdırılması, çıxarılması və saxlanması üçün istifadə olunan Microsoft Windows-un proqram komponentidir. Quraşdırma məlumatı və isteğe bağlı fayllar quraşdırma paketləri və COM Strukturlaşdırılmış Yaddaşlar kimi strukturlaşdırılmış sərbəst əlaqəli verilənlər bazaları kimi qablaşdırılır; .msi fayl uzantısına malik olan **MSI faylları** kimi tanınır. Fayl uzantısı **.mst** olan paketlər Windows Installer proqramının **Transformasiya Skriptlərini**, **.msm** uzantılı fayllar isə **Modulları birləşdirin** və fayl genişləndirilməsi **.pcp** ehtiva edir. **Yamaq Yaratma Xüsusiyyətləri** üçün istifadə olunur. Windows Installer əvvəlki versiyaları olan Setup API-dən əhəmiyyətli dəyişikliklər etdikdən sonra daha təkmilləşir. GUI çərçivəsi və quraşdırma silmə ardıcıllığının avtomatik yaradılması Windows Installer proqramının yeni xüsusiyyətləridir. İndi o, müstəqil icra edilə bilən quraşdırıcı çərçivələrə alternativ kimi nəzərdən keçirilir.

### MSI paketlərinin məntiqi strukturu
Paket bir və ya bir neçə tam məhsulun quraşdırılmasını təyin edir və ümumiyyətlə **GUID** ilə müəyyən edilir. Məhsul bir və ya bir neçə komponentdən ibarətdir və müxtəlif xüsusiyyətlərə görə qruplaşdırılır. Windows Quraşdırıcısı müxtəlif məhsullar arasındakı asılılıqları eyni vaxtda idarə etmir. Paketlərin məntiqi strukturu aşağıdakı elementlərdən ibarətdir:

- **Məhsullar**: Tək, quraşdırılmış, işləyən proqram və ya birlikdə birləşdirilmiş çoxsaylı proqramlar dəsti məhsuldur. Məhsul unikal GUID tərəfindən müəyyən edilir.
- **Xüsusiyyətlər**: İstənilən sayda komponent və digər alt funksiyalar ola bilər. Kiçik paketlər bir xüsusiyyətdən ibarət ola bilər.
- **Komponentlər**: Komponent Windows Installer tərəfindən vahid kimi qəbul edilir; proqram faylları, qovluqlar, qeyd dəftəri açarları, COM komponentləri və qısa yollardan ibarət ola bilər.
- **Key Paths**: A key path is a specific file, ODBC data source, or registry key that the package author specifies as critical for a given component.

## İstinadlar 

* [Windows Quraşdırıcısı - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Windows_Installer)



