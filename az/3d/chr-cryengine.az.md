{
   "date":"2023-10-11",
   "keywords":[
"chr",
"chr faylı",
"chr cryengine simvol faylı",
"chr faylı necə açmaq olar",
"fayl",
"chr fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CHR fayl formatı - CryENGINE xarakter faylı",
   "description":"CHR faylları yarada və aça bilən CHR CryENGINE Character fayl formatı və API-lər haqqında məlumat əldə edin.",
   "linktitle":"CHR CryENGINE",
   "menu":{
      "docs":{
         "identifier":"3d-chr-cryengine-az",
         "parent":"3d"
}
},
   "lastmod":"2023-10-11"
}

## CHR faylı nədir?

CryENGINE kontekstindəki CHR faylı **CryENGINE xarakter faylına** istinad edir. CryENGINE, Crytek tərəfindən hazırlanmış oyun mühərrikidir və bu fayllar video oyunlarda və digər real vaxt proqramlarında istifadə üçün xarakter modellərini və əlaqəli məlumatları saxlamaq üçün istifadə olunur.

## CryENGINE xarakter faylı

CryENGINE xarakter faylı adətən aşağıdakı komponentləri ehtiva edir:

1.  **Xarakter Modeli**: Bu, həndəsə, faktura və animasiyalar daxil olmaqla xarakterin 3D modelidir. Bu modellər tez-tez Autodesk Maya və ya Blender kimi proqram təminatı ilə yaradılır və sonra CryENGINE-ə idxal olunur.
    
2.  **Animasiya Məlumatı**: CryENGINE personajlar üçün mürəkkəb animasiyaları dəstəkləyir, ona görə də .chr faylına gəzinti, qaçış, tullanma və sair kimi müxtəlif animasiyalar daxil ola bilər. Bu animasiyalar adətən əsas kadr məlumatları kimi saxlanılır.
    
3.  **Rigging Information**: Rigging, modelə animasiyalar tətbiq etməyə imkan verən xarakter modeli üçün skelet strukturunun yaradılması prosesinə aiddir. .chr faylında sümük iyerarxiyası və personajın torunun bu skeletə necə qoşulması haqqında məlumat ola bilər.
    
4.  **Material və Tekstura Məlumatı**: Xarakter modelində istifadə olunan materiallar və əlaqəli faktura xəritələri haqqında məlumat .chr faylına daxil edilə bilər. CryENGINE fiziki əsaslı göstərməyi dəstəkləyir, ona görə də bu materiallar kifayət qədər təfərrüatlı ola bilər.
    
5.  **Fizika Datası**: Əgər xarakter oyun dünyası ilə qarşılıqlı əlaqə yaratmaq üçün nəzərdə tutulubsa, .chr faylına toqquşma formaları və ya ragdoll fizikası üçün məhdudiyyətlər kimi fizika məlumatları daxil ola bilər.
    
6.  **Konfiqurasiya Parametrləri**: Süni intellekt davranışı və ya skript hadisələri kimi oyun dünyasında personajın davranışı ilə bağlı müxtəlif konfiqurasiya parametrləri də .chr faylının bir hissəsi ola bilər.

## CryENGINE

CryENGINE, Alman video oyun şirkəti Crytek tərəfindən hazırlanmış güclü oyun mühərrikidir. Ən qabaqcıl qrafika imkanları ilə tanınır və vizual olaraq heyrətamiz və texnoloji cəhətdən inkişaf etmiş video oyunları yaratmaq üçün istifadə edilmişdir. CryENGINE haqqında bəzi əsas xüsusiyyətlər və məlumatlar bunlardır:

1.  **Qrafika və göstərmə**: CryENGINE inkişaf etmiş qrafik imkanları ilə tanınır. O, real vaxt rejimində qlobal işıqlandırma, yüksək keyfiyyətli dinamik işıqlandırma və kölgələr, fiziki əsaslı göstərmə (PBR) və yüksək keyfiyyətli tekstura kimi xüsusiyyətləri dəstəkləyir. Bu xüsusiyyətlər vizual olaraq heyrətamiz və real oyun dünyaları yaratmağa kömək edir.
    
2.  **Fizika Mühərriki**: CryENGINE oyun dünyasında obyektlər arasında real qarşılıqlı əlaqə yaratmağa imkan verən daxili fizika mühərrikini ehtiva edir. O, sərt bədən fizikası, yumşaq bədən fizikası və ragdoll fizikası kimi xüsusiyyətləri dəstəkləyir və onu dinamik və immersiv mühitlər yaratmaq üçün uyğun edir.
    
3.  **Ərazi və Bitki örtüyü**: CryENGINE geniş və ətraflı açıq mühit yaratmaq üçün alətlər təqdim edir. O, relyefin redaktəsini, bitki örtüyünün yerləşdirilməsini və dinamik hava sistemlərini dəstəkləyir, tərtibatçılara geniş və real açıq hava şəraiti yaratmağa imkan verir.
    
4.  **Xarakter Animasiyası**: CryENGINE xarakter animasiyası üçün güclü alətləri ehtiva edir. O, tərtibatçılara canlı xarakter hərəkətləri və animasiyalar yaratmağa imkan verən mürəkkəb xarakter qurğularını, üz animasiyasını və qarışıq ağac sistemini dəstəkləyir.
    
5.  **AI Sistemi**: Mühərrikdə ağıllı NPC (oyunçu olmayan personajlar) və düşmən süni intellekt yaratmağa imkan verən AI sisteminə malikdir. Tərtibatçılar çətin və immersiv oyun təcrübəsi yaratmaq üçün süni intellekt davranışını və qarşılıqlı əlaqəni yaza bilərlər.
       
6.  **Scripting**: CryENGINE tərtibatçılara oyun məntiqi və qarşılıqlı əlaqə yaratmağa imkan verən Schematyc adlı skript dilindən istifadə edir. Bundan əlavə, daha təkmil proqramlaşdırma ehtiyacları üçün C++ dilini dəstəkləyir.

## CryENGINE tərəfindən istifadə olunan fayl formatları

CryENGINE ilə əlaqəli bəzi ümumi fayl növləri bunlardır:

1.  **cryproj**: CryENGINE layihə faylları. Bu fayllar xüsusi oyun layihəsi üçün layihəyə xas parametrləri və konfiqurasiyaları saxlayır.
    
2.  **.səviyyə**: Səviyyə faylları ərazi, obyektlər, işıqlandırma və digər səviyyəyə aid parametrlər daxil olmaqla 3D oyun dünyası məlumatlarını ehtiva edir. Səviyyələr CryENGINE-də oyun dizaynının əsas komponentidir.
    
3.  **.cgf**: Xarakter Həndəsə Formatı. Bu fayllar simvollar, obyektlər və digər oyun aktivləri üçün 3D model məlumatlarını ehtiva edir. CGF fayllarına həndəsə, tekstura və animasiya məlumatları daxil ola bilər.
    
4.  **.chrparams**: Simvol parametrləri faylları. Bu fayllar xarakter modelləri və onların animasiyaları üçün parametrləri və konfiqurasiyaları saxlayır.
    
5.  **.dds**: DirectX Tekstura Formatı. CryENGINE diffuz xəritələr, normal xəritələr və digər tekstura növləri də daxil olmaqla teksturaları saxlamaq üçün adətən DDS fayllarından istifadə edir.
    
6.  **.cryshader**: CryENGINE Shader faylları. Bu fayllar materialların və obyektlərin oyun dünyasında necə göstərildiyini, şaderləri, material xüsusiyyətlərini və daha çoxunu təyin edir.
    
7.  **.crytif**: Tekstura Məlumat Faylı. Bu fayllar sıxılma parametrləri, mipmaplar və digər faktura ilə bağlı detallar kimi fakturalar haqqında əlavə məlumatları saxlayır.
    
8.  **.cdf**: Xarakter Tərifi Faylı. CDF faylları simvol aktivlərini və onların xassələrini, o cümlədən qoşmaları, animasiya vəziyyətlərini və xarakterlə əlaqəli parametrləri müəyyən etmək üçün istifadə olunur.
    
9.  **.dds**: CryENGINE həmçinin normal xəritələr, spekulyar xəritələr və diffuz xəritələr kimi müxtəlif tekstura xəritələri üçün DDS (DirectDraw Səthi) fayllarından istifadə edir.
    
10.  **.anim**: Animasiya faylları. Bu fayllar əsas kadrlar, sümük mövqeləri və animasiya ardıcıllıqları daxil olmaqla, simvollar və obyektlər üçün animasiya məlumatlarını saxlayır.
    
11.  **.xml**: XML faylları CryENGINE daxilində müxtəlif konfiqurasiyalar və məlumat tərifləri üçün istifadə edilə bilər, məsələn, oyun məntiqi, AI davranışı və s.
    
12.  **.pak**: [PAK files](/game/pak/) oyun aktivləri və resurslarını paketləmək üçün istifadə edilən arxiv fayllarıdır və onu oyunun paylanması və yüklənməsi üçün daha səmərəli edir.

## CHR faylını necə açmaq olar?

CHR fayllarını açan proqramlara daxildir

- **Crytek CryENGINE SDK** (Pulsuz sınaq) Windows üçün

## Digər CHR faylları

**.chr** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**3D**
- [CHR - CryENGINE Character File](/3d/chr-cryengine/)
- [CHR - 3ds Max Characters File](/3d/chr-3ds/)

**Şrift və Oyun**
- [CHR - Borland Character Set](/font/chr/)
- [CHR - Doki Doki Literature Club! Character File](/game/chr-doki/)

## İstinadlar
- [CryEngine](https://en.wikipedia.org/wiki/CryEngine)

