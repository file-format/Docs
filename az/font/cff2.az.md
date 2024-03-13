{
  "date": "2020-08-20",
  "keywords": [
"cff2 faylı",
"cff2 fayl formatı",
"cff2 faylı nədir",
"fayl",
"cff2 nümunəsi",
"cff2 fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF2 - Kompakt Şrift Fayl Formatının 2-ci versiyası",
  "description": "CFF2 faylları yaratmaq və açmaq üçün CFF2 Fayl Format və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFF2",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cff-az2"
}
},
  "lastmod": "2020-10-21"
}

## CFF2 faylı nədir?

CFF2 file format is the version 2.0 of the CFF file format and allows efficient storage of glyph outlines and metadata similar to the CFF file format. CFF2 differs from CFF in that it is intended to be used in the context of an OpenType font as a 'sfnt' table with the tag CFF2. O, müstəqil proqram kimi istifadə edilə bilməz və digər OpenType cədvəllərindəki məlumatlardan asılıdır.

## CFF2 Fayl Format

[CFF2 file format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2) fayl formatı ilə bağlı daxili məlumat tərtibatı, məlumat növləri, cədvəllər və digər daxili məlumatlar haqqında təfərrüatları ehtiva edir. Bu, tərtibatçının arayışı üçün istinad edilə bilər. Bunlarla bağlı bəzi təfərrüatlar aşağıdakı kimidir.

### Data Layout

CFF2 fayl formatının ikili məlumatları məntiqi olaraq bir sıra ayrı məlumat strukturları kimi təşkil edilmişdir. Binar verilənlər daxilində tərtibat aşağıdakı cədvəldə göstərildiyi kimidir.

|Giriş |Şərhlər|
---|---|
|Başlıq |Sabit yer|
|Üst DICT| Sabit yer|
|Qlobal Subr İNDEKSİ| Sabit yer|
|Variasiya |Mağaza|
|FDSelect |Yalnız Font DICT INDEX-də birdən çox Şrift DICT olduqda təqdim edin.|
|Şrift DICT INDEX ||
|Şrift DICT massivi| Şrift DICT INDEX-ə daxildir.|
|Şəxsi DICT| Hər Şrift DICT üçün bir.|

Yalnız ilk üç struktur sabit yerlərə əsaslanır. Qalanlara ofsetlər vasitəsilə çatılır və onların sırası dəyişdirilə bilər.

### Məlumat növləri

CFF2 fayl formatı aşağıdakı məlumat növlərindən istifadə edir.

|Adı |Rəsmi |Təsvir|
---|---|---|
|uint8 |0-dan 255-ə qədər |8 bitlik işarəsiz nömrə|
|uint16 |0 - 65535| 16 bitlik imzasız nömrə|
|uint32 |0 - 4294967295| 32 bitlik imzasız nömrə|
|Offset |dəyişir| 1, 2, 3 və ya 4 bayt ofsetlər (İndeks cədvəlində OffSize sahəsi ilə müəyyən edilir)|
|OffSize |1-dən 4-ə qədər| 1 baytlıq imzasız nömrə Ofset sahəsinin və ya sahələrin ölçüsünü müəyyən edir|

O, bütün çox baytlıq rəqəmsal məlumatları və böyük endian bayt sırası ilə ofset sahələrini saxlayır. CFF2 formatı heç bir hizalama məhdudiyyətinə əməl etmədiyi üçün doldurulma baytlarından azaddır.

### DICT Data

CFF2 faylları kompakt tokenləşdirilmiş formatda açar-dəyər cütləri kimi şrift lüğəti məlumatlarını ehtiva edir. Lüğət açarları 1 və ya 2 bayt operatorlar kimi kodlaşdırılır və lüğət dəyərləri dəyişən ölçülü rəqəmli operandlar kimi kodlaşdırılır. DICT Data formatından istifadə edən üç struktur var: `Top DICT`, `Font DICT` və `Private DICT`. Aşağıdakı cədvəldə göstərildiyi kimi müxtəlif ölçülü bir sıra tam operand növləri müəyyən edilir və kodlaşdırılır (operandın birinci baytı b0, ikincisi b1 və s.).

|Ölçü |b0 diapazonu |Dəyər diapazonu |Dəyər hesablanması|
---|---|---|---|
|1 |32 - 246| -107 - +107 |b0 - 139|
|2	|247 to 250|	+108 to +1131	|(b0 - 247) * 256 + b1 + 108|
|2	|251 to 254|	-1131 to -108|	-(b0 - 251) * 256 - b1 - 108|
|3 |28| -32768 ilə +32767| b1 << 8 | b2|
|5 |29| -(2^31) ilə +(2^31 - 1)| b1 << 24 \| b2 << 16 \| b3 << 8 \| b4|

### Başlıq

İkili məlumatlar aşağıdakı Cədvəldə göstərilən formata malik başlıqdan başlayır.

|Növü |Adı |Təsviri|
---|---|---|
|uint8| majorVersion| Əsas versiyanı formatlayın. 2-yə təyin edin.|
|uint8| minorVersion| Kiçik versiyanı formatlayın. Sıfıra təyin edin.|
|uint8| headerSize| Başlıq ölçüsü (bayt).|
|uint16| topDictLength| Baytlarda Top DICT strukturunun uzunluğu.|

## İstinadlar

 * [CFF2 Fayl Format](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2)

