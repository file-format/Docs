{
  "date" : "2023-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Archivo HDR: formato de archivo de encabezado ESRI BIL",
  "description":"¿Qué es un archivo HDR?",
  "linktitle" : "HDR",
  "menu" : {
    "docs" : {
      "identifier":"gis-hdr",
      "parent" : "gis"
}
},
  "lastmod" : "2023-01-23"
}

## ¿Qué es un archivo HDR?

Un archivo HDR es un archivo de encabezado SIG que contiene información de encabezado para un archivo de banda intercalada por línea (.BIL). Describe los datos de la imagen y tiene el mismo nombre que el del archivo de imagen. Un archivo HDR se compone de un conjunto de entradas, cada una de las cuales describe un atributo particular de la imagen. El archivo HDR describe el diseño y el formato del archivo BIL para su traducción a coordenadas del mundo real en combinación con un archivo de georreferenciación independiente.

## Formato de archivo HDR

Los archivos HDR se guardan en formato de archivo de texto ASCII. Contiene un conjunto de entradas donde cada entrada describe un atributo particular de la imagen. Cada archivo HDR tiene el siguiente formato:

```
<keyword> <value>
```

`<keyword> ` - Indica el atributo particular que se está configurando.
`<value> ` - Es el valor al que se establece el atributo.

No hay limitación en el orden de las entradas en el encabezado. Sin embargo, cada entrada debe estar en una línea separada para cumplir con el método de análisis utilizado por los lectores HDR.

## Resumen de palabras clave utilizadas en el archivo HDR

|Palabra clave |Valor aceptable |Predeterminado|
---|---|---|
|nrows |cualquier número entero > 0| ninguno
|ncols |cualquier número entero > 0| ninguno
|nbandas |cualquier número entero > 0| 1
|nbits |1, 4, 8, 16, 32| 8
|orden de bytes| I = Intel;M = Motorola |igual que la máquina host|
|diseño| bil, bip, bsq| billete|
|skipbytes| cualquier número entero ≥ 0| 0
|ulxmap |cualquier número real| 0|
|ulymap |cualquier número real |nrows - 1|
|xdim |cualquier número real| 1
|ydim |cualquier número real| 1
|bandrowbytes |cualquier número entero > 0| entero más pequeño ≥ (ncols x nbits) / 8|
|totalrowbytes |cualquier número entero > 0| para bil: nbands x bandrowbytes; para bip: entero más pequeño ≥ (ncols x nbands x nbits) / 8|
|bandgapbytes |cualquier número entero ≥ 0| 0|

## Referencias

* [Formato de archivo HRD - ArcGIS](https://webhelp.esri.com/arcgisdesktop/9.2/index.cfm?TopicName=BIL,_BIP,_and_BSQ_raster_files)

