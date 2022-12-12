{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MP файл – LaTeX MetaPost файл",
  "description":"Научете за MP файловия формат и API, които могат да създават и отварят MP файлове.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Какво е MP файл?

MP файлът е файл с векторно изображение, генериран от програмния език MetaPost за създаване на снимки. Векторни изображения, създадени с MP файлов формат, се записват като [EPS](/bg/image/eps/) (капсулиран PostScript) файлове. Освен това MetaPost се разпространява с рамки TeX и Metafont и MP файлове могат да бъдат генерирани от TEX и LTX файловете, използвани от тези приложения. MP файловете съдържат инструкции за чертане и математически алгоритмичен чертеж за изобразяване на изходния EPS файл. Машината PDFTex може да използва създадения EPS за директно генериране на [PDF](/bg/pdf/) файлове.

## MP файлов формат

MP файловете се записват на диск като двоични файлове и генерират EPS изход, когато се експортират във формат на изходен файл с векторно изображение. Чертежи, създадени с помощта на MetaPost, са включени във форматирана форма в технически документи и публикации в списания, създадени с LaTex.

### Пример за MP файл на MetaPost

Следва пример, цитиран от [Berkeley Educatational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), който съдържа стрелка и буквата „A“ точно над средата на стрелка.

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
## Препратки ##

* [MetaPost от Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latex sample Metapost от Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

