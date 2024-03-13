{
  "date": "2022-03-01",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "VPK Faylı - PlayStation Vita Tətbiq Paketi Fayl Formatı",
  "description": "VPK faylları yarada və aça bilən VPK fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "VPK",
  "menu": {
    "docs": {
      "parent": "compression",
      "identifier": "compression-vp-azk"
}
},
  "lastmod": "2022-03-01"
}

## VPK faylı nədir?

.vpk uzantılı fayl Sony PlayStation Vita oyun konsolunda üçüncü tərəf proqramlarını quraşdırmaq üçün istifadə edilən sıxılmış arxiv paketi faylıdır. Bu fayllar yalnız HENkaku tərəfindən jailbreak Vita PlayStation-da quraşdırıla bilər ki, bu da PS Vita və PSTV-yə istifadəçi tərəfindən yaradılmış məzmundan istifadə etməyə imkan verdi. VPK arxiv faylı [PNG](/image/png/) faylları kimi şəkillər, [.bin](/disc-and-media/bin/) kimi parametrlər faylları və [XML](/web/xml/) fayl formatında istənilən konfiqurasiyalar daxil olmaqla, oyunu təşkil edən bütün məzmunları ehtiva edir.

## VPK fayl formatı

VPK faylları standart sıxılmış [ZIP](/compression/zip/) arxiv kimi diskdə saxlanılır. Bunlar Vita Gaming Console-da quraşdırılacaq üçüncü tərəf proqramları üçün çoxlu qovluq və digər əlaqəli faylları ehtiva edə bilər. VPK paket faylının məzmununa baxmaq üçün onun uzantısının adını .vpu-dan .zip-ə dəyişdirin və WinZip və ya WinRAR kimi standart dekompressiya yardım proqramlarından istifadə edərək məzmunu çıxarın.

Valvessoftware [VPK file format](https://developer.valvesoftware.com/wiki/VPK_File_Format) haqqında tərtibatçının nöqteyi-nəzərindən istinad edilə bilən ətraflı məlumata malikdir.

## VPK fayllarını necə quraşdırmaq olar?

VPK faylları VPK.exe komanda xətti yardım proqramından quraşdırıla bilər. Windows OS-də faylları bütün paketlənmiş faylları ehtiva edən \*.vpk qaytaran vpk.exe faylına atmaq olar. Alternativ olaraq, komanda xətti aləti aşağıdakı kimi istifadə edilə bilər.

### VPK yaradın və Fayllar əlavə edin

```
vpk <dirname>
```

### VPK fayllarını çıxarın

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## VPK Viewer

 * [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## İstinadlar

* [VPK Fayl Formatı](https://developer.valvesoftware.com/wiki/VPK_File_Format)

* [VPK Faylları](https://developer.valvesoftware.com/wiki/VPK)


