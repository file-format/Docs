{
  "date": "2019-10-11",
  "keywords": [
"pdb faylı",
"pdb",
"uzadılması",
"format",
"Pdb faylı nədir",
"pdb fayl formatı",
"PDB metadata"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "PDB Fayl Format - Proqram verilənlər bazası faylı",
  "description": "PDB fayl formatı və PDB fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "PDB",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-pd-azb"
}
},
  "lastmod": "2020-09-10"
}

## PDB faylı nədir?

.pdb uzantısı olan fayl tərtib edilmiş icra olunan fayl (EXE/DLL) üçün sazlama məlumatını ehtiva edən proqram verilənlər bazası faylıdır. PDB faylları proqram proqramı debug rejimində tərtib edildikdə Microsoft Kompilyatorları tərəfindən yaradılır. PDB faylının mövcudluğu modulların bütün simvolları haqqında əhəmiyyətli məlumatları ehtiva etdiyi üçün icra olunan faylı tərs mühəndisləşdirməyə kömək edə bilər. Məhz bu səbəbdən bu fayllar son icra olunan fayldan ayrı saxlanılır. Microsoft-un [DgbHelp API](https://learn.microsoft.com/en-us/windows/win32/debug/dbghelp-functions) ictimai və ixrac, qlobal simvollar, yerli simvollar, tip məlumatları, mənbə faylları və sətir nömrələri kimi məlumatları əldə etmək üçün PDB faylını aça bilər.

## PDB fayl formatı

PDB Microsoft-un xüsusi fayl formatıdır və hələ heç bir yerdə rəsmi olaraq sənədləşdirilməyib. Bununla belə, [here](https://github.com/Microsoft/microsoft-pdb) başlanğıc sənədləri mövcuddur və ona istinad edilə bilər.

### PDB Axınları

PDB faylları çoxlu axınlardan ibarətdir, burada hər bir axın virtual fərdi fayl kimi çıxış edir və məlumat ehtiva edir. PDB fayl müəllifləri bu fayllara yaza bilər və fayl yalnız açıq öhdəlik verildikdən sonra yekunlaşdırılır. Kompilyator PDB faylına yazmağa davam edə bilər, lakin yalnız bütün istifadəçi kodu uğurla tərtib edildikdə öhdəlik götürə bilər. PDB faylı aşağıdakı axınlardan ibarətdir:

|Axın No. |Mündərici |Qısa Təsvir|
---|---|---|
|1| Pdb (başlıq) |Versiya məlumatı və bu PDB-ni EXE-yə qoşmaq üçün məlumat|
|2| Tpi (Tip meneceri) |İcra edilə biləndə istifadə olunan bütün növlər.|
|3| Dbi (Sazlama məlumatı) |Bölmə töhfələrini və 'Modlar' siyahısını saxlayır|
|4| NameMap| Hashed sətir cədvəlini saxlayır|
|4-(n+4)| n Mod (Modul məlumatı)| Hər Mod axını bir kompilyasiya üçün simvollar və sətir nömrələrini ehtiva edir|
|n+4| Qlobal simvol hash| Qlobal simvollarda ada görə axtarış etməyə imkan verən indeks|
|n+5| İctimai simvol hash| Ünvanlar üzrə ictimai simvollarda axtarış etməyə imkan verən indeks|
|n+6| Simvol qeydləri| Qlobal və ictimai simvolların faktiki simvol qeydləri|
|n+7| hash yazın| TPI axını tərəfindən istifadə edilən hash.|

PDB faylındakı hər bir axın ardıcıl olaraq nömrələnməyən bir neçə səhifədən ibarətdir.

### PDB başlığı

PDB faylı spesifik formatı müəyyən etmək və təsdiqləmək üçün imzadan ibarət Başlığa malikdir. İmzanın uzunluğu PDB formatından asılıdır. Başlıq bir səhifədən uzun ola bilər.

### PDB Metadata
The PDB metadata is responsible to recognize all of the component streams, giving the length, and sequence of pages for each stream. Orders are given to streams consecutively; starting with 0. Bəzi metadataları ehtiva edən sıralanmamış kök axını da var.

## İstinadlar
 * [PDB - Vikipediya](https://en.wikipedia.org/wiki/Program_database)
 * [Microsoft PDB](https://github.com/Microsoft/microsoft-pdb)

