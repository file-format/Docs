{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Plik MP - Plik LaTeX MetaPost",
  "description":"Poznaj format plików MP i interfejsy API, które mogą tworzyć i otwierać pliki MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## Czym jest plik MP?

Plik MP to plik obrazu wektorowego generowany przez język programowania MetaPost do tworzenia obrazów. Obrazy wektorowe utworzone w formacie plików MP są zapisywane jako pliki [EPS](/pl/page-description-language/eps/) (Encapsulated PostScript). Ponadto MetaPost jest dystrybuowany z frameworkami TeX i Metafont, a pliki MP można generować z plików TEX i LTX używanych przez te aplikacje. Pliki MP zawierają instrukcje rysunkowe i matematyczny rysunek algorytmiczny do renderowania wyjściowego pliku EPS. Silnik PDFTex może wykorzystywać utworzony plik EPS do bezpośredniego generowania plików [PDF](/pl/pdf/).

## Format pliku MP

Pliki MP są zapisywane na dysku jako pliki binarne i generują dane wyjściowe EPS po wyeksportowaniu do wyjściowego formatu pliku obrazu wektorowego. Rysunki utworzone za pomocą MetaPost są dołączane w sformatowanej formie do dokumentów technicznych i publikacji w czasopismach utworzonych za pomocą LaTex.

### Przykład pliku MetaPost MP

Poniżej znajduje się przykład, do którego odwołuje się [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), który zawiera strzałkę i literę „A” tuż nad środkiem strzałka.

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
## Bibliografia ##

* [MetaPost z Wikipedii](https://en.wikipedia.org/wiki/MetaPost)
* [Próbka lateksu Metapost autorstwa Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

