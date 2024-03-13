{
  "date": "2020-08-20",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WOFF - Veb Açıq Fayl Format",
  "description": "WOFF faylı Veb Açıq Şrift Formatında yaradılmış açıq şrift formatıdır.",
  "linktitle": "WOFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-wof-azf"
}
},
  "lastmod": "2020-09-30"
}

## WOFF faylı nədir?

.woff uzantısı olan fayl Veb Açıq Font Formatına (WOFF) əsaslanan veb şrift faylıdır. Onun TrueType (.TTF) və ya OpenType (.OTT) şrift növlərinə əsaslanan formata uyğun sıxılmış konteyneri var. WOFF veb şriftlərini masaüstü proqramlarda istifadə edilən şrift fayllarından fərqləndirmək məqsədi ilə təqdim edilmişdir. Bundan əlavə, format şəbəkə üzərindən serverdən müştərinin kompüterinə ötürülən şriftlərin gecikməsini azaltmağa yönəlib. WOFF fayllarını TTF və digər şrift fayl formatlarına çevirə bilən bir neçə alət mövcuddur.

## WOFF fayl formatı

WOFF şrift formatı TrueType, OpenType və Open Font Format kimi müxtəlif şrift növlərində istifadə olunan cədvəl əsaslı sfnt strukturlarının şrift məlumat cədvəllərini sıxışdırır. Bu, bu şrift növləri üçün konteyner kimidir və həmçinin şriftin metadatasını və konteynerə daxil ediləcək şəxsi istifadə məlumatlarını daxil etmək üçün otaq var. Dönüştürücülər sfnt fayllarından WOFF formatlı fayla istifadə edir və istifadəçi agentləri veb sənədlə istifadə üçün kodlanmış faylı bərpa edir. Qeyd etmək lazımdır ki, bərpa edilmiş şrift məlumatları bütün aspektlərdən daxil olan şrift formatına tam uyğun gəlir.

WOFF faylı Utilitləri tez-tez qlif alt quruluşu, doğrulama və ya şrift funksiyası əlavələri kimi əlavə funksiyaları ehtiva edir, lakin bu lazım deyil. Həm yaradıcı, həm də istifadə agentləri əsas şrift məlumatlarının etibarlılığının qorunub saxlanmasını təmin etməlidirlər.

### WOFF Fayl Strukturu

WOFF fayl strukturu sfnt şriftlərinə bənzəyir. O, hər bir şrift məlumat cədvəlinin uzunluqlarını və ofsetlərini ehtiva edən cədvəl kataloquna əsaslanır. Bu ilkin məlumatdan sonra bütün cədvəllər izlənilir. Faylda orijinal şriftlərlə eyni olan şrift verilənlər bazası var. Cədvəllərin sırası da eynidir, lakin hər biri sıxıla bilər. WOFF cədvəl kataloqu orijinal cədvəl kataloqunu əvəz edir.

WOFF faylı aşağıdakılardan ibarətdir:

 * WOFFHeader - Əsas şrift növü və versiyası olan fayl başlığı, metadata və şəxsi məlumat bloklarının ofsetləri ilə birlikdə.
 * TableDirectory - WOFF faylı daxilində hər bir cədvəlin orijinal ölçüsünü, sıxılmış ölçüsünü və yerini göstərən şrift cədvəllərinin kataloqu.
 * FontTables - Giriş sfnt şriftindən olan şrift məlumat cədvəlləri, bant genişliyi tələblərini azaltmaq üçün sıxılmışdır.
 * ExtendedMetadata - XML formatında təmsil olunan və WOFF faylında saxlanmaq üçün sıxılmış genişləndirilmiş metaməlumatların isteğe bağlı bloku.
 * PrivateData- Şrift dizayneri, tökmə zavodu və ya satıcının istifadə etməsi üçün şəxsi məlumatların isteğe bağlı bloku.

### WOFF Başlığı
WOFF başlığı fayla daxil olan məlumatların növünü göstərən eyniləşdirici imzadan ibarətdir. WOFF başlığı sahələri ilə birlikdə aşağıdakı kimidir.

|Növ|Sahənin Adı|Təsvir|
---|---|---|
|UInt32|imza |0x774F4646 'wOFF' |
|UInt32| ləzzət |Giriş şriftinin sfnt versiyası.|
|UInt32| uzunluq |WOFF faylının ümumi ölçüsü.|
|UInt16| numTables |Şrift cədvəlləri kataloqundakı qeydlərin sayı.|
|UInt16| qorunur | Qorunur; sıfıra təyin edin.|
|UInt32| totalSfntSize |sfnt başlığı, kataloqu və şrift cədvəlləri (doldurma daxil olmaqla) daxil olmaqla, sıxılmamış şrift məlumatı üçün lazım olan ümumi ölçü.|
|UInt16| majorVersion |WOFF faylının əsas versiyası.|
|UInt16| minorVersion |WOFF faylının kiçik versiyası.|
|UInt32| metaOffset |WOFF faylının əvvəlindən metadata blokuna ofset.|
|UInt32| metaLength |Sıxılmış metadata blokunun uzunluğu.|
|UInt32| metaOrigLength |Metadata blokunun sıxılmamış ölçüsü.|
|UInt32| privOffset |WOFF faylının əvvəlindən şəxsi məlumat blokuna ofset.|
|UInt32| privLength |Şəxsi məlumat blokunun uzunluğu.|

## İstinadlar

 * [w3 WOFF Fayl Format](https://www.w3.org/TR/WOFF/)

