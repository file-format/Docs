{
  "date": "2021-06-16",
  "keywords": [
"CDB",
"uzadılması",
"cdb faylı",
"cdb fayl formatı",
"Verilənlər bazası fayl növü",
"Verilənlər bazası fayl formatı",
"cdb faylı nədir"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "CDB fayl formatı və CDB faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "CDB - Daimi verilənlər bazası faylı",
  "linktitle": "CDB",
  "menu": {
    "docs": {
      "parent": "database",
      "identifier": "database-cd-azb"
}
},
  "lastmod": "2021-06-16"
}

## CDB faylı nədir?
CDB faylları e-poçt kimi kritik proqramlarda istifadə olunur. CDB daimi verilənlər bazası yaratmaq və ya oxumaq üçün sürətli, etibarlı və sadə paket olan sabit verilənlər bazası deməkdir. Verilənlər bazasının dəyişdirilməsi sistem qəzalarına qarşı təhlükəsizdir. Yenidən yazma zamanı istifadəçilərin fasilə verməsi lazım deyil. CDB assosiativ massiv (diskdə) kimi çıxış edir, açarları dəyərlərə uyğunlaşdırır və birdən çox dəyərin bir açarda saxlanmasına imkan verir.

## CDB fayl formatı

CDB fayl formatı rəqəmləri, ofsetləri, uzunluqları və hash dəyərləri kiçik endian formatında işarəsiz 32 bitlik tam ədədlər kimi saxlayır. Açarların və verilənlərin heç bir xüsusi işlənmədən qeyri-şəffaf bayt sətirləri olduğu düşünülür. Verilənlər bazasının əvvəlində sabit ölçülü başlıq fayldakı mövqelərini və uzunluqlarını yuvalarda qeyd etməklə 256 hash cədvəlini təmsil edir. Adətən məlumatlar qeydlər ardıcıllığı kimi saxlanılır, hər bir qeyd açarın uzunluğunu, məlumatların uzunluğunu, açarı və məlumatları saxlayır. Çeşidləmə və ya uyğunlaşdırma qaydaları yoxdur. Qeydlərdən sonra müxtəlif uzunluqlu 256 hash cədvəli dəsti gəlir. Sıfır etibarlı uzunluq olduğundan, verilənlər bazasında fiziki olaraq saxlanılan 256-dan az hash cədvəli ola bilər, lakin 256 cədvəl hesab edilən heç bir şey yoxdur. Hash cədvəlləri hər birində hash dəyəri və rekord ofset olan bir sıra slotlardan ibarətdir. Boş yuvalar sıfır ofsetinə malikdir.

### CDB Fayl Formatının Strukturu

CDB verilənlər bazası bir kompüter faylında bütün verilənlər toplusundan ibarətdir. Üç hissədən ibarətdir:
- Sabit ölçülü başlıq
- Məlumat
- Hash masalar dəsti.

Axtarışlar yalnız dəqiq açarlar üçün mümkündür. Axtarışlar aşağıdakı alqoritmdən istifadə edərək hərəkət edir:

- Açarı haşlayın.
- Bu qeydin hansı hash cədvəlində və yuvasında yerləşəcəyini müəyyənləşdirin.
- Hash cədvəlində göstərilən yuvanı sınayın.

Birdən çox dəyəri olan açarların axtarışları üçün, sadəcə növbəti yuvada axtarışı davam etdirməklə əlavə dəyərlər tapıla bilər.

#### Xüsusiyyətləri

CDB verilənlər bazası strukturu bir sıra xüsusiyyətləri təmin edir:

##### Sürətli axtarışlar
Nəhəng verilənlər bazasında uğurlu axtarış adətən yalnız iki diskə daxil olur, uğursuz axtarış isə yalnız bir vaxt aparır.
##### Aşağı yük
Verilənlər bazası 2048 baytdan, hər qeyd üçün 24 baytdan və açarlar və məlumatlar üçün yerdən istifadə edir.
##### Təsadüfi məhdudiyyət yoxdur
CDB 4 giqabayta qədər istənilən verilənlər bazasını idarə edə bilər. Başqa heç bir məhdudiyyət olmadığı üçün qeydlərin yaddaşa sığması belə lazım deyil. Verilənlər bazaları maşından asılı olmayan formatda saxlanılır.
##### Tez atom verilənlər bazası dəyişdirilməsi
**cdbmake** əmri bütün verilənlər bazasını digər hashing paketlərindən daha sürətli iki böyüklük sırasına yenidən yaza bilər.
##### Sürətli verilənlər bazası zibilləri
**cdbdump** verilənlər bazasının məzmununu cdbmake-ə uyğun formatda çap edə bilər.


## İstinadlar ##

* [cdb (software) - Wikipedia](https://en.wikipedia.org/wiki/Cdb_(software))
* [CDB specification](http://cr.yp.to/cdb.html)
