{
  "date": "2021-02-10",
  "keywords": [
"jpx faylı",
"jpx fayl formatı",
"jpx faylı nədir",
"fayl",
"jpx nümunəsi",
"jpx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "JPX - Şəkil Fayl Formatı",
  "description": "JPX faylları yarada və aça bilən JPX fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "JPX",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-jp-azx"
}
},
  "lastmod": "2021-02-10"
}

## JPX faylı nədir? ##

.jpx uzantısı olan fayl JPEG 2000 fayl formatının genişləndirilməsidir. O, ilk növbədə JPEG 2000 sıxılmadan istifadə edir və həmçinin təsvir üçün çoxsaylı təbəqələr, müxtəlif rəng boşluqları, qeyri-şəffaflıq və parçalanmış kod axınları kimi inkişaf etmiş funksiyaları təmin edir. JPX həmçinin JPEG 2000 sıxılma ilə yanaşı, JBIG, CCITT Group3, CCITT Group4 və s. kimi digər sıxılmalara da imkan verir. JPX fayl formatı [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html) standartı olaraq təsdiq edilib, lakin [JPEG](/image/jpeg/) fayl formatının geniş istifadəsi səbəbindən isti qəbul ala bilmədi. JPX fayllarını aça bilən proqramlara Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 və CorelDraw Graphics Suite 2020 daxildir.

## Qısa tarix

In 2000, the Joint Photographic Experts Group committee designed JP2 with the objective to improve their own discrete cosine transform-based JPEG standard with this new wavelet-based method. The JPEG committee aimed to provide their baseline methods free of license fees.in the JP2 license gaining competition among 20 companies, they won by a whisker. JPEG 2000 has been declared as an ISO standard, though most web browser are not ready to give a hand to JPEG 2000 since 2017. 2004-cü ildə ISO/IEC 15444-2 formatı açıq şəkildə JP2 fayl formatının genişləndirilməsi kimi qəbul edildi.

## JPX Fayl Format

JPX fayl formatı [JP2](/image/jp2/) fayl formatı ilə müəyyən edilmiş funksionallıqdan kənar məlumat strukturlarına ehtiyacı olan proqramların tələblərinə cavab vermək üçün tərtib edilmişdir. Qeyri-uyğun genişləndirmələri olan JP2 faylı bazarda çaşqınlığa səbəb ola bilər ki, burada bəzi oxucular bəzi JP2 fayllarını şərh edə bilər, digərləri isə yox. JPX tətbiqlərdə bu cür problemlərin qarşısını almaq üçün cavabdır.

### Fayl İdentifikasiyası

JPX faylları ənənəvi kompüter fayl sistemində saxlandıqda [JPF](/image/jpf/) kimi saxlanılır. Buna görə JPX termini JPF ilə müqayisədə ən az istifadə olunur. JPX faylı aşağıdakı baytlarla başlayır:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Fayl təşkili

JP2 kimi, JPX faylı bitişik qaydada düzülmüş qutuları olan ikili quruluşa malik qutular toplusudur. Birinci qutu faylın ilk baytı ilə başlanğıcı verir və sonuncu qutunun son baytı faylın son baytını təmsil edir.
JPX faylındakı qutunun binar strukturu [JP2](/image/jp2/) fayl formatında müəyyən edilən ilə eynidir.

### CodeStream-in JPX-də saxlanması

JPX fayl formatı şəkil kod axınının fraqmentlərə bölünməsinə imkan verir. Bu, bütün faylı yenidən yazmadan şəklin bir plitəsini dəyişdirməyə və dəyişdirilmiş plitəni faylın sonuna yazmağa imkan verir. Orijinal [JP2](/image/jp2/) fayl formatı bütün kod axınının faylın bitişik hissəsində saxlanmasını məhdudlaşdırır ki, bu da şəklin bir plitəsini dəyişdirmək və JPX vasitəsilə yuxarıda göstərilən dəstəklənməyə nail olmaq istəyən şəkil redaktə proqramları üçün problem yarada bilər. fayl formatı. Şəkil kod axınının parçalanması JPX fayl formatını JP2 fayl formatından üstün edir. Bundan əlavə, JPX fayl formatı birdən çox kod axını birləşdirməyə və göstərilən nəticə çıxarmağa imkan verir. Codestreams kompozisiya və animasiya kimi birləşdirilə bilər.

## İstinadlar ##

* [JPEG 2000-ə ümumi baxış](https://jpeg.org/jpeg2000/)


