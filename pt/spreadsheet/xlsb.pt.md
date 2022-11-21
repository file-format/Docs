{
  "date" : "2019-12-10",
  "keywords" :[ "XLSB", "arquivo", "extensão", "formato de arquivo", "Arquivo de planilha binária do Excel" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Seu guia de formato de arquivo para saber o que é um arquivo XLSB e APIs que podem criá-los e abri-los.",
  "title" :"O que é um arquivo XLSB?",
  "linktitle" : "XLSB",
  "menu" : {
    "docs" : {
      "parent" : "spreadsheet"
}
},
  "lastmod" : "2019-12-10"
}

## O que é um arquivo XLSB?

O formato de arquivo XLSB especifica o formato de arquivo binário do Excel, que é uma coleção de registros e estruturas que especificam o conteúdo da pasta de trabalho do Excel. O conteúdo pode incluir tabelas de números não estruturadas ou semiestruturadas, texto ou ambos, números e texto, fórmulas, conexões de dados externos, gráficos e imagens. Ao contrário de [XLSX](/pt/spreadsheet/xlsx/) (que é baseado no formato de arquivo Open XML), o XLSB representa o arquivo binário da pasta de trabalho do Excel. Os arquivos XLSB podem ser lidos e gravados mais rapidamente, o que os torna úteis para trabalhar com arquivos grandes. XLSB raramente é usado para armazenar pastas de trabalho, pois XLSX (e anteriormente [XLS](/pt/spreadsheet/xls/)) são os formatos de arquivo selecionados pelo usuário mais comuns para salvar pastas de trabalho. Ele pode ser aberto pelo Microsoft Office 2007 e superior.

## Especificações de formato de arquivo XLSB ##

As especificações de formato de arquivo para o formato de arquivo XLSB foram tornadas públicas em 2008 como versão 1.0. Desde então, as especificações foram revisadas várias vezes e a versão mais recente das especificações (v 10.0) foi publicada em abril de 2018. As especificações estão disponíveis publicamente pela Microsoft como [[MS-XLSB] - Especificações do formato de arquivo binário do Excel](https:/ /msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx) e deve ser consultado por qualquer pessoa para ler ou gravar arquivos no formato de arquivo XLSB.

## Estrutura de arquivo XLSB ##

Um arquivo XLSB é um pacote que consiste em uma coleção de partes. Essas partes contêm informações sobre o conteúdo de uma pasta de trabalho, incluindo dados da pasta de trabalho e a estrutura do pacote. Algumas partes contêm informações armazenadas usando registros binários, algumas como XML, enquanto outras contêm informações armazenadas como um fluxo binário de bytes. Cada registro binário contém zero ou mais campos estruturados que contêm os dados da pasta de trabalho.

#### Pacote ####

Um pacote XLSB é um arquivo [ZIP](/pt/compression/zip/) que deve conter exatamente uma parte da pasta de trabalho. Esta parte deve ser o destino de um relacionamento nesta parte de relacionamento do pacote. A parte da pasta de trabalho é a parte inicial do documento XLSB.

#### Papel ####

Uma parte é um fluxo de bytes que possui um tipo de conteúdo associado que especifica a natureza e o tipo de conteúdo armazenado na parte. Algumas partes armazenam informações em formato binário, enquanto outras armazenam informações como XML. A seção [enumeração de partes](https://msdn.microsoft.com/en-us/library/dd924091(v#office.12).aspx) do documento de especificações lista as partes válidas, tipos de conteúdo e relacionamentos obrigatórios/opcionais entre todas as peças em um pacote.

#### Relação ####

Uma origem e um recurso de destino são conectados por um relacionamento. Um relacionamento pode ser:

**Relação do pacote:** onde o destino é uma parte e a origem é o pacote como um todo

**Relação parte a parte:** onde o destino é uma parte e a origem é uma parte do pacote

**Relacionamento explícito:** onde um recurso é referenciado a partir do conteúdo de uma parte de origem, referenciando o valor do atributo ID de um elemento de relacionamento

**relacionamento implícito** é um relacionamento que não é explícito

**Relação interna:** onde o destino faz parte do pacote

**Relação externa:** onde o destino é um recurso externo que não está no pacote

#### Registro ####

Um registro é o bloco de construção básico usado para armazenar informações sobre recursos em uma pasta de trabalho. Cada registro binário é uma sequência de bytes de comprimento variável. Um registro binário consiste em três componentes:

* um tipo de registro
* um tamanho de registro, e
* os dados de registro específicos desse tipo de registro.

**Tipo de registro:** O tipo de registro mostra o tipo de registro especificado pelo registro. Também especifica a estrutura de dados de registro específica para este registro. Os tipos de registro válidos estão listados na seção [Record Enumeration](https://msdn.microsoft.com/en-us/library/dd953057(v#office.12).aspx) do documento de especificações. O tipo de registro deve ser de um ou dois bytes e deve ser maior ou igual a 128 e menor que 16384.

**Tamanho do registro:** o tamanho do registro especifica a contagem de bytes que especifica o tamanho total dos dados do registro. Este valor DEVE ser de um a quatro bytes. Este valor DEVE ser um byte se o bit alto no byte baixo for igual a 0; caso contrário, esse valor DEVE ser maior que um byte. Se a contagem de bytes for maior que um byte, o bit alto em cada byte sucessivo especifica se um byte adicional é usado. Se o bit alto do segundo byte for igual a 1, então esse valor DEVE usar um terceiro byte adicional. Se o bit alto do terceiro byte for igual a 1, então esse valor DEVE usar um quarto byte adicional. O bit alto do quarto byte DEVE ser ignorado. O valor consiste nos sete bits baixos de cada byte combinados. Os bits menos significativos estão contidos no primeiro byte, e cada byte sucessivo contém bits de ordem mais alta que o byte anterior.

**Dados de registro:** o componente de dados de registro contém campos que correspondem a um tipo de registro específico e abrangem o restante do registro. A ordem e a estrutura dos campos para um determinado tipo de registro listado em Enumeração de Registros são especificadas na seção correspondente para esse tipo de registro em Registros. O tamanho total do componente de dados de registro DEVE ser igual ao tamanho do registro. Os campos no componente de dados de registro podem conter valores simples, matrizes de valores, estruturas de vários campos, matrizes de campos e matrizes de estruturas.

#### Exemplo de registro XLSB ####

O tipo de registro e o tamanho do registro a seguir especificam um registro **BrtCommentText** com um tamanho de 200 bytes:

11111101 00000100 11001000 00000001 [Campos de registro]

O primeiro byte é 11111101, especificando um valor baixo de 125 e que o tipo de registro requer um segundo byte. O segundo byte é 00000100, especificando um valor alto de 4 * 128, que equivale a 512. O valor do tipo de registro é 125 + 512 ou 637, que corresponde a um tipo de registro **BrtCommentText**. O próximo byte é 11001000, especificando um valor baixo de 72 e que o tamanho do registro requer um segundo byte. O segundo byte é 00000001, especificando um valor maior de 1 * 128 e que o tamanho do registro não requer um byte adicional. O tamanho do registro é 72 + 128, ou 200, que especifica o tamanho total, em bytes, do componente de dados do registro. Os campos no componente de dados de registro são especificados por **BrtCommentText**.

## Referências ##

* [[MS-XLSB] - Formato de arquivo binário do Excel (.xlsb)](https://msdn.microsoft.com/en-us/library/cc313133(v#office.12).aspx)

