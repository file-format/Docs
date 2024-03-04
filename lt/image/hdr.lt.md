{
  "date": "2022-07-21",
  "author": {
    "display_name": "Kashif Iqbal"
},
  "draft": "false",
  "toc": true,
  "title": "HDR failo formatas – kas yra HDR vaizdo failas?",
  "description": "Sužinokite apie HDR failo formatą ir API, kurios gali kurti ir atidaryti HDR failus.",
  "linktitle": "HDR",
  "menu": {
    "docs": {
      "parent": "image",
      "identifier": "image-hd-ltr"
}
},
  "lastmod": "2022-07-21"
}

## Kas yra HDR failas?

HDR failas yra didelio dinaminio diapazono (HDR) rastrinio vaizdo failo formatas, skirtas skaitmeninių fotoaparatų nuotraukoms saugoti. Tai leidžia nuotraukų redaktoriams pagerinti skaitmeninių vaizdų, kurių dinaminis diapazonas yra ribotas, spalvas ir ryškumą. Ši modifikacija gali pagerinti ryškumą aplink kampus, todėl vaizdas yra artimas natūraliam. HDR failai paprastai išsaugomi kaip 32 bitų rastriniai vaizdai. Adobe Photoshop gali kurti ir atidaryti HDR failus.

HDR failai taip pat žinomi kaip HDRI.

## HDR failo formatas – daugiau informacijos

HDR failo formatas yra pagrįstas originaliu Radiance Picture (.pic) failo formatu. HDR failo pikselių duomenys paprastai saugomi nesuspausti, tačiau kai kuriais atvejais jie suglaudinami naudojant paprastą veikimo ilgio kodavimo sistemą.

### HDR failo struktūra

HDR vaizdo failą sudaro trys skyriai:

 * **Antraštė:** HDR failas atpažįstamas pagal pirmuosius vaizdo failo baitus, ty #?RADIANCE.
 * **Rezoliucijos eilutė:** po antraštės eina viena skyros eilutė, kurią sudaro 4 reikšmės; X ir Y etiketė, po kurios yra skaitinė sveikojo skaičiaus reikšmė. X ir Y tvarka rodo sukimąsi. X ir Y derinys su teigiamomis ir neigiamomis reikšmėmis apima visas galimas vaizdo orientacijas ir sukimus.
 * **Pikselių duomenys:** HDR failo pikselių duomenys yra nesuspausti arba suglaudinami naudojant standartinę vykdymo trukmės koduotę.

## Atvirojo kodo HDR / HDRI API

 * **[imageinfo](https://github.com/xiaozhuai/imageinfo)** – kelių platformų itin greita vienos antraštės [C++](/programming/cpp/) biblioteka, leidžianti gauti vaizdo dydį ir formatą neįkeliant/dekoduojant.
 * **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** – Rust biblioteka, kad gautumėte vaizdo dydį ir formatą neįkeliant / neiškoduojant. Palaiko [.avif](/image/avif/), [.bmp](/image/bmp/), [.cur](/image/cur/), [.dds](/image/dds/), [ .gif](/image/gif/), hdr (pic), [heic (heif)](/image/heic/), [.icns](/image/icns/), [.ico](/image/ico/), [.jp2](/image/jp2/), [jpeg (jpg)](/image/jpeg/), [jpx](/image/jpx/), ktx, [png](/image/png/), [psd](/image/psd/), qoi, tga, tiff (tif) ir webp.
 * **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** – HdrHistogramos Java diegimas.

## Nuorodos

 * [Radiance HDR](http://paulbourke.net/dataformats/pic/)
 * [imageinfo](https://github.com/xiaozhuai/imageinfo)

