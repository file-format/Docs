{
  "date": "2023-09-27",
  "keywords": [
"cfg",
"cfg faylı",
"cfg citrix server əlaqə faylı",
"cfg faylı nədir",
"cfg faylını necə açmaq olar",
"fayl",
"cfg fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "CFG Fayl Format - Citrix Server Əlaqə Faylı",
  "description": "CFG Citrix Server Bağlantı Fayl formatı və CFG faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "CFG Citrix",
  "menu": {
    "docs": {
      "identifier": "settings-cfg-citrix-az",
      "parent": "settings"
}
},
  "lastmod": "2023-09-27"
}

## CFG faylı nədir?

CFG faylı **Citrix Server Connection File** kimi də tanınır. Citrix serverinə qoşulma yaratmaq üçün istifadə olunan mühüm komponentdir. Bu fayl müştəri cihazı ilə Citrix serveri arasında uğurlu əlaqə üçün zəruri olan əsas məlumatları ehtiva edir. O, adətən serverin host adı və ya IP ünvanı, istifadə ediləcək xüsusi server portu və autentifikasiya üçün tələb olunan etimadnamələr kimi təfərrüatları ehtiva edir ki, bu da tez-tez istifadəçi adı və parolu əhatə edir.

Bu CFG faylları Citrix müştəri proqram təminatının konfiqurasiyasında mühüm rol oynayır və istifadəçilərə müxtəlif Citrix serverlərinə problemsiz qoşulmağa imkan verir. Onlar əsas parametrləri əvvəlcədən təyin etməklə əlaqə prosesini asanlaşdıran konfiqurasiya faylları kimi çıxış edir, istifadəçilərin Citrix serverinə hər dəfə daxil olmaq istədikləri zaman bu məlumatı əl ilə daxil etmə ehtiyacını azaldır.

## Citrix Server

Citrix XenApp və ya Citrix XenDesktop server kimi də tanınan Citrix serveri Citrix virtualizasiya həllərində istifadə olunan ixtisaslaşmış serverdir. Citrix uzaqdan giriş, proqramların virtuallaşdırılması və iş masasının virtuallaşdırılması texnologiyasını təmin edən şirkətdir. Citrix serverləri proqramların və iş masası mühitlərinin uzaq istifadəçilərə və ya müştəri cihazlarına çatdırılmasını asanlaşdırmaqla bu həllərdə mərkəzi rol oynayır.

Citrix serveri adətən necə işləyir:

1.  **Tətbiq və Masaüstü Çatdırılma**: Citrix serverləri proqramları və iş masası mühitlərini saxlayır. Proqramı birbaşa istifadəçinin cihazında işə salmaq əvəzinə, proqram və ya iş masası Citrix serverində işləyir və müştəri cihazına yalnız istifadəçi interfeysi ötürülür. Bu, istifadəçilərə PC, Mac, planşet və smartfonlar daxil olmaqla geniş çeşidli cihazlardan Windows proqramlarına və masaüstlərinə daxil olmaq imkanı verir.
    
2.  **Uzaqdan Erişim**: Citrix serverləri proqramlara və masaüstlərinə uzaqdan giriş imkanı verir və istifadəçilərə internet bağlantısı olan hər yerdən işləməyə imkan verir. Bu, ardıcıl və təhlükəsiz hesablama təcrübəsi təmin etdiyi üçün uzaq və paylanmış komandalar üçün xüsusilə dəyərlidir.
    
3.  **Yük Balansı**: Citrix serverləri daxil olan bağlantıların yükünü balanslaşdırmaq üçün çox vaxt qruplarda işləyir. Yük balansı istifadəçi sorğularının serverlər arasında bərabər paylanmasını təmin edərək, performansı və əlçatanlığı optimallaşdırır.

## Citrix Server Bağlantı Faylı

Citrix Server Bağlantı Faylı, tez-tez CFG faylı kimi istinad edilir, müştəri cihazları və Citrix serverləri arasında əlaqə yaratmaq üçün Citrix mühitlərində istifadə olunan konfiqurasiya faylıdır. Adətən Citrix Server Bağlantı Faylına daxil edilən əsas təfərrüatlar aşağıdakıları əhatə edə bilər:

1.  **Host adı və ya IP ünvanı**: Bu, müştəri cihazının qoşulmalı olduğu Citrix serverinin şəbəkə yerini müəyyənləşdirir. Citrix resurslarının harada yerləşdirildiyini müəyyənləşdirir.
    
2.  **Server Port**: Citrix serveri ilə əlaqə üçün istifadə edilən port nömrəsi. Bu, verilənlərin serverdə düzgün xidmətə ötürülməsini təmin edir.
    
3.  **İstifadəçi adı və Şifrə**: İstifadəçi adı və parol daxil olmaqla, istifadəçi etimadnamələri autentifikasiya məqsədləri üçün daxil edilə bilər. Bu etimadnamələr istifadəçilərə öz şəxsiyyətlərini sübut etməyə və Citrix resurslarına giriş əldə etməyə imkan verir.
    
4.  **Bağlantı Parametrləri**: CFG faylları şifrələmə parametrləri, seansın fasiləsi dəyərləri və ekran seçimləri kimi müxtəlif əlaqə parametrlərini ehtiva edə bilər. Bu parametrlər istifadəçi təcrübəsini və təhlükəsizlik parametrlərini konfiqurasiya etməyə kömək edir.
    
5.  **Resurs Konfiqurasiyası**: Konfiqurasiyadan asılı olaraq, CFG faylı əlaqə qurulduqda hansı Citrix resurslarının (tətbiqlər və ya masaüstləri) işə salınacağını təyin edə bilər.

## Citrix tərəfindən istifadə olunan fayl formatları

Citrix serverləri və əlaqəli Citrix texnologiyaları proqramların, masaüstlərinin və məzmunun uzaq istifadəçilərə çatdırılmasını təmin etmək üçün bir neçə fayl formatını dəstəkləyir. Citrix server yerləşdirmələri ilə əlaqəli bəzi ümumi fayl formatları bunlardır:

1.  **ICA (Müstəqil Hesablama Memarlığı)**:
    
- **.ica**: ICA faylı Citrix tətbiqinin və iş masası çatdırılmasının əsas komponentidir. O, server ünvanı, port, şifrələmə parametrləri və ekran seçimləri kimi Citrix serverinə qoşulma haqqında məlumatları ehtiva edir. İstifadəçi Citrix resursuna kliklədikdə, [.ica](/misc/ica/) faylı yaradılır və əlaqə yaratmaq üçün Citrix Receiver (və ya Citrix Workspace) müştərisi tərəfindən istifadə olunur.
2.  **Citrix Receiver (və ya Citrix Workspace) Paketləri**:
    
- **.exe**: Citrix Receiver və ya Citrix Workspace quraşdırma paketləri tez-tez müxtəlif əməliyyat sistemləri üçün icra edilə bilən formatda gəlir (məsələn, Windows üçün [.exe](/executable/exe/), macOS üçün [.dmg](/compression/dmg/)). Bu paketlər istifadəçilərə öz cihazlarında müştəri proqram təminatı quraşdırmaq imkanı verir.
3.  **Citrix Workspace App (əvvəllər Citrix Receiver)**:
    
- **.app**: macOS-da Citrix Workspace Tətbiqi macOS tətbiqi [.app](/executable/app/) faylı kimi paketlənib.
4.  **Veb Brauzer Uyğunluğu**:
    
- Citrix həllərinə adətən veb-əsaslı giriş üçün HTML5 istifadə edərək veb brauzerlər vasitəsilə daxil olmaq olar. İstifadəçilər xüsusi fayl formatları tələb etmədən URL-lər vasitəsilə Citrix resurslarına qoşulurlar.
5.  **Virtual Masaüstü Disk Şəkilləri**:
    
- **.vhd, .vhdx**: Citrix XenDesktop və XenApp virtual sabit disk [VHD](/disc-and-media/vhd/) və ya [VHDX](/disc-and-media/vhdx/) fayllarından istifadə edərək virtual masaüstləri və proqramları çatdıra bilər.
6.  **Resurs Nəşriyyatı Metaməlumatları**:
    
- **.xml**: Citrix administratorları proqram xassələri, giriş siyasətləri və istifadəçi təyinatları daxil olmaqla resurs dərci parametrlərini müəyyən etmək üçün tez-tez [XML](/web/xml/) fayllarından istifadə edirlər.
7.  **Printer Sürücü Faylları**:
    
- Citrix mühitləri uzaq proqramlardan istifadə edərkən düzgün çap funksiyasını təmin etmək üçün xüsusi printer driver faylları (məsələn, .inf) tələb edə bilər.
8.  **İstifadəçi Profili Məlumatı**:
    
- **.upm**: Citrix Profile Management sessiyalar və cihazlar arasında ardıcıl istifadəçi təcrübəsini təmin etmək üçün istifadəçi profili məlumatlarını .upm fayllarında saxlaya bilər.
9.  **Konfiqurasiya Faylları**:
    
- **.conf**: Müxtəlif konfiqurasiya faylları, yəni Citrix Lisenziya Serveri üçün konfiqurasiya faylları kimi Citrix komponentləri üçün parametrləri müəyyən etmək üçün istifadə edilə bilər (məsələn, CtxLicChk.conf).
10.  **Citrix ADC (NetScaler) Konfiqurasiyası**:

- **.nsconfig:** Əvvəllər NetScaler kimi tanınan Citrix Tətbiq Çatdırılma Nəzarətçiləri (ADC) üçün konfiqurasiya faylları yük balansı, təhlükəsizlik və trafikin idarə edilməsi ilə bağlı parametrləri saxlayır.

## CFG faylını necə açmaq olar?

CFG fayllarını açan və ya onlara istinad edən proqramlar

- Citrix Access Client (Windows, MAC, Linux)

## Digər CFG faylları

**.cfg** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Parametrlər**
- [CFG - Celestia Configuration File](/settings/cfg-celestia/)
- [CFG - Citrix Server Connection File](/settings/cfg-citrix/)
- [CFG - MAME Configuration File](/settings/cfg-mame/)
- [CFG - LightWave Configuration File](/settings/cfg-lightwave/)

**Oyun**
- [CFG - Wesnoth Markup Language File](/game/cfg-wesnoth/)
- [CFG - M.U.G.E.N Configuration File](/game/cfg-mugen/)
- [CFG - Source Engine Configuration File](/game/cfg-sourceengine/)

**Sistem və Müxtəlif**
- [CFG - CFG File](/system/cfg/)
- [CFG - Cal3D Model Configuration File](/misc/cfg-cal3d/)

## İstinadlar
* [Citrix Virtual Proqramları](https://en.wikipedia.org/wiki/Citrix_Virtual_Apps)


