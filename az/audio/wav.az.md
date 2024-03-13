{
  "date": "2019-12-13",
  "keywords": [
"WAV",
"fayl",
"uzadılması",
"format",
"audio mübadilə fayl formatı",
"musiqi"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "WAV fayl formatı və WAV fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "WAV - Waveform Audio Fayl Format",
  "linktitle": "WAV",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-wa-azv"
}
},
  "lastmod": "2019-12-13"
}

## WAV faylı nədir?

WAVE (Waveform Audio File Format) ilə tanınan WAV rəqəmsal audio faylları saxlamaq üçün Microsoft-un Resurs Mübadilə Fayl Formatının (RIFF) spesifikasiyasının alt dəstidir. Format bit axınına heç bir sıxılma tətbiq etmir və audio yazıları müxtəlif seçmə sürətləri və bit sürətləri ilə saxlayır. Audio CD-lər üçün standart formatlardan biri olmuşdur və belədir. Dalğa faylları [MP3](/audio/mp3/) kimi yeni audio fayl formatları ilə müqayisədə daha böyükdür. Bu format eyni audio keyfiyyətini qoruyarkən fayl ölçüsünü azaltmaq üçün itkili sıxılmadan istifadə edir. Bununla belə, WAV faylları Audio Compression Manager (ACM) kodeklərindən istifadə edərək sıxıla bilər. WAV fayllarını digər məşhur audio fayl formatlarına çevirə bilən bir neçə API və proqramlar mövcuddur.

**Bilirdinizmi?**
You can become a contributor at FileFormat.com to keep the file format community up to date with your findings. If you have to share anything about WAV or Audio file formats, you can post your findings in [Audio File Format News](https://news.fileformat.com/t/audio) section for people to remain up to date.

## WAV fayl formatı ##

Microsoft-un RIFF spesifikasiyasının alt dəsti olan WAVE fayl formatı fayl başlığından sonra məlumat hissələrinin ardıcıllığı ilə başlayır. WAVE faylı iki alt hissədən ibarət tək WAVE yığınına malikdir:

* "fmt" yığını - məlumat formatını təyin edir

* "məlumat" yığını - faktiki nümunə məlumatını ehtiva edir


### WAV fayl başlığı ###

WAV (RIFF) faylının başlığı 44 bayt uzunluğundadır və aşağıdakı formata malikdir:


|Vəzifələr|Nümunə Dəyər|Təsvir
---|---|---|
|1 - 4|RIFF|Faylı riff faylı kimi qeyd edir. Simvolların hər biri 1 bayt uzunluğundadır.
|5 - 8|Fayl ölçüsü (tam)|Ümumi faylın ölçüsü - 8 bayt, baytla (32 bitlik tam ədəd). Bir qayda olaraq, bunu yaratdıqdan sonra doldurardınız.
|9 -12|WAVE|Fayl Tipi Başlığı. Bizim məqsədlərimiz üçün o, həmişə DALĞAya bərabərdir.
|13-16|fmt |Yığın markerini formatlayın. Sonuncu null daxildir
|17-20|16|Yuxarıda sadalanan format məlumatlarının uzunluğu
|21-22|1|Format növü (1 PCM-dir) - 2 bayt tam ədəd
|23-24|2|Kanalların sayı - 2 bayt tam ədəd
|25-28|44100|Sample Rate - 32 bayt tam ədəd. Ümumi dəyərlər 44100 (CD), 48000 (DAT). Nümunə Tezliyi = Saniyədə Nümunələrin Sayı və ya Hertz.
|29-32|176400|(Sample Rate * BitsPerSample * Kanallar) / 8.
|33-34|4|(BitsPerSample * Kanallar) / 8.1 - 8 bit mono2 - 8 bit stereo/16 bit mono4 - 16 bit stereo
|35-36|16|Nümunə başına bitlər
|37-40|data|məlumat yığın başlığı. Məlumat bölməsinin başlanğıcını qeyd edir.
|41-44|Fayl ölçüsü (məlumat)|Məlumat bölməsinin ölçüsü.
|Nümunə dəyərləri 16 bitlik stereo mənbə üçün yuxarıda verilmişdir.

## İstinadlar ##

* [WAV - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/WAV)


