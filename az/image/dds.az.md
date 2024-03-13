{
  "date": "2022-04-02",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "DDS Fayl Format - DirectDraw Səthi Şəkil Faylı",
  "description": "DDS fayl formatı və DDS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "DDS",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-dd-azs"
}
},
  "lastmod": "2022-04-02"
}

## DDS faylı nədir?

DDS faylı DirectDraw Surface (DDS) konteyner formatından istifadə edən rastr təsvir faylıdır. O, sıxılmamış və sıxılmış (DXTn) dokuları saxlayır və müxtəlif növ məlumatların saxlanması üçün müxtəlif növləri həyata keçirir. O, həmçinin bir qatlı teksturalar, mipmaplı teksturalar, kub xəritələri, həcm xəritələri və faktura massivləri kimi bir neçə fərqli məlumat növünü dəstəkləyir. Bu, DDS fayllarına rəqəmsal fotoşəkillərə və Windows iş masası fonlarına əlavə olaraq video oyun tekstura vahidi modellərini saxlamağa imkan verir. DDS fayl formatı DirectX SDK ilə istifadə edilmək üçün Microsoft tərəfindən hazırlanmışdır.

## DDS fayl formatı

DDS faylları ikili fayllar kimi saxlanılır və DirectX SDK ilə istifadə edilə bilər. O, 3D oyunlar kimi real vaxt render proqramlarını inkişaf etdirmək üçün DirectX-in gücündən istifadə edir.

### DDS Fayl Düzeni

[DDS file layout](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide#dds-file-layout) Microsoft tərəfindən ətraflı şəkildə sənədləşdirilib. İkili DDS faylı aşağıdakı məlumatları ehtiva edir.

 * Dörd simvol kod dəyəri olan DDS (0x20534444) olan DWORD (sehrli nömrə).
 * A description of the data in the file.

DDS_HEADER verilənləri, DDS_PIXELFORMAT isə piksel formatını təsvir edir. Bunların hər ikisi köhnəlmiş DDSURFACEDESC2, DDSCAPS2 və DDPIXELFORMAT DirectDraw 7 strukturlarını əvəz edir.

```
DWORD               dwMagic;
DDS_HEADER          header;
```

[programming guide of DDS file format](https://learn.microsoft.com/en-us/windows/win32/direct3ddds/dx-graphics-dds-pguide) bu fayl formatının texniki detallarını əlavə edir.

## İstinadlar

* [DDS - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/DirectDraw_Surface)

* [ZSoft PCX Fayl Formatının Texniki Referans Təlimatı](http://qzx.com/pc-gpe/pcx.txt)


