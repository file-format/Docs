{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "HDR failas – ESRI BIL antraštės failo formatas",
  "description":"Kas yra HDR failas?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr-lt",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## Kas yra HDR failas?

HDR failas yra GIS antraštės failas, kuriame yra juostos interleaved by line (.BIL) failo antraštės informacija. Jis apibūdina vaizdo duomenis ir turi tokį patį pavadinimą kaip ir vaizdo failo. HDR failą sudaro įrašų rinkinys, kurių kiekvienas apibūdina tam tikrą vaizdo atributą. HDR faile aprašomas BIL failo išdėstymas ir formatavimas, kad būtų galima išversti į realias koordinates kartu su atskiru geografinės nuorodos failu.

## HDR failo formatas

HDR failai išsaugomi ASCII tekstinio failo formatu. Jame yra įrašų rinkinys, kuriame kiekvienas įrašas apibūdina tam tikrą vaizdo atributą. Kiekvienas HDR failas turi tokį formatą:

```
<keyword> <value>
```

`<keyword> ` – nurodo konkretų atributą, kuris yra nustatomas
`<value> ` – tai reikšmė, kuriai nustatomas atributas

Įrašų tvarka antraštėje nėra ribojama. Tačiau kiekvienas įrašas turi būti atskiroje eilutės eilutėje, kad atitiktų HDR skaitytuvų naudojamą analizavimo metodą.

## Raktinių žodžių, naudojamų HDR faile, santrauka

|Raktinis žodis |Priimtina reikšmė |Numatytasis|
---|---|---|
|nrows |bet koks sveikasis skaičius > 0| nė vienas
|ncols |bet koks sveikasis skaičius > 0| nė vienas
|nbands |bet koks sveikasis skaičius > 0| 1
|nbitai |1, 4, 8, 16, 32| 8
|baitų tvarka| I = Intel;M = Motorola |tas pats kaip pagrindinis įrenginys|
|išdėstymas| bil, bip, bsq| bil|
|praleisti baitus| bet koks sveikasis skaičius ≥ 0| 0
|ulxmap |bet koks realusis skaičius| 0|
|ulymap |bet koks realusis skaičius |eilutės - 1|
|xdim |bet koks tikrasis skaičius| 1
|ydim |bet koks realusis skaičius| 1
|bandrowbytes |bet koks sveikasis skaičius > 0| mažiausias sveikasis skaičius ≥ (ncols x nbits) / 8|
|viso baitų |bet koks sveikasis skaičius > 0| bil: n juostos x juostos baitai; bip: mažiausias sveikasis skaičius ≥ (ncols x nbands x nbits) / 8|
|bandgapbaitai |bet koks sveikasis skaičius ≥ 0| 0|

## Nuorodos

* [HRD failo formatas – ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)


