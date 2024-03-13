{
  "date": "2019-10-11",
  "keywords": [
"psb faylı",
"psb fayl formatı",
"psb faylı nədir",
"fayl",
"psb nümunəsi",
"psb fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PSB - Photoshop Big Image File Format",
  "description": "PSB faylları yarada və aça bilən PSB fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "PSB",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-ps-azb"
}
},
  "lastmod": "2019-09-10"
}

## PSB faylı nədir?
Adobe photoshop faylları iki formatda saxlayır. Ölçüsü 30.000x30.000 piksel olan fayllar PSD genişlənməsi ilə, PSD-dən 300.000-dən 300.000 pikselə qədər böyük olan fayllar isə Photoshop Big kimi tanınan PSB genişləndirilməsi ilə saxlanılır. Daha dəqiq desək, PSB faylları hündürlüyü və eni 300.000 pikselə qədər olan şəkillərlə 4 EB (4,2 milyard GB-dan çox) qədər böyük ola bilər. Digər tərəfdən, PSD-lər maksimum 2 GB-a qədər və təsvir ölçüləri 30.000 piksel ola bilər.

PSB is also known as large format size for photoshop and supports all the photoshop features like layers, effects and filters.Photoshop can convert PSB file to [PSD](/image/psd/), [JPG](/image/jpeg/), [PNG](/image/png/), [EPS](/page-description-language/eps/), [GIF](/image/gif/) and other formats as well. Photoshop large document format is available once the feature of file handling pane of Photoshop’s preferences dialog box is enabled.

## Fayl Format Məlumatı ##

Photoshop fayl formatı bölmələr arasında hərəkət etmək üçün çoxlu uzunluq işarələri olan beş əsas hissəyə bölünür.

|Fayl formatı
---|
|Fayl başlığı
|Rəng rejimi məlumatı
| Şəkil Resursları
|Layer və Maska Məlumatı
|(((
Şəkil Məlumatı
)))

### Fayl başlığı ###

Fayl başlığının sabit uzunluğu 26 baytdır və təsvirin əsas xüsusiyyətlərini ehtiva edir.

BYTE İmza [4] – '8BPS'-ə bərabərdir.

WORD Versiyası [2] – Versiya nömrəsi, PSD # 1, PSB # 2.

BYTE Reserved [6] – Qorunur və həmişə sıfırdır.

WORD Channels [2] – Alfa kanalları da daxil olmaqla təsvirdəki rəng kanallarının sayı. Onun dəyəri 1 ilə 56 arasında dəyişir.

UZUN sətirlər [4] – Şəklin piksellərlə hündürlüyü, PSD 1-30,000, PSB 1-300,000.

UZUN Sütunlar [4] – Şəklin piksellərlə eni, PSD 1-30,000, PSB 1-300,000.

SÖZ Dərinliyi [2] – Kanal başına bitlərin sayı. Dəstəklənən dəyərlər 1,8,16 və 32-dir.

WORD Mode [2] – Faylın Rəng Rejimi.

#### Rejimin Təsviri ####


|Rejim|Təsvir
---|---|
|0|Bitmap (monoxrom)
|1|Boz miqyaslı
|2|İndekslənmiş
|3|RGB
|4|CMYK
|7|Çoxkanallı
|8|Duoton (yarım ton)
|9|Lab

### Rəng Rejimi Məlumatı ###

Fayl başlığı bölməsindən sonra rəng rejimi məlumat bölməsi gəlir. Blok blokun uzunluğunu baytla verən UZUN Nömrə ilə başlayır. Rəng rejimi məlumatlarının strukturu aşağıdakı kimidir:

4 bayt – Aşağıdakı rəng məlumatlarının uzunluğu.

Dəyişən – Rəng Məlumatı

Başlıq bölməsindəki rejim sahəsinin dəyəri İndekslənmiş Rəng və ya cüt ton deyilsə, blokun uzunluğu 0 olacaq və uzunluq sahəsindən sonra heç bir məlumat olmayacaq.

İndekslənmiş Rəngli Şəkillər üçün uzunluq 256 rəng palitrası olan 768 bayt olacaq. Duoton üçün məlumatlar ekran parametrlərini və digər əlaqəli məlumatları ehtiva edir.

