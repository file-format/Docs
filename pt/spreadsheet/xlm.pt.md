{
  "date" : "2019-12-10",
  "keywords" :[ "XLM", "arquivo", "extensão", "formato de arquivo", "Arquivo de macro do Microsoft Excel", "Planilha" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo de macros XLM e APIs que podem criar e abrir arquivos XLM.",
  "title" :"O que é um arquivo XLM?",
  "linktitle" : "XLM",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo XLM?

XLM, para Excel Macro, é um tipo de arquivo de planilha que é usado para armazenar Macros. Do ponto de vista da aplicação, uma Macro é um conjunto de instruções que são usadas para automatizar processos. Uma macro é usada para registrar as etapas que são executadas repetidamente para o formato de arquivo [XLS](/pt/spreadsheet/xls/) e facilita a execução das ações executando a macro novamente. As macros são programadas com o Visual Basic for Applications (VBA) da Microsoft a partir da pasta de trabalho do Excel usando o Editor do Visual Basic e podem ser executadas/depuradas diretamente de lá.

## Breve história ##

O Microsoft Excel apoiou a programação de macros desde seu primeiro lançamento público. Os recursos das macros permaneceram os mesmos nas versões subsequentes do Excel com extensão conforme novos recursos. XLM era a linguagem de macro padrão para Excel por meio do Excel 4.0. O Excel 5.0 gravou macros no VBA por padrão, mas com a versão 5.0 a gravação XLM ainda era permitida como opção. Após a versão 5.0 essa opção foi descontinuada. Todas as versões do Excel, incluindo o Excel 2010, são capazes de executar uma macro XLM, embora a Microsoft desencoraje seu uso.

## Gravando uma Macro em XLM ##

O Excel fornece etapas fáceis de usar para gravar uma macro. Requer que você tenha as ferramentas do desenvolvedor instaladas para trabalhar com macros. Quando uma gravação de macro está em andamento, ela registra cada ação do usuário para ser reproduzida posteriormente. A gravação de macro, na verdade, envolve todas as etapas que um usuário executa após o início da gravação. Assim, se você colocar o conteúdo de uma célula em negrito, itálico e definir sua justificação de texto após o início de uma gravação de macro, todos esses comandos serão gravados. Cada macro gravada também pode receber um atalho para reprodução rápida mais tarde. A gravação de macro gera código VBA na forma de uma macro que pode ser editada usando o Visual Basic Editor (VBE).

## Modelo de objeto do Excel ##

As macros usam rotinas VBA nas costas e seguem o [Excel Object Model](https://learn.microsoft.com/en-us/office/vba/api/overview/excel/object-model) para essa finalidade. Este modelo identifica os objetos de uma planilha para interação com a planilha por meio de barras de ferramentas de comando definidas pelo usuário, barras de comando ou caixas de mensagens. Por exemplo, o acesso às propriedades da pasta de trabalho é concedido com o objeto Workbook. Da mesma forma, há um objeto Worksheet no modelo para trabalhar com as planilhas da pasta de trabalho programaticamente.

## Macros e Segurança ##

O VBA permite o acesso a todas as áreas de aplicação, bem como ao sistema de arquivos, e também pode ser perigoso. Isso levanta preocupações ao compartilhar a pasta de trabalho com alguém que pode executar o arquivo no final. Ou seja, o Microsoft Excel avisa sobre a abertura de tal arquivo. As macros podem ser certificadas com uma assinatura digital para que outros usuários verifiquem se são confiáveis. Assim, as macros podem ser habilitadas após a verificação de sua origem.

## Referências ##

* [[MS-XLS] - Estrutura de formato de arquivo binário do Excel](https://msdn.microsoft.com/en-us/library/cc313154(v#office.12).aspx)
* [Programação de macros](https://en.wikipedia.org/wiki/Microsoft_Excel#Macro_programming)

