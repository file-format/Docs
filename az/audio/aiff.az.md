{
  "date": "2021-04-26",
  "keywords": [
"aiff",
"fayl",
"uzadılması",
"format",
"audio mübadilə fayl formatı",
"musiqi",
"aiff fayl formatı",
"aiff üçün mp3",
"aiff vs wav",
"aiff-i mp3-ə çevirmək"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "AIFF fayl formatı və AIFF fayllarını yarada, çevirə və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "AIFF - Audio Mübadilə Fayl Formatı",
  "linktitle": "AIFF",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-aif-azf"
}
},
  "lastmod": "2021-04-26"
}

## AIFF faylı nədir?
AIFF (Audio Interchange File Format) 1998-ci ildə Apple tərəfindən hazırlanmış sıxılmamış audio fayl formatıdır, lakin Amiga sistemlərində istifadə olunan sarğı formatı olan **EA IFF 85** (Electronic Arts tərəfindən hazırlanmış Mübadilə Format Faylları üçün Standart) əsasında qurulmuşdur. . Bu fayl formatı seçilmiş səslərin saxlanması üçün bir standart təqdim edir. Format çeviklik baxımından kifayət qədər yaxşıdır və müxtəlif nümunə sürətlərində və nümunə genişliklərində mono və ya çoxkanallı seçmə səsləri saxlamağa imkan verir. AIFF faylları sıxılmamış olduğundan, bu, onları [MP3](/audio/mp3/) kimi digər itkili formatlardan daha böyük edir.

AIFF faylları 44.1 kHz-də qeydə alınmış 16 bit nümunə ölçüsü olan 2 sıxılmamış stereo audio kanalından ibarətdir. Audionun yüksək keyfiyyətinə görə, 5 dəqiqəlik audio [WAV](/audio/wav/) fayl formatına bənzər 50MB-a qədər disk sahəsi tuta bilər.

## AIFF vs WAV

AIFF və WAV keyfiyyət baxımından demək olar ki, eynidir. Onların hər ikisi eyni PCM (pulse-code modulation) kodlaşdırmasından istifadə edir ki, bu da onları [MP3](/audio/mp3/), [M4A](/audio/m4a/) kimi digər itkili formatlarla müqayisədə daha böyük edir. Ümumi fərqlərdən bəziləri aşağıdakı cədvəldə yazılmışdır:

|AIFF|WAV|
---|---|
|Əsasən MAC üçün istifadə olunur|Əsasən PC-lər üçün istifadə olunur|
|Metadetaya imkan verir| metadetaya icazə vermir|

## AIFF fayl strukturu

**EA IFF 85** məlumatların fayllarda saxlanması üçün ümumi strukturu müəyyən edir. **EA IFF 85** faylı bir sıra məlumat yığınlarından ibarətdir. AIFF faylının bir hissəsi bir neçə başlıq məlumatından və sonra verilənlərdən ibarətdir:
{{< figure src="../chunk.png" alt="AIFF yığını" >}}

AIFF faylı bir sıra müxtəlif növ parçaların toplusudur. AIFF fayl yığını yaratmaq üçün vacib olan iki ümumi parça növü var:
- **Ümumi Parça**: Seçilmiş səsi təsvir edən vacib parametrləri, məsələn, uzunluğu və seçmə sürətini ehtiva edir.
- **Sound Data Chunk**: Faktiki audio nümunələrini ehtiva edir.
Alət parametrlərini sadalayan, markerləri təyin edən, tətbiqlərə aid məlumatları saxlayan və s. bir çox başqa isteğe bağlı hissələr var.

### Yerli yığın növləri

AIFF yaratmaq üçün yığın növləri aşağıdakı cədvəldə verilmişdir:

|Yığın növü| Təsvir|
---|---|
|Common Chunk|Common Chunk nümunə götürülmüş səsin əsas parametrlərini təsvir edir|
|Sound Data Chunk|Sound Data Chunk faktiki nümunə çərçivələri ehtiva edir|
|Marker Chunk|Marker yığını səs məlumatında mövqeləri göstərən markerləri ehtiva edir|
|İnstrument Chunk|Alət yığını, nümunə götürən kimi alətin səs məlumatını səsləndirmək üçün istifadə edə biləcəyi əsas parametrləri müəyyənləşdirir|
|MIDI Data Chunk|MIDI Data Chunk MIDI məlumatlarını saxlamaq üçün istifadə edilə bilər|
|Audio Səsyazma Parçası|Audio Yazma Parçası audioyazı cihazlarına aid məlumatları ehtiva edir|
|Tətbiqə Xüsusi Yığma|Tətbiqə Xüsusi Yığıncaq proqram istehsalçıları tərəfindən istənilən məqsədlər üçün istifadə edilə bilər|
|Şərhlər yığını|Şərhlər yığını FORM AIFF|-də şərhləri saxlamaq üçün istifadə olunur.
|Mətn Parçaları - Ad, Müəllif, Müəlliflik hüququ, Annotasiya| Hamısı mətn parçalarıdır|

## İstinadlar ##

* [Audio Mübadilə Faylı Format - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Audio_Interchange_File_Format)


