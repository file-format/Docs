{
   "date":"2023-01-04",
   "keywords":[
"cs",
"cs faylı",
"cs cleo xüsusi skript",
"cs faylını necə açmaq olar",
"fayl",
"cs fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"CS Fayl Format - CLEO Xüsusi Skript",
   "description":"CS CLEO Xüsusi Skript formatı və CS faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
   "linktitle":"CS CLEO",
   "menu":{
      "docs":{
         "identifier":"game-cs-cleo-az",
         "parent":"game"
}
},
   "lastmod":"2023-01-04"
}

## CS faylı nədir?

CLEO kontekstindəki .CS faylı (CLEO Library üçün qısa) adətən Grand Theft Auto (GTA) video oyunları seriyasında istifadə edilən fərdi skript faylına istinad edir. CLEO, oyunçulara GTA oyunlarına xüsusi skriptlər yaratmağa və əlavə etməyə imkan verən məşhur modding çərçivəsidir ki, bu da onlara oyunu dəyişdirmək, yeni funksiyalar əlavə etmək və ümumi oyun təcrübəsini artırmaq imkanı verir.

## CS faylına ümumi baxış

CLEO-da .cs faylının nələri ehtiva edə biləcəyinə dair əsas icmal budur:

1.  **Skript Kodu**: .cs faylı CLEO skript dilində yazılmış skript kodunu ehtiva edir. Bu skript dili CLEO-ya xasdır və oyun daxilində fərdi skriptlərin davranışını müəyyən etmək üçün istifadə olunur. Kod mətn redaktoru ilə yazıla bilər və adətən müəyyən bir sintaksisə əməl edir.
    
2.  **Modifications**: CLEO scripts can make various modifications to game such as changing behavior of in-game objects, creating custom missions, adding new vehicles, weapons and more. The possibilities are extensive and depend on creativity and programming skills of script author.
    
3.  **Tetiklər**: CLEO skriptlərinə tez-tez xüsusi skriptin nə vaxt və necə işləməsini müəyyən edən tetikleyiciler daxildir. Bu tətiklər oyundaxili hadisələrə, oyunçu hərəkətlərinə və ya xüsusi şərtlərə əsaslana bilər.
    
4.  **Dəyişənlər və funksiyalar**: CLEO skriptləri verilənləri saxlamaq və manipulyasiya etmək üçün dəyişənlərdən, həmçinin kodun inkapsulyasiyası və təkrar istifadəsi funksiyalarından istifadə edə bilər. Bu dəyişənlər və funksiyalar skriptin davranışını idarə etmək üçün istifadə olunur.

## CS faylı nümunəsi

Oyunda havanı dəyişən CLEO .cs skriptinin sadə nümunəsi:

```
{$CLEO .cs}

03A4: name_thread 'WEATHER'

:WEATHER_LOOP
    // Change the weather to sunny
    0085: 0@ = 11 // Weather ID for sunny weather
    00D8: mission_cleanup
    0051: return 0@ // Exit the script

// Add more code and conditions as needed
```

## CLEO Kitabxanası

Tez-tez sadəcə olaraq CLEO adlandırılan **CLEO Kitabxanası** Grand Theft Auto (GTA) video oyunları seriyası üçün məşhur və güclü modifikasiya çərçivəsidir. Bu, oyunçulara və moderatorlara GTA oyunlarına xüsusi skriptlər yaratmağa və əlavə etməyə imkan verir ki, bu da onlara oyunu dəyişdirmək, yeni funksiyalar əlavə etmək və ümumi oyun təcrübəsini artırmaq imkanı verir. CLEO xüsusilə GTA modding icmasında çevikliyi və istifadə rahatlığı ilə məşhurdur.

CLEO Kitabxanasının bəzi əsas xüsusiyyətləri və aspektləri bunlardır:

1.  **Skript Dili**: CLEO modifikasiya çərçivəsinə xas olan skript dilini təqdim edir. Skript dili anlamaq üçün nisbətən asan və işləmək üçün onu həm təcrübəsiz, həm də təcrübəli modderlər üçün əlçatan etmək üçün hazırlanmışdır.
    
2.  **Xüsusi Skriptlər**: CLEO ilə siz oyun dünyasında geniş funksiyaları yerinə yetirə bilən fərdi skriptlər yarada bilərsiniz. Bu skriptlər oyundaxili davranışı dəyişdirə, yeni missiyalar əlavə edə, yeni nəqliyyat vasitələri və ya silahlar təqdim edə, oyun fizikasını dəyişdirə və s.
    
3.  **Tetiklər və Hadisələr**: CLEO skriptləri müxtəlif oyundaxili hadisələr, oyunçu hərəkətləri və ya xüsusi şərtlərlə işə salına bilər. Bu, moderatorlara oyun daxilində dinamik və interaktiv məzmun yaratmağa imkan verir.
    
4.  **Support for Multiple GTA Versions**: CLEO has versions tailored to different GTA games, including GTA III, GTA Vice City, GTA San Andreas, GTA IV and others. This means that modders can create and share their custom scripts for different GTA titles.

## CLEO Kitabxanası tərəfindən istifadə olunan fayl formatları

Grand Theft Auto (GTA) oyunları üçün CLEO moddingində modlar yaratmaq və quraşdırmaq üçün adətən bir neçə fayl formatından istifadə edilir. Bu fayl formatları faktiki skriptlərdən tutmuş fakturalar, modellər və ya audio kimi əlavə resursların saxlanmasına qədər müxtəlif məqsədlərə xidmət edir. CLEO modifikasiyasında istifadə olunan bəzi əsas fayl formatları bunlardır:

1.  **.cs (Fərdi skript)**: CLEO .cs faylları CLEO skript dilində yazılmış fərdi skript fayllarıdır. Bu fayllar modun davranışını və funksionallığını müəyyən edən kodu ehtiva edir. .cs faylları CLEO modifikasiyasının əsasını təşkil edir və xüsusi funksiyaları həyata keçirmək üçün oyun tərəfindən icra edilir.
    
2.  **.csa (Fərdi Skript Arxivi)**: .csa faylları çoxsaylı .cs skript fayllarını saxlaya bilən arxivlərdir. Onlar tez-tez daha asan quraşdırma və idarəetmə üçün əlaqəli skriptləri paketləmək üçün istifadə olunur.
    
3.  **.fxt (Mətn Faylları)**: .fxt faylları CLEO modları üçün mətn tərcümələrini lokallaşdırmaq və ya təmin etmək üçün istifadə edilə bilən mətn fayllarıdır. Onların tərkibində oyunda göstərilə bilən mətn sətirləri var ki, bu da modları müxtəlif dillərdə oyunçular üçün əlçatan edir.
    
4.  **[.bmp](/image/bmp/), [.png](/image/png/), [.jpg](/image/jpeg/) (Şəkil Formatları)**: Bu şəkil formatları modlar üçün tekstura və şəkilləri saxlamaq üçün istifadə olunur. Onlar xüsusi dərilər, nəqliyyat vasitələrinin teksturaları, HUD elementləri və s. üçün istifadə edilə bilər. Oyundan asılı olaraq müxtəlif şəkil formatlarına üstünlük verilə bilər.

## CS faylını necə açmaq olar?

CLEO .cs (Fərdi skript) faylının məzmununu açmaq və onlara baxmaq üçün siz istədiyiniz mətn redaktoru və ya kod redaktorundan istifadə edə bilərsiniz. Ümumi seçimlərə aşağıdakılar daxildir:

- **Notepad**: Windows ilə əvvəlcədən quraşdırılmış sadə mətn redaktoru.
- **Notepad++**: Kodlaşdırma və skript üçün nəzərdə tutulmuş daha zəngin xüsusiyyətlərə malik mətn redaktoru.
- **Visual Studio Code**: Məşhur, pulsuz və yüksək dərəcədə genişləndirilə bilən kod redaktoru.
- **Sublime Text**: Sürəti və çox yönlü olması ilə tanınan başqa bir kod redaktoru.
- **Atom**: GitHub tərəfindən hazırlanmış açıq mənbəli kod redaktoru.

## Digər CS faylları

**.cs** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

**Məlumat Faylları və Oyun**
- [CS - ColorSchemer Studio Color Scheme](/data/cs-colorschemer/)
- [CS - CLEO Custom Script](/game/cs-cleo/)

**Proqramlaşdırma**
- [CS - CSharp Code File](/programming/cs/)

## İstinadlar
* [CLEO kitabxanası](https://cleo.li/)


