{
  "date": "2021-08-11",
  "keywords": [
"vdi faylı",
"vdi fayl formatı",
"vdi faylı nədir",
"fayl",
"vdi nümunəsi",
"vdi fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "VDI faylları yarada və aça bilən VDI fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "VDI - VirtualBox Virtual Disk Şəkil Faylı",
  "linktitle": "VDI",
  "menu": {
    "docs": {
      "parent": "disc-and-media",
      "identifier": "disc-and-media-vd-azi"
}
},
  "lastmod": "2021-08-11"
}

## VDI faylı nədir?
.vdi uzantılı fayl virtual disk şəklidir; Oracle-ın VirtualBox adlı açıq mənbəli masaüstü virtuallaşdırma proqramına xasdır. VDI faylları VirtualBox virtual maşınını işə salmaq üçün istifadə olunur. VM-lər istifadəçilərə əlavə əməliyyat sistemləri və ya proqramları tək bir kompüterdə işlətməyə imkan verir. Beləliklə, VDI fayllarının üstünlüyü ondan ibarətdir ki, istifadəçilər bu disk təsvir fayllarını öz sabit disklərində saxlaya bilərlər və ehtiyac duyduqları zaman emulyatorlardan istifadə edərək onları işlədə bilərlər.

## VDI fayl formatı
Virtual Disk Şəkili (VDI) müəssisə səviyyəli virtuallaşdırma məhsulu olan VirtualBox kimi tanınan, aktiv şəkildə işlənmiş, açıq mənbəli Oracle VM üçün əsas disk fayl formatıdır. VDI fayl formatı digər virtuallaşdırma proqramlarından istifadə etməklə asanlıqla işlədilə bilən portativ disk şəkli yaratmaq üçün nəzərdə tutulmuşdur. Həm dinamik olaraq ayrılmış, həm də sabit ölçülü yaddaşı dəstəkləyir. O, artıq verilənlərdən ibarət olsa belə, şəkil faylını yaradıldıqdan sonra genişləndirməyə imkan verir.

### Diskin virtuallaşdırılması
Sistem sabit diskləri VDI disk təsvir formatında emulyasiya edir. VirtualBox VM, Microsoft Virtual PC və ya VMware-də yaradılmış əvvəlki disklərdən, həmçinin öz doğma formatından istifadə edə bilər. VirtualBox həmçinin virtual sabit disklər kimi istifadə edərək, iSCSI hədəflərinə qoşulmaq və hostda xam bölmələr yaratmaq qabiliyyətinə malikdir. VirtualBox IDE (PIIX4 və ICH6 nəzarətçiləri), SATA (ICH8M nəzarətçi), sərt disklərin qoşula biləcəyi SAS nəzarətçiləri və SCSI-ni təqlid edir.

Dəstək VirtualBox-un 2.2.0 versiyasından bəri Open Virtualization Format (OVF) üçün mövcuddur. Həm hosta qoşulmuş fiziki qurğular, həm də ISO təsvirləri CD və ya DVD diskləri kimi quraşdırıla bilər.
Varsayılan olaraq VirtualBox VESA uyğun xüsusi virtual qrafik kartı vasitəsilə qrafikləri dəstəkləyir.

### Ethernet üçün virtuallaşdırma dəstəyi
VirtualBox Ethernet şəbəkə adapteri üçün aşağıdakı Şəbəkə İnterfeys Kartlarını virtuallaşdırır:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Intel Pro/1000 MT Masaüstü (82540EM)
- Intel Pro/1000 MT Server (82545EM)
- Intel Pro/1000 T Server (82543GC)
- Paravirtuallaşdırılmış şəbəkə adapteri (virtio-net)

Təqlid edilmiş şəbəkə kartları qonaq ƏS-lərinin şəbəkə aparatları üçün drayverləri axtarmağa və quraşdırmaya ehtiyac olmadan işləməyə imkan verir, çünki onlar qonaq ƏS-nin bir hissəsi kimi mövcuddur. Xüsusi paravirtuallaşdırılmış şəbəkə adapteri xüsusi bir aparat interfeysinə uyğunlaşma ehtiyacını azaltmaqla şəbəkə performansını yaxşılaşdırır. Buna görə qonaqda xüsusi sürücü dəstəyi tələb olunur.


## İstinadlar 

* [VirtualBox - Wikipedia tərəfindən](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)



