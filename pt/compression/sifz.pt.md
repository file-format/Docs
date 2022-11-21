{
  "date" : "2021-04-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo SIFZ - Arquivo de projeto compactado do Synfig Studio",
  "description":"Saiba mais sobre o formato de arquivo SIFZ e APIs que podem criar e abrir arquivos SIFZ.",
  "linktitle" : "SIFZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-30"
}

## O que é um arquivo SIFZ?

Um arquivo SIFZ é um arquivo SIF compactado com gzip criado pelo aplicativo de criação de animações 2D de código aberto **Synfig Studio**. Ele contém vários elementos gráficos que compõem a animação. O conteúdo geral da animação é construído usando uma combinação de uma tela preenchida com formas, pinceladas ou pinceladas e texto. Todos estes são organizados em suas próprias posições, raio, tangente, ângulo, vértice e alças de largura. Os arquivos SIFZ podem ser abertos com o [Synfig Studio](https://www.synfig.org/).

## Formato de arquivo SIFZ

Os arquivos SIFZ são arquivos compactados [ZIP](/pt/compression/zip/) que são empacotados usando o método de compactação gzip. Synfig é usado para criar animações com qualidade de filme usando uma arte vetorial e bitmap. Ao contrário do antigo método de criação de animação quadro a quadro, ele permite produzir animações 2D de maior qualidade com menos recursos.

Os arquivos SIFZ, sendo compactados, são menores que os arquivos SIF não compactados. Isso também facilita a transferência em conexões de internet de baixa largura de banda.

## Referências

* [Synfig Open Source - Github](https://github.com/synfig/synfig/)
* [Documentação Synfig](https://synfig.readthedocs.io/en/latest/index.html)

