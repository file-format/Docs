{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo psd", "formato de arquivo psd", "o que é um arquivo psd", "arquivo", "exemplo psd", "extensão de arquivo psd", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PSD - Formato de arquivo de imagem do Photoshop",
  "description":"Saiba mais sobre o formato de arquivo PSD e APIs que podem criar e abrir arquivos PSD.",
  "linktitle" : "PSD",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PSD?

PSD, Photoshop Document, representa o formato de arquivo nativo do Adobe Photoshop usado para design e desenvolvimento de gráficos. Os arquivos PSD podem incluir camadas de imagem, camadas de ajuste, máscaras de camada, anotações, informações do arquivo, palavras-chave e outros elementos específicos do Photoshop. Os arquivos do Photoshop têm extensão padrão como .PSD e têm altura e largura máximas de 30.000 pixels e um limite de comprimento de dois gigabytes.

## Especificações de formato de arquivo PSD ##

Os dados em um arquivo PSD são armazenados em ordem de bytes big endian. Isso implica trocar os inteiros curtos e longos ao ler ou escrever na plataforma Windows. O formato de arquivo do Photoshop é dividido em cinco partes principais. Tem muitos marcadores de comprimento que podem ser usados para mover de uma seção para a próxima. Os marcadores de comprimento geralmente são preenchidos com bytes para arredondar para o intervalo de 2 ou 4 bytes mais próximo. As cinco partes principais são:

* Cabeçalho do arquivo
* Dados do modo de cor
* Recursos de imagem
* Informações de Camada e Máscara
* Dados de imagem

Para conformidade, os dados devem ser gravados em todos esses campos da seção, pois o Photoshop pode tentar ler a seção inteira. Também implica que zeros sejam gravados em campos ignorados durante a gravação em um arquivo. O campo de comprimento nas seções delimitadas por comprimento deve ser usado para decidir quando interromper a leitura. Na maioria dos casos, o campo de comprimento indica o número de bytes, não de registros, a seguir. Os seguintes pontos precisam ser lembrados durante a leitura de um arquivo.

* Os valores na coluna "Length" em todas as tabelas estão em bytes.
* Todos os valores definidos como string Unicode consistem em:
* Um campo de comprimento de 4 bytes, representando o número de caracteres na string (não bytes).
* A cadeia de valores Unicode, dois bytes por caractere.

### Cabeçalho do arquivo ###

O cabeçalho do arquivo contém as propriedades básicas da imagem.

|Comprimento|Descrição
---|---|
|4|Assinatura: sempre igual a '8BPS' . Não tente ler o arquivo se a assinatura não corresponder a esse valor.
|2|Versão: sempre igual a 1. Não tente ler o arquivo se a versão não corresponder a este valor. (~*~*PSB~*~* versão é 2.)
|6|Reservado: deve ser zero.
|2|O número de canais na imagem, incluindo quaisquer canais alfa. O intervalo suportado é de 1 a 56.
|4|A altura da imagem em pixels. O intervalo suportado é de 1 a 30.000.
|4|A largura da imagem em pixels. O intervalo suportado é de 1 a 30.000.
|2|Profundidade: o número de bits por canal. Os valores suportados são 1, 8, 16 e 32.
|2|O modo de cor do arquivo. Os valores suportados são: Bitmap # 0; Escala de cinza # 1; Indexado # 2; RGB # 3; CMYK # 4; Multicanal # 7; Duotone # 8; Laboratório nº 9.

### Seção de dados do modo de cor ###

A seção de dados do modo de cor é estruturada da seguinte forma:


|Comprimento|Descrição
---|---|
|4|O comprimento dos seguintes dados de cores
|variável|Os dados de cor

Os dados do modo de cor estão disponíveis apenas para cor indexada e tom duplo, conforme definido pelo campo de modo na seção Cabeçalho do arquivo. Para todos os outros modos, esta seção é representada por valores zerados de 4 bytes. Para imagens coloridas indexadas, o comprimento é 768 e os dados de cores contêm a tabela de cores da imagem, em ordem não intercalada. Para imagens Duotone, os dados de cor contêm a especificação duotone (cujo formato não está documentado). Outros aplicativos que leem arquivos do Photoshop podem tratar uma imagem duotônica como uma imagem cinza e apenas preservar o conteúdo das informações duotônicas ao ler e gravar o arquivo.

### Seção de recursos de imagem ###

A terceira seção do arquivo contém recursos de imagem. Ele começa com um campo de comprimento, seguido por uma série de blocos de recursos.


|Comprimento|Descrição
---|---|
|4|Comprimento da seção de recursos de imagem. O comprimento pode ser zero.
|Variável|Recursos de Imagem (Blocos de Recursos de Imagem)

Os recursos de imagem são usados para armazenar dados não-pixel associados a imagens, como caminhos de ferramentas de caneta. Eles são chamados de blocos de recursos porque contêm dados armazenados no recurso do Macintosh nas primeiras versões do Photoshop. A estrutura básica dos blocos de recursos de imagem é mostrada abaixo:


|Comprimento|Descrição
---|---|
|4|Assinatura: '8BIM'
|2|Identificador exclusivo do recurso. IDs de recursos de imagem contém uma lista de IDs de recursos usados pelo Photoshop.
|Variável|Nome: string Pascal, preenchida para tornar o tamanho uniforme (um nome nulo consiste em dois bytes de 0)
|4|Tamanho real dos dados do recurso a seguir
|Variável|Os dados do recurso, descritos nas seções sobre os tipos de recursos individuais. É acolchoado para uniformizar o tamanho.

Os recursos de imagem usam vários números de ID padrão.

### Informações sobre Camadas e Máscaras ###

A quarta seção de um arquivo do Photoshop contém informações sobre camadas e máscaras, como número de camadas, canais nas camadas, intervalos de mesclagem, teclas de camada de ajuste, camadas de efeitos e parâmetros de máscara. Se não houver camadas ou máscaras, esta seção será representada por um campo de 4 bytes zerado. Atenção especial deve ser dada ao comprimento das seções durante a leitura desta seção devido aos valores zerados. A disposição da seção Camada e Máscara é a seguinte:


|Comprimento|Descrição
---|---|
|4|Comprimento da seção de informações de camada e máscara. (O comprimento do PSB é de 8 bytes.)
|Variável|Informações da camada
|Variável|Informações da máscara de camada global
|Variável|Série de blocos marcados contendo vários tipos de dados.

#### Informações da camada ####

A tabela a seguir mostra a organização de alto nível das informações da camada.


|Comprimento|Descrição
---|---|
|4|Comprimento da seção de informações das camadas, arredondado para um múltiplo de 2. (O comprimento do PSB é de 8 bytes.)
|2|Contagem de camadas. Se for um número negativo, seu valor absoluto é o número de camadas e o primeiro canal alfa contém os dados de transparência para o resultado mesclado.
|Variável|Informações sobre cada camada. Consulte Registros de camada descreve a estrutura dessas informações para cada camada.
|Variável|Dados de imagem do canal. Contém um ou mais registros de dados de imagem para cada camada. As camadas estão na mesma ordem que as informações da camada

### Dados de imagem ###

Os dados de pixel de imagem estão contidos na seção Dados de imagem do arquivo. A disposição dos dados na seção Dados de imagem está em ordem planar, ou seja, primeiro todos os dados vermelhos, depois todos os dados verdes, etc. Cada plano é armazenado em ordem de linha de varredura, sem bytes de bloco, A seção de dados de imagem é organizada em um formato como mostrado na tabela a seguir.

|Comprimento|Descrição
---|---|
|2|Método de compactação: *0 = Dados brutos da imagem * 1 = RLE compactados os dados da imagem começam com as contagens de bytes para todas as linhas de varredura (linhas * canais), com cada contagem armazenada como um valor de dois bytes. Os dados compactados RLE seguem, com cada linha de varredura compactada separadamente. A compactação RLE é o mesmo algoritmo de compactação usado pela rotina de ROM do Macintosh PackBits e pelo padrão TIFF. *2 = ZIP sem previsão *3 = ZIP com previsão.
|Variável|Os dados da imagem. Ordem planar = RRR GGG BBB, etc.

## Referências ##

* [Especificações de formato de arquivo PSD - Por Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/#50577409_pgfId-1030196)
* [Formato de arquivo do Adobe Photoshop](https://en.wikipedia.org/wiki/Adobe_Photoshop#File_format)

