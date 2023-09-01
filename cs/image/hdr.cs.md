{
  "date" : "2022-07-21",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru HDR - Co je soubor obrázku HDR?",
  "description":"Další informace o formátu souboru HDR a rozhraních API, která mohou vytvářet a otevírat soubory HDR.",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2022-07-21"
}

## Co je soubor HDR?

Soubor HDR je formát rastrového obrázku s vysokým dynamickým rozsahem (HDR) pro ukládání fotografií z digitálního fotoaparátu. Umožňuje editorům fotografií vylepšit barvy a jas digitálních obrázků, které mají omezený dynamický rozsah. Tato úprava může zlepšit jas kolem rohů a výsledkem je téměř přirozený obraz. Soubory HDR se obvykle ukládají jako 32bitové rastrové obrázky. Adobe Photoshop umí vytvářet a otevírat soubory HDR.

Soubory HDR jsou také známé jako HDRI.

## Formát souboru HDR – Další informace

Formát souboru HDR je založen na původním formátu souboru Radiance Picture (.pic). Pixelová data souboru HDR jsou obvykle uložena nekomprimovaná, ale v některých případech jsou komprimována pomocí přímého systému kódování délky běhu.

### Struktura souborů HDR

Soubor obrázku HDR se skládá z následujících tří částí:

* **Header:** Soubor HDR je identifikován prvními bajty v souboru obrázku, tj. "#?RADIANCE".
* **Řetězec rozlišení:** Za záhlavím následuje jeden řádek rozlišení, který se skládá ze 4 hodnot; označení X a Y následované číselnou celočíselnou hodnotou. Pořadí X a Y označuje rotaci. Kombinace X a Y s kladnými a zápornými hodnotami pokrývá všechny možné orientace a rotace obrazu.
* **Data pixelů:** Data pixelů souboru HDR jsou buď nekomprimovaná, nebo komprimovaná pomocí standardního kódování délky běhu.

## Open-Source HDR/HDRI API

* **[imageinfo](https://github.com/xiaozhuai/imageinfo)** – Super rychlá knihovna s jedním záhlavím pro různé platformy [C++](/cs/programming/cpp/) pro získání velikosti a formátu obrázku bez načítání/dekódování.
* **[imgaeinfo-rs](https://github.com/xiaozhuai/imageinfo-rs)** – Knihovna Rust pro získání velikosti a formátu obrázku bez načítání/dekódování. Podporuje [.avif](/cs/image/avif/), [.bmp](/cs/image/bmp/), [.cur](/cs/image/cur/), [.dds](/cs/image/dds/), [. gif](/cs/image/gif/), hdr (pic), [heic (heif)](/cs/image/heic/), [.icns](/cs/image/icns/), [.ico](/cs/image/ico /), [.jp2](/cs/image/jp2/), [jpeg (jpg)](/cs/image/jpeg/), [jpx](/cs/image/jpx/), ktx, [png](/cs/image/png /), [psd](/cs/image/psd/), qoi, tga, tiff (tif) a webp.
* **[HdrHistogram](https://github.com/HdrHistogram/HdrHistogram)** – Java implementace HdrHistogramu.

## Reference

* [Radiance HDR](http://paulbourke.net/dataformats/pic/)
* [info o obrázku](https://github.com/xiaozhuai/imageinfo)

