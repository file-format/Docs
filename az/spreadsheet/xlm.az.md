{
  "date": "2019-12-10",
  "keywords": [
"XLM",
"fayl",
"uzadılması",
"fayl formatı",
"Microsoft Excel makro faylı",
"Elektron cədvəl"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "XLM makro faylının və XLM fayllarını yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "XLM faylı nədir?",
  "linktitle": "XLM",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xl-azm"
}
},
  "lastmod": "2019-12-10"
}

## XLM faylı nədir?

Excel Macro üçün XLM, makroları saxlamaq üçün istifadə olunan elektron cədvəl faylları növüdür. Tətbiq nöqteyi-nəzərindən makro, proseslərin avtomatlaşdırılması üçün istifadə olunan təlimatlar toplusudur. Makro [XLS](/spreadsheet/xls/) fayl formatı üçün təkrar-təkrar yerinə yetirilən addımları qeyd etmək üçün istifadə olunur və makronu yenidən işə salmaqla hərəkətlərin yerinə yetirilməsini asanlaşdırır. Makrolar Microsoft-un Visual Basic for Applications (VBA) ilə Visual Basic Redaktorundan istifadə edərək Excel İş Kitabı daxilində proqramlaşdırılıb və birbaşa oradan işə salına/sazlana bilər.

## Qısa tarix ##

Microsoft Excel supported programming of macros since its first public launch. The features of macros remained the same through subsequent versions fo Excel with extension as per new features. XLM was the default macro language for Excel through Excel 4.0. Excel 5.0 standart olaraq VBA-da makroları qeyd etdi, lakin 5.0 XLM versiyası ilə hələ də seçim olaraq qeyd etməyə icazə verildi. 5.0 versiyasından sonra bu seçim dayandırıldı. Excel-in bütün versiyaları, o cümlədən Excel 2010 XLM makrosunu işlətməyə qadirdir, baxmayaraq ki, Microsoft onlardan istifadə etməyi qadağan edir.

## XLM-də makro qeyd edin ##

Excel makro yazmaq üçün istifadə üçün asan addımlar təqdim edir. Makrolarla işləmək üçün sizdən Developer alətlərinin quraşdırılması tələb olunur. Makro qeydi prosesdə olduqdan sonra o, hər bir istifadəçi hərəkətini daha sonra səsləndirmək üçün qeyd edir. Makro qeydi əslində istifadəçinin qeyd başlayandan sonra yerinə yetirdiyi bütün addımları əhatə edir. Beləliklə, makro qeydinə başlandıqdan sonra xananın məzmununu qalın, kursiv etsəniz və onun mətn əsaslandırmasını təyin etsəniz, bütün bu əmrlər qeyd olunacaq. Hər bir qeydə alınmış makroya daha sonra sürətli oxutma üçün qısa yol da təyin edilə bilər. Makro qeydi Visual Basic Redaktoru (VBE) istifadə edərək redaktə edilə bilən makro şəklində VBA kodunu yaradır.

## Excel obyekt modeli ##

Makroslar arxalarında VBA rutinlərindən istifadə edir və bu məqsədlə [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model)-ə əməl edirlər. Bu model istifadəçi tərəfindən müəyyən edilmiş komanda alətlər panelləri, əmr panelləri və ya mesaj qutuları vasitəsilə elektron tablo ilə qarşılıqlı əlaqə üçün elektron cədvəlin obyektlərini müəyyən edir. Məsələn, iş kitabının xüsusiyyətlərinə giriş İş kitabı obyekti ilə verilir. Eynilə, iş kitabının iş vərəqləri ilə proqramlı şəkildə işləmək üçün modeldə Worksheet obyekti var.

## Makrolar və Təhlükəsizlik ##

VBA bütün tətbiq sahələrinə, eləcə də fayl sisteminə daxil olmaq imkanı verir və həm də təhlükəli ola bilər. Bu, iş kitabını sonunda faylı işlədə bilən biri ilə paylaşarkən narahatlıq yaradır. Yəni Microsoft Excel belə bir faylın açılması barədə xəbərdarlıq edir. Digər istifadəçilərin onların etibarlı olduğunu yoxlamaq üçün makrolar rəqəmsal imza ilə təsdiqlənə bilər. Beləliklə, makrolar onların mənbəyinin yoxlanılmasından sonra işə salına bilər.

## İstinadlar ##

* [[MS-XLS] - Excel İkili Fayl Format Strukturu](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)

* [Makro Proqramlaşdırma](https://en.wikipedia.org/wiki/Microsoft_Excel#Makro_proqramlaşdırma)


