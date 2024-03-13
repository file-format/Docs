{
  "date": "2022-07-22",
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "VHDX fayl formatı və VHDX faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "VHDX Fayl Format - VHDX faylı nədir?",
  "linktitle": "VHDX",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vhd-azx"
}
},
  "lastmod": "2022-07-22"
}

## VHDX faylı nədir?

VHDX faylı Virtual Hard Disk v2 fayl formatında disk təsvir faylıdır. Bu, müəyyən bir əməliyyat sistemi tələb edən proqram təminatının və ya işləyən proqram təminatının sınaqdan keçirilməsi üçün yüklənə və istənilən normal maşın kimi istifadə edilə bilən bütün əməliyyat sistemini ehtiva edir. VHDX, tam disk şəkli olmasına baxmayaraq, bir faylda saxlanılır. Parallels Desktop, Windows Virtual Machine və Virtual Box kimi virtual maşın proqramı disk şəklini yükləyə və aça bilər.

VHDX faylı Hyper-V Manager ilə [VHD](/disc-and-media/vhd/) və ya VirtualBox ilə [VDI](/disc-and-media/vdi/) formatına çevrilə bilər.

## VHDX Fayl Format - Ətraflı Məlumat

The VHDX file format details are completely documented and available online as [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477) on Microsoft Documentation. It is an extension to the VHD format and includes enhanced capabilities. VHDX file format provides additional features that are available at the virtual hard disk and virtual hard disk file layers. It is more optimized and gives better results for storage hardware configuration and capabilities. VHDX files can be opened

### VHDX-də Virtual Hard Disklərə dəstək

Üç növ virtual sabit diski dəstəkləyir.

 1. **Sabit Virtual Hard Disk** - Sabit məlumat ölçüsü ayrılmış virtual sabit disk. Virtual sabit diskin ölçüsü məlumatların əlavə edilməsi və ya çıxarılması ilə dəyişmir.

 1. **Dynamic Virtual Hard Disk** - Dinamik disk ölçüsü olan virtual sabit disk. Onun ölçüsü istənilən vaxt ona yazılmış faktiki məlumat və metadata qədər böyükdür. Məlumat əlavə olunduqca və ya ondan silindikcə onun fayl ölçüsü dinamik olaraq artır.

 1. **Fərqli Virtual Hard Disk** - Ana virtual sabit disk faylı ilə müqayisədə dəyişdirilmiş bloklar dəsti kimi virtual sabit diskin cərəyanını təmsil edir.

## İstinadlar

* [VHDX File Format Specifications](https://learn.microsoft.com/en-us/openspecs/windows_protocols/ms-vhdx/83e061f8-f6e2-4de1-91bd-5d518a43d477)
* [VHD - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/VHD_(file_format))


