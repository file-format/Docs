{
  "date" : "2020-01-10",
  "keywords" :[ "cd", ".cd", "o que é um arquivo cd", "como abrir um arquivo cd", "extensão", "arquivo", "arquivo cd", "formato de arquivo cd", "extensão de arquivo cd" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CD - Arquivo de diagrama de classe do Visual Studio",
  "description":"Saiba mais sobre o formato de arquivo de CD e APIs que podem criar e abrir arquivos de CD.",
  "linktitle" : "CD",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-24"
}

## O que é um arquivo de CD?

Um arquivo com extensão .cd é um arquivo de diagrama de classes do Visual Studio que fornece informações sobre a estrutura e o relacionamento entre todas as classes na solução atual. Uma solução do Visual Studio (representada por [.sln](/pt/programming/sln/)) pode conter um ou mais projetos, cada um com várias classes diferentes. O arquivo de diagrama de classes pode ser gerado clicando com o botão direito do mouse no projeto e selecionando a opção de diagrama de classes.

## Formato de arquivo de diagrama de classe (.cd) - Mais informações

Um arquivo de diagrama de classe é salvo no formato de arquivo XML padrão que representa classes em um projeto como nós XML. Se o Visual Studio não estiver disponível, esses arquivos de diagrama de classe podem ser abertos em qualquer programa de aplicativo que suporte a abertura de arquivos XML.

### Como adicionar diagramas de classe ao projeto do Visual Studio

No Visual Studio, abra a Solução/Projeto ao qual você deseja adicionar o diagrama de classes. Em seguida, clique com o botão direito do mouse no nó do projeto e escolha Adicionar > Novo item. Ou pressione Ctrl+Shift+A.

* A caixa de diálogo Adicionar novo item é aberta.

* Expanda Itens Comuns > Geral e selecione Diagrama de Classes na lista de modelos. Para projetos do Visual C++, procure na categoria Utilitário para localizar o modelo de diagrama de classe.

### Exportar diagramas de classe (CD) para imagens

O Visual Studio permite converter/exportar diagramas de classe para imagens como [PNG](/pt/image/png/), [JPEG](/pt/image/jpeg/) e [BMP](/pt/image/bmp/). Esses arquivos de diagrama de classe exportados podem ser usados para fins de registro de documentação e pacote de dados técnicos (TDP). Para converter um diagrama de classe em imagem, as etapas a seguir podem ser usadas no Microsoft Visual Studio.

1. Abra o arquivo de diagrama de classes (.cd).
1. No menu Class Diagram ou no menu de atalho da superfície do diagrama, escolha Export Diagram as Image.
1. Selecione um diagrama.
1. Selecione o formato desejado.
1. Escolha Exportar para finalizar a exportação.

## Referências

* [Aulas de design no Visual Studio](https://docs.microsoft.com/en-us/visualstudio/ide/class-designer/designing-and-viewing-classes-and-types?view=vs-2019)

