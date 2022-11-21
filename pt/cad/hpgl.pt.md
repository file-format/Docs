{
  "date" : "2020-07-28",
  "keywords" :[ "HPGL", "Formato de arquivo", "Abrir", "Ler", "Criar", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo HPGL e APIs que podem criar e abrir arquivos HPGL.",
  "title" :"Formato de arquivo HPGL - Aprenda com especialistas em formato de arquivo!",
  "linktitle" : "HPGL",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## O que é um arquivo HPGL?

Um arquivo HPGFL (Hewlett-Packard Graphics Language) contém um conjunto de instruções para controle de plotadora desenvolvido pela HP. As plotadoras HP usam esse arquivo para desenhar e imprimir conteúdo vetorial e raster no papel.

### Comando HPGL

Um comando HPGL consiste no seguinte.
* Uma seção de comando do alfabeto de dois caracteres
* Uma seção de parâmetros
* Seção do Exterminador

Cada parâmetro no arquivo deve ser dividido com um separador no caso de vários parâmetros.

### Exemplo de comando HPGL

```
Example :PA5000,1000;
  (command)    PA
  (parameter)  5000
  (separator)  ,
  (parameter)  1000
  (terminator) ;
```

### Sistema de coordenadas

Os sistemas de coordenadas são compostos por indicadores de medição bidimensionais para localizar qualquer local específico. O HPGL usa tanto as coordenadas da plotadora quanto o sistema de coordenadas do usuário para esta finalidade.

#### Sistema de coordenadas da plotadora

Este sistema de coordenadas é usado para plotar desenhos com base no movimento da plotadora. Uma unidade XY típica de movimento mínimo do plotter é 0,025 mm. A gama possível de alterações de desenho com tipos de plotadoras.

#### Sistema de coordenadas do usuário

O sistema de coordenadas especificado pelo usuário pode ser configurado usando a escala e a origem. Estes são convertidos em coordenadas da plotadora usando o comando IP e o comando SC. As coordenadas do sistema da plotadora são usadas por padrão se esta conversão não for realizada.

## Formato de arquivo HPGL
Os arquivos HPGL estão no formato ASCII (arquivo de texto) e começam com alguns comandos de configuração. Isso configura certos parâmetros para o plotter para plotagem. Um arquivo HPGL típico tem a seguinte aparência.

|Comando|Significado
---|---|
|IN;|inicializar, iniciar um trabalho de plotagem|
|IP;|defina os pontos de escala (P1 e P2) para suas posições padrão|
|SP1;|selecione a caneta 1|
|PU0,0;|levante a caneta para cima e mova para o ponto de partida para a próxima ação|
|PD100,0,100,100,0,100,0,0;|coloque a caneta para baixo e mova para os seguintes locais (desenhe uma caixa ao redor da página)|
|PU50,50;|Pen Up e mova para as coordenadas X,Y 50,50|
|CI25;|desenhe um círculo com raio 25|
|SS;|selecione o conjunto de caracteres padrão|
|DT*,1;|defina o delimitador de texto para o asterisco, e não os imprima (o 1, significando "verdadeiro")|
|PU20,80;|levante a caneta e vá para 20,80|
|LBHello World*;|desenhe uma etiqueta|

## Referências
* [HPGL pela Wikipedia](https://en.wikipedia.org/wiki/HP-GL)
* [Guia de referência HPGL](https://www.isoplotec.co.jp/HPGL/eHPGL.htm)

