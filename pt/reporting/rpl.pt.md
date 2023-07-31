{
  "date" : "2021-03-02",
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RPL - Layout da página do relatório",
  "keywords" :[ "rpl", "Layout de página de relatório", "XSD", "SQL Server", "relatório"],
  "description":"Saiba mais sobre o formato de fluxo RPL, que é um formato binário interno usado pelo Microsoft SQL Server Reporting Services ao entrar em contato com os controles do visualizador.",
  "linktitle" : "RPL",
  "menu" : {
    "docs" : {
      "parent" : "reporting"
}
},
  "lastmod" : "2021-03-02"
}

## O que é um arquivo RPL? ##

O formato de fluxo RPL (Layout de página de relatório) é um formato binário interno usado pelo MS SQL Server Reporting Services ao entrar em contato com controles de visualizador para reduzir parte do trabalho de renderização do servidor para o controle de visualizador de cliente. Os desenvolvedores podem criar designers de relatórios personalizados usando RPL, que irá gerar RPL, bem como renderizadores de relatórios personalizados que processam e exibem o arquivo RPL para exibir relatórios.

## Estruturas RPL

Um fluxo RPL inclui estrutura de fluxo, estrutura de relatório, propriedades de relatório e enumerações. Cada estrutura inclui o seguinte:

- Uma definição da estrutura.

- A gramática Augmented Backus-Naur Form (ABNF) para a estrutura.

- Um diagrama de bits da estrutura.

- Definições de todos os campos contidos na estrutura.

Aqui estão as breves notas sobre algumas das Estruturas RPL:

### Estrutura de fluxo
A estrutura de fluxo consiste em uma série de registros. Um registro contém zero ou mais campos estruturados que contêm o layout do relatório.

#### Fluxo RPL
O fluxo RPL deve ter apenas um registro de Relatório e o fluxo deve ser uma série de registros binários que mantêm a hierarquia do relatório.

#### Registro
O registro é um bloco de construção básico usado para manter as informações sobre um relatório. Um registro consiste em uma sequência de bytes de comprimento variável. Um registro consiste em dois componentes:
- Um tipo de registro
- Os dados de registro específicos desse tipo de registro.
O tipo de registro é um byte que define que tipo de informação é especificada pelo registro e como a estrutura dos dados do registro referente ao registro é ordenada e estruturada. O valor do registro depende do tipo de dados específico desse registro.

#### Estruturas de tipo de dados simples

A tabela a seguir define os tipos de dados em um fluxo RPL.

|Descrição| formato|
---|---|
|Char|Representa um valor numérico (ordinal) de 16 bits (2 bytes).|
|Byte|Representa um inteiro sem sinal de 8 bits (1 byte).|
|Int16|Representa um inteiro assinado de 16 bits (2 bytes).|
|Single|Representa um valor de ponto flutuante de precisão simples de 32 bits (4 bytes).|
|Decimal|Representa um tipo de dados de 128 bits (16 bytes).|
|DateTime|Representa uma codificação de 64 bits (8 bytes) de um valor de data e hora.|
|Int64|Representa um inteiro assinado de 64 bits (8 bytes).|
|Int32|Representa um inteiro assinado de 32 bits (4 bytes).|
|Float|Representa um valor de ponto flutuante de precisão simples de 32 bits (4 bytes).|
|Boolean|Representa um valor de tipo booleano lógico de 8 bits (1 byte). Os valores válidos são true (1) e false (0).|
|Long|Representa um inteiro assinado de 64 bits (8 bytes).|
|String|Todos os valores de String dentro do protocolo DEVEM ser UNICODE UTF-16. Por padrão, todos os valores de String começam com um inteiro que define o comprimento da String. Os valores de string são representados no protocolo como uma matriz de bytes; o número de bytes DEVE ser igual ao número de caracteres na String multiplicado por dois.|

### Estruturas de relatórios
As estruturas do relatório incluem as definições e tamanhos de suas estruturas e elementos relevantes.

A lista a seguir especifica as estruturas do relatório:

