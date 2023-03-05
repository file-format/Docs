{
  "date" : "2019-10-11",
  "keywords" :[ "soubor mng", "formát souboru mng", "co je soubor mng", "soubor", "příklad mng", "přípona souboru mng", "přípona", "formát" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formát souboru MNG - formát souboru síťové grafiky s více obrázky",
  "description":"Další informace o formátu souboru MNG a rozhraních API, která mohou vytvářet a otevírat soubory MNG.",
  "linktitle" : "MNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## Co je soubor MNG?

Soubor s příponou .mng je formát souboru Multiple-image Network Graphics, který je podobný obrázkovému formátu [PNG](/cs/image/png/), ale podporuje animované obrázky. Byl vyvinut, aby se zabránilo přetížení formátu PNG dalšími funkcemi animací. MNG je také podobný souborům [GIF](/cs/image/gif/), ale používá větší kompresi a podporuje plnou funkci alfa. Neoficiální typ média MIME pro soubory MNG je video/x-mng. Soubory MNG lze otevřít v aplikacích jako ImageMagik a IrfanView.

## Formát souboru MNG

Formát souboru MNG je podobný formátu PNG a používá stejnou strukturu chunků, jak je definována ve specifikacích PNG. Dekodér MNG musí být schopen dekódovat datové toky PNG bez specifikování jakýchkoli speciálních příznaků pro instrukce dekódování. MNG seskupuje více obrázků dohromady do „rámečku“, přičemž některé obrázky se používají jako sprite pro přesun z jednoho místa na druhé. Mechanismus umožňuje opakované použití obrazových dat bez jejich opětovného přenosu. Pro vývojáře lze odkazovat na [specifikace MNG](http://www.libpng.org/pub/mng/spec/).

### Podpis MNG

Datový tok MNG začíná 8bajtovým podpisem obsahujícím:

```
138  77  78  71  13  10  26  10  - (decimal)
8a  4d  4e  47  0d  0a  1a  0a   - (hexadecimal)
\212   M   N   G  \r  \n \032 \n - (ASCII C notation)
```

To je podobné podpisu PNG, ale místo PNG obsahuje MNG.

### Rám MNG

Rám MNG se skládá z dvourozměrného obrazu menších obrázků. Ke každému malému obrázku lze přistupovat pomocí kombinace indexu řádků a sloupců. Formát je schopen ukládat trojrozměrná „voxelová“ data, která jsou uspořádána do řady dvourozměrných rovin. Každá rovina je reprezentována datovým tokem PNG nebo Delta-PNG. Každý datový tok Delta-PNG definuje obrázek jako rozdíly od nadřazeného obrázku PNG. To poskytuje mnohem kompaktnější způsob reprezentace následujících obrázků než použití úplného datového toku PNG pro každý z nich.

## Reference ##

* [MNG](http://www.libpng.org/pub/mng/)
* [Formát MNG v 1.0](http://www.libpng.org/pub/mng/spec/)

