{
  "date": "2019-12-03",
  "keywords": [
"dok",
"fayl",
"uzadılması",
"fayl formatı",
"Söz",
"Sənəd"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DOC - Microsoft Word sənəd faylı",
  "description": "DOC faylları yarada və aça bilən DOC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DOC",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-do-azc"
}
},
  "lastmod": "2019-12-03"
}

## DOC faylı nədir?

.doc uzantılı fayllar Microsoft Word və ya ikili fayl formatında digər söz emal sənədləri tərəfindən yaradılan sənədləri təmsil edir. Artırma əvvəlcə bir neçə fərqli əməliyyat sistemində düz mətn sənədləri üçün istifadə edilmişdir. O, formatlanmış şəkillər, eləcə də düz mətn, qrafiklər, diaqramlar, daxil edilmiş obyektlər, keçidlər, səhifələr, səhifə formatı, çap parametrləri və bir çox başqa məlumatlar kimi bir neçə müxtəlif növ məlumatı ehtiva edə bilər. Bu format istifadəçilərə təlimatlar, təkliflər, spesifikasiyalar, rezyumelər, məqalələr və ya hər hansı oxşar sənədlərin yazılması üçün təklif etdiyi müxtəlif variantlara görə bütün növ sənədlər üçün məşhur idi. DOC-un yenilənmiş versiyası [DOCX](/word-processing/docx/)-dir və spesifikasiyaları açıq şəkildə mövcud olan Office OpenXML-ə əsaslanır.

## Qısa tarix ##

