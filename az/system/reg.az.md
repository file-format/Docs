{
  "date": "2023-03-07",
  "keywords": [
"reg faylı",
"reg faylı nədir",
"fayl",
"reg fayl uzantısı",
"uzadılması"
],
  "author": {
    "display_name": "Shakeel Faiz"
},
  "draft": "false",
  "toc": true,
  "title": "REG Fayl Format - Windows Qeydiyyatı Faylı",
  "description": "REG faylları yarada və aça bilən REG formatı və API-lər haqqında məlumat əldə edin.",
  "linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg-az",
      "parent": "system"
}
},
  "lastmod": "2023-03-07"
}

## REG faylı nədir?

REG faylı Windows Qeydiyyatı məlumatlarını idxal etmək və ya ixrac etmək üçün istifadə olunan fayl formatıdır. Windows Qeydiyyatı Windows əməliyyat sistemi və quraşdırılmış proqramlar üçün konfiqurasiya parametrlərini və seçimlərini saxlayan iyerarxik verilənlər bazasıdır. Reyestrdə istifadəçi seçimləri, proqram parametrləri, aparat və proqram təminatı konfiqurasiyası məlumatları və s. kimi məlumatlar var.

REG faylı adətən .reg fayl uzantısına malikdir və müəyyən formatda bir sıra qeyd qeydləri və dəyərləri ehtiva edən düz mətn faylıdır. Format, faylı qeyd dəftəri faylı kimi müəyyən edən başlıq bölməsindən, ardınca isə qeyd defteri qeydlərini təmsil edən bir sıra açar və dəyər cütlərindən ibarətdir.

## REG Fayl Format - Ətraflı Məlumat

Budur reg fayl formatına bir nümunə:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

Faylın birinci sətri qeyd redaktorunun versiyasını göstərir. Aşağıdakı sətirlər dəyər adı və dəyər məlumatı ilə izlənilən əsas yol formatında qeyd defteri qeydlərini ehtiva edir. Bu nümunədə reg faylı iki qeyddən ibarətdir: biri Windows başlanğıc siyahısına Example.exe adlı proqramı əlavə edən, digəri isə Windows Explorer-in qabaqcıl parametrlərində Gizli dəyərini doğru olaraq təyin edən.

Reg faylları Notepad kimi mətn redaktoru ilə yaradıla və redaktə edilə bilər. Onlar tez-tez ehtiyat nüsxə və bərpa məqsədləri üçün, həmçinin eyni reyestr parametrləri ilə birdən çox kompüteri konfiqurasiya etmək üçün istifadə olunur.

## Windows Qeydiyyatını İdxal və ya İxrac edin

REG faylı Windows Reyestrindən məlumatları idxal etmək və ya ixrac etmək üçün istifadə olunan bir fayl növüdür. Windows Qeydiyyatı Windows əməliyyat sistemi və quraşdırılmış proqramlar üçün konfiqurasiya parametrlərini və seçimlərini saxlayan iyerarxik verilənlər bazasıdır. Reyestrdə istifadəçi seçimləri, proqram parametrləri, aparat və proqram təminatı konfiqurasiyası məlumatları və s. kimi məlumatlar var.

Reg faylları reyestr qeydlərini yaratmaq və ya dəyişdirmək üçün istifadə edilə bilər və onlar tez-tez ehtiyat nüsxə və bərpa məqsədləri üçün, həmçinin eyni reyestr parametrləri ilə birdən çox kompüteri konfiqurasiya etmək üçün istifadə olunur. Windows Reyestrinə yeni bir qeyd qeydi əlavə etmək üçün reg faylından necə istifadə etmək olar:

1. Notepad kimi mətn redaktorundan istifadə edərək yeni mətn faylı yaradın.
2. Reyestr girişini düzgün formatda yazın. Format, faylı qeyd dəftəri faylı kimi müəyyən edən başlıq bölməsindən, ardınca isə qeyd defteri qeydlərini təmsil edən bir sıra açar və dəyər cütlərindən ibarətdir. Budur bir nümunə:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Bu, cari istifadəçinin qeyd dəftəri yuvasındakı Proqram təminatı düyməsi altında Nümunə adlı yeni açar yaradır və Setting1 dəyərini Value1 olaraq təyin edir.

3. Faylı .reg fayl uzantısı ilə saxlayın.
4. Yeni reyestr qeydini Windows Reyestrinə əlavə etmək üçün .reg faylına iki dəfə klikləyin.

Sizdən qeydi reyestrə əlavə etmək istədiyinizi təsdiqləmək istəniləcək. Təsdiq etdikdən sonra yeni qeyd reyestrə əlavə olunacaq və siz onu Registry Editor alətindən istifadə edərək yoxlaya bilərsiniz.

## İstinadlar
* [Windows Registry](https://en.wikipedia.org/wiki/Windows_Registry)


