{
  "date": "2019-11-25",
  "keywords": [
"jpeg faylı",
"jpeg fayl formatı",
"jpeg faylı nədir",
"fayl",
"jpeg nümunəsi",
"jpeg fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPEG - Şəkil faylı formatı",
  "description": "JPEG fayl formatı və JPEG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "JPEG",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jpe-azg"
}
},
  "lastmod": "2020-08-08"
}

## JPEG faylı nədir? ##

JPEG itkili sıxılma üsulu ilə saxlanılan bir şəkil formatıdır. Sıxılma nəticəsində çıxan görüntü yaddaşın ölçüsü ilə görüntü keyfiyyəti arasında mübadilədir. İstifadəçilər istədiyiniz keyfiyyət səviyyəsinə nail olmaq üçün sıxılma səviyyəsini tənzimləyə, eyni zamanda yaddaşın ölçüsünü azalda bilərlər. Şəkilə 10:1 sıxılma tətbiq edilərsə, şəkil keyfiyyətinə cüzi dərəcədə təsir edir. Sıxılma dəyəri nə qədər yüksək olarsa, görüntü keyfiyyətinin pisləşməsi bir o qədər yüksək olar.

## Fayl Formatının Xüsusiyyətləri ##

JPEG şəkil fayl formatı Birgə Fotoqrafiya Mütəxəssisləri Qrupu tərəfindən standartlaşdırılıb və buna görə də JPEG adı. Format internetdə foto şəkillərin saxlanması və ötürülməsi seçimi olmuşdur. Demək olar ki, bütün Əməliyyat sistemlərində indi JPEG şəkillərinin vizuallaşdırılmasını dəstəkləyən izləyicilər var, onlar tez-tez JPG genişləndirilməsi ilə də saxlanılır. Hətta veb brauzerlər JPEG şəkillərinin vizuallaşdırılmasını dəstəkləyir. JPEG fayl formatının spesifikasiyalarına keçməzdən əvvəl, JPEG-in yaradılmasında iştirak edən addımların ümumi prosesini qeyd etmək lazımdır.

### JPEG Sıxılma Addımları ###

