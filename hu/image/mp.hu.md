{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP fájl - LaTeX MetaPost fájl",
  "description":"További információ az MP fájlformátumról és az MP-fájlok létrehozására és megnyitására alkalmas API-król.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Mi az MP fájl?

Az MP fájl egy vektorképfájl, amelyet a MetaPost programozási nyelv generál képek létrehozására. Az MP fájlformátummal létrehozott vektorképek [EPS](/hu/image/eps/) (Encapsulated PostScript) fájlként kerülnek mentésre. Ezenkívül a MetaPost TeX és Metafont keretrendszerrel terjeszthető, és MP fájlok generálhatók az alkalmazások által használt TEX és LTX fájlokból. Az MP fájlok rajzi utasításokat és matematikai algoritmikus rajzot tartalmaznak a kimeneti EPS fájl megjelenítéséhez. A PDFTex motor a létrehozott EPS segítségével közvetlenül [PDF](/hu/pdf/) fájlokat generálhat.

## MP fájl formátum

Az MP fájlok bináris fájlokként kerülnek a lemezre, és EPS kimenetet generálnak, amikor vektoros képfájl formátumba exportálják őket. A MetaPost segítségével készített rajzok formázott formában szerepelnek a LaTex-szel készített műszaki dokumentumokban és folyóirat-kiadványokban.

### MetaPost MP fájl példa

Az alábbiakban a [Berkeley Oktatási Wiki]-ből (https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost) hivatkozott példa látható, amely egy nyilat és egy „A” betűt tartalmaz közvetlenül a lap közepe fölött. nyíl.

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
## Hivatkozások ##

* [MetaPost a Wikipedia által](https://en.wikipedia.org/wiki/MetaPost)
* [Latex minta metaposta a Berkeley Educational Wikitől](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

