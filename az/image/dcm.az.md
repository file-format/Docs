{
  "date": "2019-10-11",
  "keywords": [
"dcm faylı",
"dcm fayl formatı",
"dcm faylı nədir",
"fayl",
"dcm nümunəsi",
"dcm fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DCM Fayl Format - Rəqəmsal Tibbi Məlumat Faylı",
  "description": "DCM faylları yarada və aça bilən DCM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DCM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dc-azm"
}
},
  "lastmod": "2021-07-03"
}

## DCM faylı nədir?

.dcm uzantılı fayllar MRT, CT taramaları və ultrasəs şəkilləri kimi xəstələrin tibbi məlumatlarını saxlayan rəqəmsal təsviri təmsil edir. DCM faylları [DICOM](/image/dicom/) (Tibbdə Rəqəmsal Təsvir və Kommunikasiyalar) şəkil faylı formatından istifadə edir və istinad üçün xəstə məlumatını daxil edə bilər. O, [National Electrical Manufacturers Association](https://en.wikipedia.org/wiki/National_Electrical_Manufacturers_Association) (NEMA) tərəfindən işlənib hazırlanmışdır və tibbi təsvirlərin yayılması və baxılması üçün təsvir faylı formatını standartlaşdırmaq üçün nəzərdə tutulmuşdur.

## DCM Fayl Format

DCM faylları məlumatı DICOM şəkil formatında saxlayır. Bu fayllar DICOM IOD ilə əlaqəli SOP nümunəsini təmsil edən real dünya məlumatı olan Data Setini saxlayır. DICOM Fayl Meta Məlumatı faylda saxlanılır, ondan sonra faktiki məlumat dəstinin bayt axını.

### DICOM Fayl Meta Məlumatı ##

Hər bir DICOM faylı kapsullaşdırılmış məlumat dəsti üçün identifikasiya məlumatı başlığını ehtiva edir:
   * 128 baytlıq Fayl Preambula
   * 4 bayt DICOM prefiksi
   * Fayl Meta Elementləri

Bu başlıq hər bir DICOM faylı üçün zəruridir.

### Fayl Meta Elementləri ###
|Atributun Adı|Tag|Növü| Atribut Təsviri
---|---|---|---|
|Fayl Preambula|Teq və ya Uzunluq Sahələri Yox|1|Tətbiq Profili və ya tətbiqin müəyyən edilmiş istifadəsi üçün mövcud olan sabit 128 bayt sahə. Tətbiq Profili və ya xüsusi tətbiq tərəfindən istifadə edilmirsə, bütün baytlar 00H-ə təyin edilməlidir. Fayl dəsti Oxucular və ya Yeniləyicilər bu Faylın DICOM faylı olub-olmadığını müəyyən etmək üçün bu Preambulanın məzmununa etibar etməməlidirlər.
|DICOM Prefiksi|Teq və ya uzunluq sahələri yoxdur|1|DICM simvol sətirini ehtiva edən dörd bayt. Bu Prefiks bu Faylın DICOM Faylı olub olmadığını tanımaq üçün istifadə olunmaq üçün nəzərdə tutulub.
|Fayl Meta Məlumat Qrupu Uzunluğu|(0002,0000)|1|Qrup 2 Fayl Meta Məlumatının son Fayl Meta Elementinə qədər və bu Fayl Meta Elementindən sonra (Dəyər sahəsinin sonu) baytların sayı
|File Meta Information Version|(0002,0001)|1|This is a two byte field where each bit identifies a version of this File Meta Information header. In version 1 the first byte value is 00H and the second value byte value is 01H.Implementations reading Files with Meta Information where this attribute has bit 0 (lsb) of the second byte set to 1 may interpret the File Meta Information as specified in this version of PS3.10. Bütün digər bitlər yoxlanılmamalıdır.
|Media Storage SOP Class UID|(0002,0002)|1|Məlumat Dəsti ilə əlaqəli SOP Sinifini unikal şəkildə müəyyən edir. Media saxlanması üçün icazə verilən SOP Sinif UID-ləri PS3.4 - Media Storage Application Profiles-də göstərilmişdir.
|Media Saxlama SOP Nümunəsinin UID|(0002,0003)|1|Faylda yerləşdirilmiş və Fayl Meta Məlumatından sonra Data Dəsti ilə əlaqəli SOP Nümunəsini unikal şəkildə müəyyən edir.
|Transfer Sintaksisi UID|(0002,0010)|1|Aşağıdakı Məlumat Dəstini kodlaşdırmaq üçün istifadə edilən Transfer Sintaksisini unikal şəkildə müəyyən edir. Bu Transfer Sintaksisi Fayl Meta Məlumatına tətbiq edilmir.
|Implementation Class UID|(0002,0012)|1|Bu faylı və onun məzmununu yazan tətbiqi unikal şəkildə müəyyənləşdirir. O, mübadilə problemləri zamanı faylı sonuncu dəfə yazan icra növünün birmənalı identifikasiyasını təmin edir.
|İmplementasiya Versiyasının Adı|(0002,0013)|3|Repertuarın ən çox 16 simvolundan istifadə edərək İcra Sinfi UID (0002,0012) üçün versiyanı müəyyən edir.
|Mənbə Tətbiq Müəssisəsinin Başlığı|(0002,0016)|3|Bu faylın məzmununu yazan (və ya onu sonuncu dəfə yeniləmiş) AE-nin DICOM Tətbiq Müəssisəsi (AE) Başlığı. İstifadə olunarsa, media mübadiləsi problemləri zamanı səhvlərin mənbəyini izləməyə imkan verir.
|Private Information Creator UID|(0002,0100)|3|Şəxsi məlumatın yaradıcısının UID-i (0002,0102).
|Şəxsi Məlumat|(0002,0102)|1C|Meta Məlumat Faylında yerləşdirilən Şəxsi Məlumatı ehtiva edir. Yaradıcı (0002,0100) bəndində müəyyən edilməlidir. Şəxsi Məlumat Yaradan UID (0002,0100) mövcud olduqda tələb olunur.

### Data Set Encapsulation ###

DICOM faylı tək bir SOP Sinfi ilə əlaqəli bir SOP Nümunəsini təmsil edən tək Data Setdən ibarətdir. DICOM Fayl Meta Məlumatının Transfer Sintaksisinin UİD-i Data Setini kodlaşdırmaq üçün istifadə edilən Transfer Sintaksisini müəyyən etməlidir.

### Fayl İdarəetmə Məlumatına Dəstək ###

Media Format Layeri verilmiş DICOM Tətbiq Profili üçün lazım olduqda aşağıdakı Fayl İdarəetmə Məlumatını təmin edir.

  * Fayl məzmunu sahibinin identifikasiyası

  * Fayl giriş statistikası (məsələn, yaradılma tarixi və vaxtı)

  * Tətbiq faylına giriş nəzarəti

  * Fiziki media girişinə nəzarət (məsələn, yazmadan qorunma)

## İstinadlar ##
  * [DICOM Standard](https://www.dicomstandard.org/current/)
  * [DICOM Fayl Formatı](https://dicom.nema.org/dicom/2013/output/chtml/part10/chapter_7.html)

