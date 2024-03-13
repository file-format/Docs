{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PCL",
  "description": "PCL fayl formatı və PCL faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PCL",
  "menu": {
    "docs": {
      "parent": "page-description-language",
      "identifier": "page-description-language-pc-azl"
}
},
  "lastmod": "2019-09-10"
}

## PCL faylı nədir? ##

PCL Hewlett Packard (HP) tərəfindən təqdim edilmiş Səhifənin Təsviri Dili olan Printer Command Language mənasını verir. HP bir çox müxtəlif çap cihazlarında printer xüsusiyyətlərini idarə etmək üçün səmərəli üsul təmin etmək üçün PCL yaratmışdır. Format əvvəlcə HP-nin nöqtə matrisi və Inkjet printerləri üçün hazırlanmışdı, lakin zaman keçdikcə müxtəlif termal, matris və səhifə printerlərinin bir hissəsi olmuşdur. Format bir neçə fərqli düzəlişdən keçdi, nəticədə müxtəlif versiyalar yarandı ki, burada hər bir versiya printerin idarəetmə xüsusiyyətləri ilə bağlı zamanın tələblərinə cavab vermək üçün təkmilləşdirildi. Bu gün PCL son printer bazarında ən geniş yayılmış printer dilidir.

## PCL Versiyaları ##

PCL versiyaları funksionallıq baxımından fərqlənir (məsələn, şrift tipinə dəstək: bitmap şriftləri, genişlənən şriftlər (Intellifonts, TrueType şriftləri), raster qrafik sıxılma üsulları, HP-GL/2 qrafik dəstəyi).

**PCL 1:** təxminən 1980-ci il - Çap və Məkan funksionallığı sadə, rahat, bir istifadəçi iş stansiyası çıxışı üçün təmin edilən əsas funksiyalar dəstidir.

**PCL 2:** around 1980 - EDP (Electronic Data Processing)/Transaction functionality is a superset of PCL 1. Ümumi təyinatlı, çox istifadəçi sistemli çap üçün funksiyalar əlavə edildi.

**PCL 3**: 1984 - Office Word Processing functionality is a superset of PCL 2. Yüksək keyfiyyətli, ofis sənədlərinin hazırlanması və 300 dpi-ə qədər artan dpi üçün funksiyalar əlavə edildi. O, məhdud sayda bitmaplı şriftlərdən və qrafiklərdən istifadə etməyə icazə verdi və HP-GL-ni dəstəklədi. PCL 3 digər printer istehsalçıları tərəfindən geniş şəkildə təqlid edildi və bu şirkətlər tərəfindən LaserJet Plus Emulation adlandırıldı.
(Printerlər: HP DeskJet ailəsi, HP LaserJet seriyalı printer, HP LaserJet Plus seriyalı printer)

**PCL3+:** DeskJet və DesignJet printerlər ailəsi tərəfindən istifadə olunur.

**PCL3c:** DeskJet və DesignJet printerlər ailəsi tərəfindən istifadə olunur.

**PCL3e**: DeskJet və DesignJet printerlər ailəsi tərəfindən istifadə olunur. İndi PhotoSmart-da da istifadə olunur.

**PCL3GUI**: RTL istifadə edir və DeskJet və DesignJet printerlər ailəsi tərəfindən istifadə olunur.

**PCLSLEEK**: RTL istifadə edir və DeskJet və DesignJet printerlər ailəsi tərəfindən istifadə olunur.

