{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP-fil - LaTeX MetaPost-fil",
  "description":"Läs mer om MP-filformat och API:er som kan skapa och öppna MP-filer.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Vad är en MP fil?

En MP-fil är en vektorbildfil som genereras av MetaPosts programmeringsspråk för att skapa bilder. Vektorbilder skapade med MP-filformat sparas som [EPS](/sv/page-description-language/eps/) (Encapsulated PostScript)-filer. Dessutom kommer MetaPost distribueras med TeX- och Metafont-ramverk och MP-filer kan genereras från TEX- och LTX-filerna som används av dessa applikationer. MP-filer innehåller ritningssatser och matematisk algoritmisk ritning för att återge den utgående EPS-filen. PDFTex-motorn kan använda den skapade EPS för att generera [PDF](/sv/pdf/)-filer direkt.

## MP filformat

MP-filer sparas på skivan som binära filer och genererar EPS-utdata när de exporteras till utdatavektorbildfilformat. Ritningar skapade med MetaPost ingår i formaterad form i tekniska dokument och tidskriftspublikationer skapade med LaTex.

### Exempel på MetaPost MP-fil

Följande är ett exempel, refererat från [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), som innehåller en pil och bokstaven "A" strax ovanför mitten av pil.

```
outputtemplate:="%j%c.mps";
beginfig(1);

z1=(0,0);
z2=(10mm,10mm);

drawarrow(z1--z2);
label.ulft(btex $A$ etex, .5[z1,z2]);

endfig;

bye
```
## Referenser ##

* [MetaPost av Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latexexempel Metapost av Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

