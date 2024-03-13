{
  "date": "2020-08-20",
  "keywords": [
"cff faylı",
"cff fayl formatı",
"cff faylı nədir",
"fayl",
"cff misal",
"cff fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CFF - Yığcam Şrift Fayl Formatı",
  "description": "CFF faylları yaratmaq və açmaq üçün CFF Fayl Format və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFF",
  "menu": {
    "docs": {
      "parent": "font",
      "identifier": "font-cf-azf"
}
},
  "lastmod": "2020-10-21"
}

## CFF faylı nədir?

.cff uzantısı olan fayl Yığcam Şrift Formatıdır və PostScript Type 1 və ya CIDFont kimi də tanınır. CFF birdən çox şrifti FontSet kimi tanınan vahid vahiddə bir yerdə saxlamaq üçün konteyner rolunu oynayır. CFF şriftlərinin dizaynı printer mühitləri ilə istifadə üçün formatın əlavə çevikliyinə və genişlənməsinə imkan verən PostScript dil kodunu daxil etməyə imkan verir. CFF şrift faylları [Aspose.Font](https://products.aspose.com/font) kimi API-lərdən istifadə etməklə açıla və çevrilə bilər.

## CFF fayl formatı

CFF faylları strukturlaşdırılmış məlumat tərtibatı, müəyyən edilmiş məlumat növləri, başlıq, qlif təşkilatı və cədvəl lüğətləri olan ikili fayllardır. Bunlar haqqında ətraflı məlumatı [compact font format specifications](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)-də tapa bilərsiniz.

### Data Layout
CFF fayl formatının məlumat tərtibatı aşağıda göstərildiyi kimidir.

|Giriş|Şərhlər|
---|---|
|Başlıq|–|
|NameINDEX|–|
|Üst DICT İNDEKSİ|–|
|String INDEX|–|
|Global Subr INDEX|–|
|Kodlaşdırmalar–Şariflər|–|
|FDSelect|Yalnız CIDFonts|
|CharStrings INDEX|şrift başına|
|Font DICT INDEX|şrift başına, yalnız CIDFonts|
|Şəxsi DICT|şrift başına|
|Yerli Subr INDEX|CIDFonts üçün hər şrift və ya hər Şəxsi DICT|
|Müəlliflik hüququ və ticarət nişanı bildirişləri|–|

### Məlumat növləri

CFF məlumat növləri aşağıdakı cədvəldə göstərildiyi kimidir.

|Ad|Aralıq|Təsvir|
---|---|---|
|Kart8|0 –255|1 baytlıq imzasız nömrə|
|Kart16|0 – 65535|2 baytlıq imzasız nömrə|
|Offset|dəyişir|1, 2, 3 və ya 4 bayt ofset (OffSize sahəsi ilə müəyyən edilir)|
|OffSize|1–4|1 baytlıq işarəsiz nömrə Ofset sahəsinin və ya sahələrinin ölçüsünü müəyyən edir|
|SID|0 – 64999|2 baytlıq sətir identifikatoru|

### Başlıq

İkili məlumatlar aşağıdakı cədvəldə göstərilən formata malik başlıqdan başlayır.

|Növ|Ad|Təsvir|
---|---|---|
|Card8|major|Əsas versiyanı formatlayın (1-dən başlayaraq)|
|Kart8|minor|Kiçik versiyanı formatlayın (0-dan başlayaraq)|
|Card8|hdrSize| Başlıq ölçüsü (bayt)|
|OffSize|offSize|Mütləq ofset (0) ölçüsü|

## İstinadlar

 * [Yığcam Şrift Format Cədvəli](https://learn.microsoft.com/en-us/typography/opentype/spec/cff)
 * [CFF Fayl Format](https://adobe-type-tools.github.io/font-tech-notes/pdfs/5176.CFF.pdf)
 * [CFF2 Chartset](https://learn.microsoft.com/en-us/typography/opentype/spec/cff2charstr)

