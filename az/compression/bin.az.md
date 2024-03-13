{
   "date":"2023-07-20",
   "keywords":[
"BIN",
"BIN faylı",
"fayl",
"BIN fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"BIN Fayl Format - MacBinary Kodlanmış Fayl",
   "description":"BIN faylları yarada və aça bilən BIN formatı və API-lər haqqında öyrənin.",
   "linktitle":"BIN",
   "menu":{
      "docs":{
         "identifier":"compression-bin-az",
         "parent":"compression"
}
},
   "lastmod":"2023-07-20"
}

## BIN faylı nədir?

Macintosh kompüterlərinin kontekstində BIN faylı MacBinary formatında saxlanılan fayla istinad edə bilər. MacBinary xüsusi olaraq Macintosh fayllarını internet, e-poçt, FTP və ya portativ media üzərindən ötürmək üçün nəzərdə tutulmuş fayl formatıdır. MacBinary-nin məqsədi Macintosh fayllarının tam fayl strukturunu və atributlarını, o cümlədən həm məlumat forkunu, həm də resurs çəngəlini bir fayl daxilində qorumaqdır.

MacBinary formatı buna Macintosh İerarxik Fayl Sistemi (HFS) resurs çəngəlini və məlumat çəngəlini sıxılmış fayla daxil etməklə nail olur. O, həmçinin fayl haqqında mühüm metaməlumatları ehtiva edən tapıcı başlığını ehtiva edir. Bütün bu komponentləri bir faylda birləşdirərək, MacBinary faylın bütövlüyünü qoruyub saxlamasını və müxtəlif platformalarda asanlıqla ötürülməsini və paylaşılmasını təmin edir.

Apple-ın fayl sistemlərində və fayl ötürmə protokollarında irəliləyişlərlə BIN fayllarının və MacBinary formatının istifadəsi daha az yayılmışdır. ZIP kimi fayl formatlarının tətbiqi və HFS+ və APFS kimi daha müasir fayl sistemlərinə keçid MacBinary ilə kodlanmış fayllara ehtiyacı azaldıb. Bu yeni fayl sistemləri fayl atributları, resurs çəngəlləri və məlumat çəngəlləri ilə işləmək üçün daha səmərəli üsullar təqdim edərək MacBinary formatını bugünkü hesablama mənzərəsində daha az zəruri edir.

## BIN Fayl Format - Ətraflı Məlumat 

Macintosh kompüterlərinin ilk dövrlərində verilənlərin məhdudlaşdırılması səbəbindən fayllar iki ayrı çəngəldə saxlanılırdı. Resurs fork strukturlaşdırılmış məlumatları, məlumat çəngəli isə strukturlaşdırılmamış məlumatları ehtiva edir. Klassik Mac OS bu çəngəlləri tək bir fayl kimi qəbul etsə də, faylların qeyri-Mac sistemlərinə ötürülməsi məlumat itkisi ilə nəticələndi, çünki onlar çəngəlləri tək bir varlıq kimi tanımırdılar. Bunu həll etmək üçün MacBinary formatı Dennis Brothers, Harry Chesley və Yves Lempereur kimi şəxslər tərəfindən yaradılmışdır. MacBinary sıxılmış və qeyri-Mac sistemlərinə köçürmək üçün çəngəlləri BIN faylı kimi tanınan vahid faylda birləşdirmişdir. Mac OS-ə qayıtdıqdan sonra çəngəllər yenidən ayrılacaq. 2000-ci illərdə çəngəl əsaslı HFS-dən uzaqlaşma ilə MacBinary formatının istifadəsi əhəmiyyətli dərəcədə azaldı. Bu gün MacBinary ilə kodlanmış BIN faylı ilə qarşılaşmaq, Mac olmayan sistemdə köhnə fayla rast gəlmədiyiniz və ya internetdən yükləmədiyiniz halda nadirdir.

The MacBinary format has gone through several versions over time to accommodate changes in Macintosh systems and file handling. Here are some of the different versions of the MacBinary format:

- **MacBinary I:** 1980-ci illərin sonlarında təqdim edilmiş MacBinary-nin ilkin versiyası. O, resurs çəngəlini və məlumat çəngəlini tək ikili faylda birləşdirərək Macintosh fayllarının platformalararası ötürülməsinə imkan verirdi.

- **MacBinary II:** 1990-cı illərin əvvəllərində buraxılmış bu versiya ikili faylın başlığına fayl növü və yaradıcı kodları kimi əlavə məlumat əlavə etməklə orijinal MacBinary formatını təkmilləşdirdi. Bu kodlar köçürmə zamanı Macintosh fayllarının bütövlüyünü və identifikasiyasını qorumağa kömək etdi.

- **MacBinary III:** The MacBinary III format, introduced in the mid-1990s, further enhanced the previous versions by including additional metadata, such as file name and file creation and modification dates, in the binary file's header. This allowed for more comprehensive preservation of Macintosh file attributes during transfer.

- **MacBinary IV:** MacBinary IV 2000-ci illərin əvvəllərində yaranan Mac OS X əməliyyat sistemi ilə uyğunluq problemlərini həll etmək üçün hazırlanmışdır. O, Mac OS X-də təqdim edilən yeni fayl sistemi strukturuna və atributlarına uyğunlaşmaq üçün dəyişiklikləri özündə birləşdirdi.

## BIN faylını necə açmaq olar?

MacBinary Encoded BIN faylları müxtəlif sıxılma yardım proqramlarından istifadə etməklə açıla bilər. macOS istifadəçiləri üçün **Apple Archive Utility** uyğun seçimdir. Windows istifadəçiləri MacBinary Encoded BIN faylının məzmununu çıxarmaq üçün **Smith Micro StuffIt Deluxe** kimi proqram təminatından istifadə edə bilərlər. macOS istifadəçiləri üçün başqa bir seçim **The Unarchiver**-dir ki, bu, MacBinary daxil olmaqla, çoxsaylı fayl formatlarını idarə edə bilən universal alətdir.

Qeyd etmək lazımdır ki, .bin fayl uzantısı təkcə MacBinary deyil, müxtəlif fayl formatları tərəfindən istifadə olunur. Buna görə də, yuxarıda qeyd olunan yardım proqramları ilə aça bilməyən BIN faylı ilə qarşılaşsanız, o, başqa formatda saxlanıla bilər. Belə hallarda, fayl məzmununa daxil olmaq üçün xüsusi fayl formatını müəyyən etməli və bu format üçün nəzərdə tutulmuş müvafiq proqram və ya yardımçı proqramdan istifadə etməlisiniz.

## Macbinary Arxivi nədir?

MacBinary arxivi ilk Macintosh kompüterləri üçün nəzərdə tutulmuş, Macintosh fayllarının ikili çəngəl strukturuna müraciət edən fayl formatıdır. Macintosh fayl sistemləri verilənləri və metaməlumatları ayrıca saxlayan məlumat çəngəlindən və resurs çəngəlindən ibarətdir. Sistemlərarası uyğunluğu və şəbəkə köçürmələrini asanlaşdırmaq üçün MacBinary hər iki çəngəli tək ikili fayla kodlayır. Bu format qeyri-Macintosh sistemlərinə köçürmələr zamanı məlumatların və əlaqəli resursların bütövlüyünü qoruyur.

## Macbinary arxivini silə bilərəmmi?

Bəli, MacBinary arxiv fayllarına ehtiyacınız yoxdursa və ya məzmunu çıxarıb başqa formatda saxlamısınızsa, onları silə bilərsiniz. MacBinary arxivləri sadəcə olaraq sistemlərarası köçürmələr və ya saxlama kimi xüsusi məqsədlər üçün Macintosh fayllarını qablaşdırma üsuludur. Arxivin silinməsi onun içindəki fayllara təsir etmir.

## Macbinary arxivini iPhone-da necə açmaq olar?

iPhone-da MacBinary arxivinin açılması üçüncü tərəf proqramlarının istifadəsini tələb edə bilər, çünki iOS-un bu format üçün yerli dəstəyi yoxdur.

## Macbinary Arxiv Çıxarışı - Macintosh Bin fayllarını necə çıxarmaq olar?

Müasir kompüterdə MacBinary (zibil) fayllarını çıxarmaq üçün siz adətən bu formatı dəstəkləyən fayl çıxarma yardım proqramından və ya proqram təminatından istifadə edəcəksiniz.

Windows-da MacBinary fayllarını dəstəkləyən fayl arxivi alətindən istifadə edin. Populyar seçimlərə WinRAR, 7-Zip və ya WinZip daxildir.

Mac OS MacBinary daxil olmaqla müxtəlif arxiv formatlarını idarə edə bilən daxili Arxiv Utiliti ilə gəlir. Finder-də MacBinary faylını tapın. MacBinary faylına iki dəfə klikləyin. Arxiv Utiliti avtomatik işə salmalı və məzmunu çıxarmalıdır. Çıxarma tamamlandıqdan sonra çıxarılan faylları orijinal MacBinary faylı ilə eyni yerdə və ya müəyyən bir təyinat yerində tapa bilərsiniz.

## Digər BIN faylları

**.bin** fayl uzantısından istifadə edən digər fayl növləri bunlardır.

- [BIN - Binary Disc Image File](/disc-and-media/bin/)
- [BIN - Unix Executable File](/executable/bin/)
- [BIN - BlackBerry IT Policy File](/settings/bin/)
- [BIN - Sega Genesis Game ROM](/game/bin/)
- [BIN - PSX PlayStation BIOS Image](/game/bin-pcsx/)

## İstinadlar

* [MacBinary](https://en.wikipedia.org/wiki/MacBinary)


