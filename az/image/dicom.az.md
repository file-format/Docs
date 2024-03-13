{
  "date": "2019-10-11",
  "keywords": [
"dicom faylı",
"dicom fayl formatı",
"dicom faylı nədir",
"fayl",
"dicom nümunəsi",
"dicom fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DICOM - Rəqəmsal Görünüş və Rabitə Fayl Formatı",
  "description": "DICOM faylları yarada və aça bilən DICOM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "DICOM",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dico-azm"
}
},
  "lastmod": "2019-09-10"
}

## DICOM faylı nədir?

DICOM Tibbdə Rəqəmsal Görüntüləmə və Rabitə üçün qısaltmadır və Tibbi İnformatika sahəsinə aiddir. DICOM müxtəlif təchizatçıların printerləri, serverləri, skanerləri və s. DICOM faylları DICOM formatında şəkil məlumatlarını qəbul edə bilsələr, iki tərəf arasında paylaşıla bilər. DICOM-un rabitə hissəsi tətbiq səviyyəsi protokoludur və qurumlar arasında əlaqə yaratmaq üçün TCP/IP-dən istifadə edir. Veb xidmətləri tərəfindən dəstəklənən versiyalar 1.0, 1.1, 2 və ya daha sonrakı versiyalardır.

## Tarix ##

DICOM was developed jointly by American College of Radiology (ACR) and National Electrical Manufacturers Association (NEMA) for the exchange and viewing of medical images like MRIs, CT scans and ultrasound images. Initially, it was hard to decode the images that the machines produced. Therefore, ACR and NEMA together formed a team in 1983 which released its first standard, ACR/NEMA 300 in 1985. İkinci versiya 1988-ci ildə buraxıldı və bu, satıcılar arasında daha populyar idi, lakin tezliklə ikinci versiyanın da təkmilləşdirilməyə ehtiyacı olduğu başa düşdü. Standartın 3-cü versiyası 1993-cü ildə DICOM adı ilə buraxılmışdır. 3.0 hələ də ən son versiyadır, lakin 1993-cü ildən bəri davamlı olaraq yenilənir.

## DICOM fayl formatı ##

DICOM fayl formatı tərifinin və şəbəkə rabitə protokolunun birləşməsidir. DICOM .DCM genişlənməsindən istifadə edir. .DCM iki müxtəlif formatda mövcuddur, yəni format 1.x və format 2.x. DCM Format 1.x daha sonra normal və uzadılmış iki versiyada mövcuddur. HTTP və HTTPS protokolları DICOM-un veb xidmətləri üçün istifadə olunur.

### Fayl başlığı ###

Fayl başlığı 128 bayt Fayl Preambulasından və 4 baytlıq DICOM prefiksindən ibarətdir.

**Preambula # 128 Bayt**|**Prefiks # 4 Bayt D, I, C, M**

**Preambula** ümumi istifadə olunan şəkil fayl formatları ilə uyğunluğu təmin edən DICOM faylındakı şəkillərə və digər məlumatlara daxil olmaq üçün istifadə olunur.

**Prefiks** böyük hərf kimi DICM sətrini ehtiva edir.

### Data Set ###

Hər bir fayl SOP instansiyasını və müvafiq IOD ilə SOP Sinifini təmsil edən vahid məlumat dəstindən ibarət olmalıdır. Verilənlər toplusu real dünya məlumatlarının təmsilidir. Məlumat dəsti məlumat elementlərini, məlumat elementləri isə həmin obyektin atributlarının qiymətlərini ehtiva edir. Atributların strukturu IOD-lərdə müəyyən edilir. DICOM məlumat obyekti ad, ID və s. kimi elementlər daxil olmaqla bir sıra atributlardan və həmçinin təsvirin piksel məlumatlarını ehtiva edən bir xüsusi atributdan ibarətdir.

### Məlumat Elementləri ###

Məlumat elementi məlumat elementi Tag, Dəyər uzunluğu və Data Elementi üçün dəyərdən ibarətdir. 5 növ Məlumat elementi var, bunlar Tip 1 Tələb olunan Məlumat elementləri, Tip 1C Şərti Məlumat Elementləri, Tip 2 Tələb olunan Məlumat Elementləri, Tip 2C Şərti Məlumat Elementləri və Tip 3 Əlavə Məlumat Elementləri. Əsas üç məlumat elementi strukturu aşağıdakı kimidir.

