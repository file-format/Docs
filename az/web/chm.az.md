{
  "date": "2019-10-11",
  "keywords": [
"chm",
"chm faylı",
"chm fayl formatı",
"chm fayl növü",
"fayl",
"növü",
"chm faylı nədir"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "CHM - Tərtib edilmiş HTML Yardım Fayl Formatı",
  "description": "CHM faylı və onları yarada və aça bilən API-lərin nə olduğunu öyrənin.",
  "linktitle": "CHM",
  "menu": {
    "docs": {
      "parent": "web",
      "identifier": "web-ch-azm"
}
},
  "lastmod": "2019-09-10"
}

## CHM faylı nədir?

CHM fayl formatı HTML səhifələri toplusundan ibarət Microsoft **[HTML](/web/html/)** yardım faylını təmsil edir. O, mövzulara tez daxil olmaq və yardım sənədinin müxtəlif hissələrinə getmək üçün indeks təqdim edir. CHM faylı təmin edilmiş axtarış seçimi vasitəsilə məzmun üçün axtarış edilə bilər. CHM tez-tez proqram sənədləri üçün istifadə olunan Microsoft Mülkiyyətli onlayn yardım fayl formatıdır. Bundan əlavə, o, təlim təlimatları, interaktiv kitablar və elektron xəbər bülletenləri kimi bir sıra digər proqramlarda istifadə olunur. Müasir Microsoft İnkişaf mühitlərinin əksəriyyəti proqramda mövcud olan məlumatlardan CHM sənədlərinin yaradılmasını dəstəkləyir.

CHM fayl formatının birləşdirilmiş məzmun cədvəlini və indeksini həyata keçirmək üçün unikal qabiliyyəti onu digər standart HTML səhifələrindən fərqləndirir. Yaradılan CHM faylı nisbətən kiçik ölçülüdür və buna görə də proqram paketləri ilə asanlıqla paylana bilər. Yardım müəllifi aləti, HTML Help Workshop, yardım layihələrini və onlarla əlaqəli faylları yaratmaq və idarə etmək üçün istifadəsi asan sistem təqdim edir. CHM fayllarına mətn, şəkillər və hiperlinklər daxil ola bilər; veb brauzerdə görünə bilər; Windows və digər proqramlar tərəfindən onlayn yardım həlli kimi istifadə olunur.

## CHM fayl formatı

Yaradılan CHM faylının son forması yardım sisteminin necə tərtib olunduğundan və onun proqram və ya veb sayt üçün təyin olunmasından asılıdır. CHM faylı sıxılmış HTML faylları yaratmaq üçün LZX sıxılma ilə məlumat sıxılmasını dəstəkləyir. O, çoxlu .CHM fayllarını birləşdirmək imkanı ilə yanaşı məzmunun sürətli axtarışı üçün daxili axtarış motoruna malikdir. CHM faylı bir sıra HTML fayllarından, əlaqəli məzmun cədvəlindən və indeks faylından ibarətdir.

### HTML faylları

İstər proqramla, istərsə də İnternetdə paylanması üçün yardım mövzuları yaratmağınızdan asılı olmayaraq, müəllif olduğunuz sənədlər Hypertext Markup Language (HTML) kimi tanınan xüsusi formatlaşdırma dilindən istifadə etməklə yaradılır. HTML mövzu faylları .htm və ya .html fayl adı uzantısına malikdir.

Müəllif etdiyiniz hər bir yardım mövzusu və ya Veb səhifə üzərində mətn, qrafika və ya animasiya təsvirləri olan sənəd kimi görünsə də, .htm faylları əslində xüsusi HTML formatlaşdırma kodlarına malik mətn sənədləridir. Teqlər adlanan bu kodlar brauzerə hər səhifənin necə göstəriləcəyini bildirir. Yalnız mövzuda və ya Web səhifəsində görünən mətn əslində .htm faylındadır. Görünən istənilən qrafika, səslər, animasiya şəkilləri və ya digər elementlər HTML faylınızın işarə etdiyi ayrı fayllardır. Brauzer ona bunu bildirən etiketləri gördükdə qrafikləri, səsləri və ya digər elementləri kopyalayır və ya yükləyir.

### Mündəricat (TOC)
Mündəricatın yardım cədvəli (.hhc) faylı məzmun cədvəliniz üçün mövzu başlıqlarını ehtiva edən HTML faylıdır. İstifadəçi tərtib edilmiş yardım faylında (və ya Veb səhifədə) məzmun cədvəlini açdıqda və mövzu başlığına kliklədikdə, həmin başlıqla əlaqəli HTML faylı açılacaq.

### İndeks Faylı
İndeks (.hhk) faylı indeksiniz üçün indeks qeydlərini (açar sözlər) ehtiva edən HTML faylıdır. İstifadəçi indeksi tərtib edilmiş yardım faylında və ya veb-səhifədə açdıqda və açar sözü kliklədikdə, açar sözlə əlaqəli HTML faylı açılacaqdır.

## HTML Yardım Komponentləri

HTML Help bir neçə komponentdən ibarətdir. Bunlara aşağıdakılar daxildir:

* `HTML Help Workshop`: a help authoring tool with an easy-to-use graphical interface for creating project files, HTML topic files, contents files, index files, and everything else you need to put together an online help system or Web site.
* `HTML Help ActiveX nəzarət`: HTML faylına yardım naviqasiyasını və ikinci dərəcəli pəncərə funksionallığını daxil etmək üçün istifadə edilən kiçik, modul proqramdır.

* `The HTML Help Viewer`: onlayn yardım mövzularının görünə biləcəyi tam funksional və fərdiləşdirilə bilən üç panelli pəncərə.

* `Microsoft HTML Help Image Editor`: ekran görüntüləri yaratmaq üçün onlayn qrafik alət; və şəkil fayllarını çevirmək, redaktə etmək və baxmaq üçün.

* `The HTML Help Java Applet`: HTML faylına yardım naviqasiyasını daxil etmək üçün ActiveX nəzarəti əvəzinə istifadə edilə bilən kiçik, Java əsaslı proqram.

* `HTML Yardımı icra edilə bilən proqram`: tərtib edilmiş yardım faylına kliklədiyiniz zaman yardımı göstərən və işlədən proqram.

* `The HTML Help compiler`: layihəni, məzmunu, indeksi, mövzunu və digər faylları tərtib edilmiş yardım faylına yığan proqram.

* `The HTML Help Authoring Guide`: an online guide designed to assist help authors in using HTML Help to design a help system. The guide also contains a complete HTML Help reference for developers and an HTML tag reference for authors.

## İstinadlar

* [Microsoft HTML Yardım](https://learn.microsoft.com/en-us/previous-versions/windows/desktop/htmlhelp/microsoft-html-help-1-4-sdk)

* [Microsoft Compiled HTML Help](https://en.wikipedia.org/wiki/Microsoft_Compiled_HTML_Help)


