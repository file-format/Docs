{
  "date": "2019-10-11",
  "keywords": [
"emf faylı",
"emf fayl formatı",
"emf faylı nədir",
"fayl",
"emf nümunəsi",
"emf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EMF - Təkmilləşdirilmiş metafayl formatı",
  "description": "EMF fayl formatı və EMF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "EMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-em-azf"
}
},
  "lastmod": "2019-09-10"
}

## EMF faylı nədir?

**Təkmilləşdirilmiş metafayl formatı (EMF)** qrafik şəkilləri cihazdan asılı olmayaraq saxlayır. EMF-nin metafaylları xronoloji ardıcıllıqla dəyişən uzunluqlu qeydlərdən ibarətdir ki, onlar istənilən çıxış cihazında təhlil edildikdən sonra saxlanılan təsviri göstərə bilirlər. Bu dəyişən uzunluqlu qeydlər qapalı obyektlərin tərifləri, rəsm üçün əmrlər və təsviri dəqiq göstərmək üçün vacib olan qrafik xüsusiyyətləri ola bilər. Cihaz öz qrafik mühitindən istifadə edərək EMF metafaylını açdıqda, açılış cihazının platformasından asılı olmayaraq orijinal təsvirin nisbətləri, ölçüləri, rəngləri və digər qrafik xüsusiyyətləri eyni qalır.

## Qısa tarix ##

1990-cı ildə Microsoft, Microsoft Windows üçün Windows Metafayl ([WMF](/image/wmf/)) şəkil faylı formatını hazırladı. Windows Metafaylları bəzi bitmap komponentlərini ehtiva edə bilən 16 bitlik formatdır. WMF vektor qrafikasından ibarət ola bilər və müxtəlif proqramlar arasında portativ saxlamaq üçün nəzərdə tutulub. 1993-cü ildə Win32/GDI təkmilləşdirilmiş çeviklik və genişlənmə qabiliyyətinə malik daha yeni versiya olan Təkmilləşdirilmiş Metafayı (EMF) elan etdi. EMF həmçinin printer drayverlərini işə salmaq üçün qrafik dili əmrləri kimi istifadə olunur. Microsoft indi Windows formatı (WMF) üzərində təkmilləşdirilmiş metafayl formatını (EMF) tövsiyə edir. Windows XP təqdim edildikdə, Enhanced Metafile Format Plus (EMF+) versiyası buraxıldı. Bu daha yeni versiya GDI+ API zənglərini, eynilə WMF/EMF zənglərini GDI-yə qeyd etməklə öz yolunu tapır. EMZ kimi tanınan EMF-nin gzip sıxılmış versiyası mövcuddur.

## EMF metafayl formatı ##

Təkmilləşdirilmiş metafayl formatının əsas elementləri aşağıdakılardır:

* EMR_HEADER (versiya, ölçü, yaradılan şəklin həlli)

* GDI obyektləri üçün cədvəl

* Qorunan palitra (isteğe bağlı)

* Massiv strukturunda düzülmüş metafayl qeydləri (xüsusiyyət parametrləri, müəyyən edilmiş obyektlər, rəsm əmrləri)

* EMR_EOF qeydi (EMF metafaylında son qeyd)


## EMF versiyaları ##
* **Orijinal**: Orijinal versiya orijinal şəkli saxlamaq və cihazdan müstəqil saxlamaq üçün lazım olan qeydi müəyyən edir. Bundan əlavə, qrafik obyektləri və rəsm üçün əmrləri ehtiva edən qeydləri dəstəkləyir.

* **Versiya 1**: EMF-nin ikinci versiyası piksel formatı üçün rekord əlavə etməklə və OpenGL əmrindən istifadə təmin etməklə çevikliyi və cihazın müstəqilliyini təkmilləşdirdi.

* **Versiya 2**: Üçüncü versiya, cihazın səthi məsafələrini ölçmək üçün Metrik sistemi əlavə edərək, rekordu daha miqyaslı buraxaraq dəqiqliyi artırdı.


## Təkmilləşdirilmiş Metafayl Qeydləri ##

