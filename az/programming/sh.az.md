{
  "date": "2019-10-11",
  "keywords": [
"sh faylı",
".sh faylı",
"uzadılması",
"format",
"sh faylı nümunəsi",
"sh fayl formatı",
"sh faylını necə işə salmaq olar"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "SH - Bash Shell Skript Faylı",
  "description": "SH fayl formatı və SH faylları yarada və aça bilən API-lər haqqında məlumat əldə edin.",
  "linktitle": "SH",
  "menu": {
    "docs": {
      "parent": "programming",
      "identifier": "programming-s-azh"
}
},
  "lastmod": "2021-05-21"
}

## SH faylı nədir?

.sh uzantılı fayl, Unix qabığı tərəfindən idarə olunacaq kompüter proqramını ehtiva edən skript dili əmrləri faylıdır. O, faylların işlənməsi, proqramların icrası və digər bu kimi vəzifələri yerinə yetirmək üçün ardıcıl olaraq işləyən bir sıra əmrləri ehtiva edə bilər. Bunlar eyni zamanda birdən çox əməliyyatı yerinə yetirmək üçün istifadəçi tərəfindən və ya toplu olaraq komanda xətti interfeysindən icra edilir. Skript faylları Windows, MacOS və Linux OS-də Notepad, Notepad++, Vim, Apple Terminal və digər oxşar proqramlar kimi mətn redaktorlarında açıla bilər.

## SH fayl formatı

SH faylları müəyyən edilmiş sintaksisdən sonra düz mətnlə yazılır. Bu skript faylları dəstəkləyir:

 * `Şərhlər` - Şərhlər # ilə başlayır və qabıq tərəfindən nəzərə alınmır.
 * `Qısa yollar` - Bunlar qısa və asan icra üçün əmrin adını dəyişmək üçün istifadə edilə bilər.
 * `Batch Jobs` - Əks halda əl ilə daxil edilməli olan bir neçə əmr avtomatik olaraq yerinə yetirilə bilər. Bu, istifadəçinin ardıcıllığın hər bir mərhələsini işə salmasını gözləmək ehtiyacını aradan qaldırır.
 * `Ümumiləşdirmə` - Sadə döngələrdən istifadə edərək, şəkillərin birdən digərinə çevrilməsi kimi əməliyyatlar üçün daha çox ümumiləşdirmə əldə edilir.

## SH fayl nümunəsi

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## SH faylını necə işə salmaq olar?
SH faylları adətən Linux-da işləyir, hətta Windows-da sh fayllarını işə salmaq üçün Putty kimi proqramlardan istifadə edərək Linux terminalına qoşulmalısınız. Linux terminalında SH faylını işə salmaq üçün aşağıdakı addımlar verilmişdir.

1. Linux terminalını açın və SH faylının yerləşdiyi qovluğa gedin.
2. `Chmod` əmrindən istifadə edərək, skriptinizdə icra icazəsini təyin edin (əgər artıq quraşdırılmayıbsa).
3. Aşağıdakılardan birini istifadə edərək skripti işə salın
	1. `./filename.sh`
	2.  `sh filename.sh`
	3.  `bash script-name-here.sh`

## İstinadlar

* [Yeni başlayanlar üçün Bashscripting](https://help.ubuntu.com/community/Beginners/BashScripting)

* [Shellscript](https://www.shellscript.sh/)


