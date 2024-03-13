{
   "date":"2023-10-11",
   "keywords":[
"m2v",
"m2v faylı",
"m2v mpeg-2 video faylı",
"m2v faylını necə açmaq olar",
"fayl",
"m2v fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"M2V Fayl Format - MPEG-2 Video",
   "description":"M2V MPEG-2 Video fayl formatı və M2V faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"M2V",
   "menu":{
      "docs":{
         "identifier":"video-m2v-az",
         "parent":"video"
}
},
   "lastmod":"2023-10-11"
}

## M2V faylı nədir?

M2V fayl formatı adətən **MPEG-2 Video** ilə əlaqəli fayl uzantısıdır. MPEG-2, DVD-lər, rəqəmsal televiziya yayımı və digər video yayım üsulları üçün tez-tez istifadə olunan geniş istifadə olunan video sıxılma standartıdır. M2V formatı xüsusi olaraq yalnız video məlumatlardan ibarətdir, yəni audio və ya hər hansı digər multimedia komponentləri daxil deyil. Bu, əsasən xam və ya elementar video axınıdır.

M2V faylları DVD-lərin müəllifi və ya yayım üçün video məzmunun yaradılması da daxil olmaqla müxtəlif məqsədlər üçün istifadə edilə bilər. Məsələn, DVD-lər yaratarkən, M2V video axını adətən tam DVD video yaratmaq üçün [AC3](/audio/ac3/) və ya LPCM kimi formatlarda ayrıca audio faylı ilə qoşalaşdırılır.

M2V fayllarını video redaktə və ya müəllif proqramında istifadə etmək üçün onları müvafiq audio faylı ilə birləşdirməli, menyular yaratmalı və məzmununuzu DVD və ya başqa bir paylama formatı üçün tərtib etməlisiniz.

M2V faylları ümumiyyətlə əksər media pleyerlərində və ya video redaktə proqramında birbaşa oxutmaq üçün nəzərdə tutulmur, çünki onların tam video təcrübəsi üçün audio və digər zəruri komponentləri yoxdur. Bunun əvəzinə onlar daha böyük multimedia layihəsinin və ya paylama paketinin bir hissəsidir.

## M2V Xüsusiyyətləri

MPEG-2 video standartının bir hissəsi olan M2V faylları bəzi vacib xüsusiyyətlərə və mülahizələrə malikdir:

1.  **Video Codec**: M2V faylları MPEG-2 video kodekdən istifadə edir ki, bu da geniş şəkildə qəbul edilmiş və yaxşı qurulmuş sıxılma standartıdır. MPEG-2 yaxşı video keyfiyyəti və sıxılma səmərəliliyi təklif edir ki, bu da onu DVD və rəqəmsal yayım da daxil olmaqla müxtəlif proqramlar üçün uyğun edir.
    
2.  **Audio yoxdur**: M2V faylları yalnız video komponentdən ibarətdir, ona görə də onların audio məlumatı yoxdur. Tam video fayl yaratmaq üçün M2V faylları adətən AC3 (Dolby Digital) və ya LPCM (Xətti Pulse Kodu Modulyasiyası) kimi formatlarda olan ayrı-ayrı audio faylları ilə qoşalaşdırılır.
    
3.  **Video Keyfiyyəti**: M2V faylındakı videonun keyfiyyəti kodlaşdırma zamanı istifadə olunan bit sürəti və ayırdetmə parametrləri kimi amillərə görə dəyişə bilər. Daha yüksək bit sürətləri və ayırdetmə keyfiyyəti daha yaxşı video keyfiyyəti, həm də daha böyük fayl ölçüləri ilə nəticələnir.
       
4.  **DVD Authoring**: M2V files are commonly used in authoring of DVDs. DVD authoring software combines M2V video streams with separate audio tracks, menus and navigation features to create complete DVD video.
    
5.  **Bitrate Control**: M2V faylında video axınının bit sürəti vacib bir məsələdir. Bu, həm video keyfiyyətinə, həm də tələb olunan yaddaş həcminə təsir göstərir. Daha yüksək bit sürətləri daha keyfiyyətli, lakin daha böyük fayl ölçüləri ilə nəticələnir.
    
6.  **Aspekt Nisbəti**: M2V faylları nəzərdə tutulan ekran formatından asılı olaraq 4:3 (standart) və ya 16:9 (geniş ekran) kimi müxtəlif aspekt nisbətlərini dəstəkləyə bilər.
    
7.  **Qətiyyət**: M2V faylında videonun həlli fərqli ola bilər, ümumi təsvir ölçüsü 720x480 (standart təsvir) və 1920x1080 (yüksək təsvir) olur.
    
8.  **Çərçivə Tezliyi**: MPEG-2 video müxtəlif kadr sürətlərində kodlaşdırıla bilər, lakin ümumi kadr sürətlərinə NTSC (Şimali Amerika) video üçün 29,97 fps və PAL (Avropa) video üçün 25 fps daxildir.
    
9.  **Redaktə**: M2V faylları uyğun video redaktə proqramı ilə redaktə edilə bilər, lakin yekun, tam video yaratmaq üçün onları audio treklər və digər multimedia elementləri ilə yenidən birləşdirməlisiniz.

## Multimedia formatları ilə M2V əlaqəsi

M2V files, as MPEG-2 video streams, are related to several other multimedia formats and components within context of video authoring, playback and distribution. Here are some of key relationships:

1.  **Audio Formatlar (AC3, LPCM və s.)**: Tam video fayl yaratmaq üçün M2V faylları adətən AC3 (Dolby Digital) və ya LPCM (Xətti Pulse Kodu Modulyasiyası) kimi formatlarda ayrı-ayrı audio faylları ilə qoşalaşdırılır. Bu audio formatlar multimedia məzmunu üçün audio komponenti təmin edir.
    
2.  **DVD Format (VOB)**: When authoring DVDs, M2V files, along with audio and other assets, are often combined into Video Object (VOB) format. VOB files contain video, audio, subtitles and menu information for DVD video discs.
    
3.  **Nəqliyyat axını (TS)**: Rəqəmsal yayımda MPEG-2 videosu çox vaxt Nəqliyyat Axını (TS) daxilində bükülür. Bu format rəqəmsal televiziya yayımı üçün video, audio və metadata daxildir və DVB (Rəqəmsal Video Yayımı) və ATSC (Qabaqcıl Televiziya Sistemləri Komitəsi) kimi xidmətlərdə istifadə olunur.
    
4.  **Proqram axını (PS)**: Proqram axını formatı (PS) MPEG-2 video, audio və digər məlumatların saxlanması üçün istifadə edilən başqa bir konteynerdir. Tez-tez videoların yayılması və saxlanması üçün istifadə olunur.
    
5.  **MPG (MPEG) Format**: .MPG fayl genişləndirilməsi adətən həm video, həm də audio ehtiva edən MPEG-2 video fayllarını işarələmək üçün istifadə olunur. M2V faylları daha geniş MPEG formatının alt dəstidir, xüsusilə səssiz videoya diqqət yetirir.
    
6.  **VOB (Video Obyekt) Faylları**: DVD videonun bir hissəsi kimi VOB faylları M2V video axınlarını ehtiva edə bilər. DVD yaratdığınız zaman VOB fayllarında video məzmunu çox vaxt M2V video və onu müşayiət edən audiodan ibarətdir.
    
7.  **Video Redaktə Proqramı**: Adobe Premiere Pro, Final Cut Pro və ya Sony Vegas kimi video redaktə proqramı redaktə məqsədləri üçün M2V faylları ilə işləyə bilər. Redaktorlar tam video layihələri yaratmaq üçün M2V video axınlarını audio və digər aktivlərlə birləşdirir.
    
8.  **Media Pleyerlər**: VLC və ya Windows Media Player kimi media pleyerlər adətən M2V fayllarını birbaşa oxutmaq üçün uyğun deyillər, çünki onların səsi yoxdur. Bu pleyerlər həm video, həm də audio daxil olan AVI, MP4 və ya MKV kimi daha çox yayılmış multimedia formatlarını idarə etmək üçün nəzərdə tutulub.
    
9.  **Blu-ray Format (M2TS)**: M2V ilə birbaşa əlaqəli olmasa da, M2TS formatı adətən Blu-ray disklərində yüksək dəqiqlikli video üçün istifadə olunur. M2TS fayllarında MPEG-2 video axınları, həmçinin H.264 və ya VC-1 video axınları və müxtəlif audio formatları ola bilər.
    
10.  **Video Sıxılma Standartları**: M2V fayllarında istifadə edilən MPEG-2 video, təkmilləşdirilmiş sıxılma səmərəliliyini təklif edən MPEG-4 (H.264 və H.265 daxil olmaqla) və VP9 kimi digər video sıxılma standartları ilə bağlıdır. və video keyfiyyəti. Bu standartlar rəqəmsal yayım, onlayn video və Blu-ray kimi daha yeni optik disk formatları üçün istifadə olunur.

## M2V faylını necə açmaq olar?

M2V fayllarını açan proqramlara daxildir

- VLC media pleyeri (platformalar arası)
- Apple QuickTime Player (Mac)
- Nullsoft Winamp
- CyberLink PowerDVD 21
- Windows Media Player (Windows)
- Media Player Classic (Windows)

## İstinadlar
* [Video fayl formatı](https://en.wikipedia.org/wiki/Video_file_format)


