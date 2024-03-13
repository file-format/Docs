{
  "date": "2021-06-30",
  "keywords": [
"mst faylı",
"mst fayl formatı",
"mst faylı nədir",
"fayl",
"mst misal",
"mst fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "MST fayl formatı və MST fayllarını yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "title": "MST - Windows Quraşdırıcı Paket Faylı",
  "linktitle": "MST",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-ms-azt"
}
},
  "lastmod": "2021-06-30"
}

## MST faylı nədir?
.mst uzantılı fayllar MSI paketinin məzmununu dəyişdirmək üçün istifadə olunur. Onlar adətən sistem administratorları tərəfindən mövcud MSI faylına xüsusi parametrləri tətbiq etmək üçün istifadə olunur. MST faylları orijinal MSI paketi ilə birlikdə qrup siyasətləri kimi proqram paylama sistemlərində istifadə olunur. MST faylları ümumiyyətlə proqram təminatının işlənib hazırlanmasında və proqram təminatının inkişaf etdirilməkdə olan versiyalarını konfiqurasiya etmək üçün sınaqda istifadə olunur.

## MST fayl formatı
MST və ya Transform faylı Microsoft Windows Quraşdırıcısını faylda istifadə edən proqramlar üçün quraşdırma seçimlərini toplamaq üçün istifadə olunur. Bu fayllar adətən Quraşdırıcı (MSIEXEC.EXE) komanda xəttində istifadə olunur və ya proqram təminatının quraşdırılmasının Qrup Siyasətində istifadə olunur; Microsoft Active Directory domenində. MST faylları bükülmüş icra edilə bilən quraşdırıcılarla da istifadə edilə bilər. Ümumi hal odur ki, kimsə əmr satırı parametrlərini sarılmış quraşdırıcıya ötürmək istəyir. Bunu etmək üçün sizə WRAPPED_ARGUMENTS xassəsini xüsusiyyət cədvəlinə əlavə edən MST faylı lazımdır. Bu fayllar ümumi redaktorlardan istifadə etməklə yaradıla və ya redaktə edilə bilməz. Bunun üçün xüsusi alətlər mövcuddur.

### MST fayllarından necə istifadə etmək olar?
MST faylları müxtəlif alətlərdən istifadə etməklə yaradıla bilər və Ocra ümumiyyətlə MST faylları yaratmaq üçün istifadə olunur. Sonra parametrlər ehtiyaca uyğun olaraq fərdiləşdirilə və onları müəyyən bir yerdə saxlaya bilər. Bundan sonra MST faylları MSI faylları ilə birlikdə istifadə edilə bilər. Bu faylları sınamaq istəyirsinizsə; komanda xəttində aşağıdakı sintaksisi istifadə edin

```
msiexec /i setup_1.0.msi TRANSFORMS=mylog.mst
```
### Əmlakı DÖNÜŞÜR

Siz həmçinin Windows quraşdırıcısının **TRANSFORMS** xassəsindən istifadə edə bilərsiniz ki, bu da paketi quraşdırarkən quraşdırıcının tətbiq etdiyi transformasiyaların siyahısıdır. Quraşdırıcı transformasiyaları TRANSFORM xassəsində sadalanan ardıcıllıqla yerinə yetirir. Transformasiyalar .mst uzantısı və ya tam yolu ilə fayl adı ilə müəyyən edilə bilər. Birdən çox transformasiyanı təyin etmək üçün aşağıdakı nümunə kimi hər bir fayl adını və ya nöqtəli vergülü ayırın.

```
TRANSFORMS=transform1.mst;transform2.mst;transform3.mst
```

## İstinadlar 

* [MST Transformasiya Faylları](https://www.exemsi.com/documentation/mst-transformation-files/)

* [TRANSFORMS mülkiyyəti](https://learn.microsoft.com/en-us/windows/win32/msi/transforms)



