{
  "date": "2019-10-11",
  "keywords": [
"wmf faylı",
"wmf fayl formatı",
"wmf faylı nədir",
"fayl",
"wmf nümunəsi",
"wmf fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "WMF - Microsoft Windows Metafayl Format",
  "description": "WMF fayl formatı və WMF fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "WMF",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-wm-azf"
}
},
  "lastmod": "2019-09-10"
}

## WMF faylı nədir?

WMF uzadılması olan fayllar vektor, eləcə də bitmap formatlı şəkillər məlumatlarını saxlamaq üçün Microsoft Windows Metafaylını (WMF) təmsil edir. Daha dəqiq desək, WMF cihazdan asılı olmayan Qrafik fayl formatlarının vektor fayl formatı kateqoriyasına aiddir. Windows Qrafik Qurğu İnterfeysi (GDI) ekranda təsviri göstərmək üçün WMF faylında saxlanılan funksiyalardan istifadə edir. Təkmilləşdirilmiş Meta Fayllar (EMF) kimi tanınan WMF-nin daha təkmil versiyası daha sonra nəşr olundu ki, bu da formatı daha zəngin xüsusiyyətlərə malikdir. Praktiki olaraq WMF SVG-yə bənzəyir.

## WMF Fayl Formatının Xüsusiyyətləri ##

A WMF file referred to 16-bit file format at the time of its launching with Windows 3.0. Fayl formatı qrafik rəsm əmrlərini, obyekt təriflərini və xassələrini ehtiva edən bir sıra dəyişən uzunluqlu qeydlərdən ibarətdir. WMF faylları təsvirin çəkilməsi üçün GDI-yə verilən əmrlərə əsaslandığından, o, eyni zamanda həmin təsviri yenidən yaratmaq üçün oxudula bilən təsvirin rəqəmsal qeydi kimi də tanınır. WMF-nin tam fayl formatı spesifikasiyası onlayn mövcuddur və WMF faylları ilə işləmək üçün proqramların hazırlanması üçün onlara istinad edilməlidir. WMF faylı aşağıdakı şəkildə təşkil edilir:

* WMF Başlıq Qeydi

* WMF Rekordları

* WMF Fayl Sonu Qeydi


### WMF Başlıq Qeydi ###

**META_HEADER Qeydi** metafaylın xüsusiyyətlərini təyin edən məlumatları ehtiva edir, o cümlədən:

* Metafaylın növü

* Metafaylın versiyası

* Metafaylın ölçüsü

* Metafaylda müəyyən edilmiş obyektlərin sayı

* Metafayldakı ən böyük tək qeydin ölçüsü


### WMF Yerləşdirilə bilən Başlıq Qeydi ###

**META_PLACEABLE Record** şəkillə bağlı geniş məlumatı ehtiva edir, o cümlədən:

* Məhdudlaşdıran düzbucaqlı

* Ölçmə üçün məntiqi vahid ölçüsü

* Doğrulama üçün yoxlama məbləği


### WMF Rekordu ###

WMF qeydləri spesifikasiyalar sənədində göstərilən ümumi formata malikdir. Hər bir WMF qeydi aşağıdakı məlumatları ehtiva edir:

* Rekord ölçüsü

* Qeyd funksiyası

* Parametrlər, əgər varsa, qeyd funksiyası üçün


## İstinadlar ##

* [[MS-WMF]: Windows Metafayl Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)

* [Windows MetaFile - Vikipediya](https://en.wikipedia.org/wiki/Windows_Metafile)


