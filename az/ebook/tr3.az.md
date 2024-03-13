{
  "date": "2021-04-10",
  "keywords": [
"TR3",
"Fayl",
"Uzatma",
"Fayl Format",
"elektron kitab",
"TomeRaider",
"Yadabayt"
],
  "author": {
    "display_name": "Sami Cheema"
},
  "draft": "false",
  "toc": true,
  "description": "TR3 fayl formatı və TR3 fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "TR3 - TomeRaider 3 elektron kitab faylı",
  "linktitle": "TR3",
  "menu": {
    "docs": {
      "parent": "ebook",
      "identifier": "ebook-tr-az3"
}
},
  "lastmod": "2021-04-10"
}

## TR3 faylı nədir? ##

TR3 faylı sürətli axtarış və sıxılma üçün dəstək verən TomeRaider 3 e-kitabıdır. Bu, TomeRaider ilə əlaqəli proqram vasitəsilə düzgün işləyə bilər. Yadabyte bu proqram təminatının tərtibatçısı, Britaniya proqram təminatı və Böyük Britaniyada yerləşən veb inkişaf şirkətidir. TomeRaider elektron kitab oxuyucu proqramı bu TR3 fayllarının düzgün işləməsi və məzmununun idarə edilməsi üçün istifadə edilə bilər. Bu əlaqəli e-kitab oxuyucusu Microsoft Windows əsaslı sistemlərdə və bir çox ötürülə bilən qadcetlərdə işləyən kompüterlərdə quraşdırıla bilər. TR3 faylı Windows 10, Windows 7, Windows 8 / 8.1, Windows Vista, Windows XP kimi əməliyyat sistemlərində istifadə olunan e-kitab faylları qrupuna aiddir.

TR3 xüsusi **HTML teqləri** aşağıdakı kimidir:

|Etiket|Təsvir|
---|---|
|\<new> |Mətn fayllarından TomeRaider faylları yaratmaq üçün Yeni teq lazımdır.<new> teq səhifələrin başlanğıcını müəyyən edir.|
|\<CATDEF> ... \</CATDEF> |kateqoriya adını müəyyən edir|
|\<META> ... \</META> |fayl formatında istifadə olunan bütün metaməlumatları müəyyən etmək üçün istifadə olunan teqdir. Bu teq bir sıra parametrləri ehtiva edir.|
|\<EXPMSG> |Bu teq faylın müddəti bitdikdə görünən mesajı idarə edir. Hər dəfə istifadəçi faylın müddəti bitdikdən sonra səhifəyə baxmaq istəsə, faktiki səhifə mətni yerinə bitmə mesajı görünür.|
|\<DIEMSG> |Bu teq EXPMSG ilə oxşardır. Fayl öldüyü zaman mesajı göstərmək üçün istifadə olunur.|
|\<ENGMSG> |Bu teq şifrələnmiş səhifələr üçün göstərilən mesaj yaratmaq üçün istifadə olunur. İstifadəçi şifrələnmiş səhifəni kiliddən çıxarmazdan əvvəl açmağa cəhd edərsə, səhifə mətni əvəzinə mesaj görünür.|
|\<expmsg> ,\<diemsg> və \<encmsg> |Səhifə mətnində nəzərə alınmır. Onlar birincidən əvvəl fayl başlığı bölməsində yerləşdirilməlidir<new> tag.|
|\<SELECTION> . \</ SELECTION> |Query'ləri dəstəkləmək üçün istifadə olunur. Bu etiket birincidən əvvəl olmalıdır<new> etiket. O, istifadəçi sorğusu üçün seçim məlumatlarını tərtib edir.|
|\<catset> . \</catset> | Hər bir mövzu üçün kateqoriya adları təyin etmək üçün istifadə olunur.|


## TR3 faylını açmaqla bağlı problemlər ##

Burada yarana biləcək və fayl formatının düzgün işləməməsinə səbəb ola biləcək bəzi ümumi problemlərin siyahısı verilmişdir:

* Zədələnmiş fayl
* Virus səbəbiylə yoluxmuş fayl
* Arxiv girişlərində TR3 faylına düzgün olmayan keçidlər
* Faylları açmaq üçün sistemə giriş hüququ yoxdur
* Sisteminizdə köhnəlmiş disk
* TR3 hesabatının Windows arxivindən çıxarılması
* Daha yaxşı çıxış üçün tərtibatçı ilə əlaqə saxlamaq daha yaxşı seçim ola bilər

