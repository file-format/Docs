{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo vrml", "formato de arquivo vrml", "o que é um arquivo vrml", "arquivo", "exemplo vrml", "extensão de arquivo vrml", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo VRML",
  "description":"Saiba mais sobre o formato de arquivo VRML e APIs que podem abrir e criar arquivos VRML.",
  "linktitle" : "VRML",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo VRML?
A Linguagem de Modelagem de Realidade Virtual (VRML) é um formato de arquivo para representação de objetos do mundo interativos [3D](/pt/3d/) na World Wide Web (www). Ele encontra seu uso na criação de representações tridimensionais de cenas complexas, como ilustrações, definições e apresentações de realidade virtual. O formato foi substituído por [X3D](/pt/3d/x3d/). Muitos aplicativos de modelagem 3D podem salvar objetos e cenas no formato VRML.

## Formato de arquivo VRML

VRML é um formato de arquivo de texto que especifica informações como vértices e arestas de um polígono 3D juntamente com informações como cor da superfície, texturas mapeadas por UV, brilho, transparência e assim por diante. Ele tem a capacidade de representar objetos estáticos e animados, além de ter hiperlinks para outras mídias, como som, filmes e imagens. Isso permite abrir elementos com hiperlinks quando o usuário clica nesses objetos.

Os arquivos TVRML na terminologia comum são chamados de "mundos" e têm a extensão .wrl. A natureza textual desses arquivos permite reduzir o tamanho do arquivo usando formatos de compactação como gzip, tornando-os mais favoráveis para transferência rápida pela internet. As especificações de formato de arquivo para [VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html) funcionam como referência do desenvolvedor para a criação de aplicativos compatíveis para leitura/gravação desses arquivos.

## Critério de projeto ##

O objetivo e o design do VRML giram em torno dos seguintes requisitos.

* **Autorabilidade** - Possibilita desenvolver geradores e editores de aplicativos e importar dados de outros formatos industriais
* **Completeness** - Fornece todas as informações necessárias para implementação e aborda um conjunto completo de recursos para ampla aceitação do setor
* **Composabilidade** - A capacidade de usar elementos de VRML em combinação e, assim, permitir a reutilização.
* **Extensibilidade** - A capacidade de adicionar novos elementos.
* **Implementação** -Capaz de implementação em uma ampla gama de sistemas.
* **Potencial multiusuário** - Não deve impedir a implementação de ambientes multiusuário.
* **Ortogonalidade** - Os elementos do VRML devem ser independentes entre si, ou seja, quaisquer dependências devem ser estruturadas e bem definidas.
* **Desempenho** - Os elementos devem ser projetados com ênfase no desempenho interativo em uma variedade de plataformas de computação.
* **Escalabilidade** - Os elementos de VRML devem ser projetados para composições infinitamente grandes.
* **Prática padrão** - Apenas os elementos que refletem a prática existente, que são necessários para apoiar a prática existente, ou que são necessários para apoiar os padrões propostos devem ser padronizados.
* **Bem estruturado** - Um elemento deve ter uma interface bem definida e um propósito incondicional simplesmente declarado. Elementos multiuso e efeitos colaterais devem ser evitados.

## Referências ##

* [VRML - Por Wikipedia](https://en.wikipedia.org/wiki/VRML)
* [Especificações do formato de arquivo VRML v 2.0](http://gun.teipir.gr/VRML-amgem/spec/index.html)

