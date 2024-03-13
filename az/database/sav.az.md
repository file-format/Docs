{
  "date" : "2021-06-14",
  "keywords" : [ "SAV", "extension", "sav file", "sav file format", "Database File Type", "Database File Format", "what is a sav file" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" : "SAV faylları yarada və aça bilən SAV fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "SAV - SPSS məlumat faylı",
  "linktitle" : "SAV",
  "menu" : {
    "docs" : {
      "identifier":"database-sav-az",
      "parent" : "database"
}
},
  "lastmod" : "2021-06-14"
}

## SAV faylı nədir?
SAV faylı Sosial Elmlər üçün Statistika Paketi (SPSS) tərəfindən yaradılmış məlumat faylıdır, bu proqram bazar tədqiqatçıları, səhiyyə tədqiqatçıları, sorğu şirkətləri, hökumət, təhsil tədqiqatçıları, marketinq təşkilatları, statistik təhlil üçün məlumat mədənçiləri tərəfindən geniş istifadə olunur. SAV xüsusi ikili formatda saxlanılır və verilənlər dəstindən, həmçinin verilənlər dəstini təmsil edən lüğətdən ibarətdir, məlumatları satır və sütunlarda saxlayır.

## SAV fayl formatı
SAV fayl formatı nisbətən sabit hala gəldi, lakin biz onu statik deyə bilmərik. Geri və irəli uyğunluq lazım olduqda isteğe bağlı olaraq mövcuddur, lakin düzgün saxlanılmır. SAV faylındakı məlumatlar aşağıdakı bölmələrə bölünür:

### Fayl başlığı
176 baytdan ibarətdir. İlk 4 bayt fayl üçün istifadə olunan simvol kodlaşdırmasında **$FL2** və ya **$FL3** sətrini göstərir. Son üç bayt fayldakı məlumatların **ZLIB** istifadə edərək sıxıldığını göstərir. Növbəti 60 baytlıq sətir **@(#) SPSS DATA FILE** ilə başlayır və həmçinin faylı yaradan əməliyyat sistemini və SPSS versiyasını müəyyən edir. Başlıq daha sonra hər müşahidə üçün dəyişənlərin sayını və sıxılma üçün rəqəm kodunu ehtiva edən altı rəqəmli sahə ilə davam edir və yaradılma tarixini və vaxtını və fayl etiketini göstərən simvol məlumatları ilə bitir.
### Dəyişən deskriptor qeydləri
Qeyd, SPSS tərəfindən istifadə olunan formatlaşdırma məlumatı ilə birlikdə dəyişənin tipini və adını təsnif edən sabit sahələr ardıcıllığını ehtiva edir. Hər bir dəyişən qeyd isteğe bağlı olaraq 120 simvola qədər dəyişən etiketi və üçə qədər çatışmayan dəyər spesifikasiyasını ehtiva edə bilər.
### Dəyər etiketləri
The value labels are optional and stored in pairs of records with integer tags 3 and 4. Teq 3 olan ilk qeyddə hər bir cütdə bir dəyər və əlaqəli dəyər etiketi olan sahə cütləri ardıcıllığı var. Teq 4 olan ikinci qeyd dəyər/etiket dəstinin hansı dəyişənlərə aid olduğunu göstərir.
### Sənədlər
Single or multiple records with integer tag 6. Könüllü sənədlər. 80 simvoldan ibarət sətirlərdən ibarətdir.
### Genişləndirmə qeydləri
Single or multiple records with integer tag 7. Artırma qeydləri təhlükəsiz şəkildə nəzərə alına bilən, lakin qorunan məlumatı təmin edir, bir çox hallarda geriyə uyğunluğu qorumaq üçün daha yeni proqram təminatı tərəfindən yazılmış fayllara imkan verir. Genişləndirmə qeydlərində tam ədəd alt tipli teqlər var.
### Lüğət terminatoru
Only record with integer tag 999. O, lüğəti məlumat müşahidələrindən ayırır.
### Məlumat müşahidələri
Məlumat müşahidə qaydasında olduğu üçün hesab edilir, məsələn, birinci müşahidə üçün bütün dəyişən dəyərlər, ardınca ikinci müşahidə üçün bütün dəyərlər və s. Məlumat qeydinin formatı fayl başlığı qeydindəki sıxılma kodundan asılı olaraq dəyişir. .sav faylının məlumat hissəsi sıxıla bilər:
- **kod 0**: bayt kodu ilə sıxılmışdır
- **kod 1**: ZLIB sıxılması ilə sıxılmışdır
 






## İstinadlar ##

* [SPSS Sistem Məlumat Faylı Format Ailəsi (.sav)](https://www.loc.gov/preservation/digital/formats/fdd/fdd000469.shtml)


