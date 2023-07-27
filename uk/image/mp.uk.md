{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Файл MP - файл LaTeX MetaPost",
  "description":"Дізнайтеся про формат файлу MP та API, які можуть створювати та відкривати файли MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Що таке файл MP?

MP-файл — це векторний файл зображення, створений мовою програмування MetaPost для створення зображень. Векторні зображення, створені у форматі MP, зберігаються як файли [EPS](/uk/page-description-language/eps/) (Encapsulated PostScript). Крім того, MetaPost постачається разом із фреймворками TeX і Metafont, а файли MP можна генерувати з файлів TEX і LTX, які використовуються цими програмами. MP-файли містять оператори креслення та математичне алгоритмічне креслення для відтворення вихідного файлу EPS. Механізм PDFTex може використовувати створений EPS для безпосереднього створення файлів [PDF](/uk/pdf/).

## Формат файлу MP

MP-файли зберігаються на диску як двійкові файли та генерують вихід EPS під час експорту у вихідний формат файлу векторного зображення. Малюнки, створені за допомогою MetaPost, включені у відформатовану форму в технічні документи та публікації журналів, створені за допомогою LaTex.

### Приклад файлу MetaPost MP

Нижче наведено приклад із посиланням на [Berkeley Educatational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), який містить стрілку та літеру «A» трохи вище середини стрілка.

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
## Посилання ##

* [MetaPost від Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Latex sample Metapost by Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

