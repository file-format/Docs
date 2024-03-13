{
  "date": "2021-08-31",
  "keywords": [
"xbe faylı",
"xbe fayl formatı",
"xbe faylı nədir",
"fayl",
"xbe misal",
"xbe fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "XBE faylları yarada və aça bilən XBE fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "XBE - iOS Tətbiq Paketi Faylı",
  "linktitle": "XBE",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-xb-aze"
}
},
  "lastmod": "2021-08-31"
}

## XBE faylı nədir?
.xbe uzantısına malik fayl Xbox video oyun diskindən icra edilə bilən proqramdır. XBE faylları Xbox Sistemində icra edilən əsas fayllardır və adətən kompüterdə açılması nəzərdə tutulmur, lakin onlar Xbox emulyasiya proqramı ilə PC-də açıla bilər. Bu fayllar adətən oyun tərtibatçıları tərəfindən yaradılır və sonra Microsoft tərəfindən imzalanır. Fayl strukturu Windows PE fayllarına bənzəyir, lakin onu XBox-da işlək etmək üçün XBox parametrlərinə uyğun bəzi mühüm dəyişikliklər tətbiq edilir.

## XBE fayl formatı
XBE faylı şəkil başlığından, bölmə başlıqları toplusundan, sertifikatdan, mövzunun yerli yaddaş məlumatlarından, kitabxana versiyaları toplusundan, Microsoft bitmapından və kod və resursları ehtiva edən bölmələrdən ibarətdir.

### Şəkil Başlığı
Şəkil başlığı icra olunan faylın digər komponentlərinin fayl daxilində harada yerləşdiyini və işlədilən faylın necə işlənilməsi və yüklənməsini izah edən məlumatdan ibarətdir.

### TLS Cədvəli
TLS Cədvəli yerli yerli yaddaşı düzgün qurmaq üçün XBE tərəfindən lazım olan bütün məlumatlardan ibarətdir. O, əsasən PE32 fayllarında olan TLS Directory üçün unikaldır və birbaşa oradan kopyalana bilər. XBE faylı heç bir yerli iplik yaddaşından istifadə etmirsə və şəkil başlığında müvafiq sahə sıfıra təyin olunarsa, bu cədvəl buraxıla bilər.

| Ofset | Ölçü | Adı | Təsvir |
--------|--------|--------|------------|
| 0x0000 | 0x0004 | Raw Data Start | Proqram təsvirindəki TLS dəyişən məlumatının mütləq (yəni RVA deyil) başlanğıc ünvanı. |
| 0x0004 | 0x0004 | Raw Data End | Proqram təsvirindəki TLS dəyişən məlumatının sonunun mütləq (yəni RVA deyil) ünvanı. |
| 0x0008 | 0x0004 | İndeksin ünvanı | TLS İndeksi dəyişəninin mütləq (yəni RVA deyil) ünvanı. |
| 0x000C | 0x0004 | Geri Zənglərin Ünvanı | Sıfırla dayandırılmış TLS geri çağırış funksiyaları cədvəlinin mütləq (yəni RVA deyil) ünvanı. |
| 0x0010 | 0x0004 | Sıfır Doldurma Ölçüsü | Yaddaşda sıfıra təyin edilməli olan xam məlumatdan sonra gələn baytların sayı. |
| 0x0014 | 0x0004 | Xüsusiyyətlər | Uyğunlaşmanı təsvir edir. |

### Sertifikat

 A a certificate is mandatory for each Xbox executable that contains information about the titles:
 
- Sertifikatın yaradıldığı vaxt və tarix
- Başlıq ID
- Başlıq adı
- Alternativ başlıq identifikatorları
- İcra oluna bilən medianın icazə verilən növləri (HD, DVD, CD və s.)
- Oyun bölgəsi
- Oyun reytinqləri
- Disk nömrəsi
- Versiya
- System Link üçün istifadə edilən LAN açarı xam data
- İmza açarı xam data (saxlayan oyunlara imza atmaq üçün istifadə olunur)
- Alternativ imza açarları
- Sertifikatın orijinal ölçüsü
- Onlayn xidmət adı (erkən icra olunan proqramlarda yoxdur)
- İş vaxtı təhlükəsizlik bayraqları (erkən icra olunan proqramlarda yoxdur)
 
### İcazə verilən media növləri
İcra edilə bilən tərəfindən işə salınmağa icazə verilən media növləri. Aşağıdakı dəyərlər məlumdur:
| Media növü | Dəyər |
---------------------|------------|
| HARD_DISK | 0x00000001 |
| DVD_X2 | 0x00000002 |
| DVD_CD | 0x00000004 |
| CD | 0x00000008 |
| DVD_5_RO | 0x00000010 |
| DVD_9_RO | 0x00000020 |
| DVD_5_RW | 0x00000040 |
| DVD_9_RW | 0x00000080 |
| DONGLE | 0x00000100 |
| MEDİA_BOARD | 0x00000200 |
| NONSECURE_HARD_DISK | 0x40000000 |
| NONSECURE_MODE | 0x80000000 |
| MEDİA_MASK | 0x00FFFFFF |

### Bölmələr
Bölmələr bölmə başlıqları ilə ifadə edilir. Bölmə başlıqları sertifikatdan dərhal sonra başlayır və faylda faktiki bölmələrin olduğu məlumatları ehtiva edir. Ən azı iki bölmə həmişə Xbox icra olunan proqramında mövcuddur:
- .mətn
- .data


## İstinadlar 

* [Xbe - XBox Executable](https://xboxdevwiki.net/Xbe)



