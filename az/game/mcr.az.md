{
  "date": "2022-12-13",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "description": "MCR faylları yarada və aça bilən MCR fayl formatı və API-lər haqqında məlumat əldə edin.",
  "title": "MCR - Minecraft Region fayl formatı",
  "linktitle": "MCR",
  "menu": {
    "docs": {
      "parent": "game",
      "identifier": "game-mc-azr"
}
},
  "lastmod": "2022-12-14"
}

## MCR faylı nədir?

Minecraft MCR fayl formatı Minecraft Dünyasının ərazi hissələrini saxlamaq üçün Minecraft tərəfindən istifadə edilən məlumat formatıdır. O, məşhur açıq mənbəli oyun mühərriki Minecraft Forge-un tərtibatçıları tərəfindən hazırlanmış NBT (Named Binary Tag) formatına əsaslanır. MCR fayl növü lap əvvəlində təqdim edilmiş və sonradan [MCA file format](/game/mca/) ilə əvəz edilmişdir.

## MCR fayl formatı

MCR fayl formatı hər biri müəyyən tipli məlumat ehtiva edən bir sıra adlandırılmış ikili teqlər kimi strukturlaşdırılmışdır. Üst səviyyə teq, bir oyun səviyyəsi üçün bütün məlumatları ehtiva edən Səviyyə teqidir. Səviyyə teqində, oyun dünyası haqqında məlumatı saxlayan Data teqləri və Müəssisələr və TileEntities teqləri kimi müxtəlif məlumat növlərini saxlayan bir neçə başqa adlandırılmış teq var. dünyada müvafiq olaraq oyun obyektləri və kafel obyektləri.

## MCR Fayl Formatında nə var?

Minecraft MCR fayl formatında bölgə oyun dünyasının 32x32 blok sahəsidir. MCR formatı məlumatları daha səmərəli idarə etmək və oyun səviyyələrinin daha sürətli yüklənməsinə və saxlanmasına imkan vermək üçün oyun dünyasını regionlara bölür. Hər bir bölgə ayrı bir faylda saxlanılır və MCR fayl formatı oyun dünyasında hər bir bölgənin mövqeyini müəyyən etmək üçün koordinatlar sistemindən istifadə edir. Bölgənin koordinatları bölgənin aşağı sol küncünün blok koordinatları ilə müəyyən edilir. Məsələn, koordinatları (-1,0) olan bir bölgə oyun dünyasının mənşəyindən bir sola və sıfır bölgəyə doğru yerləşəcəkdir.

## MCR Fayl Formatının Xüsusiyyətləri

MCR fayl formatının spesifikasiyası ictimaiyyətə açıqdır. MCR formatının əsaslandığı NBT formatının spesifikasiyası Minecraft Forge veb saytında mövcuddur. Əlavə olaraq, [Minecraft Wiki](https://minecraft.fandom.com/wiki/Region_file_format) MCR fayl formatı, o cümlədən onun strukturu və dəstəklədiyi müxtəlif məlumat növləri haqqında ətraflı məlumata malikdir.

### MCR fayllarında sıxılmış məlumat

Minecraft MCR fayl formatı sıxılmanı dəstəkləyir. MCR fayl formatı verilənlərin sıxılmış formada saxlanmasına imkan verən [NBT format](https://minecraft.fandom.com/wiki/NBT_format)-ə əsaslanır. Bu, MCR fayllarının ölçüsünü azaltmağa və onların ötürülməsi və saxlanmasını daha səmərəli etməyə kömək edir. Bu, MCR fayl formatının vacib xüsusiyyətidir, çünki oyunçulara böyük Minecraft World ərazi məlumatlarını başqaları ilə paylaşmağa imkan verir.

## İstinadlar

* [Minecraft üçün Dünya Redaktoru](https://www.mcedit.net/)

* [Minecraft haqqında](https://www.minecraft.net/)

* [Region Fayl Formatı](https://minecraft.fandom.com/wiki/Region_file_format)

* [NBT Format](https://minecraft.fandom.com/wiki/NBT_format)


