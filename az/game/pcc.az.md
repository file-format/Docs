{
  "date": "2021-09-08",
  "keywords": [
"pcc faylı",
"pcc fayl formatı",
"pcc faylı nədir",
"fayl",
"pcc nümunəsi",
"pcc fayl uzantısı",
"uzadılması",
"format"
],
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "PCC faylları yarada və aça bilən Mass Effect PCC fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "PCC - Mass Effect Paket Faylı",
  "linktitle": "PCC",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-pc-azc"
}
},
  "lastmod": "2021-09-08"
}

## PCC faylı nədir?

.pcc ilə fayl modellər, teksturalar və otaqlar kimi oyun məzmununu dəyişdirmək üçün oyun datasını ehtiva edən [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3) fayldır. Mass Effect 2 və 3 Unreal Engine 3 oyun mühərrikinə əsaslanan ilk atıcı oyunlardır. Oyun əvvəlcə oyun resurslarının əksəriyyətini öz şəxsi PCC fayl formatında saxlayan [Bioware](https://www.bioware.com/about/) tərəfindən hazırlanmışdır. Bioware, aparıcı qlobal interaktiv əyləncə nəşriyyatı olan Electronic Arts tərəfindən alınıb.

## PCC Fayl Format - Ətraflı Məlumat

PCC faylları ümumi fayl təşkilinə töhfə verən sıxılmış və/və ya sıxılmamış strukturları ehtiva edir.

### Sıxılmış PCC Strukturu

Sıxılmış PCC faylı hissələrə bölünmüş cədvəllər və verilənlərdən ibarətdir. Hər bir hissədə dəyişən sayda sıxılmış bloklar var.

 * `Chunks Header` - Parçalar haqqında məlumatı ehtiva edən 16 baytlıq ümumi başlıq.
 * `Chunk Header` - Blok formasında olan xam sıxılmış məlumatlar haqqında məlumatları ehtiva edən 16 baytlıq başlıq.

### Sıxılmamış PCC Strukturu

Sıxılmamış PCC faylları aşağıdakı beş hissəyə bölünür.

 * `Başlıq` - PCC faylının strukturu haqqında əsas məlumatları ehtiva edir.
 * `Ad Cədvəli` - idxal sinifləri, ixrac və ixrac xassələri daxil olmaqla paketin içərisində olan adı ehtiva edir.
 * `İdxal Cədvəli` - PCC tərəfindən idxal edilən bütün sinifləri və obyektləri ehtiva edir.
 * `İxrac Cədvəli` - paketdə saxlanılan bütün obyektləri ehtiva edir. Hər bir ixrac ölçüsü fərqli ola bilər.

## İstinadlar

 * [Me3Explorer - PCC Fayl Format](https://me3explorer.fandom.com/wiki/PCC_File_Format)
 * [Mass Effect Game](https://www.ea.com/games/mass-effect/mass-effect-3)
 * [Bioware](https://www.bioware.com/about/)

