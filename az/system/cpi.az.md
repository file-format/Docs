{
   "date":"2023-10-18",
   "keywords":[
"cpi",
"cpi faylı",
"cpi kod səhifəsi məlumat faylı",
"cpi faylını necə açmaq olar",
"fayl",
"cpi fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CPI Fayl Format - Codepage Məlumat Faylı",
   "description":"CPI faylları yarada və aça bilən CPI Codepage Məlumat fayl formatı və API-lər haqqında öyrənin.",
   "linktitle":"CPI",
   "menu":{
      "docs":{
         "identifier":"system-cpi-az",
         "parent":"system"
}
},
   "lastmod":"2023-10-18"
}

## CPI faylı nədir?

Microsoft Windows və DOS əməliyyat sistemləri kontekstində olan `.cpi` faylı adətən **Kod Səhifəsi Məlumat Faylıdır.** Bu fayllar mətnin kodlaşdırılması və simvol dəstinin xəritələşdirilməsi üçün istifadə edilən kod səhifələri haqqında məlumatı ehtiva edir. Kod səhifələri müxtəlif dillərdə və simvol dəstlərində mətni göstərmək və emal etmək üçün vacibdir.

Windows və DOS kontekstində kod səhifələri simvolların müxtəlif dillərdə və bölgələrdə necə təmsil olunduğunu və kodlaşdırıldığını müəyyən etmək üçün istifadə olunur. Bu kod səhifələri simvolların yaddaşda necə saxlandığını və ekranda necə göstərildiyini müəyyən edir. Hər bir kod səhifəsinin unikal identifikatoru var və `.cpi` faylları simvol xəritələri və şrift məlumatı kimi təfərrüatlar daxil olmaqla, bu kod səhifələri haqqında məlumatı saxlayır.

`.cpi` faylları adətən Windows və ya DOS sistem qovluqlarında tapılır və onlar əməliyyat sisteminin müxtəlif dillər və simvol dəstləri üçün mətni düzgün göstərməsinə imkan yaratmaqda mühüm rol oynayır. Onlar sistemə müxtəlif dillərdən və kodlaşdırmalardan simvolları necə şərh etməyi və göstərməyi başa düşməyə kömək edir.

## Kod Səhifə Məlumat Faylları

Gəlin Kod Səhifəsi Məlumat Fayllarına (.cpi) və onların MS-DOS və Microsoft Windows-un əvvəlki iterasiyaları çərçivəsində necə işlədiyinə daha yaxından nəzər salaq:

1.  **Xarakterlərin Kodlanması və Kod Səhifələri**: Kod səhifələri mətnin necə kodlaşdırıldığını və kompüterdə necə göstərildiyinin mühüm komponentidir. Onlar xüsusi dil və ya simvol dəsti üçün simvol kodlamasını müəyyənləşdirirlər. Hər bir kod səhifəsi simvollara ədədi dəyərlər (kod nöqtələri) təyin edir, kompüterə onları təmsil etməyə və göstərməyə imkan verir. Məsələn, kod səhifəsi 437 adətən ABŞ və Qərbi Avropada istifadə olunur, kod səhifəsi isə 850 Latın-1 kodlaması üçün istifadə olunur.
    
2.  **Sistemin Başlanması**: Sistemin işə salınması zamanı (kompüter işə salındıqda), MS-DOS və Windows-un köhnə versiyaları hansı kod səhifələrinin dəstəklənəcəyini müəyyən etmək üçün `.cpi` fayllarını oxuyurdu. Bu məlumat mətnin göstərilməsi, klaviatura daxil edilməsi və simvol dəstinin çevrilməsi üçün çox vacib idi.
    
3.  **Ekran və Klaviatura Dəstəyi**: Bu fayllar simvolların ekranda necə göstərilməli olduğu və klaviatura daxil edilməsi üçün hansı simvol dəstlərinin və ya kod səhifələrinin dəstəklənəcəyi barədə məlumat verir. Fərqli kod səhifələri müxtəlif simvol dəstlərini müəyyənləşdirir, buna görə də bu fayllar əməliyyat sisteminə istifadəçi daxiletməsini necə idarə etməyi və mətni düzgün göstərməyi öyrənməyə kömək edir.
    
4.  **Lokallaşdırma**: `.cpi` faylları əməliyyat sisteminin lokallaşdırılması üçün vacibdir. Onlar sistemin müxtəlif dillərə, bölgələrə və simvol dəstlərinə uyğunlaşmasına imkan verir və bu, bütün dünya üzrə istifadəçilərə MS-DOS və ya Windows-dan öz seçdikləri dillərdə istifadə etməyə imkan verir.
    
5.  **Birdən çox `.cpi` Fayl**: Çoxdilli dəstəyi olan kompüterdə müxtəlif kod səhifələrinə uyğun gələn bir neçə `.cpi` faylı tapa bilərsiniz. Məsələn, sistem ABŞ üçün `437.cpi`, Latın-1 üçün `850.cpi`, Mərkəzi Avropa üçün `852.cpi` və s. ola bilər. Müvafiq fayl istifadəçinin dili və ya seçilmiş kod səhifəsi əsasında yüklənir.
    
6.  **Şrift Məlumatı**: Simvolların təsvirinə əlavə olaraq, bu fayllarda hər bir kod səhifəsi üçün hansı şriftlərin istifadə olunacağını göstərən şrift məlumatı ola bilər. Bu, mətni uyğun üslubda və ölçüdə göstərmək üçün vacibdir.
    
7.  **Legacy Systems**: `.cpi` faylları MS-DOS və Windows-un köhnə versiyalarında daha çox yayılmışdır. Müasir Windows versiyaları (məsələn, Windows 10 və sonrakı versiyalar) adətən geniş simvol və dilləri dəstəkləyən mətn kodlaşdırması üçün Unicode istifadə edir. Unicode çoxdilli mühitlər üçün mətn emalını asanlaşdırır və müasir proqram təminatı üçün standartdır.

## CPI faylını necə açmaq olar?

.CPI (Kod Səhifə Məlumatı) faylının açılması tipik istifadəçi hərəkəti deyil və bu faylların ümumiyyətlə əl ilə açılması nəzərdə tutulmur. Onlar əməliyyat sistemi tərəfindən mətn kodlaşdırması və simvol dəstlərini idarə etmək üçün istifadə olunur və onların məzmunu sistem tərəfindən avtomatik olaraq əldə edilir və istifadə olunur.

Bununla belə, məlumat məqsədləri üçün .CPI faylının məzmununa baxmaqla maraqlanırsınızsa, onu mətn redaktoru və ya onaltılıq görüntüləyici ilə açmağa cəhd edə bilərsiniz. .CPI faylını necə açmağa cəhd edə bilərsiniz:

1.  **Mətn Redaktoru**: Siz .CPI faylını açmaq və baxmaq üçün Notepad (Windows-da) və ya digər əməliyyat sistemlərində istənilən düz mətn redaktoru kimi mətn redaktorundan istifadə edə bilərsiniz. Nəzərə alın ki, .CPI fayllarının məzmunu insanlar tərəfindən oxuna bilər və siz şərhi çətin olan simvollar seriyasını görə bilərsiniz.
    
2.  **Hexadecimal Viewer**: Hexadecimal Viewer və ya hex redaktor .CPI faylının məzmununu ikili formada açmaq və yoxlamaq üçün istifadə edilə bilər. Hex redaktorları fayl məlumatlarının daha təfərrüatlı görünüşünü təmin edir, bu da onun strukturunu anlamağa çalışdığınız zaman faydalı ola bilər. Belə proqram təminatına misal olaraq HxD, Hex Fiend (macOS üçün) və 010 Editor daxildir.

## Digər CPI faylları

**.cpi** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Video və Sistem**
- [CPI - AVCHD Video Clip Information](/video/cpi/)
- [CPI - Codepage Information File](/system/cpi/)

## İstinadlar
* [Kod səhifəsi](https://en.wikipedia.org/wiki/Code_page)


