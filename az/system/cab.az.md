{
  "date": "2021-06-29",
  "keywords": [
"KABİNƏ",
"uzadılması",
"fayl",
"format",
"sistemi",
"Windows kabinet faylı",
"Microsoft",
"Quraşdırıcı",
"Qurmaq",
"AdvPak"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "title": "CAB - Windows kabinet faylı",
  "description": "CAB faylları yarada və aça bilən CAB fayl formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "CAB",
  "menu": {
    "docs": {
      "parent": "system",
      "identifier": "system-ca-azb"
}
},
  "lastmod": "2021-06-29"
}

## CAB faylı nədir? ##

.cab uzantısı olan fayl sistem faylları kateqoriyasına aid olan Windows kabinet faylına aiddir. Bu, [LZX](/compression/lzx/), Quantum və [ZIP](/compression/zip/) kimi sıxılmış məlumat alqoritmlərini dəstəkləyən Microsoft Windows versiyalarında arxiv fayl formatında saxlanılan fayldır. İstifadəçi və ya tərtibatçı proqram quraşdırma məlumatlarını və fayllarını ehtiva etmək və paylaşmaq istədikdə fayl həyati əhəmiyyət kəsb edir. Məlumatların itkisiz sıxılması xüsusiyyətləri və bu fayllara daxil olan rəqəmsal sertifikatlaşdırma bu faylı belə faylların saxlanması və paylaşılması üçün mükəmməl edir. Device Installer, SetUp API və AdvPak kimi müxtəlif Microsoft quraşdırıcılarını dəstəkləyir.

## Qısa tarix ##

CAB faylı Microsoft tərəfindən hazırlanmış məlumat sıxılma fayl növüdür. Əvvəlcə Brilyant adlanırdı, lakin sonra xalq arasında Kabinet sözünün qısası olan CAB faylı kimi tanındı.

## Texniki Spesifikasiya ##

CAB faylı adətən maksimum 65535 qovluqdan ibarət ola bilər ki, bu da öz növbəsində hər birində maksimum 65536 fayl ola bilər. CAB fayl saxlama mexanizmi vaxt və məkan baxımından səmərəlidir, çünki o, hər bir faylı ayrıca sıxmaq və saxlamaq əvəzinə hər bir qovluğu sıxılmış blok kimi saxlayır. Boş qovluqları CAB arxiv qovluqlarında saxlamaq olmaz. CAB faylı ilk dəfə Microsoft tərəfindən hazırlanmışdır və bir qədər fərqli formatda InstallShield kimi müxtəlif quraşdırıcılarda istifadə olunur. CAB faylları adətən öz-özünə açılan proqramlara qoşulur. Microsoft CAB faylları formatı müəyyən etməyə kömək edən unikal marker sayəsində asanlıqla tanınır. Bütün Microsoft CAB faylları üçün unikal marker dörd sözdən ibarət olan MSCF prefiksidir. Bu kodu görən istifadəçi Microsoft CAB faylını digər fayllardan asanlıqla fərqləndirə və ona uyğun olaraq kompressorlarda və ya versiyalarda istifadə edə bilər. Fayllar daha çox proqram quraşdırma məlumatları ilə sıxıla bilər və ya mövcud məlumatlar düzgün proqram təminatından istifadə edərək açıla bilər.


## CAB Nümunəsi ##

Aşağıdakı nümunə CAB fayl strukturunda fayllar və qovluqlar arasındakı əlaqəni göstərir:

{{< figure src="../cab.png" alt="CAB fayl formatı" >}}

## İstinad ##

* [CAB - WIKIPEDIA](https://en.wikipedia.org/wiki/Cabinet_(file_format))
