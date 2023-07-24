{
  "date" : "2019-11-25",
  "keywords" :[ "soubor jpm", "formát souboru jpm", "co je soubor jpm", "soubor", "příklad jpm", "přípona souboru jpm", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPM - formát složených souborů JPEG 2000",
  "description":"Další informace o formátu souborů JPM a rozhraních API, která mohou vytvářet a otevírat soubory JPM.",
  "linktitle" : "JPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-08"
}

## Co je soubor JPM?

JPM označuje systém kódování obrázků JPEG 2000 část 6, který se používá pro zobrazování dokumentů. Je založen na standardu Mixed Raster Content Standard (ISO/IEC 16485) a obsahuje vrstvené statické obrázky, které používají JPEG 2000 a další kódování. Kromě vlastních specifikací dědí formát souboru JPM vlastnosti od svého rodiče, tj. formátu souboru [jp2](/cs/image/jp2/).

## Formát souboru JPM

Formát souboru JPM je definován [ISO/IEC 15444-6:2003](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124) – obrázek JPEG 2000 kódovací systém -- Část 6: Formát souboru složeného obrázku. Složený obraz může obsahovat naskenované obrazy, syntetické obrazy nebo obojí, což vyžaduje kombinaci kontinuálních tónových a dvouúrovňových kompresních metod. Formát souboru JPM definuje kompoziční model, který popisuje metodu kombinování více obrázků za účelem generování složeného obrázku pomocí vícevrstvého zobrazovacího modelu MRC (Mixed Raster Content), definovaného v ITU-T T.44 | ISO/IEC 16485.

### Specifikace JPM
Standard formátu souboru JPM specifikuje, že se jedná o binární kontejner reprezentující složený obrázek, pomocí kterého lze spojit více obrázků do jednoho obrázku. Nastavuje mechanismus pro seskupování více obrázků v hierarchii objektů rozložení, stránek a kolekcí stránek pro ukládání JPEG 2000 a dalších komprimovaných formátů obrazových dat. Formát zahrnuje mechanismus začlenění metadat (často označovaných jako strukturální metadata v projektech digitálních knihoven).

## Reference

* [ITU-T Rec. T.805](http://www.itu.int/rec/T-REC-T.805/en)
* [ISO/IEC 15444-6: 2013](http://www.iso.org/iso/home/store/catalogue_ics/catalogue_detail_ics.htm?csnumber=61124)
* [Wikipedia:JPEG 2000](https://en.wikipedia.org/wiki/JPEG_2000)

