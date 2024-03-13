{
  "date": "2022.01.31",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "P7S Faylı - Rəqəmsal İmzalı E-poçt Mesajı",
  "description": "P7S fayl formatı və P7S fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "P7S",
  "menu": {
    "docs": {
      "parent": "email",
      "identifier": "email-p7-azs"
}
},
  "lastmod": "2022.01.31"
}

## P7S faylı nədir?

P7S faylı rəqəmsal imzalanmış e-poçtla qəbul edilən rəqəmsal imzadır. Bu faylın e-poçta əlavə olaraq olması e-poçtun orijinal mənbədən göndərilməsini təsdiqləyir. Bu, göndərənin kompüterində quraşdırılmış E-poçt İmzalama sertifikatına malik olmasını təmin edir. Bu cür imzalanmış e-poçt istifadəçinin kompüterindən göndərildikdə, ona göndərənin adını ehtiva edən P7S faylı əlavə olunur. İmzalanmış e-poçtları dəstəkləyən e-poçt müştəriləri göndərənin məlumatlarını görə bilər.

## P7S Fayl Format - Ətraflı Məlumat

S/MIME (Təhlükəsiz/Çoxməqsədli İnternet Poçt Genişləndirmələri) P7S faylları insanların oxuna biləcəyi düz mətn formatında məlumatları ehtiva edir. Microsoft Outlook, Apple Mail və Mozilla Thunderbird kimi e-poçt müştəriləri S/MIME e-poçtundan rəqəmsal imzalanmış məlumatları oxumaq üçün dəstək verir. E-poçtun imzalanması göndərənin şəxsiyyətini təsdiq edir və alıcıya mesajın həqiqi olduğunu bildirir. E-poçtlar e-poçt müştərilərindən endirildikdə ([EML](/email/eml/) və ya [MSG](/email/msg/) kimi), bu P7S faylları bu e-poçtlara əlavə olunur.

P7S faylı aşağıdakı məlumatları ehtiva edir:

 * E-poçtun mənşəyi
 * Göndərilmə tarixi və vaxtı,
 * Onun ötürülmə zamanı dəyişdirilib-dəyişdirilməməsi

Bu məlumat şifrlənmiş imzaları e-poçta rəqəmsal şəkildə əlavə etmək üçün İctimai Açar Kriptoqrafiya Standartı №7 (PKCS7) texnologiyasından istifadə etməklə daxil edilmişdir.

## İstinadlar ##

* [Microsoft Sign Tool](https://learn.microsoft.com/en-us/windows-hardware/drivers/devtest/signtool)


