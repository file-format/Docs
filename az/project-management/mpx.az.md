{
  "date": "2019-10-11",
  "keywords": [
"mpx faylı",
"mpx fayl formatı",
"mpx faylı nədir",
"fayl",
"mpx nümunəsi",
"mpx fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MPX - Microsoft Project Exchange fayl formatı",
  "description": "MPX fayl formatı və MPX faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MPX",
  "menu": {
    "docs": {
      "parent": "project-management",
      "identifier": "project-management-mp-azx"
}
},
  "lastmod": "2021-05-07"
}

## MPX faylı nədir? ##

.mpx uzantılı fayl Microsoft Exchange Fayl Formatıdır. Primavera Project Planner, Sciforma və Timerline Precision Estimating daxil olmaqla, MSP və MPX fayl formatını dəstəkləyən digər proqramlar arasında layihə məlumat mübadiləsini asanlaşdırmaq üçün MPX fayl formatı Microsoft Project (MSP) tərəfindən hazırlanmışdır. MPX fayllarından istifadə edərək, siz hər cür məlumatı layihədən fərqli sistemə köçürə bilərsiniz, məsələn, ətraflı resurs təyinatı məlumatı, təqvim məlumatı və ya Layihə Məlumatı informasiya qutusundan məlumat.

Microsoft Project 4.0 introduced support for creating and reading MPX file formats that continued to be used through Microsoft Project 98. Bununla belə, MPX fayllarının yaradılması dəstəyi Microsoft Project 2000-in buraxılışını dayandırdı və Microsoft Project 2010-a qədər olan versiyalar yalnız MPX oxunmasını dəstəkləyir. MPX fayl formatı MSP 2010-dan sonrakı versiyalarda dəstəklənmir.

## MPX Fayl Format ##

MPX faylının spesifikasiyasına ümumi baxış bu bölmədə verilmişdir. Tam spesifikasiyalar bu [Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae) məqaləsində tapıla bilər və təfərrüatlar üçün istinad edilə bilər.

### Qeydlər ###

MPX faylının qeydi layihə üçün məlumatdan ibarətdir. Hər qeydin öz sırası olduğu müxtəlif növ qeydlər var. Hər bir qeyd növü öz rekord nömrəsi ilə müəyyən edilir. MPX faylı üçün Fayl Yaradılması qeyd tipini ehtiva etmək lazımdır. Digər növ qeydlər məcburi deyil. Aşağıdakı cədvəl bütün qeyd növlərini, onların qeyd nömrələrini və hər bir növün MPX faylında ola biləcəyi qeydlərin sayını göstərir. MPX faylına qeydin daxil edilməsi hər hansı yerə şərhlər daxil edilməklə cədvəl sırasına əməl etməlidir.

|Qeyd adı|Qeyd nömrəsi|Yazıların maksimum sayı
---|---|---|
|Fayl yaradılması (tələb olunur)|heç biri|1
|Valyuta Parametrləri|10|1
|Defolt Parametrlər|11|1
|Tarix və Saat Parametrləri|12|1
|Baza Təqvim Tərifi|20|250
|Baza Təqvim Saatları|25| Baza Təqvim Tərifi qeydinə görə 7
|Baza Təqvim İstisnası|26| Baza Təqvim Tərifi qeydinə görə 250
|Layihə Başlığı|30|1
|Mətn Resurs Cədvəli Tərifi|140|1- (Və ya Rəqəmsal Resurs Cədvəli Tərifi qeydindən istifadə edə bilərsiniz)
|Rəqəm Resurs Cədvəli Tərifi|41|1
|Resurs|50|9,999
|Resurs Qeydləri|51| Hər Resurs qeydinə 1
|Resurs Təqvim Tərifi|55| Hər Resurs qeydinə 1
|Resurs Təqvim Saatları|56| Resurs Təqvimi üçün 7
|Resurs Təqvim İstisnası| Resurs Təqvimi üçün 57|250
|Mətn Tapşırığı Cədvəli Tərifi|60|1 (Və ya Rəqəmsal Tapşırıq Cədvəli Tərifi qeydindən istifadə edə bilərsiniz)
|Rəqəm tapşırıq cədvəlinin tərifi|61|1
|Tapşırıq|70|9
|Tapşırıq qeydləri|71| Hər tapşırıq üçün 1 qeyd
|Təkrarlanan tapşırıq|72| Hər tapşırıq üçün 1 qeyd
|Resurs Təyinatı|75| Tapşırıq qeydinə görə 100
|Tapşırıq İşçi Qrupu sahələri|76| Tapşırıq qeydinə görə 1
|Layihə adları|80|500
|DDE və OLE Müştəri Linkləri|81|500
|Şərhlər|0|məhdudiyyətsiz

### Fayl strukturu ###

MPX faylı yuxarıda qeyd olunan qeydlərdən ibarətdir ki, onlar fayl daxilində əvvəlcədən müəyyən edilmiş qaydada yerləşdirilir. Bu qeyd növləri ilə bağlı təfərrüatlar aşağıdakı kimi müzakirə olunur:

**Fayl Yaratma Qeydi (FCR):** Bu, məqsədi aşağıdakıları müəyyən etmək olan məcburi qeyddir:

* Fayl formatı (MPX)

* Faylda istifadə olunan siyahı ayırıcı simvol

* Fayl yaratmaq üçün istifadə olunan proqram və versiya nömrəsi

* Faylda istifadə olunan MPX fayl formatının versiya nömrəsi

* Fayl yaratmaq üçün kod səhifəsi istifadə olunur


Bu fayldakı ilk qeyd olmalıdır. Microsoft Project-dən ixrac edərkən siyahı ayırıcı simvol Windows İdarəetmə Panelindəki Regional Parametrlər elementində müəyyən edilir. FCR Qeydinə aşağıdakı sahələr daxildir:

* MPX-dən dərhal sonra siyahı ayırıcı simvol

* Proqramın adı/identifikatoru

* Faylın versiya nömrəsi

* Kod Səhifəsi (850, 437, MAC, ANSI)


Məsələn, qeyddə **MPX, Microsoft Project, 3.0** məlumat ola bilər ki, bu da bu MPX faylında siyahı ayırıcı simvol kimi vergülün istifadə edildiyini göstərir. Faylda istifadə olunan MPX formatının versiyası Microsoft Project 3.0 versiyasından ixrac edilmişdir.

**Valyuta Parametrləri** Rekord nömrəsi 10 olan bu qeyd Seçimlər dialoq qutusunda valyuta seçimləri üçün parametrləri müəyyən edir. Bu qeyd daxil deyilsə, Seçimlər dialoq qutusundakı cari parametrlər istifadə olunur. Minlərlə və Ondalık ayırıcılar Windows İdarəetmə Panelindəki Regional Parametrlər bəndində göstərilmişdir.
Bu qeydə daxil edilən sahələr:

* Valyuta simvolu

* Simvol mövqeyi (0 # sonra, 1 # əvvəl, 2 # sonra boşluq, 3 # əvvəl boşluq)

* Valyuta Rəqəmləri (0,1,2)

* Minlərlə Ayırıcı

* Ondalık Ayırıcı


**Misal:** 10,$,1,2,,,.
Bu misal göstərir ki, valyuta dəyərlərinə onlardan əvvəl dollar işarəsi ($) daxildir, ondalık nöqtədən sonra iki rəqəm daxil edilir, minləri ayırmaq üçün vergüldən istifadə edilir və ondalıq nöqtə kimi nöqtə istifadə olunur. Siyahı ayırıcı simvolu Minlərlə Ayırıcı sahəsinə daxil edildiyi üçün sahə dırnaq işarələri ilə əhatə olunub.

**Defolt Parametrlər:** 11 nömrəli rekorda malik bu qeyd Seçimlər dialoq qutusunda standart seçimlər üçün parametrləri müəyyən edir. Müddət göstərilməyibsə, düzgün müddət vahidi hesablamaları üçün Defolt Müddət Vahidi təyin edilməlidir. Bu qeyd daxil deyilsə, Seçimlər dialoq qutusundakı cari parametrlər istifadə olunur.
Bu qeydə daxil edilən sahələr:

* Defolt Müddət Vahidləri (0 # dəqiqə, 1 # saat, 2 # gün, 3 # həftə)

* Defolt Müddət Növü (0 # sabit deyil, 1 # sabit)

* Defolt İş Vahidləri (0 # dəqiqə, 1 # saat, 2 # gün, 3 # həftə)

* Defolt Saat/Gün

* Defolt Saat/Həftə

* Defolt Standart Rate

* Defolt İş vaxtı dərəcəsi

* Tapşırıq Statusunun Yenilənməsi Resurs Vəziyyətinin Yenilənməsi (0 # yox, 1 # bəli)

* Davam etməkdə olan tapşırıqları bölün (0 # yox, 1 # bəli)


**Date and Time Settings:** This record, having record number 12, specify settings for the date and time options in the Options dialog box, and the Bar Text Date Format option in the Layout dialog box. If this record is not included, the current settings in the Options dialog box are used.
\\Bu qeydə daxil edilən sahələr:

* Tarix Sifarişi (0 # ay/gün/il, 1 # gün/ay/il, 2 # il/ay/gün)

* Vaxt formatı (0 # 12 saat, 1 # 24 saat)

* Defolt vaxt (gecə yarısından sonrakı dəqiqələrin sayı)

* Tarix Ayırıcı

* Vaxt Ayırıcı

* 0:00 - 11:59 Mətn

* 12:00-dan 23:59-a qədər Mətn

* Tarix Format (0 -14)*

* Bar Mətni Tarixi Format (0 -194)*


**Baza Təqvim Tərifi:** Rekord sayı 20 olan bu qeydlər əsas təqvimləri və onların həftənin iş və qeyri-iş günlərini müəyyən edir. Bir gün ərzində heç bir giriş olmadıqda, standart parametrlər istifadə olunur. Standart parametrlər iş günləri üçün bazar ertəsindən cümə gününə qədər, qeyri-iş günləri üçün isə şənbə və bazar günləridir. Bu qeyddə Ad sahəsi tələb olunur. Günlərin hər biri üçün 0 qeydi günün qeyri-iş günü olduğunu, 1 qeydi isə günün iş günü olduğunu bildirir.
Bu qeydə daxil edilən sahələr:

* Ad

* Bazar günü

* Bazar ertəsi

* Çərşənbə axşamı

* Çərşənbə

* Cümə axşamı

* Cümə

* Şənbə


**Baza Təqvim Saatları:** Rekord nömrəsi 25 olan bu qeydlər standart parametrlərdən fərqli olduqda həftənin günləri üçün iş saatlarını müəyyənləşdirir. Defolt iş saatları 8:00-dan 12:00-a qədər və 13:00-dan 17:00-a qədərdir. Hər bir Baza Təqvim Saatları qeydi əvvəlki Əsas Təqvim Tərifi qeydinə aiddir. Bu qeydlərdən yeddiyə qədər hər bir Baza Təqvim Tərifi qeydini izləyə bilər.

* Həftənin günü (1 - 7, burada 1 # bazar və 7 # şənbə)

* Vaxt 1

* Zamana 1

* Zaman 2

* Zamana 2

* Zaman 3

* Zamana 3


**Baza Təqvim İstisnası:** Rekord nömrəsi 26 olan bu qeydlər əvvəlki iki qeyd növündə göstərilən günlər və saatlar üçün istisnaları müəyyən edir. Bu qeydlərdən 250-yə qədəri hər bir Baza Təqvim Tərifi qeydini izləyə bilər. Bu qeydlər xronoloji ardıcıllıqla sadalanmalıdır. İstisna bir gündürsə, Tarix sahəsini boş qoya bilərsiniz. Heç bir vaxt göstərilməyibsə, standart saat 8:00-dan 12:00-a qədər və 13:00-dan 17:00-a kimi istifadə olunur.
Bu qeydə daxil edilən sahələr:

* Tarixdən

* Bu günə qədər

* İşləməyən/İşləyən (0 # işləmir, 1 # işləyir)

* Vaxt 1

* Zamana 1

* Zaman 2

* Zamana 2

* Zaman 3

* Zamana 3


**Project Header:** This record, having record value 30,  sets global project fields, such as the project start date and project finish date. The fields in this record correspond to the information in the Project Info and Statistics dialog boxes.
Bu qeydə daxil olan sahələr və tablar bunlardır:

* Layihə nişanı

* Şirkət

* Menecer

* Təqvim (Giriş yoxdursa standart istifadə olunur)

* Başlama Tarixi (Bu sahə və ya növbəti sahə, Cədvəldən asılı olaraq idxal edilmiş fayl üçün hesablanır)

* Bitmə tarixi

* Cədvəl (0 # başlanğıc, 1 # bitiş)

* Hal-hazırki Tarix*

* Şərhlər

* Xərc

* Baza dəyəri

* Faktiki xərc

* İş

* Əsas iş

* Faktiki iş

* İş

* Müddət*

* Əsas Müddət*

* Faktiki Müddət

* Faiz tamamlandı

* Əsas başlanğıc

* İlkin bitirmə

* Faktiki Başlanğıc

* Faktiki bitirmə

* Fərqliliyə başlayın

* Fərqi tamamlayın

* Mövzu

* Müəllif

* Açar sözlər


**Mətn Resurs Cədvəli Tərifi**: Bu qeyd idxal və ya ixrac edilən resurs sahələrini sıra ilə sadalayır. İdxal edilmiş fayllar üçün adlar Microsoft Project-də istifadə olunan sahə adlarına uyğun olmalıdır. İxrac edilmiş fayllar üçün bu qeyd resursun İxrac cədvəlindən gəlir. Ya bu qeyd, ya da Rəqəmsal Resurs Cədvəli Tərifi qeydindən istifadə edilməlidir. Microsoft Project-dən ixrac edərkən bu qeydlərin hər ikisi daxil edilir.

**Rəqəmsal Resurs Cədvəli Tərifi:** Adlardan çox nömrələrdən istifadə edərək, bu qeyd idxal və ya ixrac edilən resurs sahələrini sıra ilə siyahıya alır. Bu, hər bir Resurs qeydinə daxil olan resurs sahələrini müəyyən etmək üçün alternativ üsuldur və xarici dil məhsulu tərəfindən yaradılmış MPX faylını təyin edərkən faydalıdır.

**Resurs:** Bu qeydlər idxal və ya ixrac edilən hər bir resurs üçün məlumatı ehtiva edir. Hər Resurs qeydi bir mənbəni təsvir edir. Siz məlumatı idxal etdiyiniz zaman daxil edilən sahələr Mətn Resursları Cədvəli Tərifi qeydi və ya Rəqəmsal Resurs Cədvəli Tərifi qeydi ilə müəyyən edilir. Siz məlumatı ixrac etdiyiniz zaman daxil edilən sahələr resursun İxrac cədvəlində qeyd olunan sahələrdir.

**Resurs Qeydləri:** Bu qeydlərdə dərhal əvvəlki Resurs qeydi haqqında qeydlər var. Qeyd daxilində yeni sətir üçün ASCII simvolu 127 istifadə olunur. Qeydə siyahı ayırıcı simvol daxildirsə, qeydi dırnaq işarəsinə daxil edin.

**Resurs Təqvimi Tərifi:** Bu qeydlər dərhal əvvəlki Resurs qeydində göstərilən resurs üçün iş günlərini müəyyənləşdirir. İdxal edilmiş fayllar üçün, Baza Təqvim Adı sahəsində heç bir qeyd yoxdursa, Standart istifadə olunur. Müəyyən gün üçün heç bir qeyd günün standart olaraq təyin edildiyini göstərmir (2). Resurs Təqvimi Tərifi qeydləri yoxdursa, Standart resurs üçün əsas təqvim kimi istifadə olunur və standart günlər üçün istifadə olunur. Günlərin hər biri üçün 0 qeydi günün qeyri-iş günü olduğunu, 1 günün iş günü olduğunu, 2 isə defoltdan istifadə edildiyini bildirir.

**Resurs Təqvim Saatları:** Bu qeydlər resursun istifadə etdiyi əsas təqvimdən fərqli olan resurs üçün iş saatlarını müəyyən edir. Bu qeydlər bu qeyddən dərhal əvvəl olan Resurs Təqvim Tərifi qeydinə aiddir. Bu qeydlərdən yeddiyə qədər hər bir Resurs Təqvim Tərifi qeydini izləyə bilər.

**Resurs Təqvim İstisnası:** Bu qeydlər əvvəlki iki qeyd növündə göstərilən günlər və saatlar üçün istisnaları müəyyən edir. Bu qeydlərdən 250-yə qədər hər bir Resurs Təqvim Tərifi qeydini izləyə bilər. Bu qeydlər xronoloji ardıcıllıqla sadalanmalıdır. İstisna yalnız bir gündürsə, Tarix sahəsini boş qoya bilərsiniz. Heç bir vaxt göstərilməyibsə, standart saat 8:00-dan 12:00-a qədər və 13:00-dan 17:00-a kimi istifadə olunur.

**Text Task Table Definition:** This record lists the task fields, in order, that are being imported or exported. For imported files, the names must match the field names used in Microsoft Project. If the file is being exported, this record comes from the task Export table. When exporting from Microsoft Project, both of these records are included. Fields that are calculated by Microsoft Project, such as Scheduled Start and Scheduled Finish, are ignored if imported. If you have task start or finish dates that are fixed, use the Constraint Type and Constraint Date fields.

**Rəqəmsal Tapşırıq Cədvəli Tərifi:** Adlardan çox nömrələrdən istifadə edərək, bu qeyd idxal və ya ixrac edilən tapşırıq sahələrini sıralayır. Bu, hər bir Tapşırıq qeydinə daxil olan tapşırıq sahələrini müəyyən etmək üçün alternativ üsuldur və xarici dil məhsulu tərəfindən yaradılmış MPX faylını təyin edərkən faydalıdır.

**Tapşırıq:** Bu qeydlər idxal və ya ixrac edilən hər bir tapşırıq üçün məlumatı ehtiva edir. Hər Tapşırıq qeydi bir tapşırığı təsvir edir. Məlumatı idxal etdiyiniz zaman, daxil edilən sahələr Mətn Tapşırığı Cədvəli Tərifi qeydi və ya Rəqəmsal Tapşırıq Cədvəli Tərifi qeydi ilə müəyyən edilir. Siz məlumatı ixrac etdiyiniz zaman daxil edilən sahələr tapşırıq İxrac cədvəlində sadalanan sahələrdir.

**Tapşırıq Qeydləri:** Bu qeydlərdə dərhal əvvəlki Tapşırıq qeydləri haqqında qeydlər var. Qeyd daxilində yeni sətir göstərmək üçün ASCII simvolu 127-dən istifadə edin. Qeydə siyahı ayırıcı simvol daxildirsə, qeydi dırnaq işarəsinə daxil edin.

**Resurs Təyinatı**: Bu qeydlər əvvəlki Tapşırıq qeydində müəyyən edilmiş tapşırığa təyin edilmiş resurslar haqqında məlumatı siyahıya alır. Əgər siz faylları birləşdirirsinizsə və resurs təyinatı məlumatının saxlanmasını istəyirsinizsə, məlumatı MPX faylına daxil etməlisiniz. Əgər birləşdirsəniz, birləşdirilən tapşırıqlar üzrə bütün mövcud tapşırıqlar silinəcək. Əgər siz Unikal ID-lərə əsaslanan faylları birləşdirirsinizsə, resurslar ID-lərdən deyil, Resurs Unikal İdentifikatorlarından istifadə etməklə təyin edilir.

**Resource Assignment Workgroup Fields:** These records list the information that is stored with each assignment for the Workgroup features of Microsoft Project 4.0 and 4.1. Əgər İşçi Qrupu funksiyalarından istifadə edirsinizsə, məlumatların heç birinin itirilməməsini təmin etmək üçün bu qeydi daxil etməlisiniz.

**Layihə Adları:** Bu qeydlər layihədə saxlanılan bütün DDE keçid adlarının siyahısını verir.

**DDE və OLE Müştəri Linkləri:** Bu qeydlər layihəyə daxil olan DDE bağlantılarını siyahıya alır.

**Şərhlər:** Bu qeydlər fayla şərhlər əlavə etmək üçün istifadə edilə bilər və faylda istənilən mövqedə görünə bilər. Hər Şərh qeydi 0 ilə başlamalıdır.

## MPX faylını açmaqla bağlı problemlər ##

Budur, MPX formatının düzgün işləməməsinə səbəb ola biləcək bəzi ümumi problemlərin siyahısı:

 *   Dəstəkləyici proqram təminatının olmaması
 *   Zədələnmiş fayl
 *   Virus səbəbiylə yoluxmuş fayl
 *   Sistemdə faylları açmaq hüququ yoxdur
 *   Sisteminizdə köhnəlmiş disk
 *   Faylın genişləndirilməsinin adı dəyişdirilir

## İstinadlar ##

* [MPX - Microsoft Knowledge Base](https://support.microsoft.com/en-us/office/file-formats-supported-by-project-desktop-face808f-77ab-4fce-9353-14144ba1b9ae)