**Transformasiya:** Rəngli şəkillər RGB-dən parlaqlıq/xrominasiya təsvirinə çevrilir (Göz rənglənməyə deyil, parlaqlığa həssasdır, beləliklə, rənglilik hissəsi çox məlumat itirə bilər və beləliklə, yüksək sıxılmış ola bilər.

**Aşağı Nümunə Alma:** Aşağı seçmə parlaqlıq komponenti üçün deyil, rəngli komponent üçün aparılır. Aşağı seçmə ya üfüqi olaraq 2:1 və şaquli olaraq 1:1 nisbətində aparılır (2 saat 1 V). Beləliklə, 'y' komponentinə toxunulmadığı üçün şəkil ölçüsü azalır, görüntü keyfiyyətində nəzərəçarpacaq itki yoxdur.

**Qruplarda təşkil:** Hər bir rəng komponentinin pikselləri 8×2 piksellik qruplarda təşkil edilir, əgər sətirlərin və ya sütunların sayı 8-dən çox deyilsə, məlumat vahidləri” adlanır, aşağı sətir və ən sağdakı sütunlar təkrarlanır.

**Discrete Cosine Transformation:** Discrete Cosine Transformation (DCT) sonra hər bir məlumat vahidinə transformasiya edilmiş komponentlərin 8×8 xəritəsini yaratmaq üçün tətbiq edilir. DCT kompüter hesabının məhdud dəqiqliyinə görə bəzi məlumat itkisini nəzərdə tutur. Bu o deməkdir ki, xəritə olmasa belə, görüntü keyfiyyətində müəyyən itkilər olacaq, lakin adətən kiçikdir.

**Kvantlaşdırma:** Məlumat vahidindəki 64 transformasiya edilmiş komponentin hər biri Kvantlaşdırma əmsalı (QC) adlı ayrıca ədədə bölünür və sonra tam ədədə yuvarlaqlaşdırılır. İnformasiyanın geri qaytarıla bilməyəcəyi yer budur, Böyük QC daha çox itkiyə səbəb olur. Ümumiyyətlə, əksər JPEG alətləri JPEG standartı tərəfindən tövsiyə olunan QC cədvəllərindən istifadə etməyə imkan verir.

**Kodlaşdırma:** Hər bir məlumat vahidinin 64 kvantlaşdırılmış transformasiya edilmiş əmsalı (indi tam ədədlərdir) RLE və Huffman kodlaşdırmasının birləşməsindən istifadə etməklə kodlaşdırılır.

**Başlığın əlavə edilməsi:** Son addım başlığı və istifadə edilən bütün JPEG parametrlərini əlavə edir və nəticəni çıxarır.

JPEG dekoderi sıxılmışdan orijinal təsviri yaratmaq üçün tərs addımlardan istifadə edir.

### Fayl strukturu ###

JPEG şəkli hər seqmentin markerlə başladığı seqmentlər ardıcıllığı kimi təqdim olunur. Hər bir marker 0xFF baytı ilə başlayır və ardınca markerin növünü göstərmək üçün marker bayrağı gəlir. Markerin ardınca gələn faydalı yük marker növünə görə fərqlidir. Ümumi JPEG marker növləri aşağıdakı kimidir:

|Qısa ad|Bayt|Yük|Ad|Şərhlər
---|---|---|---|---|
|SOI|0xFF, 0xD8|heç biri|Şəkilin başlanğıcı|
|S0F0|0xFF, 0xC0|dəyişən ölçü|Çərçivənin başlanğıcı|
|S0F2|0xFF, 0xC2|dəyişən ölçü|Çərçivə üçün başlanğıc|
|DHT|0xFF, 0xC4|dəyişən ölçü|Hufman cədvəllərini müəyyənləşdirin|
|DQT|0xFF, 0xDB|dəyişən ölçü|Kvantlaşdırma Cədvəl(lər)ini müəyyənləşdirin|
|DRI|0xFF, 0xDD|4 bayt|Yenidən Başlama Aralığını Müəyyən Edin|
|SOS|0xFF, 0xDA|dəyişən ölçü|Skanın Başlanması|
|RSTn|0xFF, 0xD//n//(//n//#0..7)|heç biri|Yenidən başladın|
|APPn|0xFF, 0xE//n//|dəyişən ölçü|Tətbiq üçün xüsusi|
|COM|0xFF, 0xFE|dəyişən ölçü|Şərh|
|EOI|0xFF, 0xD9|heç biri|Şəklin Sonu|

Entropiya kodlu məlumat daxilində, hər hansı 0xFF baytdan sonra kodlayıcı tərəfindən növbəti baytdan əvvəl 0x00 bayt daxil edilir ki, heç birinin nəzərdə tutulmadığı yerdə marker görünməsin və çərçivə səhvlərinin qarşısını alır. Dekoderlər bu 0x00 baytı atlamalıdırlar. [byte stuffing](https://en.wikipedia.org/wiki/Byte_stuffing) adlanan bu texnika (JPEG spesifikasiyası bölməsi F.1.2.3-ə baxın) yalnız entropiya ilə kodlanmış məlumatlara tətbiq edilir, faydalı yük məlumatlarına deyil. Bununla belə, qeyd edin ki, entropiya kodlu verilənlərin özünəməxsus bir neçə markerləri var; xüsusilə Paralel dekodlamağa imkan vermək üçün entropiya ilə kodlanmış məlumatların müstəqil hissələrini təcrid etmək üçün istifadə edilən Sıfırlama markerləri (0xD0 - 0xD7) və kodlayıcılar bu Sıfırlama markerlərini müntəzəm olaraq daxil etməkdə sərbəstdirlər (baxmayaraq ki, bütün kodlayıcılar bunu etmir).

