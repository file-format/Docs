{
  "date": "2021-06-29",
  "keywords": [
"com faylı",
"com faylı nədir",
"fayl",
"com nümunəsi",
"com fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Muhammad Umar"
},
  "draft": "false",
  "toc": true,
  "description": "COM faylları yarada və aça bilən COM fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "COM - DOS əmr faylı formatı",
  "linktitle": "COM",
  "menu": {
    "docs": {
      "parent": "executable",
      "identifier": "executable-co-azm"
}
},
  "lastmod": "2021-06-29"
}

## COM faylı nədir?
COM faylları sadəcə olaraq bir sıra əmr və ya göstərişləri yerinə yetirmək üçün istifadə olunur. COM faylı Windows və ya MS-DOS-dan idarə oluna bilən icra edilə bilən proqramdan ibarətdir. Eyni şəkildə EXE faylı, COM faylı da ikili formatda saxlanılır, lakin EXE faylından fərqlidir, çünki onun başlığı və ya metadatası yoxdur və həmçinin maksimum ölçüsü təxminən 64KB-dır. COM faylı 32 bitlik sistemdə ilk dəfə işlədikdə, NT Virtual DOS Maşını (NTVDM) komponentini quraşdırmağı təklif edir. COM faylı MS-DOS mühitini dəstəkləyən virtual maşınla Microsoft Windows-un 64-bit versiyasında işlədilə bilər.

## COM fayl formatı
COM fayl formatı Microsoft Windows və ya MS-DOS-da istifadə olunan ikili icra edilə bilən formatdır. Onun strukturu sadəcə təlimatlar toplusundan ibarətdir; onun başlığı yoxdur və standart metadata yoxdur. O, bütün məlumatlarını və kodunu yalnız bir seqmentdə saxlayır və ikili faylı maksimum 64KB ölçüsünə malikdir. Bu fayl formatı yenidən işə salmağa cəhd edərkən yerini dəyişmir. Beləliklə, əməliyyat sistemi onu əvvəlcədən təyin edilmiş ünvanda yükləyir. Üstəlik, hər iki əməliyyat sistemi altında **fat binar** şəklində icra etmək üçün bir COM faylı etmək mümkündür. Təlimat səviyyəsində heç bir faktiki uyğunluq yoxdur. Giriş nöqtəsindəki təlimatlar funksionallıq baxımından bərabər, lakin hər iki əməliyyat sistemində fərqli olaraq seçilir və proqramı işə salır, istifadə olunan əməliyyat sisteminin bölməsinə keçin. Bu, əsasən bir faylda eyni prosedura malik iki fərqli proqramdır, ondan əvvəl istifadə ediləcək birini seçən koddur.
### COM fayl nümunəsi
COM faylını icra edərkən, təlimatlar birinci baytdan oxunur və sonuncu təlimat tapılana qədər ardıcıl olaraq yerinə yetirilir. Budur bir ASM kodu nümunəsi:

```
[BITS 16]		;Set code generation to 16 bit mode
[ORG 0x0100]		;Set code start address to 0100h


[SEGMENT .text]		;Main code segment
    mov ah, 9 ; DOS print string function
    mov dx, hello
    int 21h
    ;Exit to DOS
    mov ah, 4ch
    int 21h
[SEGMENT .data]		;Initialised data segment
hello:   db   'Hello, .COM programmer!',13,10,'$'
```

## İstinadlar 

* [COM faylı - Wikipewdia tərəfindən](https://en.wikipedia.org/wiki/COM_file)