**PCL 4**: 1985 - Page formatting functionality is a superset of PCL 3. Dəstəklənən makrolar, daha böyük bitmaplı şriftlər və qrafiklər. (Printerlər: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - Office Publishing functionality is a superset of PCL 4. Yeni nəşr imkanlarına şrift miqyası və HP-GL/2 (vektor) qrafikası daxildir. (Printerlər: HP LaserJet III)

**PCL 5e:** 1994 - Bu, Adaptiv Sıxılma Sistemi, 2 bayt simvol kodlaşdırması, vektor şriftləri üçün dəstək və iki istiqamətli konfiqurasiya əmrləri kimi yeni xüsusiyyətləri özündə cəmləşdirən əsas versiyadır. Yolları kəsməzdən əvvəl Windows dəstəyini təkmilləşdirmək üçün Məntiqi Əməliyyatlar (GDI ROP-larına uyğundur) daxildir. (Printerlər: HP LaserJet 4)

**PCL 5j:** Yapon rezidenti genişlənə bilən şriftlər, şaquli yazılar, Yapon kağız ölçüləri və şrift sətirləri üçün 2 bayt simvol dəstəyi kimi yeni xüsusiyyətlər. (Printerlər: HP LaserJet 4PJ)

**PCL 5c:** 1995 - Colour support and Logical Operations was added to PCL5. PCL5c predates PCL5e. Some models also support clipping paths. (Printers: HP Colour LaserJet, HP PaintJet 300 XL (first printer with PCL5c), HP DeskJet 1200C/1600C (these model numbers have been re-used and the newer models are not PCL 5c)

**PCL 5ce:** Agfa Microtype miqyaslı şriftləri dəstəkləyir. (Printerlər: HP 2500c Pro Printer)

**PCL 6 / XL:** 1996 - PCL 6 və ya PCL XL 1995-ci ildə təqdim edilmiş yeni formatdır və PCL-in əvvəlki versiyaları ilə uyğun gəlmir. (Printerlər: HP LaserJet 5, 5M və 5N)

## PCL 6 İcmal ##

HP 1996-cı ildə PCL dilinin və əlaqəli texnologiyaların növbəti təkamülü olan PCL 6-nı təqdim etdi. Onun aşağıdakı komponentləri var:

**PCL 6 Enhanced:** MS Windows və OS/2 kimi qrafik istifadəçi interfeyslərindən (GUI) çap üçün optimallaşdırılmış versiya təmin edir.

**PCL 6 Standard:** keçmiş HP LaserJet printerləri ilə tam geriyə uyğunluğu təmin edir

**PCL Font Synthesis:** miqyaslı şriftləri, şriftlərin idarə edilməsini və forma və şriftlərin saxlanmasını təmin edir.

Genişləndirilmiş PCL XL versiyası bir çox proqramın istifadə etdiyi GDI-yə daha yaxındır. Bu, daha az tərcümənin həyata keçirilməsini təmin edir ki, bu da WYSIWYG imkanlarının artmasına və Təkmilləşdirilmiş sürücü tərəfindən həyata keçirilən qaçışları dəstəkləyən proqramlarla daha yaxşı performansa səbəb olur. Təkmilləşdirilmiş (PCL XL) drayverinin çıxışı Standart drayverin çıxışı ilə eyni olmaya bilər. Çıxış gözlənildiyi kimi deyilsə, əvəzinə Standart (PCL5e) sürücüsünü seçin.

PCL 6 Enhanced əmrləri GUI əsaslı proqramlar üçün qrafik çap tələblərinə optimal uyğunlaşmaq üçün nəzərdə tutulmuşdur. Əksər hallarda, GUI-nin yerinə yetirmək istədiyi hər bir qrafik çap əmri üçün uyğun PCL 6 Enhanced əmri var. Bu, qrafik səhifəni təsvir etmək üçün tələb olunan əmrlərin sayını azaldır. PCL 6 Enhanced-dəki hər bir əmr əsas kompüterdən printerə minimal məlumat ötürülməsini tələb etmək üçün nəzərdə tutulmuşdur. Bu, səhifəni təsvir etmək üçün tələb olunan məlumatların miqdarını azaldır.

Əksər HP LaserJet printerləri üçün Windows Çap Sistemi iki ayrı sürücü təmin edir: Standart və Təkmilləşdirilmiş. Standart sürücü sadə mətn və ya qarışıq mətn və qrafik səhifələri çap etmək üçün PCL 6 Standard (PCL5e) əmrlərindən istifadə edərək geriyə uyğunluğu təmin edir. Təkmilləşdirilmiş sürücü mürəkkəb qrafik səhifələrin çapı üçün optimallaşdırılmış PCL 6 Enhanced əmrlərindən istifadə edir.

## PCL 6 Sinfi Reviziyaları ##

#### Sinif 1.1 ####

**Çəkmə alətləri:** Rəsm xətləri, qövslər/ellipslər/akkordlar, (dairəvi) düzbucaqlılar, çoxbucaqlılar, Bezier yolları, kəsilmiş yollar, rastr şəkilləri, skan xətləri, rastr əməliyyatlarını dəstəkləyin.
**Rənglə işləmə:** 1/4/8-bit palitraları, RGB/boz rəng məkanını dəstəkləyir. Fərdi yarım ton naxışlarını dəstəkləyin (maksimum 256 naxış).
**Sıxılma:** RLE-ni dəstəkləyir.
**Ölçü vahidləri:** Düym, millimetr, millimetrin onda biri.
**Kağızla işləmə:** Ümumi Letter, Legal, A4 və s. daxil olmaqla xüsusi və ya əvvəlcədən təyin edilmiş kağız növləri dəstlərini dəstəkləyin. Əl ilə qidalanma, qablar və kasetlərdən kağız seçə bilərsiniz. Kağız üfüqi və ya şaquli olaraq duplekslənə bilər. Kağız portret, mənzərə və ya əvvəlki ikisinin 180 dərəcə fırlanması ilə istiqamətləndirilə bilər.
**Font:** Supports bitmap or TrueType fonts, 8 or 16-bit code points. Choosing character set uses different symbol set code from PCL 5. Bitmap şriftindən istifadə edildikdə, bir çox miqyaslama əmrləri mövcud deyil. TrueType şriftindən istifadə edildikdə, dəyişən uzunluqlu deskriptorlar, davam blokları dəstəklənmir. Kontur şrifti döndərilə, ölçülü və ya kəsilə bilər.

#### Sinif 2.0 ####

**Sıxılma:** JetReady adlı xüsusi JPEG sıxılma əlavə edildi.
**Kağızla işləmə:** Media müxtəlif çıxış qutularına yönləndirilə bilər (256-ya qədər). A6 və Yapon B6 əvvəlcədən təyin edilmiş media ölçüləri əlavə edildi. Əlavə edilmiş Üçüncü kasetin əvvəlcədən təyini, 248 xarici tepsi media mənbəyi.
**Şrift:** Mətn şaquli şəkildə yazıla bilər.

#### Sinif 2.1 ####

**Rənglə işləmə:** Rəng uyğunlaşdırma xüsusiyyəti əlavə edildi.
**Sıxılma:** Delta Sırası əlavə edildi.
**Kağızla işləmə:** Yeni səhifə elan edilərkən oriyentasiya, media ölçüsü isteğe bağlıdır. B5, JIS 8K, JIS 16K, JIS Exec kağız növləri əlavə edildi.

#### Sinif 3.0 ####

**Rənglə işləmə:** Vektor və ya rastr qrafika, mətn üçün müxtəlif yarımton parametrlərindən istifadə etməyə icazə verin. Adaptiv yarım tonlaşdırmanı dəstəkləyir.
**Protocol:** Supports PCL passthrough, allowing PCL 5 features to be used by PCL 6 streams. However, some PCL 6 states are not preserved when using this feature.
**Şrift:** PCL şriftlərini dəstəkləyir.
**Viewer/Converter:** PCLReader (pulsuz proqram) PCL 6-nın istənilən səviyyəsini (JetReady daxil olmaqla) istənilən printerə baxa, çevirə və ya çap edə bilər.

## İstinadlar ##

* [PCL - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Printer_Command_Language)


