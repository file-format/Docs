{
  "date": "2019-10-11",
  "keywords": [
"j2c faylı",
"j2c fayl formatı",
"j2c faylı nədir",
"fayl",
"j2c nümunəsi",
"j2c fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "J2C",
  "description": "J2C faylları yarada və aça bilən J2C fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "J2C",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-j2-azc"
}
},
  "lastmod": "2021-02-14"
}

## J2C faylı nədir?

.j2c uzantısı olan fayl JPEG fayl formatının variantıdır və dalğacık sıxılması ilə sıxılır. O, JPEG 2000 fayl formatı ilə demək olar ki, eyni markerlər və seqmentlər sisteminə malikdir. J2C fayl formatı həm itkili, həm də itkisiz sıxılmanı dəstəkləyən JPEG 2000 stendinin 1-ci hissəsində müəyyən edildiyi kimidir. JPEG 2000 kod axını [JP2](/image/jp2/) və ya başqa fayl formatına daxil edilmək üçün nəzərdə tutulmuşdur, baxmayaraq ki, o, öz-özünə faylda görünə bilər. J2C faylı Adobe Photoshop 2020, Adobe Illustrator 2020 və Corel Paintshop Pro proqramlarından istifadə etməklə açıla bilər.

## J2C fayl formatı

J2C fayl formatı tez-tez .jp2 və .jpc kimi saxlanılan JPEG 2000 ilə eynidir. Bu, J2C fayllarını XML formatında metaməlumatların kodlaşdırılmasına eyni yanaşmanı tətbiq edir, burada Standart 12234-1 Exif teqləri və XML komponentləri arasında istinad kimi istifadə olunur. O, animasiya mexanizmini və kod axını konfiqurasiyalarını bir təsvirdə birləşdirən JPEG 2000 part-2 genişləndirilməsi ilə daha da təkmilləşdirilmişdir. Belə genişləndirilmiş fayl formatlı fayllar [.jpx](/image/jpx/) kimi saxlanılır.

### JPEG2000 Faylının Düzəlişi

JPEG2000 genişləndirilə bilən fayl formatlarına uyğunluğa əsaslanan müxtəlif proqramları dəstəkləyir. Ən sadə tipdə bir şəkil ola bilsə də, daha mürəkkəb növlər bir-birinin üstünə yığılmış və ya zamana əsaslanan ardıcıllıqla bir sıra şəkilləri əhatə edə bilər.

#### JP2 Qutusu
Bu, JP2 fayl formatının ən yüksək səviyyəli tikinti blokudur və başlıqda növ və uzunluq sahələrini və məlumat bölməsini ehtiva edir. Qutuların ən diqqətəlayiq növü bitişik kod axını qutusudur. Bu qutu məlumat bölməsində JPEG2000 kod axını saxlayır.

#### JPEG2000 CodeStream

JPEG2000 CodeStream JPEG2000 sıxılmış şəklin şifrəsini açmaq üçün tələb olunan bayt ardıcıllığıdır. Əgər faylda bu kod axınından başqa heç nə yoxdursa, ona xam kod axını faylı deyilir. Adətən JPEG kod axını, yeganə yol olmasa da, JPEG2000 sıxılma alqoritminin şəkil üzərində tətbiqidir.

#### Kafel hissələri ####

JPEG2000 kodlu təsvir paket adlanan məlumat vahidlərinin toplusudur. Bu paketlər kafel hissələri adlanan paket qrupları daxilində kod axınında saxlanılır. Şəkli kodlaşdırmadan əvvəl, kodlayıcı təsviri bloklardan ibarət düzbucaqlı şəbəkəyə ayırır, bunlar plitələr adlanır, burada hər bir plitə digər plitələrdən asılı olmayaraq ayrıca kodlanır.

{{< figure src="../JPEG2000_Codestream.png" alt="JPEG2000 Fayl Formatı" >}}

## J2C sıxılma
JPEG 2000 dalğacıqların sıxılma texnologiyasından istifadə edir ki, bu, tamaşaçının görüntünü göstərdiyi hər hansı görünüş pəncərəsində və ya pəncərədə nisbətən az piksel göstərilməsinə əsaslanaraq onu sürətləndirir. Bunu çox böyük ölçülü şəkillər (giqabaytlarla) üçün ekranda yalnız bir neçə meqabayt piksel görünməsi ilə vurğulamaq olar. Bu, görüntü məlumatının yalnız displey piksellərini doldurmaq üçün tələb olunan hissəsini sürətlə əldə etməyə və göstərməyə kömək edir. Bu, həm də tez bir zamanda tələb olunan təsvirləri yaratmaq üçün təsvirin əldə edilməsi mexanizmini sürətləndirmək üçün yüksək sürətli dekompressiya texnologiyasını tələb edir.

J2C sürətli dekompressiyadan istifadə edir və görünən təsvirlərin bir hissəsini tez bir zamanda ekranlara göstərmək üçün piksel məlumatları üçün yalnız lazımi məlumatları alır. J2C ilk növbədə məlumatlara baxmaq və onları redaktə etmək üçün nəzərdə tutulmuşdur.

## J2C İdentifikasiyası
JPEG 2000 fayllarında `FF 4F FF 51` imza baytları var.

### Mim növləri
JPEG 2000 faylları üçün qeydə alınmış Mime növlərinə aşağıdakılar daxildir:
  * şəkil/j2c
  * şəkil/jpx
  * şəkil/jpm
  * video/mj2

## JPEG standartı üzərində təkmilləşdirmələr
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

