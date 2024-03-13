{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "HDR Faylı - ESRI BIL Başlıq Fayl Formatı",
  "description":"HDR faylı nədir?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-az",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## HDR faylı nədir?

HDR faylı sətir (.BIL) faylı ilə interleaved Band üçün başlıq məlumatını ehtiva edən GIS başlıq faylıdır. O, şəkil məlumatını təsvir edir və şəkil faylı ilə eyni ada malikdir. HDR faylı hər biri təsvirin müəyyən bir atributunu təsvir edən bir sıra qeydlərdən ibarətdir. HDR faylı ayrıca georeferensasiya faylı ilə birlikdə real dünya koordinatlarına tərcümə üçün BIL faylının tərtibatını və formatını təsvir edir.

## HDR Fayl Format

HDR faylları ASCII mətn faylı formatında saxlanılır. Bu, hər bir girişin təsvirin müəyyən bir atributunu təsvir etdiyi bir sıra qeydləri ehtiva edir. Hər bir HDR faylı aşağıdakı formata malikdir:

```
<keyword> <value>
```

`<keyword> ` - Bu təyin olunan xüsusi atributu göstərir
`<value> ` - Bu, atributun təyin olunduğu dəyərdir

Başlıqdakı girişlərin sırasına dair heç bir məhdudiyyət yoxdur. Bununla belə, HDR oxuyucularının istifadə etdiyi təhlil metoduna uyğun olmaq üçün hər bir giriş xəttin ayrıca sətirində olmalıdır.

## HDR faylında istifadə olunan açar sözlərin xülasəsi

|Açar söz |Məqbul dəyər |Defolt|
---|---|---|
|nrows |hər hansı tam> 0| heç biri
|ncols |hər hansı tam ədəd > 0| heç biri
|nbands |hər hansı tam ədəd > 0| 1
|nbitlər |1, 4, 8, 16, 32| 8
|byteorder| I = Intel;M = Motorola |ana maşınla eyni|
|layout| bil, bip, bsq| bil|
|skipbayt| istənilən tam ədəd ≥ 0| 0
|ulxmap |hər hansı real rəqəm| 0|
|ulymap |hər hansı real ədəd |sətirlər - 1|
|xdim |hər hansı real ədəd| 1
|ydim |hər hansı real ədəd| 1
|bandrowbaytlar |hər hansı tam ədəd > 0| ən kiçik tam ədəd ≥ (ncols x nbits) / 8|
|totalrowbayt |hər hansı tam ədəd > 0| bil üçün: nbands x bandrowbayt;bip üçün: ən kiçik tam ədəd ≥ (ncols x nbands x nbits) / 8|
|bandqapbayt |hər hansı tam ədəd ≥ 0| 0|

## İstinadlar

* [HRD Fayl Format - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


