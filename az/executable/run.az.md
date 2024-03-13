{
  "date" : "2023-01-31",
  "keywords" : ["run file", "what is a run file", "file", "how to open run file", "run file extension","extension"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" : "RUN faylları yarada və aça bilən RUN fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title" : "RUN Fayl Format - Linux İcra edilə bilən Fayl",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run-az",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## RUN faylı nədir?

.run fayl formatı adətən Linux mühitində proqram təminatı və ya proqram quraşdırıcılarının paylanması üçün istifadə olunur. Proqram təminatını quraşdırmaq üçün faylı icra edilə bilən hala gətirməlisiniz, bu, aşağıdakı əmrdən istifadə etməklə edilə bilər:

```bash
chmod +x file_name.run 
```

Sonra, aşağıdakı əmrdən istifadə edərək faylı işə sala bilərsiniz:

```bash
./file_name.run 
```

Quraşdırma prosesi quraşdırmaq istədiyiniz xüsusi fayl və proqramdan asılı olaraq dəyişə bilər.

.run fayl formatı Linux mühitində proqram təminatı və ya proqram quraşdırıcılarını yaymaq üçün istifadə edilən qabıq skriptinin bir növüdür. Bu, ikili fayllar, kitabxanalar və konfiqurasiya faylları daxil olmaqla, proqramı quraşdırmaq üçün lazım olan hər şeyi özündə cəmləşdirən müstəqil paketdir.

Qeyd etmək vacibdir ki, .run fayllarında zərərli kod da ola bilər, ona görə də onu işə salmazdan əvvəl faylın mənbəyini yoxlamaq və viruslara qarşı skan etmək həmişə yaxşı olar.

Bundan əlavə, bəzi .run faylları işə salmaq və quraşdırmaq üçün kök imtiyazları tələb edə bilər, ona görə də faylı yüksək icazələrlə işə salmaq üçün sudo əmrindən istifadə etməli ola bilərsiniz:

```bash
sudo ./filename.run
```

## RUN faylını necə açmaq olar?

.run faylını açmaq üçün onu icra edilə bilən etmək lazımdır, bunu chmod əmri ilə etmək olar:

```bash
chmod +x filename.run 
```

Fayl icra edilə bilən hala gətirildikdən sonra onu yazaraq işə sala bilərsiniz:

```bash
./filename.run
```

.run faylını işə salmaq onu mətn redaktorunda açmaqla eyni deyil. .run faylını işə salmaq onun göstərişlərini yerinə yetirəcək, bu proqram quraşdırmadan skripti işə salmağa qədər hər şey ola bilər. .run faylının məzmununa baxmaq üçün onu nano və ya vim kimi mətn redaktorunda açmalısınız:

```
nano filename.run
```
və ya
```
vim filename.run
```

## İstinadlar
* [Ubuntuda .bin və .run fayllarını necə icra etmək olar](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)



