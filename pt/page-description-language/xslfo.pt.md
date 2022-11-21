{
  "date" : "2019-10-11",
  "keywords" :[ "XSLFO", "Objetos de formatação XSL", "Arquivo", "Extensão", "Formato de arquivo", "Linguagem de folha de estilo extensível"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XSLFO",
  "description":"Saiba mais sobre o formato de arquivo XSLFO e APIs que podem criar e abrir arquivos XSLFO.",
  "linktitle" : "XSLFO",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo XSL-FO? ##

XSL-FO (XSL Formatting Objects) é uma poderosa linguagem de folha de estilo para formatação de documentos XML. A semântica da forma limitada de papel e impressão é expressa por XSL-FO quando as dimensões são fixas. Em contraste com o HTML, que representa a semântica da forma ilimitada de uma janela do navegador com dimensões variáveis. Os documentos XML formatados por XSL-FO são usados principalmente para gerar arquivos PDF. XSL (Extensible Stylesheet Language) é um conjunto de tecnologias W3C com recursos completos destinados ao design para formatação e troca de documentos XML e parte XSL-FO dessa linguagem. XSLT e XPath também são outras partes do XSL.

Propõe-se que os documentos XML sejam transformados primeiro em XSL-FO, sendo o PDF um exemplo deste critério. Em PDF, os resultados são renderizados usando XSLT primeiro e depois o formatador XSL-FO. Dessa forma, os documentos XML podem ser formatados aleatoriamente. Embora o XSL-FO tenha a vantagem de usar as propriedades Cascading Style Sheet (CSS) e estendê-las sempre que necessário para o formato real, ele abriga o fornecimento de modelos de página chamados mestres de página na terminologia do XSL-FO. O XSL-FO também fornece formatação para documentos bastante sofisticados e oferece suporte à geração de índice.

## História e Conceitos Básicos ##

Em janeiro de 2012, o Projeto de Trabalho do XSL-FO foi atualizado pela última vez e, em novembro de 2013, seu Grupo de Trabalho foi encerrado. Uma folha de estilo XSL especifica a apresentação de uma classe de documentos XML descrevendo como uma instância da classe é transformada em um documento XML que usa o vocabulário de formatação. XSL-FO é uma linguagem de apresentação integrada e não possui marcações semânticas que são usadas em HTML. Além disso, essa linguagem armazena todos os dados do documento dentro de si mesma, ao contrário do CSS que altera as configurações padrão de um documento HTML ou XML externo.

O critério geral de uso do XSL-FO é que o usuário escreva um documento em uma linguagem XML em vez de escrever em FO. Depois disso, ocorre uma transformação XSLT. Essa transformação XSLT é responsável pela conversão de XML em XSL-FO. Assim que o documento XSL-FO é gerado, ele é então entregue a um aplicativo chamado processador FO. Os processadores FO são responsáveis por transformar este documento em um documento legível e imprimível. Arquivos PDF ou PS são exemplos da saída mais comum do XSL-FO. Mas isso não significa que o processador FO possa produzir apenas esses dois tipos de formato como saída. Alguns processadores FO podem produzir arquivos RTF ou até mesmo uma janela pode aparecer na GUI do usuário, esta janela exibe a sequência da página e seu conteúdo.

Um documento XSL-FO é diferente de um PDF ou PS no sentido em que não define o layout do texto em diferentes páginas. Talvez, estilize as páginas e determine os locais para exibir o conteúdo. Além disso, um processador FO organiza o texto dentro dos limites especificados pelo documento FO. Esta especificação permite até que diferentes processadores FO se comportem de acordo com as páginas criadas resultantes. Um exemplo de tal comportamento é a hifenização, poucos processadores FO podem hifenizar palavras para economizar espaço quando uma linha quebra, enquanto alguns processadores não selecionam esta opção. Depende dos processadores escolher diferentes algoritmos de hifenização que correspondam aos seus requisitos. Esses algoritmos de hifenização podem ser muito simples ou talvez mais complexos. Em algumas situações, a especificação XSL-FO sanciona explicitamente os processadores FO, com algum grau de escolha no contexto do layout.

Essa variação entre os processadores de FO gera resultados variados, sobre os quais os processadores geralmente permanecem despreocupados. Porque o foco geral do XSL-FO é produzir documentos paginados/impressos. Os próprios documentos XSL-FO normalmente atuam como intermediários, sua principal função é gerar arquivos PDF ou um documento que pode ser impresso como saída a ser distribuída. Em HTML/CSS ou XSL-FO, distribuir o PDF como resultado final em vez de inserir a linguagem de formatação indica que os receptores não são afetados pela versatilidade resultante que é produzida devido a diferenças entre os intérpretes da linguagem de formatação. Por outro lado, é evidente que não existe uma maneira fácil de um documento atender às diferentes necessidades dos destinatários, por exemplo, tamanho de página variável ou tamanho de fonte desejado, ou adaptação para página ou impressão.

## Formato de arquivo XSLFO ##

Os documentos SL-FO são basicamente documentos XML, mas não seguem nenhum esquema. Em seu lugar, os documentos SL-FO seguem a sintaxe definida na especificação de sua própria linguagem. Há duas seções necessárias em cada documento XSL-FO:

1. Uma seção que especifica uma lista de layouts de página rotulados.
1. Uma seção com todos os detalhes dos dados do documento, com marcação, que determina a exibição do conteúdo em diferentes páginas através de vários layouts de página.

As propriedades da página são mencionadas nos layouts de página, que podem definir a organização do texto, de acordo com as convenções para o idioma específico. Além disso, o tamanho da página, suas margens e sequências de páginas (que sanciona propriedades diferentes para as páginas ímpares e pares) também são definidos pelos layouts de página.

A parte de dados do documento é dividida em uma série de fluxos, onde cada fluxo é conectado a um layout de página. Os fluxos incluem uma lista de blocos neles. Essa lista de blocos pode conter recursos de marcação em linha ou uma lista de dados de texto, ou talvez ambos ao mesmo tempo. As margens do documento também podem exibir os números das páginas ou os títulos dos capítulos. A funcionalidade de blocos e elementos inline permanece a mesma do CSS, mas algumas regras de preenchimento e margem são diferentes entre FO e CSS.

A direção de orientação da página é totalmente especificada para a extensão de blocos e inlines, fazendo com que os documentos FO funcionem em idiomas diferentes do inglês. A linguagem da especificação FO usa as palavras início e fim em vez de esquerda e direita para a descrição das direções. As regras básicas de marcação e cascata de conteúdo do XSL-FO são extraídas do CSS. A linguagem do XSL-FO está de acordo com as seguintes especificações.

## Várias colunas ##

Uma página pode ter várias colunas e blocos e pode se estender de uma coluna para outra por padrão. Várias páginas podem ter larguras e números de colunas diferentes. Todas as características do FO seguem os limites de uma página com várias colunas.

### Listas ###

Uma lista XSL-FO é estabelecida por dois conjuntos de blocos dispostos lado a lado. Conceitualmente, em uma lista, um bloco à esquerda indica um número, um marcador ou uma sequência de texto, enquanto o bloco do lado direito pode funcionar conforme o previsto. A numeração das listas XSL-FO geralmente é feita pelo XSLT.

### Tabelas ###

Uma tabela FO é semelhante a uma tabela HTML/CSS. O usuário pode selecionar as linhas de dados, informações de estilo, cor de fundo para cada célula individual. Usando informações de estilo distintas, o usuário tem o privilégio de selecionar a primeira linha como uma linha de cabeçalho da tabela. O processador FO pode ser informado explicitamente sobre a especificação de espaço de cada coluna, ou para ajustar automaticamente o texto na tabela.

### Indexação ###

O XSL-FO 1.1 possui recursos que ajudam a gerar um índice referenciando elementos devidamente marcados.

### Benefícios ###

* Apropriado para publicação baseada em conteúdo
* Fácil de usar
* Baixo custo

## Referências ##

* [O que é XSL-FO?](https://www.xml.com/articles/2017/01/01/what-is-xsl-fo/)
* [Objetos de formatação XSL](https://en.wikipedia.org/wiki/XSL_Formatting_Objects)

