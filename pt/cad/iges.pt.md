{
  "date" : "2020-03-16",
  "keywords" :[ "Arquivo IGES", "Formato de arquivo", "CAD" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo IGES e APIs que podem criar e abrir arquivos IGES.",
  "title" :"Formato de arquivo IGES",
  "linktitle" : "IGES",
  "menu" : {
    "docs" : {
      "parent" : "cad"
}
},
  "lastmod" : "2020-07-28"
}

## O que é um arquivo IGES?

Um arquivo com extensão .iges é usado para trocar informações de projeto entre aplicativos de desenho assistido por computador (CAD). IGES significa Initial Graphics Exchange Specifications. As informações trocadas usando IGES incluem diagrama de circuito, estrutura de arame, superfície de forma livre ou representações de modelagem sólida. O IGES encontra suas aplicações em desenhos de engenharia tradicionais, análise de modelos e funções de fabricação. O formato pode trocar informações de projeto 2D ou 3D entre programas CAD. Os arquivos IGES podem ser abertos com vários aplicativos CAD, como Autodesk e CADSoftTools ABViewer. Existem também várias APIs disponíveis para abrir e converter arquivos IGES programaticamente.

## Formato de arquivo IGES

Os arquivos IGES estão no formato de texto ASCII e podem ser abertos em qualquer editor de texto para visualizar o conteúdo do arquivo. As informações textuais em um arquivo IGES são representadas no formato "Hollerith". Um arquivo IGES comum pode conter milhares de linhas para representar as informações 2D ou 3D que podem ser trocadas de acordo com esse formato. Um arquivo IGES é dividido em cinco seções, indicadas pela letra maiúscula específica na 73ª coluna. Essas seções são as seções `Start` (S), `Global` (G), `Data Entry` (D), `Parameter Data` (P) e `Terminate` (T). As seções Data Entry e Parameter Data são comumente abreviadas como DE e PD, respectivamente.

### Cabeçalho do arquivo IGES

As seções Iniciar e Global contêm informações básicas sobre:
* Nome do arquivo e sua fonte
* Delimitadores para a seção Parameter Data
* Autor do arquivo e outras informações gerais.

As seções Iniciar e Global do documento de exemplo na Wikipedia são as seguintes.
```
S      1
1H,,1H;,4HSLOT,37H$1$DUA2:[IGESLIB.BDRAFT.B2I]SLOT.IGS;,                G      1
17HBravo3 BravoDRAFT,31HBravo3->IGES V3.002 (02-Oct-87),32,38,6,38,15,  G      2
4HSLOT,1.,1,4HINCH,8,0.08,13H871006.192927,1.E-06,6.,                   G      3
31HD. A. Harrod, Tel. 313/995-6333,24HAPPLICON - Ann Arbor, MI,4,0;     G      4
```
Como pode ser visto, o campo inicial contém descrições legíveis do arquivo, e eu tenho quaisquer caracteres nas colunas 1-72, com a linha terminando com o cabeçalho da seção e o número da linha da seção. Deve haver pelo menos 1 linha da seção Iniciar. A seção global contém dados do pré-processador. Também deve estar presente no arquivo e terminar com o formato G000000#.

### Seção de Entrada de Dados (DE) e Dados de Parâmetro (PD)

#### Seção de entrada de dados
Um arquivo IGES consiste em várias entidades que contêm as informações sobre os dados básicos do formato de arquivo IGES. Uma entidade contém informações sobre diferentes elementos de um formato de dados IGES e é usada para desenho. As entidades mais comumente usadas incluem:
* Arco circular
* Curva Composta
* Arco Cônico
* Avião
* Linha

Estas são apenas algumas e existem cerca de 150 entidades diferentes no IGES. Cada entidade é identificada por um número de tipo, como:
* ARCO CIRCULAR (Tipo 100)
* LINHA (Tipo 110)

##### Propriedades da entidade

Cada entidade declarada tem as seguintes propriedades.

|Nome do Campo|Descrição|
---|---|
|Tipo de Entidade |Este é o tipo de entidade que está sendo descrito. Por exemplo, 116 descreve uma entidade Point.|
|Ponteiro PD |Dá a localização dos dados desta entidade na seção Dados do Parâmetro. Esse local é simplesmente o número da linha dentro da seção PD que tem a primeira linha dos dados dessa entidade.|
|Estrutura |Zero ou ponteiro para entidade de definição. Não aplicável para a maioria das entidades|
|Padrão de fonte de linha| Número ou ponteiro para entidade de padrão de fonte de linha. Número significa: * 0 Nenhum padrão especificado (padrão) * 1 Sólido * 2 Tracejado * 3 Fantasma * 4 Linha central * 5 Pontilhado|
|Nível| Especifica os níveis a serem associados a esta entidade. Permite que a entidade apareça em mais de um nível|
|Visualizar| Especifica as opções de visualização. São eles: 0 Indica visibilidade e características iguais em todas as vistas. Ponteiro padrão para a entidade View (Tipo 410) que pode ser visualizada a partir de Referência a uma entidade View Visible Associativity (Type 402, Form 3)
|Ponteiro de matriz de transformação| Faz referência a uma entidade de matriz de transformação (Tipo 124) ou é zero por padrão (sem transformação)|
|Associatividade de exibição de rótulo| Refere-se a uma associatividade de exibição de rótulo (tipo 402, formulário 5) que define como o rótulo da entidade aparece.|
|Número de status| Contém quatro seções de dois números. 1-2: Status em branco. Ou 00 para normal ou 01 para apagado. 3-4: Chave de entidade subordinada: é 00 para independente, 01 para dependente fisicamente, 02 para dependente lógico e 03 para ambos. 5-6: Sinalizador de Uso de Entidade: é 00 para Geometria, 01 para anotação, 02 para definição, 03 para Outro, 04 para Lógico, 05 para paramétrico 2D e 06 para Geometria de construção. Finalmente, 7-8 é a hierarquia, onde 00 indica top down global (use as características desta entidade), 01 é adiamento global (não use as características desta entidade) e 02 é use a propriedade da hierarquia (use Hierarchy Entity (Tipo 406, Formulário 10)para determinar características de agrupamento hierárquico).|
|Número de sequência| Especificado por D#, onde # é o número da linha para esta seção (não da parte superior do arquivo). Isso também é usado para apontar para essa entidade de entrada de dados.|
|Tipo de Entidade| é especificado duas vezes por listagem de entidade|
|Número do Peso da Linha| Especifica a espessura ao exibir a entidade. O menor é 1, 0 é o padrão|
|Número de cor| Especifica a cor da entidade. Os valores inteiros permitidos são: 0 Sem cor (padrão) 1 Preto 2 Vermelho 3 Verde 4 Azul 5 Amarelo 6 Magenta 7 Ciano 8 Branco|
|Número de contagem de linha de parâmetro| Especifica o número de linhas que esta entidade ocupa na Seção de Dados de Parâmetro|
|Número do formulário| Indica a forma ou a representação desta entidade. Altera como os dados do parâmetro são interpretados. O padrão é 0|
|Campo Reservado| Não usado|
|Campo Reservado| Não usado|
|Etiqueta da entidade| Identificador especificado do aplicativo - justificado à direita|
|Número do Subscrito| Qualificador numérico para o rótulo da entidade. Ambos juntos formam um identificador único para a entidade|
|Número de sequência Consulte acima. |Será D#+1, pois cada entidade é especificada em duas linhas.|

#### Seção de dados de parâmetro
A seção Entradas de Dados é seguida pela seção Dados de Parâmetros. Ele lista os dados para cada entrada respectiva e lista os parâmetros para a entidade com base nos delimitadores especificados na seção Global (geralmente vírgulas para separar os parâmetros e um ponto e vírgula para finalizar a listagem).


## Referências
* [IGES por WikiPedia](https://en.wikipedia.org/wiki/IGES)

