{
  "date": "2021-04-23",
  "keywords": [
"RES faylı",
"res faylını necə açmaq olar",
"res faylı nədir",
"uzadılması",
"format",
"RES fayl formatı"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "title": "RES - C++ Tərtib edilmiş Resurs Skripti",
  "description": "RES nümunəsi və RES faylları yarada və aça bilən API ilə RES fayl formatı haqqında məlumat əldə edin.",
  "linktitle": "RES",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-re-azs"
}
},
  "lastmod": "2021-04-23"
}

## RES faylı nədir?
.res şəkilçisi və ya uzantısı olan fayl bir çox fayl formatı kateqoriyasına aid ola bilər. Burada biz C++ Tərtib edilmiş Resurs Skripti olan RES fayl formatını müzakirə edirik; resurs məlumatlarını ehtiva edən Microsoft Resurs Kompilyatoru (rc) tərəfindən yaradılmış ikili fayl; resurs tərifi faylının məzmunu əsasında; əsas proqram layihəsinə uyğundur. .res faylı adətən onu proqramın icra olunan faylı ilə əlaqələndirmək üçün resurs obyekt faylına yenidən formatlanır.

## RES fayl formatı
RES fayl formatı Microsoft Resurs Kompilyatoruna (rc) aiddir. Resurs tərtibçisi proqramınızın istifadə etdiyi kursorlar, nişanlar, menyular və dialoq qutuları kimi resursları tərtib edən alətdir. Resurs faylları adətən .res uzantısına malikdir; kursorlar, şəkillər və versiya məlumatları kimi resursları ehtiva edir. RES faylı 16 və ya 32 bitlik resurs faylı ola bilər.
## Resurs fayl strukturu
Resurs faylı bir sıra müxtəlif resurs qeydlərini ehtiva edir. Hər bir giriş resurs başlığını və müvafiq məlumatları ehtiva edir. Resurs başlığı adətən faylda DWORD-a uyğunlaşdırılır və aşağıdakıları ehtiva edir:

- Resurs başlığının ölçüsünü müəyyən etmək üçün **DWORD**
- Resurs məlumatının ölçüsünü təyin etmək üçün **DWORD**
- Resurs növü
- Resursun adı
- Əlavə resurs məlumatı

The resource header structure defines the format of the RES file. The data for the resource follows the resource header. Some resources also add a resource-specific group header pattern to provide information about a group of resources. Following are some of the resource entry types and their description:

### Sürətləndirici Cədvəl Resursları
Sürətləndirici cədvəl qrup başlığı olmayan RES faylında resurs girişidir. **ACCELTABLEENTRY** nümunəsi sürətləndirici cədvəldəki hər bir girişi müəyyənləşdirir. RES faylında birdən çox sürətləndirici cədvəl ola bilər.

### Kursor və İkon Resursları
Baxmayaraq ki, sistem hər bir ikona və kursoru tək bir fayl kimi nəzərdən keçirir, lakin bunlar RES fayllarında bir qrup ikon resursları və ya kursor resursları qrupu kimi saxlanılır. Simge və kursor resurslarının fayl formatları eynidir. Resurs qrupu başlığı .res faylındakı bütün fərdi ikona və ya kursor qrupu komponentlərini izləyir.

### Dialoq Qutusu Resursları
Dialoq qutusu RES faylında resurs girişi kimi də həyata keçirilir. O, bir **DLGTEMPLATE** dialoq qutusunun başlıq nümunəsini və dialoq qutusundakı hər bir xüsusi nəzarət üçün bir **DLGITEMTEMPLATE** nümunəsini ehtiva edir. **DLGTEMPLATEEX** və **DLGITEMTEMPLATEEX** nümunələri genişləndirilmiş dialoq qutusu resurslarının formatını izah edir.

### Şrift Resursları
Menyu resursunda **MENUHEADER** nümunəsi, sonradan bir və ya daha çox **NORMALMENUITEM** və ya **POPUPMENUITEM** nümunələri var, menyu şablonunda hər bir menyu elementi üçün bir. **MENUEX_TEMPLATE_HEADER** və **MENUEX_TEMPLATE_ITEM** nümunələri genişləndirilmiş menyu resurslarının formatını izah edir.

### Mesaj Cədvəli Resursları
Mesaj cədvəli səhv mesajı və ya mesaj qutusunda göstərilmək üçün formatlaşdırılmış mətndən ibarətdir. Mesaj cədvəli resursunda əsas nümunə **MESSAGE_RESOURCE_DATA** strukturudur.

### Versiya Resursları
Versiya resursunda əsas nümunə **VS_FIXEDFILEINFO**-dur. Əlavə nümunələrə dil məlumatı ilə bağlı məlumatları saxlamaq üçün **VarFileInfo** və xüsusi sətir məlumatı üçün **StringFileInfo** daxildir.




## İstinadlar

 * [Resource File Formats](https://learn.microsoft.com/en-us/windows/win32/menurc/resource-file-formats)
 
 

