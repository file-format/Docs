{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo xpm", "formato de arquivo xpm", "o que é um arquivo xpm", "arquivo", "exemplo xpm", "extensão de arquivo xpm", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPM - Formato de arquivo X PixMap",
  "description":"Saiba mais sobre o formato de arquivo XPM e APIs que podem criar e abrir arquivos XPM.",
  "linktitle" : "XPM",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo XPM?

Um arquivo com extensão .xpm é um formato de arquivo de imagem que foi usado pelo Sistema X Windows. Ele suporta pixels transparentes e geralmente visa a criação de pixmaps de ícones. Ele suporta dados de pixmap monocromáticos, gra-scale e coloridos. Eles foram projetados para serem editáveis manualmente e podem ser incluídos no código [C](/pt/programming/c/). Para isso, os arquivos XPM estão em formato de arquivo de texto simples e seguem a sintaxe da linguagem de programação C. Os arquivos XPM podem ser abertos com uma variedade de aplicativos de visualização de imagens, como
CorelDRAW Graphics Suite 2020, Corel PaintShop Pro, IrfanView e Canvas X.

## Formato de arquivo XPM

O formato de arquivo XPM usa a sintaxe C para que eles sejam integrados em programas C e C++. Consiste nas seguintes seis seções diferentes.

* \<Values>
* \<Colors>
* \<Pixels>
* \<Extensions>

As seções são na verdade um array de strings como segue.

```
/* XPM */
static char*<variable_name>[] = {
  <Values>
  <Colors>
  <Pixels>
  <Extensions>
};
```
Seguem os detalhes de cada seção.

`<Values> ` - Esta seção é uma string que contém quatro ou seis inteiros que estão na base 10 e correspondem a:

* largura e altura do pixmap
* número de cores
* número de caracteres por pixel
* coordenadas de hotspot opcionais e tag XPMEXT

`<Colors> ` - Esta seção contém tantas strings quanto cores. Cada string é a seguinte:

```
<chars>{<key><color> }+
```
`<Pixels> ` - Esta seção é composta por<height> cordas e<width> \*<chars_per_pixel> personagens. Todo<chars_per_pixel> string de comprimento deve ser um dos grupos definidos anteriormente no<Colors> seção.

`<Extension> ` - A seção de extensão deve ser rotulada, se não estiver vazia, no<Values> seção. Pode consistir em vários<Extension> subseções que podem ser dos dois tipos seguintes:

* uma string independente composta da seguinte forma: XPMEXT<extension-name><extension-data>
* ou um bloco composto por várias strings:XPMEXT<extension-name><related extension-data composed of several strings>

## Referências

* [XPM - Wikipedia](https://en.wikipedia.org/wiki/X_PixMap)
* [Manual XPM](http://www.xfree86.org/current/xpm.pdf)

