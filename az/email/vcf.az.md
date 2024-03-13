{
  "date": "2019-10-11",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VCF - Virtual Əlaqə Faylı",
  "description": "VCF fayl formatı və VCF faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "VCF",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-vc-azf"
}
},
  "lastmod": "2019-09-10"
}

## VCF faylı nədir?

VCF (Virtual Kart Format) və ya vCard əlaqə məlumatlarını saxlamaq üçün rəqəmsal fayl formatıdır. Bu format məşhur məlumat mübadiləsi proqramları arasında məlumat mübadiləsi üçün geniş istifadə olunur. Windows və MacOS kimi əksər əməliyyat sistemləri bu faylları yaratmaq və açmaq üçün standart proqramlarla gəlir. Tək VCF faylında bir və ya bir neçə kontakt üçün əlaqə məlumatı ola bilər. VCF faylı adətən bir sıra digər sahələrə əlavə olaraq əlaqənin adı, ünvanı, telefon nömrəsi, e-poçtu, doğum günü, fotoşəkillər və audio kimi məlumatları ehtiva edir. E-poçt müştəriləri və xidmətləri tərəfindən dəstəklənən vCard formatından istifadə etməklə kontaktların ötürülməsi zamanı məlumat itkisi yoxdur. VCF fayl formatı üçün media növü mətn/vcard-dır.

## VCF fayl formatı

VCF faylları təbiətcə mətnlidir və insanlar tərəfindən oxuna bilər. Bunlar Microsoft Windows-da Notepad və MacOS-da TextEdit kimi mətn redaktorlarında aça bilər. Faylda şəkil varsa, o, mətn redaktorunda göstərilməyəcək.

[Microsoft Outlook](https://support.office.com/en-us/article/send-and-save-contacts-as-vcards-vcf-files-94a17a6f-105f-46c7-9308-33658c1c2690) VCF fayllarının açılması, eləcə də məşhur [MSG](/email/msg/) formatı kimi bir sıra digər formatlara çevrilməsi üçün dəstək təqdim edir. VCF fayl formatı zaman keçdikcə fayl formatına ətraflı məlumat əlavə etməklə 2.1-dən 4.0-a qədər təkmilləşdirilmişdir. Format həmçinin telefon kontaktlarını ixrac etmək və daha sonra başqa cihaza idxal etmək üçün istifadə olunur.

!["VCF File Format"](../email/VCF.png "VCF File Format")

### VCF 2.1 Nümunə

Aşağıda 2.1 versiyasının nümunəsi verilmişdir.

```
BEGIN:VCARD
VERSION:2.1
N:Gump;Forrest;;Mr.
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;WORK;VOICE:(111) 555-1212
TEL;HOME;VOICE:(404) 555-1212
ADR;WORK;PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;WORK;PREF;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:100 Waters Edge#0D#
 #0ABaytown\, LA 30314#0D#0AUnited States of America
ADR;HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;HOME;ENCODING#QUOTED-PRINTABLE;CHARSET#UTF-8:42 Plantation St.#0D#0A#
 Baytown, LA 30314#0D#0AUnited States of America
EMAIL:forrestgump@example.com
REV:20080424T195243Z
END:VCARD
```

### VCF 3.0 Nümunəsi

Aşağıda 3.0 versiyasının nümunəsi verilmişdir.

```
BEGIN:VCARD
VERSION:3.0
N:Gump;Forrest;;Mr.;
FN:Forrest Gump
ORG:Bubba Gump Shrimp Co.
TITLE:Shrimp Man
PHOTO;VALUE#URI;TYPE#GIF:http://www.example.com/dir_photos/my_photo.gif
TEL;TYPE#WORK,VOICE:(111) 555-1212
TEL;TYPE#HOME,VOICE:(404) 555-1212
ADR;TYPE#WORK,PREF:;;100 Waters Edge;Baytown;LA;30314;United States of America
LABEL;TYPE#WORK,PREF:100 Waters Edge\nBaytown\, LA 30314\nUnited States of America
ADR;TYPE#HOME:;;42 Plantation St.;Baytown;LA;30314;United States of America
LABEL;TYPE#HOME:42 Plantation St.\nBaytown\, LA 30314\nUnited States of America
EMAIL:forrestgump@example.com
REV:2008-04-24T19:52:43Z
END:VCARD
```

### VCF 4.0 Nümunəsi

Aşağıda 4.0 versiyasının nümunəsi verilmişdir.

```
BEGIN:VCARD
VERSION:4.0
N:Gump;Forrest;;Mr.;
FN:Sheri Nom
ORG:Sheri Nom Co.
TITLE:Ultimate Warrior
PHOTO;MEDIATYPE#image/gif:http://www.sherinnom.com/dir_photos/my_photo.gif
TEL;TYPE#work,voice;VALUE#uri:tel:+1-111-555-1212
TEL;TYPE#home,voice;VALUE#uri:tel:+1-404-555-1212
ADR;TYPE#WORK;PREF#1;LABEL#"Normality\nBaytown\, LA 50514\nUnited States of America":;;100 Waters Edge;Baytown;LA;50514;United States of America
ADR;TYPE#HOME;LABEL#"42 Plantation St.\nBaytown\, LA 30314\nUnited States of America":;;42 Plantation St.;Baytown;LA;30314;United States of America
EMAIL:sherinnom@example.com
REV:20080424T195243Z
x-qq:21588891
END:VCARD
```

## İstinadlar

* [VCF - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/VCard)


