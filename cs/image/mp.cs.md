{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP File - LaTeX MetaPost File",
  "description":"Další informace o formátu souborů MP a rozhraních API, která mohou vytvářet a otevírat soubory MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Co je soubor MP?

Soubor MP je soubor vektorového obrázku generovaný programovacím jazykem MetaPost pro vytváření obrázků. Vektorové obrázky vytvořené pomocí formátu MP se ukládají jako soubory [EPS](/cs/page-description-language/eps/) (Encapsulated PostScript). Kromě toho je MetaPost distribuován s rámci TeX a Metafont a soubory MP lze generovat ze souborů TEX a LTX používaných těmito aplikacemi. Soubory MP obsahují příkazy výkresu a matematický algoritmický výkres pro vykreslení výstupního souboru EPS. PDFTex engine může použít vytvořený EPS k přímému generování [PDF](/cs/pdf/) souborů.

## Formát souboru MP

Soubory MP se ukládají na disk jako binární soubory a při exportu do formátu výstupního vektorového obrázku generují výstup EPS. Výkresy vytvořené pomocí MetaPost jsou zahrnuty ve formátované podobě do technických dokumentů a časopiseckých publikací vytvořených pomocí LaTex.

### Příklad souboru MP MetaPost

Následuje příklad odkazovaný z [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), který obsahuje šipku a písmeno „A“ těsně nad středem šipka.

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
## Reference ##

* [MetaPost od Wikipedie](https://en.wikipedia.org/wiki/MetaPost)
* [Latexový ukázkový Metapost od Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

