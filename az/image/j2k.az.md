{
  "date": "2019-10-11",
  "keywords": [
"j2k faylı",
"j2k fayl formatı",
"j2k faylı nədir",
"fayl",
"j2k nümunəsi",
"j2k fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2K",
  "description": "J2K fayl formatı və J2K faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "J2K",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-azk"
}
},
  "lastmod": "2020-08-03"
}

## J2K faylı nədir?

**J2K** faylı DCT sıxılması əvəzinə dalğaların sıxılması ilə sıxılmış şəkildir. Bu fayl formatı Joint Photographic Experts Group (JPEG) 2000 faylları tərəfindən istifadə olunur. J2K faylları bu məqsəd üçün EXIF formatından istifadə edən .jpeg və ya .jpg-dən fərqli olaraq, şəkil faylı haqqında metadata məlumatını XML-də saxlayır. J2K faylları 15 bit rəng, alfa şəffaflığı və itkisiz sıxılmanı dəstəkləyir. J2K-Codec kimi JPEG 2000 şəkillərini deşifrə etmək üçün bir neçə kommersiya API mövcuddur. J2K faylı standart görüntü görüntüləyicilərindən istifadə edərək Windows OS-də açıla bilər.

## J2K Fayl Format ##

J2K fayl formatı tez-tez .jp2 və .jpc kimi saxlanılan JPEG 2000 ilə eynidir. Bu, J2K fayllarını XML formatında metaməlumatların kodlaşdırılmasına eyni yanaşmanı tətbiq edir, burada Standart 12234-1 Exif teqləri və XML komponentləri arasında istinad kimi istifadə olunur. O, animasiya mexanizmini və kod axını konfiqurasiyalarını bir təsvirdə birləşdirən JPEG 2000 part-2 genişləndirilməsi ilə daha da təkmilləşdirilmişdir. Belə genişləndirilmiş fayl formatlı fayllar .jpx kimi saxlanılır.

### JPEG2000 faylının tərtibatı ###

JPEG2000 genişləndirilə bilən fayl formatlarına uyğunluğa əsaslanan müxtəlif proqramları dəstəkləyir. Ən sadə tipdə bir şəkil ola bilsə də, daha mürəkkəb növlər bir-birinin üstünə yığılmış və ya zamana əsaslanan ardıcıllıqla bir sıra şəkilləri əhatə edə bilər.

#### JP2 Qutusu ####
Bu, JP2 fayl formatının ən yüksək səviyyəli tikinti blokudur və başlıqda növ və uzunluq sahələrini və məlumat bölməsini ehtiva edir. Qutuların ən diqqətəlayiq növü bitişik kod axını qutusudur. Bu qutu məlumat bölməsində JPEG2000 kod axını saxlayır.

#### JPEG2000 CodeStream ####

JPEG2000 CodeStream, JPEG2000 sıxılmış şəklin şifrəsini açmaq üçün tələb olunan bayt ardıcıllığıdır. Əgər faylda bu kod axınından başqa heç nə yoxdursa, ona xam kod axını faylı deyilir. Adətən JPEG kod axını, yeganə yol olmasa da, JPEG2000 sıxılma alqoritminin şəkil üzərində tətbiqidir.

#### Kafel hissələri ####

JPEG2000 kodlu təsvir paket adlanan məlumat vahidlərinin toplusudur. Bu paketlər kafel hissələri adlanan paket qrupları daxilində kod axınında saxlanılır. Şəkli kodlaşdırmadan əvvəl, kodlayıcı təsviri bloklardan ibarət düzbucaqlı şəbəkəyə ayırır, bunlar plitələr adlanır, burada hər bir plitə digər plitələrdən asılı olmayaraq ayrıca kodlanır.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 Fayl Formatı" >}}

## J2K Sıxılma ##
JPEG 2000 dalğacıqların sıxılma texnologiyasından istifadə edir ki, bu, tamaşaçının görüntünü göstərdiyi hər hansı görünüş pəncərəsində və ya pəncərədə nisbətən az piksel göstərilməsinə əsaslanaraq onu sürətləndirir. Bunu çox böyük ölçülü şəkillər üçün (giqabaytlarda) ekranda yalnız bir neçə meqabayt piksel görünməsi ilə vurğulamaq olar. Bu, görüntü məlumatının yalnız displey piksellərini doldurmaq üçün tələb olunan hissəsini sürətlə əldə etməyə və göstərməyə kömək edir. Bu, həm də tez bir zamanda tələb olunan təsvirləri yaratmaq üçün təsvirin əldə edilməsi mexanizmini sürətləndirmək üçün yüksək sürətli dekompressiya texnologiyasını tələb edir.

J2K sürətli dekompressiyadan istifadə edir və görünən təsvirlərin bir hissəsini tez bir zamanda ekranlara göstərmək üçün piksel məlumatları üçün yalnız lazımi məlumatları alır. J2K ilk növbədə məlumatlara baxmaq və onları redaktə etmək üçün nəzərdə tutulmuşdur.

## J2K İdentifikasiyası ##
JPEG 2000 faylları 6A 50 20 20 imza baytına malikdir.

### Mime növləri ###
JPEG 2000 faylları üçün qeydə alınmış Mime növlərinə aşağıdakılar daxildir:
  * şəkil/jp2
  * şəkil/jpx
  * şəkil/jpm
  * video/mj2

## JPEG standartı üzərində təkmilləşdirmələr ##
JPEG standartı üzərindəki təkmilləşdirmələrə aşağıdakılar daxildir:
  * Üstün sıxılma performansı
  * Çoxsaylı rezolyusiya təqdimatı
  * Piksel və qətnamə dəqiqliyi ilə proqressiv ötürülmə
  * İtkisiz və ya itkili sıxılma seçimi
  * Səhv davamlılığı, Çevik fayl formatı
  * Yüksək dinamik diapazon dəstəyi
  * Yan kanalın məkan məlumatı

## İstinadlar ##
  * [Taubman, David; Marcellin, Michael (2012)](https://books.google.com/books?id=y7HeBwAAQBAJ&pg=PA402)

