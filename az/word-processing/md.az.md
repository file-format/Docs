{
  "date": "2019-10-11",
  "keywords": [
"md faylı",
"md fayl formatı",
"md faylı nədir",
"fayl",
"md nümunəsi",
"md fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "MD - MarkDown Dil Faylı",
  "description": "MD fayl formatı və MD faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "MD",
  "menu": {
    "docs": {
      "parent": "word-processing",
      "identifier": "word-processing-m-azd"
}
},
  "lastmod": "2019-09-10"
}

## MD faylı nədir?

Markdown dili dialektləri ilə yaradılmış mətn faylları **.md** və ya **.MARKDOWN** fayl uzantısı ilə saxlanılır. MD faylları mətnin girintilər, cədvəl formatı, şriftlər və başlıqlar kimi necə formatlaşdırıla biləcəyini müəyyən edən, həmçinin daxili mətn simvollarını ehtiva edən Markdown dilindən istifadə edən düz mətn formatında saxlanılır. MD faylları Markdown adlı proqramla HTML-yə çevrilə bilər. Markdown dili John Gruber tərəfindən buraxılmışdır.

MD faylları mətn fayllarını HTML versiyalarına çevirmək üçün əsasən Markdown tərəfindən istifadə olunan tərtibatçı faylları kimi təsnif edilə bilər ki, istifadəçilər oxumaq və yazmaq asan olan fayllar yarada bilsinlər. .md faylını aça bilən proqramlar aşağıdakılardır:

* Microsoft Notepad

* Notepad 2

* Apple TextEdit

* Microsoft WordPad


Ehtiyatlı olmaq üçün .md fayllarının genişlənməsinin adını dəyişməyin. Əgər belədirsə, bu, fayl növünü dəyişməyəcək, çünki faylı bir növdən digərinə dəyişdirmək üçün xüsusi çevirmə proqramları mövcuddur. Yuxarıda müzakirə edildiyi kimi .MD faylları Markdown dil proqramında yaradılmış faylların uzantılarıdır. **Markdown** bir məqsəd üçün nəzərdə tutulmuş [lightweight markup language](https://en.wikipedia.org/wiki/Lightweight_markup_language)-dir və internetdə mətni düz mətn formatlaşdırma sintaksisi ilə formatlaşdırmaq üçün istifadə olunur. Aydın olsun ki, Markdown HTML-i əvəz etmir, çünki onun sintaksisi çox kiçikdir və HTML teqlərinin çox kiçik bir hissəsini ehtiva edir. Markdown-un səbəbi nəsri oxumağı, yazmağı və redaktə etməyi asanlaşdırmaqdır. Başqa sözlə deyə bilərik ki, HTML nəşriyyat formatıdır, Markdown isə yazı formatıdır.

Markdown indi dünyanın ən məşhur işarələmə dillərindən biridir. Microsoft Word-dən istifadə edərkən sözlər və ifadələr düymələrə basmaqla formatlanır və dəyişikliklər dərhal görünür. Lakin Markdown belə deyil. Markdown formatlı fayl yaradıldıqda, hansı söz və ifadələrin fərqli görünə biləcəyini göstərmək üçün mətnə Markdown sintaksisi əlavə edilir. Məsələn, başlığı göstərmək üçün ondan əvvəl rəqəm işarəsi əlavə olunur (məsələn, # Başlıq Bir). Qalın cümlə qurmaq üçün ondan əvvəl və sonra iki ulduz işarəsi əlavə olunur (məsələn, **bu mətn qalındır**). Markdown sintaksisi mətndə olarkən görünə bilər.

## Qısa tarix

2004-cü ildə John Gruber və Aaron Swartz Markdown dilini insanlara oxumaq və yazmaq üçün asan mətn formatından istifadə edərək və onu XHTML və ya HTML-yə çevirmək seçimi ilə yazmağa imkan yaratmaq ideyası ilə yaratdılar. Dizaynının arxasında duran məqsəd oxunaqlılıqdır – dil, etiketlər və formatlaşdırma təlimatlarının aydın olduğu RTF və ya HTML kimi işarələmə dillərində olduğu kimi etiketlənməmiş və ya formatlaşdırma təlimatları ilə əlavə edilmiş kimi görünmədən olduğu kimi oxuna bilir. Əsas ilham e-poçtda düz mətni qeyd etmək üçün mövcud konvensiyalardan istifadə etməkdir.

O vaxtdan bəri Markdown başqaları tərəfindən, eləcə də [CPAN](https://en.wikipedia.org/wiki/CPAN) və müxtəlif digər proqramlaşdırma dillərində mövcud olan Perl [module](https://en.wikipedia.org/wiki/Modular_programming) dillərində yenidən tətbiq edilmişdir. O, [BSD-style license](https://en.wikipedia.org/wiki/BSD_license) altında paylanır və bir neçə [content-management systems](https://en.wikipedia.org/wiki/Content_management_system) ilə birlikdə və ya plagin kimi mövcuddur.

## MD fayllarının texniki xüsusiyyətləri

Markdown-da bir şey yazıldıqda, mətn əvvəlcə .md və ya .markdown uzantısı ilə açıq mətn faylında saxlanılır, sonra Dillinger kimi markdown proqramı Markdown faylının işlənməsi üçün Markdown formatlı mətni HTML-ə çevirmək üçün istifadə olunur, onu vebdə göstərmək üçün. brauzerlər. Markdown proqramları Markdown formatlı mətni götürmək və onu HTML formatına çıxarmaq üçün //Markdown prosessorundan// istifadə edir (həmçinin adətən analizator” və ya tətbiqetmə” kimi istinad edilir). Prosesin axın diaqramı aşağıdakı kimidir:

Qısacası, aşağıdakı kimi dörd addımlı bir prosesdir:

1. Birincisi, mətn redaktoru və ya .md və ya .markdown genişləndirilməsi ilə Markdown proqramı ilə Markdown fayllarının yaradılması.
1. Markdown faylı daha sonra Markdown proqramında açılır.
1. Markdown proqramı Markdown faylını HTML sənədinə çevirmək üçün istifadə olunur.
1. HTML faylı daha sonra veb brauzerdə baxılır və ya onu PDF kimi başqa fayl formatına çevirmək üçün Markdown proqramı istifadə olunur.

Markdown sürətli və asanlıqla qeydlər aparmaq, vebsayt üçün məzmun yazmaq, çapa hazır sənədlər hazırlamaq, kitablar nəşr etmək, təqdimatlar yaratmaq və sənədlər hazırlamaq üçün istifadə olunur.

Markdown-dakı bəzi versiyalar digər versiyalara o qədər əhəmiyyətli təsir göstərdi ki, tez-tez onların digər versiyaların bir hissəsi kimi sitat gətirildiyini görə bilərsiniz. Məsələn, kitabxanalar CommonMark (GFM) üçün dəstəyi qeyd edirlər. Gəlin bunlara qısaca nəzər salaq.

### GFM
Markdown tərtibatçılar arasında çox populyardır, çünki açıq mənbə paylaşma platforması Github dili çəpərlənmiş kod blokları, URL aultlinking, üstü xətt, cədvəllər və görüləcək işlər yaradan Github Flavored Markup (GFM) adlı versiya ilə qəbul edib və genişləndirib.

### Ümumi İşarə
Markdown tərtibatçıları bu yaxınlarda markdown-u standartlaşdırmağa çalışdılar, daha möhkəm və CommonMark adlanan dil üçün versiya, testlər və sənədlər yaratmaq üçün birləşdilər. Bu format bir qədər yenidir və bir çox funksiyaları dəstəkləmir, lakin tezliklə bir çox MultiMarkdown funksiyaları əlavə olunacaq.

### Çox İşarələmə
Multi-Markdown dilə digər versiyalar tərəfindən dəstəklənən müxtəlif funksiyalar əlavə etdi. Əvvəlcə Perl-də yazılmışdı, lakin sonradan C-yə köçürüldü. O, hasarlanmış kod bloklarını, sintaksisi vurğulamağı, cədvəlləri, metadataları, fraqmentlər/çarpaz istinadlar bağlantılarını, alt qeydləri, üstündən xətt çəkmək, tərif siyahıları, riyaziyyatı dəstəkləyir.

## Niyə MarkDown?

MD faylları aşağıdakı səbəblərdən istifadə üçün məşhur seçimdir.

1. **Sadə Sintaksis:** Markdown öyrənmək və yazmaq asan olan sadə və intuitiv sintaksisdən istifadə edir. Sintaksis düz mətn kimi oxunaqlı olmaq üçün nəzərdə tutulmuşdur ki, bu da onu HTML və ya digər mürəkkəb işarələmə dilləri ilə tanış olmayan istifadəçilər üçün əlçatan edir.

1. **Platformadan Müstəqil:** Markdown faylları Windows, Mac və Linux daxil olmaqla istənilən platformada yaradıla və redaktə edilə bilər, çünki onlar sadə mətn fayllarıdır. Bu, onları xüsusilə müxtəlif komanda üzvlərinin müxtəlif əməliyyat sistemlərindən istifadə edə biləcəyi paylanmış komandalarda əməkdaşlıq üçün məşhur seçim halına gətirir.

1. **Daşıma qabiliyyəti:** Markdown faylları portativdir, yəni HTML, PDF və Word kimi digər formatlara asanlıqla çevrilə bilər. Bu, onları müxtəlif formatlarda paylaşılması lazım olan sənədlər, blog yazıları və digər məzmun növləri yaratmaq üçün ideal format edir.

1. **Versiyaya Nəzarət:** Markdown faylları Git kimi versiyaya nəzarət sistemlərindən istifadə etməklə asanlıqla izlənilə və idarə oluna bilər. Bu, digər komanda üzvləri ilə sənədlər üzərində işləməyi, zamanla dəyişiklikləri izləməyi və lazım gələrsə, əvvəlki versiyalara qayıtmağı asanlaşdırır.

1. **Əlçatanlıq:** Markdown faylları əlilliyi olan istifadəçilər üçün əlçatandır, çünki onlar Brayl şrifti, audio və ekranda oxuna bilən mətn kimi digər formatlara asanlıqla çevrilə bilər.

## İstinadlar

 * [Mastering MarkDown](https://docs.github.com/en/get-started/writing-on-github/getting-started-with-writing-and-formatting-on-github/basic-writing-and-formatting-syntax)