**Açıq VR ilə Data Elementi**

|Qrup Nömrəsi|Element Nömrəsi|Dəyər Təmsilçiliyi|Qorunmuş|Dəyər Uzunluğu|Dəyər Sahəsi
---|---|---|---|---|---|
|2 Bayt|2 Bayt|2 Bayt|2 Bayt # 0x00, 0x00|4 Bayt|Dəyər Uzunluğu Baytları

**Açıq VR ilə Data Elementi**

|Qrup nömrəsi|Element nömrəsi|Dəyər təmsili|Dəyər uzunluğu|Dəyər sahəsi
---|---|---|---|---|
|2 Bayt|2 Bayt|2 Bayt|2 Bayt|Dəyər Uzunluğu Baytları

**Qeyri-müəyyən VR ilə Məlumat Elementi**


|Qrup nömrəsi|Element nömrəsi|Dəyər uzunluğu|Dəyər sahəsi
---|---|---|---|
|2 Bayt|2 Bayt|4 Bayt|Dəyər Uzunluğu Baytları

1. **Data Element Tag**: Qrup nömrəsini və element nömrəsini təmsil edən sifarişli tam ədəd
1. **Value Representation VR**: VR data Elementinin VR-ni təmsil edən simvol sətridir.
1. **Dəyər Uzunluğu**: işarəsiz tam ədəd dəyər sahəsinin açıq uzunluğunu təmsil edir.
1. **Dəyər Sahəsi**: Məlumat elementlərinin dəyərlərini təsvir edir.

## Transfer Sintaksisi ##

Transfer sintaksisi daha mücərrəd sintaksisləri birmənalı şəkildə təmsil etmək üçün kodlaşdırma qaydaları toplusudur. Transfer sintaksisinin köməyi ilə ünsiyyət quran qurumlar dəstəklədikləri ümumi kodlaşdırma üsulları üzərində danışıqlar aparırlar.

## SOPs ##

IOD və DIMSE Birliyi SOP Sinifini müəyyən edir. SOP Class tərifi DIMSE Xidmət Qrupunda və ya IOD Atributlarında xidmətlərdən istifadəni məhdudlaşdıra bilən qaydalar və semantikaları ehtiva edir. Xidmət Elementlərinə Nümunələr Saxla, Al, Tap, Köçür və s. Obyektlərə misal olaraq CT şəkilləri, MR şəkilləri, həmçinin cədvəl siyahıları, çap növbələri və s. daxildir.

## Xidmətlər ##

DICOM əsasən məlumatların kommunikasiyası ilə bağlı müxtəlif xidmətlər təqdim edir. Hər biri aşağıda qısaca təsvir edilmişdir:


**Mağaza:** DICOM Mağazası xidməti şəkilləri və ya digər obyektləri şəkil arxivləşdirmə və kommunikasiya sisteminə (PACS) və ya serverə göndərir.


**Saxlama öhdəliyi:** Saxlama öhdəliyi xidməti şəklin hər hansı bir media növündə cihazda daimi saxlandığını təsdiqləmək üçün istifadə olunur.


**Sorğu/alınma:** Bu xidmət iş stansiyasına şəkillərin və ya digər obyektlərin siyahılarını tapmaq və sonra onları PACS-dən əldə etmək imkanı verir.


**Modallıq iş siyahısı:** Modallıq iş siyahısı xidməti təsvirin əldə edilməsi cihazı tərəfindən yerinə yetirilməsi üçün planlaşdırılan təsvir prosedurlarının siyahısını verir.


**Çap edin:** Bu xidmət şəkilləri printerə göndərir.

## IP ## üzərindən port nömrələri

DICOM aşağıdakı TCP və UDP portlarından istifadə edir:

1. 104
1. 2761
1. 2762
1. 11112

## İstinadlar ##

* [https://en.wikipedia.org/wiki/DICOM](https://en.wikipedia.org/wiki/DICOM)

* [https://www.leadtools.com/sdk/medical/dicom-spec](https://www.leadtools.com/sdk/medical/dicom-spec)

* [https://www.dicomstandard.org/concepts/](https://www.dicomstandard.org/concepts/)

* [https://www.dicomlibrary.com/dicom/](https://www.dicomlibrary.com/dicom/)


