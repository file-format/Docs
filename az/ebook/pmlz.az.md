{
  "date": "2021-03-30",
  "keywords": [
"PMLZ",
"Sıxılmış Palm İşarələmə Dil Faylı",
"uzadılması",
"Fayl",
"format",
"elektron kitab",
"Palm İşarələmə Dili"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "PMLZ fayl formatı, Palm Markup Language və PMLZ faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "PMLZ - Zipped Palm Markup Language File",
  "linktitle": "PMLZ",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-pml-azz"
}
},
  "lastmod": "2021-03-30"
}

## PMLZ faylı nədir?

Palm Inc elektron kitab fayl növünü təqdim etdi; [PML](/ebook/pml/) fayl formatının sıxılmış versiyası olan PMLZ fayl formatı kimi tanınır, buna görə də .pmlz uzantıları olan fayllar **Zipped Palm Markup Language File** kimi tanınır. PMLZ faylı **eReader** (planşet kompüter kimi elektron kitab oxuma cihazı kimi tanınır) üçün sənədlər yaratmaq üçün [PDB](/programming/pdb/) faylları tərtib edən faylın sadəcə zip konteyneridir. PML faylı Palm Cihazında göstərmək üçün PDB faylına (müxtəlif məlumat faylları olan) tərtibatı verir. Halbuki, PDB faylı Quicken, Pegasus, Microsoft Visual Studio və Palm Pilot daxil olmaqla müxtəlif proqramlar tərəfindən istifadə olunan verilənlər bazası faylıdır. Bir sözlə, PMLZ PML və PDB fayllarının sıxılmış konteyneridir.


## Palm Markup Language haqqında bilik
Aşağıdakı cədvəl PML əmrlərini təyin edir:

|Əmr|Təsvir|
---|---|
| \p | Yeni səhifə |
| \x | Yeni fəsil; həm də yeni səhifə qırılmasına səbəb olur. Fəsil başlığını (və istənilən üslub kodlarını) \x və \x | ilə əlavə edin
| \Xn | Fəsil dialoqunda yeni fəsil, girintili n səviyyə (0 və 4 daxil olmaqla n arasında); səhifə qırılmasına səbəb olmur. Fəsil başlığını (və istənilən üslub kodlarını) \Xn və \Xn | ilə əlavə edin
| \Cn=Fəsil başlığı | Səviyyə n (məsələn, \Xn) ilə fəsil siyahısına Fəsil başlığı daxil edin. Mətn səhifədə göstərilmir və səhifəni kəsməyə məcbur etmir. Bu, məsələn, fəslin girişinin əvvəlinə fəsil işarəsi qoymaq üçün bəzən faydalı ola bilər. |
| \c | Bu mətn blokunu mərkəzləşdirin; sətrin əvvəlində \c ilə bağlayın |
| \r | Sağ əsaslandırma mətn bloku; sətrin əvvəlində \r ilə bağlayın |
| \i | Blok kursiv; \i | ilə bağlayın
| \u | Alt xətt bloku; \u | ilə bağlayın
| \o | Overstrike bloku; \o | ilə bağlayın
| \v | Görünməz mətn; \v ilə bağlayın (şərhlər üçün istifadə edilə bilər) |
| \t | Giriş bloku. Xəttin əvvəlindən başlayın, sətrin sonunda \t ilə bağlayın |
| \T=50% | Ekran eninin müəyyən edilmiş faizini, bu halda 50%-ni daxil edir. Cari çertyoj mövqeyi artıq göstərilən ekran yerini keçibsə, bu teq nəzərə alınmır. |
| \w=50% | Ekranın verilmiş faiz eninin üfüqi qaydasını yerləşdirin, bu halda 50%. Bu teq ondan əvvəl və sonra sətir kəsilməsinə səbəb olur. Qayda mərkəzləşdirilmişdir. Faiz işarəsi məcburidir. |
| \n | İstifadəçi tərəfindən müəyyən edilən normal şriftə keçin |
| \s | stdFont-a keçin; normal şriftə qayıtmaq üçün \s ilə bağlayın |
| \b | BoldFont-a keçin; Normal şriftə qayıtmaq üçün \b ilə bağlayın (köhnəlmişdir; əvəzinə \B istifadə edin) |
| \l | bigFont-a keçid; Normal şriftə qayıtmaq üçün \l ilə bağlayın |
| \B | Mətni qalın olaraq qeyd edin. \b teqindən fərqli olaraq, \B şrifti dəyişmir, ona görə də böyük qalın mətnə sahib ola bilərsiniz. Siz eyni PML faylında \b və \B-ni qarışdıra bilməzsiniz. |
| \Sp | Mətni yuxarı işarə kimi qeyd edin. Qalın, kursiv və s. kimi digər üslublarla qarışdırılmamalıdır. Üstündəki mətni \Sp ilə əlavə edin. |
| \Sb | Mətni alt işarə kimi qeyd edin. Qalın, kursiv və s. kimi digər üslublarla qarışdırılmamalıdır. Yazılı mətni \Sb ilə əlavə edin. |
| \k | Qapalı mətni kiçik hərflərlə yazın; \k ilə bağlayın. \k teqlərinə daxil edilmiş hər hansı simvol (vurğu olanlar da daxil olmaqla) böyük hərflə hazırlanır və adi böyük hərfdən daha kiçik nöqtə ölçüsündə göstərilir. |
| \\ | Tək tərs kəsişməni təmsil edir |
| \aXXX | Windows-1252 kodu onluq XXX olan ASCII olmayan simvol daxil edin. Ətraflı məlumat üçün PML xarakter cədvəlinə baxın. |
| \UXXXX | Unicode kodu onaltılıq XXXX olan qeyri-ASCII simvol daxil edin. Ətraflı məlumat üçün Genişləndirilmiş PML simvol cədvəlinə baxın. |
| \m=imagename.png | Adlandırılmış şəkli daxil edin. Aşağıdakı Şəkillər bölməsinə baxın. |
| \q=#linkanchorBəzi mətn\q | Sənədin başqa yerində olan keçid ankerinə istinad edin. Lövbər spesifikasiyasından sonra və arxadan \q-dan əvvəl olan sətir sənədə baxarkən keçid kimi göstərilir və ya başqa şəkildə göstərilir. |
| \Q=linkanchor | Sənəddə keçid ankerini göstərin. |
| \- | Yumşaq defis daxil edin. Yumşaq tire yalnız bir sətir boyunca sözü kəsmək lazım olduqda görünür. |
| \Fn=footnote11\Fn | 1-i PML sənədinin sonunda işarələnmiş, adı alt qeyd1 olan haşiyə ilə əlaqələndirin. Aşağıdakı Haşiyələr və Yan panellər bölməsinə baxın. |
| \Sd=sidebar1Yan çubuğu\Sd | Kənar panel mətnini PML sənədinin sonunda işarələnmiş, adı yan panel1 olan yan panellə əlaqələndirin. Aşağıdakı Haşiyələr və Yan panellər bölməsinə baxın. |
| \I | İstinad indeks elementi kimi qeyd edin. İndeks elementini (və istənilən üslub kodlarını) \I və \I.| ilə əlavə edin


## İstinadlar

* [Palma İşarələmə Dili - MobileRead tərəfindən](https://wiki.mobileread.com/wiki/EReader)

* [E-Reader - MobileRead tərəfindən](https://en.wikipedia.org/wiki/E-reader)


