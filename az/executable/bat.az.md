{
  "date": "2021-06-24",
  "keywords": [
"bat faylı",
"yarasa faylı nədir",
"fayl",
"bat fayl nümunəsi",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "BAT faylları yarada və aça bilən BAT fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "BAT - Toplu fayl formatı",
  "linktitle": "BAT",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ba-azt"
}
},
  "lastmod": "2021-06-24"
}

## BAT faylı nədir?
BAT faylı DOS və cmd.exe altında Windows-un bütün versiyaları ilə işləyən toplu fayl kimi tanınır. O, Windows daxilində texniki xidmət proqramlarını işə salmaq və ya tipik proqramları işə salmaq kimi müxtəlif tapşırıqları yerinə yetirmək üçün əmr xətti tərcüməçisi tərəfindən yerinə yetiriləcək düz mətndə bir sıra sətir əmrlərindən ibarətdir. Toplu iş faylına tərcüməçi tərəfindən interaktiv şəkildə qəbul edilə bilən hər hansı əmr daxil ola bilər və toplu iş faylında yazıldığı kimi şərti budaqlanma və dövriyyəni təmin edən kod strukturundan istifadə edə bilər.
## BAT fayl formatı
BAT fayl formatı sadəcə olaraq təkrarlanan əmr ardıcıllığını avtomatlaşdırmaq üçün birləşdirilmiş skriptdir. Paket termini toplu emal üçün istifadə olunur, interaktiv olmayan icra kimi qəbul edilə bilər. Buna görə də toplu iş faylı birdən çox məlumat toplusunu emal etməyə bilər. Köhnə Disk Əməliyyat Sistemində (DOS) toplu fayl fayl adını və .bat uzantısını yazaraq komanda xətti interfeysi altında işlədilib. Microsoft Windows kimi əvvəlki Microsoft qrafik interfeysə əsaslanan əməliyyat sistemi DOS-dan asılı idi. İstifadəçilər Windows-u təmir etmək, optimallaşdırmaq və ya yenidən quraşdırmaq kimi tipik əməliyyatları yerinə yetirmək üçün DOS-dan istifadə etməli idilər. Daha sonra Microsoft DOS əməliyyat sistemindən asılı olmayan Windows NT-ni təqdim etdi. Buna görə də, toplu faylları müasir günlərdə Microsoft əməliyyat sistemlərində Command Prompt və ya **cmd.exe** istifadə edərək işlədilə bilər.
### Toplu fayl parametrləri
Komanda əmri toplu işin adına və yoluna və toplu iş daxilindəki doqquz çağırış parametrinə istinad etmək üçün **%0, %1 - %9** kimi bir sıra xüsusi dəyişənləri dəstəkləyir. Mövcud olmayan parametrlər sıfır uzunluğa malik sətirlə əvəz olunur. Baxmayaraq ki, onlar ətraf mühit dəyişənlərinə bənzər istifadə oluna bilər, lakin ətraf mühitdə saxlanmır. Microsoft və IBM bu dəyişənlərə əvəzedici parametrlər kimi istinad edir, Novell, Digital Research və Caldera isə onlar üçün əvəzedici dəyişənlər terminini təqdim etmişlər.

