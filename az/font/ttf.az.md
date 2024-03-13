{
  "date": "2020-08-20",
  "keywords": [
"ttf faylı",
"ttf fayl formatı",
"ttf faylı nədir",
"fayl",
"ttf nümunəsi",
"ttf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "TTF - TrueType şrift fayl formatı",
  "description": "TrueType şriftləri (TTF) ilkin olaraq Apple, Inc tərəfindən hazırlanmış rəqəmsal şrift texnologiyası spesifikasiyalarına əsaslanır. Həm Apple, həm də Microsoft Mac və Windows Əməliyyat sistemlərində TTF-dən istifadə edirdilər.",
  "linktitle": "TTF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-tt-azf"
}
},
  "lastmod": "2020-09-21"
}

## TTF faylı nədir?

.ttf uzantısı olan fayl TrueType spesifikasiyaları şrift texnologiyasına əsaslanan şrift fayllarını təmsil edir. Əvvəlcə Mac OS üçün Apple Computer, Inc tərəfindən hazırlanmış və işə salınmış və daha sonra Windows OS üçün Microsoft tərəfindən qəbul edilmişdir. TrueType şriftləri rezolyusiyadan asılı olmayaraq kompüter ekranlarında və printerlərdə yüksək keyfiyyətli ekranı təmin edir. Şriftlərdən istifadə edən bütün müasir proqramlar TTF faylları ilə işləyə bilir. TTF şrift faylları internet üzərindən sərbəst mövcuddur və həmçinin OTF və WOFF kimi digər şrift fayl formatlarına çevrilə bilər.

## Qısa tarix

Designed by Apply Computer, Inc in 1980s for MacOS, the TTF font format was aimed at resolving some technical limitations by Adobe's Type 1 format. Apple included support for TrueType fonts in Mac in 1991. TTF şriftlərinin dizayn məqsədi saxlama və emalda səmərəlilik və genişlənmə qabiliyyəti idi. Bu genişlənmə qabiliyyətinə əsasən, mövcud şriftlər TrueType formatına çevrilə bilər.

Microsoft ilk dəfə TrueType şriftlərini Windows 3.1-də 1992-ci ilin aprelində Apple TrueType-ı Microsoft-a lisenziyalaşdırmağa razılaşdıqdan sonra istifadə etdi. O, rasterləşdirmə mexanizmini təkmilləşdirdi, onun səmərəliliyini və performansını yaxşılaşdırdı.

## True Type Fayl Formatının Xüsusiyyətləri

TrueType şrift faylı birləşdirilmiş cədvəllər ardıcıllığından ibarət ikili fayldır. Hər bir cədvəl sözlər ardıcıllığıdır və `Tag` kimi tanınan bir ada malikdir. Hər bir teq uint32 məlumat tipinə malikdir və dörd simvoldan ibarətdir. Fayldakı birinci cədvəl şrift faylındakı digər cədvəllərə giriş imkanı verən şrift kataloqudur. Şrift məlumatları şrift kataloqu cədvəlindən sonra gələn digər cədvəllərdə yer alır. Hər cədvələ öz etiketi ilə daxil olmaq mümkün olduğundan, cədvəllər faylda istənilən ardıcıllıqla görünə bilər.

Tələb olunan cədvəllər və onların etiket adları aşağıdakı cədvəldə göstərilmişdir.

|**Tag**|**Cədvəl**|
---|---|
|'cmap'| simvoldan qlifə xəritəçəkmə|
|'glyf'| qlif məlumatları|
|'baş'| şrift başlığı|
|'hhea'| üfüqi başlıq|
|'hmtx'| üfüqi ölçülər|
|'yer'| yerin indeksi|
|'maxp'| maksimum profil|
|'ad'| adlandırma|
|'post'| PostScript|

### Məlumat növləri
TrueType şriftləri aşağıdakı cədvəldə sadalanan standart tam ədəd və əlavə məlumat növlərindən istifadə edir.

|**Məlumat Tipi** | **Təsvir** |
---|---|
|shortFrac| 16 bitlik işarəli fraksiya|
|Sabit| 16.16-bit imzalı sabit nöqtəli nömrə|
|FWord| FUnits-də kəmiyyəti, em məkanında ölçülə bilən ən kiçik məsafəni təsvir edən 16-bit işarəli tam ədəd.|
|uFWord| FUnits-də kəmiyyəti, em məkanında ölçülə bilən ən kiçik məsafəni təsvir edən 16 bitlik işarəsiz tam ədəd.|
|F2Dot14| Fraksiyanı təmsil edən aşağı 14 bit ilə 16 bit imzalanmış sabit nömrə.|
|longDateTime|	The long internal format of a date in seconds since 12:00 midnight, January 1, 1904. It is represented as a signed 64-bit integer.|

### Şrift kataloqu

TrueType şriftindəki birinci cədvəl digər cədvəllərdəki məlumatlara daxil olmaq üçün tələb olunan məlumatlara çıxışı təmin edən şrift kataloqudur. Bundan əlavə, aşağıdakılardan ibarətdir:

 * Ofset alt cədvəli' - şriftdəki cədvəllərin qeydini aparır və kataloqdakı hər bir cədvələ daxil olmaq üçün ofset məlumatını təmin edir.
 * `Cədvəl kataloqu` - Şriftdəki hər bir cədvəl üçün qeydləri ehtiva edir

#### Ofset Alt Cədvəli
Ofset alt cədvəli aşağıda göstərilmişdir.

|**Növ**|**Ad**|**Təsvir**|
---|---|---|
|uint32| miqyaslayıcı növü| Bu şrifti rasterləşdirmək üçün istifadə ediləcək OFA miqyasını göstərmək üçün etiket; ətraflı məlumat üçün aşağıdakı miqyaslayıcı növü üzrə qeydə baxın.|
|uint16| numTables| cədvəllərin sayı|
|uint16| searchRange| (maksimum güc 2 <= say Cədvəl)*16|
|uint16| entrySelector| log2(2 <= Cədvəllərin maksimum gücü)|
|uint16| rangeShift| numTables*16-searchRange|

#### Cədvəl kataloqu
Cədvəl kataloqu ofset alt cədvəlindən dərhal sonra gəlir. Onun strukturu aşağıdakı cədvəldə göstərildiyi kimidir.

|**Növ**|**Ad**|**Təsvir**|
---|---|---|
|uint32| tag| 4 bayt identifikator|
|uint32| checksum| bu cədvəl üçün yoxlama məbləği|
|uint32| ofset| sfnt| əvvəlindən ofset
|uint32| uzunluq| bu cədvəlin baytla uzunluğu (faktiki uzunluq doldurulmamış uzunluq)|

Şrift faylındakı hər bir cədvəlin öz cədvəl kataloqu girişi olmalıdır. Cədvəldəki qeydlər etiketə görə artan qaydada sıralanmalıdır.


## İstinadlar
 * [TrueType Font Reference Manual](https://developer.apple.com/fonts/TrueType-Reference-Manual/)
 * [TrueType İcmal](https://learn.microsoft.com/en-us/typography/truetype/)

