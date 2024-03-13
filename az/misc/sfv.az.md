{
  "date" : "2024-03-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "SFV Faylı - Sadə Fayl Doğrulama Faylı - .sfv faylı nədir və onu necə açmaq olar?",
  "description" : "SFV Sadə Fayl Doğrulama Faylı və onu necə açmaq barədə məlumat əldə edin.",
  "linktitle" : "SFV",
  "menu" : {
    "docs" : {
      "identifier" : "misc-sfv-az",
      "parent" : "misc"
}
},
  "lastmod" : "2024-03-08"
}

## SFV faylı nədir?

Sadə Fayl Doğrulama mənasını verən SFV fayl formatı adətən faylların, xüsusən də internet üzərindən yayılanların bütövlüyünü yoxlamaq üçün istifadə olunur. SFV faylları SFV faylında sadalanan hər bir fayl üçün yoxlama məbləğlərini (adətən CRC32 yoxlama cəmi) ehtiva edir. Bu yoxlama məbləğləri müvafiq faylların məzmunu əsasında hesablanır.

SFV faylının məqsədi istifadəçilərə yüklədikləri və ya qəbul etdikləri faylların hər hansı şəkildə pozulduğunu və ya dəyişdirildiyini tez yoxlamaq imkanı verməkdir. Bunun üçün onlar SFV faylını oxuyan, fayllar üçün yoxlama məbləğlərini yenidən hesablayan və SFV faylında saxlanan yoxlama məbləğləri ilə müqayisə edən SFV yoxlayıcı proqramından istifadə edə bilərlər. Hər hansı yoxlama cəmləri uyğun gəlmirsə, bu, müvafiq faylın dəyişdirildiyini və ya zədələndiyini göstərir.

## SFV Fayl Format - Ətraflı Məlumat

SFV faylları tez-tez fayl paylaşımı ilə birlikdə, xüsusilə proqram, media faylları və ya arxivlər kimi böyük faylları və ya fayl kolleksiyalarını yaymaq üçün istifadə olunur. Onlar yüklənmiş faylları tamamilə yenidən yükləməyə ehtiyac olmadan bütövlüyünü təmin etmək üçün sadə və səmərəli üsul təqdim edir.

SFV faylının strukturu adətən sadədir, hər bir sətir faylı və ona uyğun yoxlama məbləğini təmsil edən mətn sətirlərindən ibarətdir. Budur bir nümunə:

```
file1.txt 12345678
file2.jpg ABCDEFGH
file3.exe 98765432
```

Bu misalda, hər bir sətir faylın adını və onun yoxlama məbləğini ehtiva edir. SFV faylına əlavə məlumat və ya metadata da daxil ola bilər, lakin əsas struktur eyni qalır.

## SFV faylını necə açmaq olar?

SFV faylını açmaq və istifadə etmək üçün sizə adətən xüsusi SFV yoxlayıcı və ya doğrulama aləti lazımdır. SFV faylını açmaq və istifadə etmək üçün ümumi addımlar bunlardır:

1. QuickSFV və ya RapidCRC kimi SFV yoxlama proqramını yükləyin.
1. Proqramı quraşdırın və açın.
1. SFV faylını açmaq üçün proqramdan istifadə edin.
1. Proqram avtomatik olaraq yoxlama məbləğlərini yoxlayacaq və hər hansı uyğunsuzluğu göstərəcək.
1. Nəticələri nəzərdən keçirin və zədələnmiş faylları yenidən yükləmək kimi müvafiq tədbirləri həyata keçirin.

## İstinadlar
* [Sadə fayl yoxlaması](https://en.wikipedia.org/wiki/Simple_file_verification)