Budur bəzi faydalı Batch faylı əmrləri:
| Komanda | Təsvir |
------|------------|
| VER | Bu toplu əmr istifadə etdiyiniz MS-DOS versiyasını göstərir. |
|ADD| Bu, genişlənməni fayl növü (FTYPE) ilə əlaqələndirən, mövcud assosiasiyaları göstərən və ya assosiasiyanı silən toplu əmrdir. |
|CD| Bu toplu əmr başqa bir kataloqa dəyişikliklər etməyə kömək edir və ya cari kataloqu göstərir. |
|CLS| Bu toplu əmr ekranı təmizləyir. |
|KOPYALA| Bu toplu əmr faylları bir yerdən digərinə köçürmək üçün istifadə olunur. |
|DEL| Bu toplu əmr qovluqları deyil, faylları silir. |
|DIR| Bu toplu əmri kataloqun məzmununu sadalayır. |
|TARİX| Bu toplu əmr sistem tarixini tapmağa kömək edir. |
|EXO| Bu toplu əmr mesajları göstərir və ya əmr əks-sədasını yandırır və ya söndürür. |
|ÇIXIŞ| Bu toplu əmr DOS konsolundan çıxır. |
|MD| Bu toplu əmr cari yerdə yeni qovluq yaradır. |
|HƏRƏKƏT| Bu toplu əmr faylları və ya qovluqları qovluqlar arasında köçürür. |
|PATH| Bu toplu əmr yol dəyişənini göstərir və ya təyin edir. |
|PAUSE| Bu toplu əmr istifadəçiyə müraciət edir və giriş xəttinin daxil edilməsini gözləyir. |
|TESLİM| Bu toplu əmr cmd.exe sorğusunu dəyişdirmək və ya sıfırlamaq üçün istifadə edilə bilər. |
|RD| Bu toplu əmr qovluqları silir, lakin qovluqlar silinməzdən əvvəl boş olmalıdır. |
|REN| Faylların və qovluqların adlarını dəyişdirir |
|REM| Bu toplu əmr toplu fayllarında qeydlər üçün istifadə olunur, qeydin məzmununun icrasına mane olur. |
|START| Bu toplu əmr proqramı yeni pəncərədə işə salır və ya sənədi açır. |
|ZAMAN| Bu toplu əmr vaxtı təyin edir və ya göstərir. |
|TYPE| Bu toplu əmri çıxışa fayl və ya faylların məzmununu çap edir. |
|VOL| Bu toplu əmri həcm etiketlərini göstərir. |
|ATTRIB| Kurret kataloqunda faylların atributlarını göstərir və ya təyin edir |
|CHKDSK| Bu toplu əmr diski hər hansı problemə görə yoxlayır. |
|SEÇİM| Bu toplu əmr istifadəçiyə seçimlərin siyahısını təqdim edir. |
|CMD| Bu toplu əmr əmr sorğusunun başqa bir nümunəsini çağırır. |
|COMP| Bu toplu əmr fayl ölçüsünə əsasən 2 faylı müqayisə edir. |
|DÖNÜŞTÜRÜN| Bu toplu əmr həcmi FAT16 və ya FAT32 fayl sistemindən NTFS fayl sisteminə çevirir. |
|DRIVERQUERY| Bu toplu əmr bütün quraşdırılmış cihaz sürücülərini və onların xüsusiyyətlərini göstərir. |
|GENİŞLEDİR| Bu toplu əmr sıxılmış .cab kabinet fayllarından faylları çıxarır. |
|TAP | Bu toplu əmr uyğun sətirləri çıxararaq fayllarda və ya girişdə sətir axtarır. |
|FORMAT| Bu toplu əmr FAT, FAT32 və ya NTFS kimi Windows tərəfindən dəstəklənən fayl sistemindən istifadə etmək üçün diski formatlaşdırır və bununla da diskin əvvəlki məzmununun üzərinə yazır. |
|YARDIM| Bu toplu əmr Windows tərəfindən təmin edilən əmrlərin siyahısını göstərir. |
|IPCONFIG| Bu toplu əmr Windows IP Konfiqurasiyasını göstərir. Bağlantı və həmin əlaqənin adı ilə konfiqurasiyanı göstərir. |
|ETİKET| Bu toplu əmr disk etiketini əlavə edir, təyin edir və ya silir. |
|DAHA| Bu toplu əmr fayl və ya faylların məzmununu hər dəfə bir ekranda göstərir. |
|NET| İstifadə olunan əmrdən asılı olaraq müxtəlif şəbəkə xidmətləri təqdim edir. |
|PING| Bu toplu əmr ICMP/IP echo paketlərini şəbəkə üzərindən təyin olunmuş ünvana göndərir. |
|BAĞLAMA| Bu toplu əmr kompüteri bağlayır və ya cari istifadəçini sistemdən çıxarır. |
|SORT| Bu toplu əmri mənbə faylından daxiletməni götürür və onun məzmununu əlifba sırası ilə A-dan Z və ya Z-yə qədər çeşidləyir. O, çıxışı konsolda çap edir. |
|SUBST| Bu toplu əmr yerli qovluğa sürücü məktubu təyin edir, cari tapşırıqları göstərir və ya tapşırığı silir. |
|SİSTEMİNFO| Bu toplu əmr kompüterin və onun əməliyyat sisteminin konfiqurasiyasını göstərir. |
|TASKKILL| Bu toplu əmr bir və ya daha çox işi bitirir. |
|TASKLIST| Bu toplu əmr tapşırıq adı və proses id (PID) daxil olmaqla vəzifələri siyahıya alır. |
|XCOPY| Bu toplu əmr faylları və qovluqları daha təkmil şəkildə kopyalayır. |
|AĞAC| Bu toplu əmr cari kataloqun bütün alt kataloqlarının istənilən rekursiya və ya dərinlik səviyyəsinə qədər ağacını göstərir. |
|FC |Bu toplu əmr iki fayl arasındakı faktiki fərqləri sadalayır. |
|DISKPART |Bu toplu əmr disk bölmələrinin xassələrini göstərir və konfiqurasiya edir. |
|TITLE |Bu toplu əmr konsol pəncərəsində göstərilən başlığı təyin edir. |
|SET | Cari sistemdəki mühit dəyişənlərinin siyahısını göstərir. |

## BAT fayl nümunəsi
Toplu skriptlər adətən sadə mətn faylları kimi saxlanılır; ardıcıllıqla yerinə yetirilən əmrləri ehtiva edir. Bu fayllar .bat uzantısı ilə saxlanılır; **Command Interpreter** proqram təminatından istifadə etməklə tanınır və icra edilir. Bu proqram **cmd.exe** adı ilə Microsoft Windows-da mövcuddur.

Budur, cari qovluqdakı bütün faylları silən nümunə toplu skript:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## İstinadlar 

* [Batch Script - Tez Bələdçi](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)

* [Paket faylı - Wikipewdia tərəfindən](https://en.wikipedia.org/wiki/Batch_file)