- Relatório
- Versão
- Propriedades do relatório
- Elemento de matriz de deslocamento
- Conteúdo da página
- Página
- Propriedades da página
- Layout da página
- Seção
- Seção Simples
- Seção Mista
- Propriedades da Seção
- Elemento da área do corpo
- Elemento do cabeçalho da página
- Elemento de rodapé de página
- Elemento do corpo
- Propriedades do elemento
- Propriedades do Elemento Compartilhado
- Usar Propriedades do Elemento Compartilhado
- InlineSharedElementProperties
- NonSharedElementProperties
- Estilo
- Propriedades de Estilo Compartilhado
- Propriedades Não Compartilhadas
- ActionInfo
- ActionInfoContent
- Ação
- ActionImageMapAreas
- ActionInfoWithMaps
- DynamicImageData
- ImageConsolidationOffsets
- Item de relatorio
- Linha
- Imagem
- ImageDataProperties
- UseSharedImageDataProperties
- InlineSharedImageDataProperties
- NonSharedImageDataProperties
- ImageData
- ImageMapAreas
- ImageMapArea
- Gráfico
- GaugePanel
- Mapa
- Retângulo
- Sub-relatório
- RichTextBox
- Parágrafo Conteúdo
- TextRun
- Parágrafo
- RichTextBoxStructure
- Tablix
- Conteúdo Tablix
- TablixEstrutura
- TablixMedições
- ColumnsWidths
- ColumnInfo
- RowHeights
- RowInfo
- TablixRow
- TablixRowCell
- TablixCorner
- TablixColumnHeader
- TablixRowHeader
- TablixBodyRowCells
- TablixBodyRow
- TablixBodyCell
- TablixRowMembersDef
- TablixColMembersDef
- TablixMemberDef
- Medidas
- Medição
- ReportElementEnd

### Propriedades
A seguir está a lista de propriedades que podem ser usadas em um RPL Stream:

- EU IRIA
- ColumnCount
- Espaçamento entre colunas
- Nome único
- Nome
- Etiqueta
- Marca páginas
- Dica de ferramenta
- Alternar Item
- Descrição
- Localização
- ConsumeContainerWhiteSpace (RPL 10.6)
- Linguagem
- Tempo de execução
- Autor
- Atualização automática
- ReportName
- Altura da página
- Largura da página
- MargemTopo
- Margem Esquerda
- Margem Direita
- MargemInferior
- Colunas
- PageName (RPL 10.6)
- Inclinação
- Pode crescer
- Pode Encolher
- Valor
- ToggleState
- Pode Classificar
- SortState
- Fórmula
- IsToggleParent
- Código de Tipo
- Valor original
- É simples
- ContentOffset
- StreamName
- Dimensionamento
- LinkToChild
- Imprimir na primeira página
- Imprimir entre seções (RPL 10.4)
- FormattedValueExpressionBased
- Processado com erro
- ImageMIMEType
- Nome da imagem
- Largura
- Altura
- Resolução horizontal
- Resolução Vertical
- Formato bruto
- Hiperlink
- FavoritoLink
- DrillthroughId
- DrillthroughUrl
- Cor da borda
- BorderColorLeft
- BorderColorRight
- BorderColorTop
- BorderColorBottom
- Estilo de borda
- BorderStyleLeft
- BorderStyleRight
- BorderStyleTop
- BorderStyleBottom
- Largura da Borda
- BorderWidthLeft
- BorderWidthRight
- BorderWidthTop
- BorderWidthBottom
- Preenchimento Esquerdo
- Preenchimento Direita
- AcolchoamentoTopo
- Acolchoamento Inferior
- Estilo de fonte
- Família de fontes
- Tamanho da fonte
- Espessura da fonte
- Formato
- TextoDecoração
- Alinhamento de texto
- VerticalAlign
- Cor
- Altura da linha
- Direção
- Modo de Escrita
- Unicode BiDi
- Imagem de fundo
- Cor de fundo
- Fundo de repetição
- NumeralIdioma
- Variante Numeral
- Calendário
- ColumnHeaderRows
- RowHeaderColumns
- ColsBeforeRowHeader
- Direção do Layout
- DefiniçãoCaminho
- Nível
- MemberCellIndex
- CellItemOffset
- ColSpan
- Expansão de linha
- DefIndex
- ColumnIndex
- RowIndex
- Etiqueta do Grupo
- Nível de alternância recursivo
- Estilo de lista
- ListaNível
- Número do Parágrafo
- Recuo Direito
- LeftIndent
- HangingIndent
- Espaço Antes
- EspaçoDepois
- Primeira linha
- Marcação
- ConteúdoTopo
- ConteúdoEsquerda
- Largura do Conteúdo
- Altura do Conteúdo
- Estado
- CellItemState
- MemberDefState

### Enumerações
A lista a seguir mostra as enumerações que podem ser usadas no fluxo RPL:

- Opções de classificação
- Dimensionamentos
- Tipo de Forma
- ImageRawFormat
- Estilos de fonte
- FontWeights
- TextoDecorações
- Alinhamentos de Texto
- Alinhamentos Verticais
- Instruções
- Modos de escrita
- UnicodeBiDiTypes
- Calendários
- Estilos de borda
- BackgroundRepeatTypes
- ListStyles
- Estilos de marcação
- Código de Tipo
- StateValues
- TablixMemberStateValues
- TablixMemberDefStateValues
- RPLSize





## Referências ##

- [Formato de fluxo binário de layout de página de relatório (RPL)](https://learn.microsoft.com/en-us/openspecs/sql_server_protocols/ms-rpl/9c4ff7ba-f6da-4092-9670-aa0e54e73887)

