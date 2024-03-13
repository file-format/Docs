{
  "date": "2023-06-22",
  "keywords": [
"rmd",
"rmd faylı",
"rmd faylı nədir",
"rmd faylını necə yaratmaq olar",
"rmd faylını necə açmaq olar",
"fayl",
"rmd fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "RMD Fayl Format - R Markdown Fayl",
  "description": "RMD faylları yarada və aça bilən RMD formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "RMD",
  "menu": {
    "docs": {
      "identifier": "word-processing-rmd-az",
      "parent": "word-processing"
}
},
  "lastmod": "2023-06-22"
}

## RMD faylı nədir?

R Markdown (RMD) faylı Markdown mətnini daxil edilmiş R kodu parçaları ilə birləşdirən .rmd uzantılı mətn faylıdır. O, təkrarlana bilən tədqiqat və məlumatların təhlili üçün güclü vasitədir, çünki o, kod daxil olmaqla hekayə mətni yazmağa və dinamik hesabat və ya sənədlər yaratmağa imkan verir. O, YAML metadatasını, Markdown formatlı düz mətni və RStudio-dan istifadə edilərkən, mürəkkəb məlumat təhlili sənədini yaratmaq üçün birləşən R kodu hissələrini ehtiva edir.

R Markdown faylları adətən RStudio IDE-də istifadə olunur, lakin siz onlarla istənilən mətn redaktorunda da işləyə bilərsiniz. RMD faylını göstərdiyiniz zaman kod parçaları yerinə yetirilir və çıxış (cədvəllər, süjetlər və ya mətn kimi) yekun sənədə daxil edilir. Bu, məlumat təhlilinizi və vizuallaşdırmanızı yazılı izahatlarınızla mükəmməl şəkildə birləşdirməyə imkan verir.

## RMD faylını necə yaratmaq olar?

RMD faylı yaratmaq üçün istədiyiniz mətn redaktorundan istifadə edə bilərsiniz. Yeni faylı açıb onu R Markdown formatını ifadə edən .rmd uzantısı ilə yadda saxlamaqla başlayın. Markdown sintaksisi sənədin məzmununu yazmaq üçün əsas kimi xidmət edir. Markdown, mətni asanlıqla strukturlaşdırmağa və formatlamağa imkan verən yüngül işarələmə dilidir. Başlıqlar, paraqraflar, siyahılar, keçidlər və şəkillər asanlıqla sənədinizə daxil edilə bilər, aydınlıq və oxunaqlılıq təmin edilir.

R Markdown-un əsas üstünlüklərindən biri R kodu hissələrini birbaşa sənədinizə daxil etmək imkanıdır. Üç arxa işarə `(```)` və `({ })` əyri mötərizə içərisində `r` hərfi ilə əhatə olunmuş bu kod parçaları sizə R kodunu qüsursuz yazmağa və icra etməyə imkan verir. Siz məlumatların təhlilini həyata keçirə, vizuallaşdırmalar yarada, statistika hesablaya və hətta interaktiv elementləri daxil edə bilərsiniz. RMD faylını göstərdiyiniz zaman kod parçaları yerinə yetirilir və nəticədə nəticə avtomatik olaraq yekun sənədə daxil edilir, bu da təhlilinizin və hekayənizin tam inteqrasiya olunmasını təmin edir.

RMD faylınız tamamlandıqdan sonra onu asanlıqla HTML, PDF və ya Word kimi müxtəlif formatlara çevirə bilərsiniz. RStudio kimi inteqrasiya olunmuş inkişaf mühitləri (IDE) sizin spesifikasiyalarınıza əsasən sənədi təqdim edən Toxunma düyməsi ilə qüsursuz təcrübə təmin edir. Alternativ olaraq, RMD faylını proqramlı şəkildə göstərmək üçün R-də `rmarkdown::render()` funksiyasından istifadə edə bilərsiniz.

## RMD faylını necə açmaq olar?

Ümumiyyətlə, RMD faylını RStudio-da açmalısınız, çünki o, RMD sintaksisini dəstəkləyir və əslində RMD faylında olan kodu icra edə bilir. RMD faylını uyğun mətn redaktorunda və ya IDE-də açmaqla siz asanlıqla faylla işləyə, onun məzmununu dəyişdirə, R kodu hissələrini icra edə və daxil edilmiş kod və Markdown mətni əsasında istədiyiniz nəticə və ya hesabatlar yarada bilərsiniz.

Əgər niyyətiniz yalnız RMD faylının məzmununa baxmaqdırsa, onu istənilən mətn redaktorundan istifadə edərək aça bilərsiniz.

## İstinadlar
* [R Markdown-a giriş](https://rmarkdown.rstudio.com/articles_intro.html)