Metafayl qeydləri massiv şəklində düzülür. Bu qeydlər ENHMETARECORD strukturuna malikdir və uzunluğu dəyişəndir. ENHMETARECORD təkmilləşdirilmiş metafayl formatından istifadə edərək şəkil yaratmaq üçün GDI funksiyalarını təyin edən məlumatları təyin edir. **ENHMETAHEADER** strukturu həmişə bu formatda ilk qeyddir. Bu EMF başlığı aşağıdakı məlumatları ehtiva edir.

Every record of enhanced metafile has two members of EMR (provides the base structure) in the beginning. The first member recognizes GDI function (parameters are used in record) which determines the type of record and is known as iType. The other member nSize define the size of each record. Remaining parameters (if any) and additional data arranged immediately below nSize. Immediately following the header an optional text description may present. The name of picture and author is recorded in that text description. The palette whose presence is an option specifies the colors used in enhanced metafile creation. The other records used to specify the GDI function which is essential in picture creation.

Hər metafaylda ən azı bir EMF qeydi olmalıdır. Bir qeyddən digərinə keçid məlumatı EMF qeydlərindən asılıdır, ona görə də bu qeydlər bitişik şəkildə yerləşdirilməlidir. EOF_record istisna olmaqla, metafaylda hər hansı bir qeyddə həmin xüsusi qeydin uzunluğu növbəti qeydə keçməyi müəyyən edir.

## Təkmilləşdirilmiş Metafayl Yaradılması ##

**CreateEnhMetaFile** funksiyası təkmil metafayl yaratmaq üçün istifadə olunur. Bu funksiyaların arqumentləri diskdə/yaddaşda şəklin ölçüləri və saxlanması üçün istifadə olunur. Bundan əlavə, bu funksiya şəklin ilk göründüyü cihazın ölçüsünü (istinad edilən cihaz) və istinad cihazının (DC) kontekstini tələb edir. Beləliklə, bu DC-ni idarə etmək üçün arqumentlər **CreateEnhMetaFile** funksiyasını çağırarkən təmin edilməlidir. Funksiya sintaksisi aşağıdakı kimidir:
```
HDC CreateEnhMetaFileExample(

  HDC        hdc,

  LPCSTR     lptoFilename,

  const OVAL *lprc,

  LPCSTR     lpDesc

);
```
**HDC:** istinad cihazı ilə əlaqə saxlayın.

**lptoFilename:** Fayl adına göstərici.

**lprc:** Oval strukturun göstəricisi şəkil ölçülərini mm ilə müəyyən edir.

**lpDesc:**  a pointer to a string for the title of picture and application name that created the picture.

## Təkmilləşdirilmiş metafayl əməliyyatları ##

Aşağıda təkmilləşdirilmiş metafaylın idarəedicisindən istifadə etməklə yerinə yetirilə bilən işlər verilmişdir.

* Saxlanılan şəkli göstərin və redaktə edin.

* Təkmil metafayl nüsxələrini yaradın.

* Retrieve the copy of an EMF header, optional description and binary version of an enhanced metafile
* Palitradakı rəngləri təkrarlayın.


## Qrafik Obyektlər ##

Rəsm və rəngləmə əməliyyatlarında qrafik obyektləri obyekt yaratma qeydləri ilə yaradıla və sonrakı istifadə üçün saxlaya bilər. `EMR_SELECTOBJECT` qeydi oxutma cihazı kontekstindən istifadə edərək bu qrafik obyektləri əldə edə bilər. Qələmlər, palitralar, fırçalar, rəng boşluqları, şriftlər və fond obyektləri bəzi təkrar istifadə edilə bilən obyekt növləridir.

## Bayt Sifarişi ##

Little-endian formatı metafayl qeydlərində məlumatları saxlamaq üçün istifadə olunur.

## Versiya ##

The EMF file format has been revised twice. The changed versions are original, extension 1, and extension 2. Genişləndirilmiş versiyalarda OpenGL qeydləri və daxili piksel formatı üçün əlavə deskriptor var. Göstərilən ölçülər üçün mililitrlərdə ölçmə qurğusu əlavə olunur.

## İstinadlar ##

* [Təkmilləşdirilmiş Formatlı Metafayllar | Microsoft Sənədləri](https://learn.microsoft.com/en-us/windows/desktop/gdi/enhanced-format-metafiles)

* [Təkmilləşdirilmiş metafayl formatı və spesifikasiyası](https://msdn.microsoft.com/en-us/library/cc230514.aspx)


