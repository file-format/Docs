{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo obj", "formato de arquivo obj", "o que é um arquivo obj", "arquivo", "exemplo obj", "extensão de arquivo obj", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo OBJ",
  "description":"Saiba mais sobre o formato de arquivo OBJ e APIs que podem abrir e criar arquivos OBJ.",
  "linktitle" : "OBJ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo OBJ?

Os arquivos **OBJ** são usados pelo aplicativo Visualizador Avançado do Wavefront para definir e armazenar os objetos geométricos. A transmissão para trás e para frente de dados geométricos é possível através de arquivos OBJ. Tanto a geometria poligonal como pontos, linhas, vértices de textura, faces e geometria de forma livre (curvas e superfícies) são suportadas pelo formato OBJ. Este formato não suporta animação ou informações relacionadas à luz e posição das cenas.

Um arquivo OBJ geralmente é um produto final do processo de modelagem 3D gerado por um CAD (Computer Aided Design). A ordem padrão para armazenar vértices é no sentido anti-horário, evitando a declaração explícita de normais de face. Embora os arquivos OBJ declarem informações de escala em uma linha de comentário, nenhuma unidade foi declarada para as coordenadas OBJ.

## História do formato 3D OBJ

A Wavefront Technologies criou o formato de arquivo OBJ para seu aplicativo Advanced Visualizer para armazenar objetos geométricos e dados 3D. Sua versão 2.11 foi substituída por uma versão 3 recentemente documentada. O formato de arquivo é aberto e foi implementado por outros fornecedores para seus aplicativos gráficos 3D. A Wavefront Technologies manteve esse formato de arquivo de código aberto e neutro.

## Formato de arquivo OBJ

Em objetos 3D, codificar a geometria da superfície é um trabalho desafiador que o formato de arquivo OBJ realizou muito bem. Este formato é bastante versátil, pois oferece várias opções para codificar a geometria da superfície. A seguir estão três formatos permitidos com seus próprios benefícios e deficiências:

### Tesselação com faces poligonais

O formato de arquivo OBJ facilita ao usuário a tesselação de uma superfície de modelo 3D usando formas geométricas simples ou complexas. Para codificação de geometria de superfície de um modelo, um arquivo armazena os vértices e a normal para cada polígono. Embora a tesselação aumente a grosseria do modelo, ainda é necessário descobrir o equilíbrio correto entre o tamanho de um arquivo e sua qualidade de impressão.

### Curva de forma livre

O formato de arquivo OBJ permite que as curvas de superfície de forma livre definidas pelo usuário especifiquem a geometria da superfície de um modelo. Como as curvas de forma livre são mais complexas que as faces poligonais, com poucos parâmetros matemáticos, as linhas curvas podem ser melhor definidas por curvas de forma livre. Portanto, com menos dados em comparação com mosaicos poligonais, curvas de forma livre usadas para gerar uma codificação de alta qualidade de qualquer modelo 3D sem expandir o tamanho do arquivo.

### Superfícies de forma livre

O formato de arquivo OBJ também especifica a disposição lado a lado da geometria da superfície com patches de superfície de forma livre. Este tipo de remendos de superfície de forma livre (NURBS) é muito adequado para superfícies sem dimensões radiais rígidas como a carroceria de um caminhão, as asas de um helicóptero ou o casco de um barco. O uso de superfícies de forma livre é muito vantajoso, pois são mais precisos para manter tamanhos de arquivo menores com maior precisão. Essas superfícies são parte essencial da indústria aeroespacial e automotiva, onde a baixa precisão é implacável.

As palavras-chave a seguir são organizadas por tipo de dados para definir a geometria da superfície.


|Elementos|Declarações de corpo de superfície/curva de forma livre|Atributos de curva/superfície de forma livre
---|---|---|
|p|Ponto|parm|Valores dos parâmetros|graus|Grau
|l|Linha|trim|Loop de corte externo|bmat|Matriz de base
|f|Face|furo|Loop de corte interno|passo|Tamanho do passo
|curv|Curve|scrv|Special curve|cstype|Curva ou tipo de superfície
|curv2|curva 2D|sp|Ponto especial|**Conectividade e agrupamento de superfícies**
|surf|Surface|end|End statement|con|connect
|**Atributos de exibição/renderização**|g|Nome do grupo
|chanfrado|Interpolação de chanfro|shadow_obj|Shadow casting|s|Smoothing group
|lod|Nível de detalhe|trace_obj|Ray tracing|mg|Mesclar grupo
|d_interp|Dissolver interpolação|ctech|Técnica de aproximação de curva|o|Nome do objeto
|c_interp|Interpolação de cores|stech|Técnica de aproximação de superfície|
|usemtl|Nome do material|mtllib|Biblioteca de materiais|
|**Vértices geométricos**|
|v|Vértices geométricos|vn|Normais de vértice|
|vt|Vértices de textura|vp|Vértices do espaço de parâmetros|

### Cor e textura

O arquivo OBJ permite que informações de cor e textura sejam armazenadas em um formato de arquivo associado chamado Material Template Library (MTL). Modelos geométricos multicoloridos são renderizados usando esses dois arquivos juntos. Os arquivos MTL são baseados em ASCII e facilitam a renderização por computador, descrevendo as propriedades refletoras de luz de uma superfície usando o modelo de reflexão Phong. O padrão foi adotado por um grande número de fornecedores de software que se beneficiam do intercâmbio de materiais. O formato MTL está um pouco desatualizado por não ter suporte em tecnologias mais recentes, como mapas especulares e parallax.

## Referências

* [arquivo .obj do Wavefront](https://en.wikipedia.org/wiki/Wavefront_.obj_file)

