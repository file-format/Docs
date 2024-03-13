{
  "date": "2019-12-09",
  "keywords": [
"zip faylı",
"zip fayl formatı",
"zip faylı nədir",
"fayl",
"zip nümunəsi",
"zip fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "ZIP",
  "description": "ZIP faylları yarada və aça bilən ZIP faylı və API nədir.",
  "linktitle": "ZIP",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-zi-azp"
}
},
  "lastmod": "2019-12-09"
}

## ZIP faylı nədir? ##

A file with .zip extension is an archive that can hold one or more files or directories. The archive can have compression applied to the included files in order to reduce the ZIP file size. ZIP file format was made public back in February 1989 by Phil Katz for achieving archiving of files and folders. The format was made part of [PKZIP](https://www.pkware.com/pkzip) utility, created by PKWARE, Inc. Right after the availability of [available specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT), many companies made ZIP file format part of their software utilities including Microsoft (since Windows 7), Apple (Mac OS X ) and many others.

## ZIP Fayl Formatının Qısa Tarixi

ZIP fayl formatının tarixçəsi System Enhancement Associates (SEA) tərəfindən PKWARE-yə qarşı ARC yardım proqramından ticarət nişanı və məhsulun görünüşü və istifadəçi interfeysinin müəllif hüquqları icazəsi olmadan istifadə etdiyinə görə qaldırdığı məhkəmə iddiası ilə bağlıdır. Bundan əvvəl Phil Katz SEA-nın mənbə kodunu yenidən yazmış və MS-DOS əsaslı sistemlər üçün pulsuz proqram kimi ARC çıxaran PKXARC və fayl kompressoru olan PKARC-ni buraxmışdı. Məhkəməyə uduzaraq, PKWARE artıq ARC ilə əlaqəli heç bir şeydən istifadə edə bilmədi. PKWARE, Inc-də PKZIP yardım proqramının bir hissəsi olan ZIP adlanan yeni bir fayl sıxışdırmasının yaradılması burada baş verdi.

Katz sıkıştırma və çıxarma yardım proqramı, yəni PKZIP üzərində mülkiyyət hüquqlarını saxlamaqla, ZIP fayl formatının spesifikasiyalarını ictimai domenə buraxdı. ZIP sıxılma sistemi fayl ölçülərini sıxışdırmaq üçün 32 bitlik siklik ehtiyat yoxlaması ([CRC](https://en.wikipedia.org/wiki/Cyclic_redundancy_check)) alqoritmi vasitəsilə qovluqdakı faylları arxivləşdirə bilirdi (və edir). ARC-dən fərqli olaraq, .ZIP qovluqları, sıxılmış faylları göstərmək üçün lazım olan məlumatları özündə saxlayan, kriptoqrafın kod kitabçası rolunu oynayan kataloq faylını ehtiva edirdi.

## ZIP-də dəstəklənən sıxılma üsulları

.ZIP Fayl Formatının spesifikasiyasına uyğun olaraq, aşağıdakı sıxılma üsulları dəstəklənir.

* Mağaza - heç bir sıxılma nəzərdə tutur

* Büzülmək

* Azaltma (Bu, 1-ci səviyyədən 4-cü səviyyəyə qədər dəyişən sıxılma amillərini nəzərdə tutur)

* Implode

* Söndürmək

* Deflat64

* BZIP2

* LZMA (EFS)

* WavPack

* PPMd I versiyası, Rev 1


DEFLATE is the commonly used compression method which is a lossless date compression algorithm that uses a combination of the LZ77 and Huffman coding and is detailed in [RFC 1951](https://tools.ietf.org/html/rfc1951).

## ZIP Fayl Formatının Xüsusiyyətləri

ZIP faylları müxtəlif sıxılma üsullarından istifadə edərək birdən çox faylı saxlamaq imkanına malikdir, eyni zamanda faylın sıxılmadan saxlanmasını dəstəkləyir. Hər bir fayl fərdi olaraq saxlanılır/sıxılır ki, bu da bütün arxivə sıxılma və ya dekompressiya tətbiq etmədən onları çıxarmağa və ya yenilərini əlavə etməyə kömək edir.

### Ümumi ZIP Fayl Format

Hər bir Zip faylı aşağıdakı şəkildə qurulur:


|ZIP Fayl formatı
---|
|Yerli Fayl Başlığı 1
|Fayl Məlumatı 1
|Məlumatların təsviri 1
|Yerli Fayl Başlığı 2
|Fayl Məlumatı 2
|Məlumatların təsviri 2
| ....
| ....
|Yerli Fayl Başlığı N
|Fayl Məlumatı N
|Məlumatların təsviri N
|Arxiv Deşifrə Başlığı
|Arxiv əlavə məlumat qeydi
|Mərkəzi Kataloq

ZIP fayl formatı arxivləşdirmə məqsədi ilə 32 bitlik CRC alqoritmindən istifadə edir. Sıxılmış faylları göstərmək üçün ZIP arxivi sonunda arxiv faylında olan faylların girişini və onların yerini saxlayan bir qovluq saxlayır. Beləliklə, sıxılmış faylları göstərmək üçün lazım olan məlumatları əhatə etmək üçün kodlaşdırma rolunu oynayır. ZIP oxucuları bütün ZIP arxivini oxumadan faylların siyahısını yükləmək üçün kataloqdan istifadə edirlər. Bu format məlumat itkisinə qarşı daha çox qorunma təmin etmək üçün kataloq strukturunun ikili nüsxəsini saxlayır.

ZIP arxivindəki hər bir fayl fərdi giriş kimi təqdim olunur, burada hər bir giriş Yerli Fayl Başlığından və ardınca sıxılmış fayl datasından ibarətdir. Arxivin sonundakı Kataloq bütün bu fayl qeydlərinə istinadları saxlayır. ZIP faylı oxuyucuları yerli fayl başlıqlarını oxumaqdan çəkinməlidirlər və bütün növ fayl siyahısı Kataloqdan oxunmalıdır. Bu Kataloq arxivdəki etibarlı fayl qeydləri üçün yeganə mənbədir, çünki fayllar arxivin sonuna da əlavə edilə bilər. Odur ki, oxucu ZIP arxivinin yerli başlıqlarını əvvəldən oxuyarsa, o, arxivdən silinən Kataloqun bir hissəsi olmayan etibarsız (silinmiş) qeydləri də oxuya bilər.

Mərkəzi kataloqdakı fayl qeydlərinin sırası arxivdəki fayl qeydlərinin sırası ilə üst-üstə düşməməlidir.

### ZIP fayl girişləri

ZIP faylındakı qeydlər bir-birinin ardınca düzülür, burada hər bir giriş aşağıdakılardan ibarətdir:

* Yerli Fayl Başlığı

* Könüllü Əlavə Məlumat Sahələri

* İstifadəçi məlumatları (istəyə görə sıxılmış/istəyə görə şifrələnmiş)


Hər bir girişin Yerli Fayl Başlığı şərh, fayl ölçüsü və fayl adı kimi fayl haqqında məlumatı təmsil edir. Əlavə məlumat sahələri (isteğe bağlı) ZIP formatının genişlənmə variantları üçün məlumatı yerləşdirə bilər.

#### Yerli Fayl Başlığı

Yerli Fayl Başlığı çox bayt dəyərlərindən ibarət xüsusi sahə strukturuna malikdir. Bütün dəyərlər kiçik endian bayt sırasında saxlanılır, burada sahə uzunluğu baytlarda uzunluğu hesablayır. ZIP faylındakı bütün strukturlar hər bir fayl girişi üçün 4 baytlıq imzalardan istifadə edir. Mərkəzi kataloq imzasının sonu 0x06054b50-dir və öz unikal imzasından istifadə etməklə fərqləndirilə bilər. Aşağıda Yerli Fayl Başlığında saxlanılan məlumatların sırası verilmişdir.


|Ofset|Bayt|Təsvir
---|---|---|
|0|4|Yerli fayl başlığı imzası # 0x04034b50 (kiçik endian nömrə kimi oxunur)
|4|2|Çıxarış üçün lazım olan versiya (minimum)
|6|2|Ümumi təyinatlı bit bayrağı
|8|2|Sıxılma üsulu
|10|2|Faylın son dəyişiklik vaxtı
|12|2|Faylın son dəyişiklik tarixi
|14|4|CRC-32
|18|4|Sıxılmış ölçü
|22|4|Sıxılmamış ölçü
|26|2|Fayl adının uzunluğu (n)
|28|2|Əlavə sahə uzunluğu (m)
|30|n|Fayl adı
|30+n|m|Əlavə Sahə

#### Mərkəzi Kataloq Fayl Başlığı


|Ofset|Bayt|Təsvir
---|---|---|
|0|4|Mərkəzi kataloq faylı başlıq imzası # 0x02014b50
|4|2|Tərəfindən hazırlanmış versiya
|6|2|Çıxarış üçün lazım olan versiya (minimum)
|8|2|Ümumi təyinatlı bit bayrağı
|10|2|Sıxılma üsulu
|12|2|Faylın son dəyişiklik vaxtı
|14|2|Faylın son dəyişiklik tarixi
|16|4|CRC-32
|20|4|Sıxılmış ölçü
|24|4|Sıxılmamış ölçü
|28|2|Fayl adının uzunluğu (n)
|30|2|Əlavə sahə uzunluğu (m)
|32|2|Fayl şərhinin uzunluğu (k)
|34|2|Faylın başladığı disk nömrəsi
|36|2|Daxili fayl atributları
|38|4|Xarici fayl atributları
|42|4|Lokal fayl başlığının nisbi ofseti. Bu, faylın baş verdiyi ilk diskin başlanğıcı ilə yerli fayl başlığının başlanğıcı arasındakı baytların sayıdır. Bu, mərkəzi kataloqu oxuyan proqram təminatına ZIP faylı daxilində faylın yerini müəyyən etməyə imkan verir.
|46|n|Fayl adı
|46+n|m|Əlavə sahə
|46+n+m|k|Fayl şərhi

#### Mərkəzi Kataloq qeydinin sonu


|Ofset|Bayt|Təsvir
---|---|---|
|0|4|Mərkəzi kataloq imzasının sonu # 0x06054b50
|4|2|Bu diskin sayı
|6|2|Mərkəzi kataloqun başladığı disk
|8|2|Bu diskdə mərkəzi kataloq qeydlərinin sayı
|10|2|Mərkəzi kataloq qeydlərinin ümumi sayı
|12|4|Mərkəzi kataloqun ölçüsü (bayt)
|16|4|Arxivin başlanğıcına nisbətən mərkəzi kataloqun başlanğıcının ofseti
|20|2|Şərh uzunluğu (n)
|22|n|Şərh

## İstinadlar

* [PKWARE ZIP File Format Specifications](https://pkware.cachefly.net/webdocs/casestudies/APPNOTE.TXT)
* [PKZip Faylının Strukturu](https://users.cs.jmu.edu/buchhofp/forensics/formats/pkzip-printable.html)


