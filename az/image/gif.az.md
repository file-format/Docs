{
  "date": "2019-10-11",
  "keywords": [
"gif faylı",
"gif fayl formatı",
"gif faylı nədir",
"fayl",
"gif nümunəsi",
"gif fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "GIF - Şəkil faylı formatı",
  "description": "GIF faylları yarada və aça bilən GIF fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "GIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-gi-azf"
}
},
  "lastmod": "2019-09-10"
}

## GIF faylı nədir? ##

GIF və ya Qrafik Mübadilə Formatı yüksək sıxılmış görüntü növüdür. Unisys-ə məxsus olan GIF şəkil keyfiyyətini aşağı salmayan LZW sıxılma alqoritmindən istifadə edir. Hər bir şəkil üçün GIF adətən piksel başına 8 bitə qədər icazə verir və təsvir boyu 256 rəngə qədər icazə verilir. 16 milyona qədər rəng göstərə bilən və insan gözünün sərhədlərinə kifayət qədər toxunan [JPEG](/image/jpeg/) təsvirdən fərqli olaraq. İnternet ortaya çıxanda GIF-lər ən yaxşı seçim olaraq qalırdı, çünki onlar aşağı bant genişliyi tələb edirdilər və bərk rəng sahələrini istehlak edən qrafika ilə uyğun gəlirdilər. Animasiya edilmiş GIF çoxsaylı şəkilləri və ya çərçivələri bir faylda birləşdirir və cizgi klipi və ya qısa video yaratmaq üçün onları ardıcıllıqla göstərir. Rəng məhdudiyyətləri hər bir çərçivə üçün 256-ya qədərdir və rəng gradienti ilə digər şəkillər və fotoşəkilləri təkrar istehsal etmək üçün ən az uyğundur.

## GIF fayl formatı ##

Konseptual olaraq, GIF faylları sıfır və ya daha çox təsvirlə doldurulmuş sabit ölçülü qrafik sahəsinə malikdir. Bəzi GIF faylları sabit ölçülü qrafik sahəsini və ya bloklarını animasiya edilmiş GIF vəziyyətində animasiya çərçivələri kimi fəaliyyət göstərə bilən alt şəkillərə bölür. GIF formatı bitmap məlumatlarını saxlamaq üçün 1 ilə 8 bit piksel dərinliklərindən istifadə edir. RGB rəng modeli və palitrası məlumatları həmişə şəkilləri saxlamaq üçün istifadə olunur. Versiyadan asılı olaraq, sabit uzunluqlu başlıq (GIF87a və ya GIF89a) tipik GIF faylının başlanğıcını müəyyən edir.

Hazırda GIF-in iki versiyası mövcuddur: 87a və 89a. Birincisi orijinal GIF formatıdır, ikincisi isə yeni GIF formatıdır. Bu fayl formatında blokların xüsusiyyətləri və piksel ölçüləri sabit uzunluqlu Məntiqi Ekran Deskriptorunda qeyd olunur. Qlobal Rəng Cədvəlinin mövcudluğu və ölçüsü, əgər varsa, əlavə təfərrüatları izləyən ekran deskriptoru ilə müəyyən edilə bilər. Treyler, ASCII nöqtəli vergülün bir baytını saxlayan faylın son baytıdır. Tipik bir GIF87a fayl tərtibatı aşağıdakı kimidir:

### Başlıq ###

Başlıq altı baytdan ibarətdir və faylın növünü GIF kimi təyin etmək üçün istifadə olunur. Məntiqi Ekran Deskriptoru faktiki başlıqdan ayrılsa da, bəzən ikinci başlıq kimi də qəbul edilir. Başlığı saxlamaq üçün istifadə edilən eyni struktur Məntiqi Ekran Deskriptorunu saxlaya bilər. Bütün GIF faylları 3 baytlıq imza ilə başlayır və identifikator kimi GIF” simvollarından istifadə edir. Versiya həmçinin üç bayt ölçüdədir və GIF faylının versiyasını elan edir.

### Məntiqi Ekran Deskriptoru ###

Sabit uzunluqlu Şəkil Deskriptoru GIF şəklini yaratmaq üçün lazım olan ekran və rəng məlumatlarını təyin edir. Hündürlük və Genişlik sahələri şəkil məlumatlarını göstərmək üçün məcburi olan ekran həllinin ən kiçik dəyərini əhatə edir. Əgər displey cihazı müəyyən edilmiş təsvir ölçüsünü göstərmək iqtidarında deyilsə, şəkli uyğun göstərmək üçün miqyaslama tələb olunacaq. Ekran və Rəng Xəritə məlumatı aşağıdakı cədvəlin dörd alt sahəsi ilə göstərilir (halbuki bit 0 ən az əhəmiyyətli bitdir):


|Bits|Alt sahələr
---|---|
|0-2|Qlobal Rəng Cədvəlinin Ölçüsü
|3|Rəng Cədvəli Çeşidləmə Bayrağı
|4-6|Rəng ayırdetmə qabiliyyəti
|7|Qlobal Rəng Cədvəli Bayrağı

#### Qlobal Rəng Cədvəli ####

İsteğe bağlı Qlobal Rəng Cədvəli Məntiqi Ekran Deskriptorundan dərhal sonra yerləşdirilir. Bu cədvəl şəkil məlumatlarının içərisindəki piksel rəng məlumatlarını indeksləşdirmək üçün tərtib edilmişdir. Qlobal Rəng Cədvəli olmadıqda, GIF faylındakı hər bir şəkil öz Yerli Rəngindən istifadə edir. Həm Qlobal, həm də Yerli Rəng Cədvəli yoxdursa, standart rəng cədvəlini təqdim etmək daha yaxşıdır. Üç baytlıq üçlük seriyası rəng cədvəlinin elementlərini təşkil edir. Hər bayt bir RGB rəng dəyərini xarakterizə edir. Qırmızı, yaşıl və mavi rənglər hər bir rəng cədvəli elementinin dəyərləri kimi istifadə olunur. Qlobal Rəng Cədvəlindəki qeydlər maksimum 256 daxil olur və həmişə ikinin gücündə təmsil olunur.

#### Şəkil Datası ####

Şəkil verilənləri kodlanmamış simvolların bir baytını saxlayır, sonra LZW ilə kodlanmış verilənlərlə birlikdə alt siyahıların əlaqələndirilmiş siyahısı.

#### Treyler ####

Treyler fayldakı son simvol olan bir bayt məlumatı təmsil edir. Bu baytın dəyəri daimi olaraq 3Bh-dir və məlumat axınının sonunu təyin edir. Hər bir GIF faylında hər bir faylın sonuncusunda treyler olmalıdır.

## İstinadlar ##

* [GIF fayl formatı](https://en.wikipedia.org/wiki/GIF)