### Şəkil Resursları ###

Rəng rejimi məlumat bölməsindən sonra üçüncü blok şəkil resursu bölməsidir. İlk dörd bayt blokun uzunluğunu təyin edən UZUN nömrədir, sonra bir sıra resurs bloklarıdır. Şəkil resurs blokunun strukturu aşağıdakı kimidir:

BYTE Növü [4] – İmza '8BIM

WORD ID [2] – Şəkil Resursunun İD-si. İstinad linkindən görünə bilən Resurs İdentifikatorlarının siyahısı var.

BYTE Adı [Dəyişən] – Adı: Cüt uzunluqlu Paskal sətri. ** **

UZUN Ölçü [4] – Aşağıdakı resurs məlumatlarının faktiki ölçüsü.

BYTE Data [Dəyişən} – Resurs məlumatları. O, bərabər ölçüdə olmaq üçün yastıqlıdır.

Resurs formatlarından bəziləri aşağıda qısaca izah olunur:

**Şəbəkə və Bələdçilərin Resurs Formatı:** Şəbəkə və Bələdçilər məlumatı resurs blokunda saxlanılır. Bu resurs bloklarında 16 baytlıq şəbəkə və bələdçi başlığı, ardınca 5 bayt bələdçi məlumat bloku var.

**Tumbnail Resurs Format:** Miniatür məlumatı RGB-də 28 bayt başlıqdan və JFIF miniatürdən ibarət ilkin baxış keçirmək üçün şəkil resursu blokunda saxlanılır.

**Rəng seçiciləri Resurs Formatı:** Rəng seçiciləri məlumatı 8 baytlıq başlıq ilə şəkil resurs blokunda saxlanılır və ardınca dəyişən uzunluqlu rəng seçiciləri məlumat bloku verilir.

### Qat və Maska Məlumatı ###

Dördüncü blok təbəqə və maska məlumat blokudur və təbəqələr və maskalar haqqında məlumat ehtiva edir. Qat məlumatları əvvəlcə saxlanılır, sonra isə maska məlumatları.

**Layer Məlumatı:** Layer məlumatı təbəqə məlumatının uzunluğunu göstərən UZUN dəyərlə başlayır. Bundan sonra izləniləcək təbəqə qeydlərinin sayını göstərən WORD dəyərinin sayı var.

[8] – təbəqələrin uzunluğu

[2] – Qat sayı

[Dəyişən] – Hər təbəqə haqqında məlumat.

[Dəyişən] – Kanal şəkli datası.** **

**Maska Məlumatı:** Maska strukturu aşağıdakı formata malikdir:


|Məlumat strukturu|Sahənin adı| Təsvir
---|---|---|
|SÖZ| Overlay Rəng Məkanı| (Sənədləşdirilməyib)
|BYTE[8]| Rəng Komponentləri| 4x2 bayt rəngli komponentlər
|SÖZ| Qeyri-şəffaflıq| 0#şəffaf, 1#şəffaf
|BYTE| növ| 0#inverted, 1#protected, 128#saxlanılan dəyərdən istifadə edin
|BYTE| dolgu| sıfıra təyin edin

### Şəkil Data ###

Son hissədə təsvirin piksel məlumatı var. Şəkil verilənləri müstəvilərdə ardıcıllıq seriyası kimi saxlanılır, yəni əvvəlcə bütün qırmızı məlumatlar, sonra bütün yaşıl məlumatlar və s. Hər sətrin əvvəlindəki WORD hər bir skan xəttinə aid olan bayt ölçüsünü göstərir.

[2] – Sıxılma üsulu:

[Dəyişən] – Planar qaydada şəkil məlumatları, yəni RRRR, GGGG, BBBB və s.

Sıxılma üsulları:

0 – Raw Şəkil Məlumatı

1 – RLE Sıxılmış

2 - Proqnoz olmadan zip

3 - Proqnozla zip

## İstinad ##

* [PSB Fayl Format - Adobe tərəfindən](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

* [PSB - Wikipedia](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)


