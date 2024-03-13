{
  "date": "2019-10-11",
  "keywords": [
"exif faylı",
"exif fayl formatı",
"exif faylı nədir",
"fayl",
"exif nümunəsi",
"exif fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "EXIF",
  "description": "EXIF fayl formatı və EXIF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "EXIF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-exi-azf"
}
},
  "lastmod": "2019-09-10"
}

## EXIF faylı nədir?
EXIF stands for “Exchangeable Image File Format”, the definition first given by [Japan Camera Industry Association](https://en.wikipedia.org/wiki/Japan_Electronic_Industries_Development_Association) (JCIA) in 1985. Standart bu gündən etibarən Yaponiya Elektron və İnformasiya Texnologiyaları Sənayesi Assosiasiyası (JEITA) tərəfindən idarə olunur. EXIF əsasən rəqəmsal kameralar və skanerlər tərəfindən istifadə olunan şəkil və səs formatlarının spesifikasiyası üçün standartdır.

EXIF standartına şəkil faylı ilə etiketləmə və metadata məlumatı daxildir. Metaməlumatlar kamera modeli, çekim sürəti, Tarix və vaxt, diyafram, istehsalçı, ekspozisiya vaxtı, X ayırdetmə qabiliyyəti, Y təsviri və s. kimi məlumatları ehtiva edə bilər. Adətən EXIF məlumatları defolt olaraq gizlədilir. EXIF məlumatlarına baxmaq üçün şəkilə baxmaq proqramında görünüş xüsusiyyətlərini seçmək lazımdır. Exif metaməlumatına həmçinin bir şəkil faylında texniki və ilkin təsvir məlumatları ilə yanaşı miniatürlər də daxil ola bilər.

## Tarix və versiyalar ##

* Oktyabr 1995-ci ildə JEIDA Versiya 1-i qurdu. Bu versiyada JEIDA şəkil məlumat formatı və atribut məlumatlarından və əsas teqlərdən ibarət strukturu müəyyən etdi.

* Noyabr 1997-ci ildə 1.1 versiyası 1-ci versiyanın əksər teqləri ilə təqdim edildi, eyni zamanda əlavə atribut məlumatı və format əməliyyatı üçün müddəalar əlavə edildi.

* İyun 1998, sRGB rəng məkanı, sıxılmış miniatürlər və audio faylları ilə Versiya 2.

* Dekabr 1998, təkmilləşdirilmiş yaddaş və atribut məlumatı ilə Versiya 2.1.

* Fevral 2002, Versiya 2.2, çap sonunun əlavə edilməsi ilə təkmilləşdirilmiş 2.1 versiyası.

* Sentyabr 2003, adobe RGB kimi tanınan əlavə rəng sahəsi ilə Versiya 2.21.


## EXIF fayl formatı

EXIF xüsusi metadata əlavə etməklə aşağıdakı fayl formatlarından istifadə edir.

1. [JPEG](/image/jpeg/) - sıxılmış şəkil faylları üçün diskret kosinus çevrilməsi (DCT).
1. Sıxılmamış şəkil faylları üçün [TIFF](/image/tiff/) Rev. 6.0 (RGB və ya YCbCr).
1. Audio fayllar üçün [RIFF](https://en.wikipedia.org/wiki/Resource_Interchange_File_Format) [WAV](https://en.wikipedia.org/wiki/WAV) (Sıxılmamış audio data üçün Xətti [PCM](https://en.wikipedia.org/wiki/Pulse-code_modulation) və ya ITU-T [G.711](https://en.wikipedia.org/wiki/G.711) μ-Qanun PCM və [IMA](https://en.wikipedia.org/wiki/Interactive_Multimedia_Association)-[ADPCM](https://en.wikipedia.org/wiki/ADPCM) sıxılmış audio məlumatları üçün).

### EXIF tərəfindən istifadə edilən marker ###

0xFFE0~~0xFFEF markeri istifadəçi proqramı tərəfindən istifadə edilən Tətbiq Markeridir. Məsələn, köhnə rəqəmsal kameralar şəkilləri saxlamaq üçün JFIF (JPEG Fayl Mübadilə Formatından) istifadə edir. JFIF rəqəmsal kamera konfiqurasiyası məlumatlarını və miniatür şəklini daxil etmək üçün APP0 (0xFFE0) Markerindən istifadə edir. Bundan əlavə, EXIF məlumat daxil etmək üçün Tətbiq Markerindən də istifadə edir, lakin EXIF JFIF formatı ilə ziddiyyətdən qaçmaq üçün APP1 (0xFFE1) Markerindən istifadə edir. Hər EXIF fayl formatı bu formatdan başlayır.


|SOI Marker|APP1 Marker|APP1 Data|Digər Marker
---|---|---|---|
|FFD8|FFE1|SSSS 457869660000 TTTT......|FFXX SSSS DDDD......

O, SOI (0xFFD8) Markerindən başlayır, ona görə də JPEG faylıdır. Sonra APP1 Marker dərhal izləyir. EXIF-in bütün məlumatları bu APP1 məlumat sahəsində saxlanılır. Üst cədvəldəki SSSS hissəsi APP1 məlumat sahəsinin (EXIF məlumat sahəsi) ölçüsünü bildirir. Diqqət yetirin ki, SSSS ölçüsü həm də deskriptorun ölçüsünü ehtiva edir. SSSSdən sonra APP1 məlumatları başlayır. Birinci hissə EXIF olub-olmadığını müəyyən etmək üçün xüsusi məlumatdır, ASCII simvolu EXIF və 2 bayt 0x00 istifadə olunur. APP1 Marker sahəsindən sonra digər JPEG Markerləri izləyir.

### Exif Data Strukturu ###

EXIF məlumatlarının kobud strukturu (APP1) aşağıda göstərilmişdir. Yuxarıda müzakirə edildiyi kimi, EXIF məlumatları ASCII EXIF simvolundan və 2 bayt 0x00-dan başlayır, sonra EXIF məlumatları izləyir. EXIF məlumatları saxlamaq üçün TIFF formatından istifadə edir.


|FFE1|APP1 Marker
---|---|
|SSSS|APP1 Data|APP1 Data Ölçüsü
|45786966 0000|Exif Başlığı
|49492A00 08000000|TIFF Başlığı
|XXX. . . .|IFD0 (əsas şəkil)|Kataloq
|LLLLLLLL|IFD1 ilə əlaqə
|XXX. . . .|IFD0 məlumat sahəsi
|XXX. . . .|Exif SubIFD|Kataloq
|00000000|Linkin sonu
|XXX. . . .|Exif SubIFD-nin məlumat sahəsi
|XXX. . . .|IFD1(kiçik şəkil)|Kataloq
|00000000|Linkin sonu
|XXX. . . .|IFD1-in məlumat sahəsi
|FFD8XXXX. . . XXXXFFD9|Kiçik şəkil

#### TIFF Başlığı ####

8 baytlıq [TIFF](/image/tiff/) fayl başlığı aşağıdakı məlumatları ehtiva edir:

`Bayt 0-1:` Fayl daxilində istifadə olunan bayt sırası. Hüquqi dəyərlər bunlardır:II”(4949.H)MM” (4D4D.H).

II” formatında bayt sırası həmişə həm 16-bit, həm də 32-bit tam ədədlər üçün ən az əhəmiyyətli baytdan ən əhəmiyyətli bayta doğru olur. Buna kiçik endian bayt sırası deyilir. MM” formatında bayt sırası həm 16-bit, həm də 32-bit tam ədədlər üçün həmişə ən əhəmiyyətlidən ən az əhəmiyyətliyə doğru olur. Buna big-endian bayt sırası deyilir.

`Bayt 2-3:` Faylı TIFF faylı kimi müəyyən edən ixtiyari, lakin diqqətlə seçilmiş nömrə (42). Bayt sırası 0-1 Baytın dəyərindən asılıdır.

`Bayt 4-7:` İlk IFD-nin ofseti (baytlarda). Kataloq başlıqdan sonra faylın istənilən yerində ola bilər, lakin söz sərhədindən başlamalıdır. Xüsusilə, Şəkil Faylı Kataloqu təsvir etdiyi şəkil məlumatlarını izləyə bilər. Oxucular hara gətirib çıxarsalar da, göstəricilərə əməl etməlidirlər. Bayt ofset termini həmişə TIFF faylının başlanğıcı ilə bağlı bir yerə istinad etmək üçün bu sənəddə istifadə olunur. Faylın ilk baytı 0 ofsetinə malikdir.

#### Şəkil fayl kataloqu ####

IFD-də şəkil haqqında məlumat, eləcə də faktiki təsvir məlumatlarına göstəricilər var. O, kataloq girişlərinin sayının (yəni sahələrin sayının) 2 baytlıq hesabından və ardınca 12 baytlıq sahə girişlərinin ardıcıllığından ibarətdir. , ardınca növbəti IFD-nin 4 baytlıq ofseti (və ya yoxdursa 0). TIFF faylında ən azı 1 IFD olmalıdır və hər IFD-də ən azı bir giriş olmalıdır.

##### IFD Girişi #####

Hər 12 baytlıq IFD Girişi aşağıdakı formatdadır.


|Bayt|Təsvir
---|---|
|0-1|Sahəni müəyyən edən Teq
|2-3|Sahə növü
|4-7|Göstərilən növün sayı
|8-11|Dəyər Ofseti, sahə üçün Dəyərin fayl ofseti (baytlarla). Dəyərin söz sərhədindən başlaması gözlənilir; müvafiq Dəyər Ofset beləliklə cüt ədəd olacaqdır. Bu fayl ofseti, hətta şəkil məlumatından sonra da faylın istənilən yerini göstərə bilər

TIFF sahəsi TIFF etiketindən və onun dəyərindən ibarət məntiqi varlıqdır. Bu məntiqi konsepsiya IFD Girişi kimi həyata keçirilir, üstəgəl dəyər/ofset hissəsinə, IFD Girişinin son 4 baytına uyğun gəlmirsə, faktiki dəyər. TIFF sahəsi və IFD girişi terminləri əksər kontekstlərdə bir-birini əvəz edir.

#### Kiçik şəkil ####

Exif format contains thumbnail of image (except Ricoh RDC-300Z). Usually it is located next to the IFD1. Miniatürlər üçün 3 format var; JPEG formatı (JPEG YCbCr istifadə edir), RGB TIFF formatı, YCbCr TIFF formatı.

##### JPEG Format Miniatürü #####

If the value of Compression(0x0103) Tag in IFD1 is '6', thumbnail image format is JPEG. Most of Exif image uses JPEG format for thumbnail. In that case, you can get offset of thumbnail by JpegIFOffset(0x0201) Tag in IFD1, size of thumbnail by JpegIFByteCount(0x0202) Tag. Data format is ordinary JPEG format, starts from 0xFFD8 and ends by 0xFFD9. Görünür, JPEG formatı və 160x120 piksel ölçüsü Exif2.1 və ya daha sonrakı versiyalar üçün tövsiyə olunan miniatür formatıdır.

##### TIFF Format Miniatürü #####

IFD1-də Compression(0x0103) Tag dəyəri '1' olarsa, kiçik şəkil formatı sıxılma deyildir (TIFF şəkli adlanır). Miniatür məlumatının başlanğıc nöqtəsi StripOffset(0x0111) Tag, miniatür ölçüsü StripByteCounts(0x0117) Tag-in cəmidir.

## İstinadlar ##

* [EXIF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Exif)

* [EXIF fayl formatı](https://www.media.mit.edu/pia/Research/deepview/exif.html)


