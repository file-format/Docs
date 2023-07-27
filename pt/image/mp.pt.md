{
  "date" : "2022-02-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo MP - Arquivo MetaPost LaTeX",
  "description":"Saiba mais sobre o formato de arquivo MP e APIs que podem criar e abrir arquivos MP.",
  "linktitle" : "MP",
  "menu" : {
    "docs" : {
      "identifier":"image-mp",
      "parent" : "image"
}
},
  "lastmod" : "2022-02-23"
}

## O que é um arquivo MP?

Um arquivo MP é um arquivo de imagem vetorial gerado pela linguagem de programação MetaPost para criar imagens. As imagens vetoriais criadas usando o formato de arquivo MP são salvas como arquivos [EPS](/pt/page-description-language/eps/) (Encapsulated PostScript). Além disso, o MetaPost vem distribuído com frameworks TeX e Metafont e arquivos MP podem ser gerados a partir dos arquivos TEX e LTX usados por esses aplicativos. Os arquivos MP contêm instruções de desenho e desenho algorítmico matemático para renderizar o arquivo EPS de saída. O mecanismo PDFTex pode usar o EPS criado para gerar arquivos [PDF](/pt/pdf/) diretamente.

## Formato de arquivo MP

Os arquivos MP são salvos no disco como arquivos binários e geram saída EPS quando exportados para o formato de arquivo de imagem vetorial de saída. Desenhos criados usando MetaPost são incluídos de forma formatada dentro de documentos técnicos e publicações de periódicos criados com LaTex.

### Exemplo de arquivo MP MetaPost

A seguir está um exemplo, referenciado em [Berkeley Eductational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost), que contém uma seta e a letra "A" logo acima do meio do flecha.

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
## Referências ##

* [MetaPost da Wikipedia](https://en.wikipedia.org/wiki/MetaPost)
* [Metapost de amostra de látex por Berkeley Educational Wiki](https://math.berkeley.edu/computing/wiki/index.php/Latex_sample_metapost)

