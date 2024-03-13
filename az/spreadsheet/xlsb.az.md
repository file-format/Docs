{
  "date": "2019-12-10",
  "keywords": [
"XLSB",
"fayl",
"uzadılması",
"fayl formatı",
"Excel ikili cədvəl faylı"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "XLSB faylının və onları yarada və aça bilən API-lərin nə olduğunu bilmək üçün fayl formatı bələdçisi.",
  "title": "XLSB faylı nədir?",
  "linktitle": "XLSB",
  "menu": {
    "docs": {
      "parent": "spreadsheet",
      "identifier": "spreadsheet-xls-azb"
}
},
  "lastmod": "2019-12-10"
}

## XLSB faylı nədir?

XLSB fayl formatı Excel iş kitabının məzmununu təyin edən qeydlər və strukturlar toplusu olan Excel İkili Fayl Formatını müəyyən edir. Məzmuna strukturlaşdırılmamış və ya yarı strukturlaşdırılmış rəqəmlər cədvəlləri, mətn və ya hər iki rəqəm və mətn, düsturlar, xarici məlumat əlaqələri, diaqramlar və şəkillər daxil ola bilər. [XLSX](/spreadsheet/xlsx/) (Açıq XML fayl formatına əsaslanır) fərqli olaraq, XLSB ikili Excel iş kitabı faylını təmsil edir. XLSB faylları daha sürətli oxuna və yazıla bilər ki, bu da onları böyük fayllarla işləmək üçün faydalı edir. XLSX (və əvvəllər [XLS](/spreadsheet/xls/)) iş kitablarını saxlamaq üçün istifadəçi tərəfindən ən çox seçilən fayl formatları olduğundan XLSB nadir hallarda iş kitablarını saxlamaq üçün istifadə olunur. O, Microsoft Office 2007 və yuxarı versiyalar tərəfindən aça bilər.

## XLSB Fayl Formatının Xüsusiyyətləri ##

The file format specifications for XLSB file format were made public back in 2008 as version 1.0. O vaxtdan bəri, spesifikasiyalara bir neçə dəfə yenidən baxıldı və spesifikasiyaların ən son versiyası (v 10.0) 2018-ci ilin aprelində nəşr olundu. Spesifikasiyalar Microsoft tərəfindən [[MS-XLSB] - Excel Binary File Format specifications](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx kimi açıq şəkildə mövcuddur və oxumaq və ya oxumaq üçün hər kəslə məsləhətləşməlidir. XLSB fayl formatında faylların yazılması.

## XLSB Fayl Strukturu ##

XLSB faylı hissələr toplusundan ibarət paketdir. Bu hissələr iş kitabının məzmunu, o cümlədən iş kitabı məlumatları və paketin strukturu haqqında məlumatları ehtiva edir. Bəzi hissələr ikili qeydlərdən istifadə edərək, bəziləri XML kimi, digərləri isə ikili bayt axını kimi saxlanılan məlumatları ehtiva edir. Hər ikili qeyddə iş kitabı məlumatlarını ehtiva edən sıfır və ya daha çox strukturlaşdırılmış sahələr var.

#### Paket ####

XLSB paketi [ZIP](/compression/zip/) arxividir və orada tam olaraq bir iş kitabı hissəsi olmalıdır. Bu hissə bu paket əlaqəsi hissəsində əlaqənin hədəfi olmalıdır. İş dəftəri hissəsi XLSB sənədinin başlanğıc hissəsidir.

#### Hissə ####

Hissə hissədə saxlanılan məzmunun xarakterini və növünü təyin edən əlaqəli məzmun növü olan bayt axınıdır. Bəzi hissələr məlumatı ikili formatda, digərləri isə XML olaraq saxlayır. Spesifikasiyalar sənədinin [parts enumeration](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) bölməsi paketdəki bütün hissələr arasında etibarlı hissələri, məzmun növlərini və tələb olunan/istəyə bağlı əlaqələri sadalayır.

#### Münasibət ####

Mənbə və hədəf resurs əlaqə ilə bağlıdır. Əlaqələr ola bilər:

**Paket əlaqəsi:** burada hədəf bir hissədir və mənbə bütövlükdə paketdir

**Hissə-hissə əlaqəsi:** burada hədəf bir hissədir və mənbə paketin bir hissəsidir

**Açıq əlaqə:** burada əlaqə elementinin ID atribut dəyərinə istinad etməklə mənbənin mənbə hissəsinin məzmunundan istinad edilir

**qeyri-müəyyən əlaqə** açıq-aşkar olmayan münasibətdir

**Daxili əlaqə:** burada hədəf paketin bir hissəsidir

**Xarici əlaqə:** burada hədəf paketdə olmayan xarici resursdur

#### Qeyd ####

Qeyd, iş kitabındakı xüsusiyyətlər haqqında məlumatı saxlamaq üçün istifadə olunan əsas tikinti blokudur. Hər ikili qeyd baytların dəyişən uzunluqlu ardıcıllığıdır. İkili qeyd üç komponentdən ibarətdir:

* rekord növü

* rekord ölçü və

* həmin qeyd növünə xas olan qeyd məlumatları.


**Qeyd növü:** Qeyd növü qeyd tərəfindən müəyyən edilmiş qeydin növünü göstərir. O, həmçinin bu qeyd üçün xüsusi qeyd məlumatlarının strukturunu müəyyən edir. Etibarlı qeyd növləri spesifikasiyalar sənədinin [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) bölməsində verilmişdir. Qeyd növü bir və ya iki bayt olmalıdır və 128-dən böyük və ya ona bərabər və 16384-dən kiçik olmalıdır.

**Qeyd ölçüsü:** Qeyd ölçüsü qeyd məlumatının ümumi ölçüsünü təyin edən baytların sayını təyin edir. Bu dəyər bir-dörd bayt olmalıdır. Aşağı baytdakı yüksək bit 0-a bərabərdirsə, bu dəyər bir bayt olmalıdır; əks halda, bu dəyər bir baytdan çox olmalıdır. Baytların sayı bir baytdan çox olarsa, hər bir ardıcıl baytdakı yüksək bit əlavə baytdan istifadə edilib-edilmədiyini müəyyən edir. İkinci baytın yüksək biti 1-ə bərabərdirsə, bu dəyər əlavə üçüncü baytdan istifadə etməlidir. Üçüncü baytın yüksək biti 1-ə bərabərdirsə, bu dəyər əlavə dördüncü baytdan istifadə etməlidir. Dördüncü baytın yüksək bitinə məhəl qoyulmamalıdır. Dəyər birləşdirilmiş hər baytın yeddi aşağı bitindən ibarətdir. Aşağı, ən az əhəmiyyətli bitlər birinci baytda yerləşir və hər bir ardıcıl bayt əvvəlki baytdan daha yüksək sıra bitlərini ehtiva edir.

**Qeyd Məlumatı:** Qeyd məlumatı komponenti xüsusi qeyd növünə uyğun gələn və qeydin qalan hissəsini təşkil edən sahələri ehtiva edir. Record Enumeration-da sadalanan verilmiş qeyd növü üçün sahələrin sırası və strukturu Records-da həmin qeyd növü üçün müvafiq bölmədə müəyyən edilir. Qeyd məlumatı komponentinin ümumi ölçüsü qeyd ölçüsünə bərabər olmalıdır. Qeyd məlumatı komponentindəki sahələr sadə dəyərləri, dəyərlər massivlərini, bir neçə sahənin strukturlarını, sahələrin massivlərini və strukturların massivlərini ehtiva edə bilər.

#### XLSB Qeyd Nümunəsi ####

Aşağıdakı qeyd növü və qeyd ölçüsü 200 bayt ölçüsü olan **BrtCommentText** qeydini təyin edir:

11111101 00000100 11001000 00000001 [Qeyd Sahələri]

The first byte is 11111101, specifying a low value of 125 and that the record type requires a second byte. The second byte is 00000100, specifying a high value of 4 * 128, bu 512-yə bərabərdir. Qeyd növü dəyəri 125 + 512 və ya **BrtCommentText** qeyd növünə uyğun gələn 637-dir. Növbəti bayt 11001000-dir, aşağı dəyəri 72 və qeyd ölçüsü üçün ikinci bayt tələb olunur. İkinci bayt 00000001-dir, daha yüksək 1 * 128 dəyərini və qeyd ölçüsünün əlavə bayt tələb etmədiyini göstərir. Qeydin ölçüsü 72 + 128 və ya 200-dür ki, bu da qeyd məlumatı komponentinin baytla ümumi ölçüsünü müəyyən edir. Qeyd məlumatı komponentindəki sahələr **BrtCommentText** ilə müəyyən edilir.

## İstinadlar ##

* [[MS-XLSB] - Excel (.xlsb) İkili Fayl Formatı](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)


