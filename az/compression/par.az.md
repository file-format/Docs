{
   "date":"2023-07-18",
   "keywords":[
"PAR",
"PAR faylı",
"par faylı necə açmaq olar",
"fayl",
"PAR fayl uzantısı",
"uzadılması",
"fayl"
],
   "author":{
      "display_name":"Shakeel Faiz"
},
   "draft":"false",
   "toc":true,
   "title":"PAR Fayl Format - Parchive Index Fayl",
   "description":"PAR faylları yarada və aça bilən PAR formatı və API-lər haqqında məlumat əldə edin.",
   "linktitle":"PAR",
   "menu":{
      "docs":{
         "identifier":"compression-par-az",
         "parent":"compression"
}
},
   "lastmod":"2023-07-18"
}

## PAR faylı nədir?

Parchive (PAR) arxivlərində .par faylı paritet həcmləri və ya paritet blokları qrupunu ehtiva edən indeks faylına istinad edir. Bu indeks faylı arxivdəki bir və ya bir neçə fayl itirildikdə və ya zədələndikdə səhvlərin aşkarlanması və bərpası məqsədləri üçün istifadə olunur.

Parxiv arxivi adətən həm orijinal məlumat fayllarından, həm də müvafiq paritet həcmlərindən ibarətdir. Paritet həcmləri Reed-Solomon xəta korreksiyası alqoritmlərindən istifadə etməklə yaradılır. Bu paritet həcmləri orijinal məlumat fayllarını bərpa etmək üçün istifadə edilə bilən lazımsız məlumatları ehtiva edir.

Paritet həcm dəsti kimi də tanınan .par faylı arxiv daxilində paritet həcmlərinin strukturu və yeri haqqında məlumatları ehtiva edir. O, bərpa prosesi üçün indeks və ya xəritə kimi xidmət edir. .par faylından istifadə etməklə, ixtisaslaşmış PAR proqram təminatı hansı paritet həcmlərə ehtiyac olduğunu və çatışmayan və ya zədələnmiş faylları yenidən qurmaq üçün onlardan necə istifadə edilməli olduğunu müəyyən edə bilər.

Parxiv arxivindəki bir və ya bir neçə fayl əlçatmaz olduqda və ya zədələndikdə, .par faylı itirilmiş məlumatları bərpa etmək üçün mövcud paritet həcmləri ilə birlikdə istifadə edilə bilər. PAR proqramı .par faylını oxuyur, çatışmayan və ya zədələnmiş faylları müəyyən edir və onları yenidən qurmaq üçün paritet həcmlərdən istifadə edir.

## PAR faylını necə açmaq olar?

.par fayllarını açmaq və istifadə etmək üçün sizə xüsusi PAR proqramı lazımdır. .par fayllarını idarə edə bilən bir neçə məşhur proqram variantları bunlardır:

- **QuickPar:** QuickPar Windows üçün geniş istifadə olunan PAR proqramıdır. Bu, PAR fayllarını yaratmağa, yoxlamağa və təmir etməyə imkan verir. Siz .par faylını QuickPar-da onun bütövlüyünü yoxlamaq üçün aça və ya Parchive arxivində zədələnmiş və ya çatışmayan faylları təmir etmək üçün istifadə edə bilərsiniz.

- **MultiPar:** MultiPar Windows üçün mövcud olan başqa bir məşhur PAR proqramıdır. O, həm PAR, həm də PAR2 fayl formatlarını dəstəkləyir və arxivlərin yaradılması, yoxlanılması və təmiri üçün qabaqcıl funksiyalar təqdim edir. MultiPar .par fayllarını aça və verilən paritet həcmlərinə əsaslanaraq səhvlərin aşkarlanması və bərpası əməliyyatlarını həyata keçirə bilər.

- **MacPAR deLuxe:** MacPAR deLuxe xüsusi olaraq macOS üçün nəzərdə tutulmuş PAR proqramdır. O, PAR və PAR2 fayl formatlarını dəstəkləyir və QuickPar və MultiPar kimi oxşar funksiyaları təmin edir. MacPAR deLuxe .par fayllarını aça və arxivləri yoxlamağa və zədələnmiş və ya itkin faylları bərpa etməyə kömək edə bilər.

## PAR Fayl Format - Ətraflı Məlumat

PAR fayl formatı, adətən Parchive olaraq adlandırılır, paritet məlumatları yaratmaq və fayl arxivlərində səhvlərin aşkarlanması və bərpası üçün istifadə olunan xüsusi fayl formatıdır. PAR fayl formatı adətən üç növdən ibarətdir: PAR, PAR2 və PAR3.

- **PAR:** PAR1 kimi də tanınan orijinal PAR fayl formatı Parchive layihəsi tərəfindən hazırlanmışdır. Buraya orijinal məlumat fayllarından yaradılan paritet məlumatları daxildir. PAR faylları səhvlərin aşkarlanması və bərpasının əsas səviyyəsini təmin edir, lakin səhvlərin düzəldilməsi imkanları baxımından məhdudiyyətlərə malikdir.

- **PAR2:** PAR2 PAR fayl formatının təkmilləşdirilmiş versiyasıdır. O, daha təkmil xətaların düzəldilməsi imkanları və təkmilləşdirilmiş bərpa xüsusiyyətləri təklif edir. PAR2 faylları adətən arxiv daxilində itirilmiş və ya zədələnmiş faylları bərpa edə bilən paritet məlumatları yaratmaq üçün istifadə olunur. PAR2 faylları məlumatların pozulmasına qarşı daha yaxşı qorunma təmin edir və fayl arxivləşdirmə məqsədləri üçün geniş istifadə olunur.

- **PAR3:** PAR3 is the latest version of the PAR file format and provides further improvements in error correction and recovery. It offers even higher levels of redundancy and error correction capabilities compared to PAR2. PAR3 faylları arxivlərdə saxlanılan məlumatlar üçün daha möhkəm qorunma və bərpa seçimlərini təmin etmək üçün nəzərdə tutulmuşdur.

Həm PAR2, həm də PAR3 fayl formatları PAR proqramı tərəfindən geniş şəkildə dəstəklənir və arxiv daxilində faylların bütövlüyünü yoxlamaq və itirilmiş və ya zədələnmiş məlumatları bərpa etmək imkanı təklif edir. PAR və PAR2 faylları hələ də tez-tez istifadə olunur, PAR3 faylları isə təkmilləşdirilmiş səhvlərin düzəldilməsi imkanlarına görə tədricən mənimsənilir.

## İstinadlar
* [Parxiv](https://en.wikipedia.org/wiki/Parchive)