WordPerfect, a product of [Corel](https://www.corel.com/en/), used DOC as the extension of their proprietary format. In 1980s, WordPerfect remained the choice of usage on most of the computers due to its easy availability, conformance with most computer machines and Operating systems. However, WordPerfect saw its downfall on Windows OS when Microsoft introduced Microsoft Word as its product for documents file format and chose DOC extension for their proprietary format. As Microsoft Word became more and more popular, the DOC file format underwent several revisions from Microsoft Word 97 - 2003. Defolt DOC fayl formatının Office Open XML formatı (DOCX kimi tanınır) ilə əvəz edildiyi və Microsoft Word-ün yeni versiyaları indi bu yeni uzantıyı standart fayl formatı kimi istifadə edəndə 2007-ci il idi.

## DOC Fayl Formatının Xüsusiyyətləri - Ətraflı Məlumat

Microsoft didn't release the DOC file format specifications for a long time until 2008. In Feb 2008, format specifications were released for .doc file format under the Microsoft Open Specification Promise. Though the specification does not describe all of the features used by the DOC format, it gives ample information about the knowledge required to work with this file format. Still, reverse engineering is required to make use of the available information. The specifications have been updated several times and the latest [revision](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx) is 8.0 which was updated as of August 2018.

### Bəzi Əsas Konsepsiyalar ###

DOC üçün fayl formatının spesifikasiyası haqqında hər hansı təfərrüata keçməzdən əvvəl, bu fayl formatı ilə işləmək üçün bəzi fundamental anlayışları başa düşmək lazımdır.

**Fayl Məlumat Bazası (Fib):** Fib strukturu sənəd haqqında məlumatları ehtiva edir və sənədi təşkil edən müxtəlif hissələrə fayl göstəricilərini təyin edir.
Fib dəyişən uzunluqlu bir quruluşdur. Ölçüsü sabit olan əsas hissə istisna olmaqla, hər bölmənin qarşısında növbəti bölmənin ölçüsünü təyin edən sayma sahəsi var.

**Xarakter Mövqesi:** CP və ya Xarakter Mövqesi sənəd mətnindəki simvolun sıfır əsaslı indeksi kimi xidmət edən imzasız 32 bitlik tam ədədi təmsil edir. Fayldakı hər simvolun yeri və ölçüsü birbaşa əldə edilə bilməz və əvvəlcədən müəyyən edilmiş alqoritmdən istifadə edərək hesablanmalıdır. Simvollara daxildir:

* Sənədin mətni

* Dipnotlar və ya mətn qutuları kimi obyektlərin ankerləri

* Paraqraf işarələri və cədvəl xana işarələri kimi nəzarət simvolları


**PLC:** PLC strukturu CP-lər massivindən sonra məlumat elementləri massividir. Hər hansı bir PLC üçün məlumat elementləri sıfır və ya daha çox bayt ölçüsündə eyni olmalıdır və bu səbəbdən CP-lərin sayı məlumat elementlərinin sayından bir çox olmalıdır. PLC strukturları müxtəlif növlərə malikdir, burada hər bir növ dublikat CP-lərə bu tip üçün icazə verilib-verilmədiyini müəyyən edir. PLC strukturu aşağıdakılardan ibarətdir:

* **aCP (dəyişən uzunluq):** CP elementlərinin massivi. **PLC** strukturunun hər bir növü CP elementlərinin mənasını və icazə verilən diapazonu müəyyən edir.

* **aData (dəyişən uzunluq):** **PLC** strukturunun hər bir növü məlumat elementlərinin strukturunu və mənasını, məlumat elementlərinin sayına qoyulan hər hansı məhdudiyyətləri və orada olan məlumatlara qoyulan hər hansı məhdudiyyətləri müəyyən edir. O, həmçinin məlumat elementləri ilə müvafiq CP-lər arasındakı əlaqəni müəyyənləşdirir.


**Valid Seçim:** .DOC fayl konstruksiyaları əsasən bir sıra CP-lərlə təsvir olunur. Microsoft tərəfindən müəyyən edilmiş bir sıra [rules](https://msdn.microsoft.com/en-us/library/dd908861(v#office.12).aspx) var ki, bu halda riayət edilməlidir.

**STTB:** STTB, elementlər massivindən sonra gələn başlıqdan ibarət sətir cədvəlidir. **cData** dəyəri massivdə olan elementlərin sayını təyin edir.

**Əmlak yaddaşı:** Söz faylı mətn, paraqraflar, cədvəllər, şəkillər və bölmələr kimi müxtəlif elementlərə malik ola bilər, burada hər birinin öz xüsusiyyətləri ola bilər. Bunların xassələri standartdan fərqli olaraq Word faylında saxlanılır. Bu cür fərqlər Vahid Xüsusiyyət Dəyişdiricisi (Sprm) və onun operandından ibarət PRl tərəfindən müəyyən edilir. Tətbiq **Prl**s siyahılarının tətbiqi ilə xassələrin son dəstini müəyyən edə bilər.

**Şifrə Mühafizəsi:** Word faylları da parolla qoruna bilər, bunun üçün aşağıdakı mexanizmlərdən biri istifadə edilə bilər.

* XOR çaşqınlığı

* Office ikili sənəd RC4 şifrələməsi

* Ofis binar sənədi RC4 CryptoAPI şifrələməsi


Əgər FibBase.fEncrypted və FibBase.fObfuscation hər ikisi 1-dirsə, XOR çaşqınlıqdan istifadə etməklə fayl çaşqınlaşdırılır.

FibBase.fEncrypted 1 və FibBase.fObfuscation 0 olarsa, fayl ya Office Binary Document RC4 Encryption, ya da Office Binary Document RC4 CryptoAPI Encryption vasitəsilə şifrələnir, Cədvəlin ilk FibBase.lKey axın baytlarında saxlanılan EncryptionHeader. EncryptionHeader.EncryptionVersionInfo faylı şifrələmək üçün hansı şifrələmə mexanizmindən istifadə olunduğunu müəyyən edir.

### Fayl strukturu ###

Öz orijinallığı ilə ikili Word faylı bir neçə yaddaşdan və axınlardan ibarət OLE mürəkkəb faylıdır. Bu anbarlar və axınlar yazı və oxuma parametrlərini təyin edən öz strukturuna və ölçülərinə malikdir. Bunlar:

#### WordDocument Stream ####

This stream contains the document text and other information referenced from other parts of the file. The stream has no predefined structure other than the FIB at the beginning which is mandatory and should be at offset 0. Bu axın 2147 MB-dan böyük olmamalıdır.

#### 1TableStream və ya 0TableStream ####

İkili Word faylında 1Cədvəl axını və ya 0Cədvəl axını kimi tanınan Cədvəl Axınları ola bilər. Sənəddə bunlardan ən azı biri olmalıdır. Bununla belə, əgər sənəd həm 1Cədvəl, həm də 0Cədvəl axınını ehtiva edirsə, yalnız base.fWhichTblStm tərəfindən istinad edilən axın istifadə olunur. İstinad edilməmiş axın nəzərə alınmamalıdır.
Cədvəl axını 2147 MB-dən böyük OLMALIDIR.

#### Məlumat axını ####

Məlumat axınının əvvəlcədən təyin edilmiş strukturu yoxdur. O, FIB-dən və ya faylın digər hissələrindən istinad edilən məlumatları ehtiva edir. Əgər ona istinad yoxdursa, bu axın mövcud olmamalıdır. Məlumat axını 2147 MB-dən böyük OLMALIDIR.

#### Obyekt Hovuzu Saxlama ####

Obyekt Hövzəsi yaddaşında quraşdırılmış OLE obyektləri üçün saxlama yerləri var. Sənəddə daxil edilmiş OLE obyektləri yoxdursa, bu yaddaşın mövcud olmasına ehtiyac yoxdur.

#### Xüsusi XML Məlumat Yaddaşı ####

Fərdi XML Məlumat yaddaşı isteğe bağlı yaddaşdır və adı MsoDataStore olmalıdır.

#### Xülasə məlumat axını ####

Xülasə Məlumat axını isteğe bağlı axındır, onun adı \005SummaryInformation olmalıdır, burada \005 \005 sətri deyil, 0x0005 dəyəri olan simvoldur.

#### Sənədin Xülasə Məlumat axını ####

Sənəd Xülasə Məlumat axını isteğe bağlı axındır, onun adı \005DocumentSummaryInformation olmalıdır, burada \005 \005 sətri deyil, 0x0005 dəyəri olan simvoldur.

#### Şifrələmə axını

Şifrələmə axını isteğe bağlı axındır və onun adı şifrələmə olmalıdır. Aşağıdakı şərtlərin hər ikisi yerinə yetirilmədikcə, bu axın MÜMKÜN OLMALIDIR:

* Sənəd Office Binary Document RC4 CryptoAPI Encryption ilə şifrələnib.

* fDocProps dəyəri EncryptionHeader.Flags-da təyin edilmişdir.


#### Makro Yaddaş

Makro yaddaşı fayl üçün makroları ehtiva edən isteğe bağlı yaddaşdır. Mövcuddursa, o, Layihə Kök Saxlama yeri olmalıdır.

#### XML İmza Yaddaşı

XML imza yaddaşı isteğe bağlı yaddaşdır və onun adı \_xmlsignatures olmalıdır.

#### İmza axını

İmza axını isteğe bağlı axındır və onun adı \_signatures olmalıdır. Bu axın rəqəmsal imzaları ehtiva edir.

#### İnformasiya Hüquqlarının İdarə Edilməsi Məlumat Məkanının Saxlanması

İnformasiya Hüquqlarının İdarə Edilməsi Məlumat Məkanı yaddaşı isteğe bağlı yaddaşdır, onun adı \006DataSpaces olmalıdır, burada \006 \006 sətri deyil, 0x0006 dəyəri olan simvoldur. Bu yaddaş mövcuddursa, Qorunan Məzmun Axını da MÜTLƏQ OLMALIDIR.
Əgər bu yaddaş mövcuddursa, bu yaddaşdan və Qorunan Məzmun Yayımından başqa bütün müəyyən edilmiş axınlar və yaddaşlar [MS-OFFCRYPTO]-da göstərildiyi kimi Qorunan Məzmun Yayımından OXUNMALIDIR və əgər bu axın və yaddaşlardan hər hansı biri Qorunan Məzmundan kənarda mövcuddursa Yayım, onlara məhəl qoyulmamalıdır.

#### Qorunan Məzmun Yayımı

Qorunan Məzmun Yayımı isteğe bağlı yayımdır, onun adı \009DRMContent OLMALIDIR, burada \009 \009 sətri deyil, 0x0009 dəyəri olan simvoldur.
Bu axın mövcuddursa, İnformasiya Hüquqlarının İdarə Edilməsi Məlumat Məkanı Saxlanması da MÜTLƏQDİR.

## İstinadlar ##
* [MS-DOC File Formation Specifications](https://msdn.microsoft.com/en-us/library/cc313153(v#office.12).aspx)
* [Doc Computing](https://en.wikipedia.org/wiki/Doc_(computing))
