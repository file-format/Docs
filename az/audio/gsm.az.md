{
  "date": "2021-08-05",
  "keywords": [
"gsm",
"fayl",
"uzadılması",
"format",
"Audio",
"Mobil Audio üçün Qlobal Sistem",
"gsm uzadılması",
"gsm faylları"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "GSM fayl formatı və GSM fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "GSM - Mobil Audio Fayl Formatının Qlobal Sistemi",
  "linktitle": "GSM",
  "menu": {
    "docs": {
      "parent": "audio",
      "identifier": "audio-gs-azm"
}
},
  "lastmod": "2021-08-05"
}

## GSM faylı nədir?

GSM Mobil Audio Format Faylları üçün Qlobal Sistem ilə əlaqəli fayl uzantısıdır. GSM genişləndirmələri olan fayllar Linux, Windows və Mac OS platformalarında açıla bilər. GSM fayl formatı audio faylları kateqoriyasına aiddir.

GSM faylı itkili CBR (Daimi bit sürəti) səs sıxılma kodek ilə kodlanır. GSM audio faylında nümunə sürəti saniyədə 8000 nümunə, məlumat sürəti isə 13 kbps civarındadır. GSM faylları daxilindəki bit sürəti səs yazma zamanı keyfiyyəti təmin edir. Bundan əlavə, GSM fayl formatı mobil telefonlarda istifadə ediləcək qlobal standart format kimi də tanınır və WAV faylları da GSM fayl formatından istifadə edərək asanlıqla kodlaşdırıla bilər. GSM faylı ilə bağlı hər hansı problem mütəxəssisə müraciət etmədən istifadəçinin özü tərəfindən asanlıqla həll edilə bilər.

İstifadəçilər həmçinin GSM fayllarını [MP3](/audio/mp3/) və [MP4](/video/mp4/) formatlarına çevirə bilərlər.

## GSM Fayl Formatının Qısa Tarixi

GSM Avropada internet telefoniya üçün yaradılmış audio fayl formatıdır. O, Avropa Telekommunikasiya Standartları İnstitutu (ETSI) tərəfindən mobil telefonlar və planşetlərdə istifadə olunan 2G rəqəmsal mobil rabitə kimi istifadə edilmək üçün hazırlanmışdır. Bu gün telefon danışıqlarının və səsli mesajların qeydlərini saxlamaq üçün istifadə olunur.

## GSM File Format Specifications ##

GSM aşağıdakı bölmələrdən ibarət strukturlaşdırılmış şəbəkə üzərində işləyir:

- **Modulyasiya**: Bu, daxil edilmiş məlumatların asanlıqla ötürülə bilən formata çevrilməsi prosesidir. Göndərilən məlumatlar qəbuledici tərəfdə demodulyasiya edilir
- **Ötürülmə sürəti**: GSM 270 kbps-dən çox bit sürətinə malik rəqəmsal sistemdir
- **Uplink Tezlik diapazonu** : 933-960 MHz
- **Downlink Tezlik diapazonu**: 890 – 915 MHz
- **Kanal Aralığı** : Bu, təxminən 200 kHz olmalıdır bitişik maneələr arasındakı məsafə deməkdir
- **Dupleks Məsafə**: 80 MHz olması lazım olan yuxarı və aşağı bağlantı tezlikləri arasındakı boşluqdur.
- **Nitq Kodlaşdırma**: GSM Xətti Proqnoz Kodlaşdırmadan (LPC) istifadə edir. LPC bit sürətini sıxır. Səs siqnalı filtrdən keçdikdə və səs traktını təqlid etdikdə. GSM nitqi 13kbps-də kodlayır

| Audio sıxılma formatı | Alqoritm | Nümunə dərəcəsi | Bit dərəcəsi çevrilməsi | Gecikmə | CBR | VBR | Stereo | Çoxkanallı |
| ---------------------------------- | --------- | ----------- | ------------------ | -------- | --- | --- | ------ | ------------ |
| |
| GSM-HR | VSELP | 8 kHz | 5,6 kbit/s | 25 ms | Bəli | Yox | Yox | Yox |
| GSM-FR | RPE-LTP | 8 kHz | 13 kbit/s | 20–30 ms | Bəli | Yox | Yox | Yox |
| GSM-EFR | ACELP | 8 kHz | 12,2 kbit/s | 20–30 ms | Bəli | Yox | Yox | Yox |

## İstinadlar ##

* [GSM - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/Comparison_of_audio_coding_formats)


