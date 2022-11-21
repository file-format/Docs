{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "categories" :[ "fundamentos" ],
  "description":"Portable Document Format (PDF) é uma representação padrão de documentos independentes de software, hardware e sistema operacional. Os padrões de PDF incluem PDF/A, PDF/E, PDF/UA, PDF/VT e PDF/X.",
  "title" :"Formato de arquivo PDF - O que é um arquivo PDF?",
  "linktitle" : "PDF",
  "menu" : {
    "docs" : {
      "parent" : "pdf",
      "weight" : "01"
}
},
  "lastmod" : "2019-09-10"
}

Portable Document Format (PDF) é um tipo de documento criado pela Adobe na década de 1990. O objetivo deste formato de arquivo foi introduzir um padrão para representação de documentos e outros materiais de referência em um formato independente do software aplicativo, hardware e sistema operacional. O formato de arquivo PDF tem capacidade total para conter informações como texto, imagens, hiperlinks, campos de formulário, rich media, assinaturas digitais, anexos, metadados, recursos geoespaciais e objetos 3D que podem se tornar parte do documento de origem.

Na maioria dos casos, os documentos existentes são convertidos em PDF em vez de criar um novo PDF do zero. Mas isso não significa que não existam softwares para criação ou manipulação de arquivos PDF.

**(Tem que compartilhar algo sobre o formato de arquivo PDF? Você pode postar suas descobertas na seção [Notícias em formato de arquivo PDF](https://news.fileformat.com/t/PDF).)**

## Formato de arquivo PDF - Breve Histórico

Uma rápida passagem pela linha do tempo sobre a formação do arquivo PDF em termos de linha do tempo é a seguinte:

**1993** - A Adobe Systems disponibilizou gratuitamente as especificações do PDF

**2008** - PDF foi lançado como padrão aberto em 1º de julho de 2008 e foi publicado pela International Organization for Standardization como **ISO 32000-1:2008**.

**2008** - A Adobe publicou uma Licença Pública de Patente para o formato ISO 32000-1, direitos isentos de royalties para todas as patentes de propriedade da Adobe que sejam necessárias para fazer, usar, vender e distribuir implementações compatíveis com PDF.

A primeira versão do PDF designada como PDF 1.0 que posteriormente passou por revisões até o PDF 1.7. O PDF 1.7, que se tornou o ISO 32000-1, inclui algumas tecnologias proprietárias não padronizadas, como Adobe XML Forms Architecture (XFA) e extensão JavaScript para Acrobat. Foi em 28 de julho de 2017, quando foi publicado o PDF 2.0, conhecido como ISO 32000-2:2017, que não inclui nenhuma tecnologia não padronizada.

## Especificações de formato de arquivo PDF

Um arquivo PDF é um conjunto de bytes que podem ser agrupados em tokens de acordo com as regras de sintaxe definidas pelas especificações do PDF. Uma ou mais tokens são combinados para formar entidades sintáticas de nível superior, principalmente objetos, que são os valores de dados básicos a partir dos quais um documento PDF é construído.

### Estrutura de arquivos de arquivos PDF

O conteúdo do arquivo PDF é organizado na seguinte sequência dentro do arquivo.

|Cabeçalho
|Corpo
|Tabela de Referência Cruzada
|Reboque

#### Cabeçalho do arquivo PDF ####

Independentemente da versão do PDF, um arquivo PDF começa com um cabeçalho contendo um identificador exclusivo para PDF e a versão do formato, como %PDF-1.x, onde x varia de 1 a 7.

#### Corpo do arquivo ####

O corpo de um arquivo PDF consiste em uma sequência de objetos indiretos que representam o conteúdo de um documento. Os objetos, conforme descrito acima, representam componentes do documento, como fontes, páginas e imagens de amostra. A partir do PDF 1.5, o corpo também pode conter fluxos de objetos, cada um contendo uma sequência de objetos indiretos.

#### Tabela de referência cruzada ####

A tabela de referência cruzada contém informações que permitem acesso aleatório a objetos indiretos dentro do arquivo para que o arquivo inteiro não precise ser lido para localizar qualquer objeto específico. A tabela deve conter uma entrada de uma linha para cada objeto indireto, especificando o deslocamento de byte desse objeto no corpo do arquivo. (A partir do PDF 1.5, algumas ou todas as informações de referência cruzada podem, alternativamente, estar contidas em fluxos de referência cruzada.

#### Trailer do arquivo ####

O trailer de um arquivo PDF permite que um leitor em conformidade encontre rapidamente a tabela de referência cruzada e certos objetos especiais. Leitores em conformidade devem ler um arquivo PDF a partir do final. A última linha do arquivo deve conter apenas o marcador de fim de arquivo, %%EOF. As duas linhas anteriores devem conter, uma por linha e em ordem, a palavra-chave startxref e o deslocamento de byte no fluxo decodificado desde o início do arquivo até o início da palavra-chave xref na última seção de referência cruzada.

### Objetos PDF ###

Um arquivo PDF inclui vários tipos diferentes de objetos que são dos seguintes tipos

* Valores booleanos - representando condicional verdadeiro ou falso
* Números - Valores inteiros e reais
* Strings - contém caracteres entre parênteses
* Nomes - comece com um caractere / para a frente, por exemplo, /ASomewhatLongerName resulta em ASomewhatLongerName
* Matrizes - PDF suporta matrizes unidimensionais. Arrays de dimensões mais altas podem ser construídos usando arrays como elementos aninhados
* Dicionários - coleção de objetos como pares chave-valor. Pode ter zero entradas.
* Streams - representa a sequência de bytes que também pode ter comprimento ilimitado
* Null Object - representa um valor nulo

Pode haver outros objetos, como comentários, que são introduzidos com o sinal % e podem conter caracteres de 8 bits.

### Objetos indiretos ###

Qualquer objeto em um arquivo PDF pode ser rotulado como objeto indireto. Os objetos indiretos recebem um identificador de objeto exclusivo pelo qual outros objetos podem se referir a ele. As referências cruzadas são mantidas em uma tabela de índice e marcadas com a palavra-chave xref que segue o corpo principal e fornece o deslocamento de byte de cada objeto indireto desde o início do arquivo.

### Layouts de PDF lineares e não lineares ###

Os layouts de PDF são categorizados como Llnear e não lineares, dependendo dos aplicativos de destino e de outros fatores.

Não linear - Arquivos PDF não lineares usam menos espaço em disco em comparação com arquivos PDF lineares. As páginas PDF do documento residem de forma dispersa no arquivo PDF e é por isso que os arquivos não lineares são mais lentos em comparação com os arquivos lineares.

PDF Linear - Visando visualizadores de PDF online, os arquivos PDF Linear são construídos de forma que sejam gravados em disco de maneira linear. Isso não requer plugins do navegador para que o documento inteiro seja carregado primeiro antes da exibição.

### Visão geral dos objetos ###

Como mencionado, o corpo do PDF é uma coleção de objetos mencionados acima. O PDF é amplamente baseado em PostScript sem os recursos de controle de linguagens de programação, como comandos if e loop. Comandos emitidos por código Postscript para gerar conteúdo gráfico são coletados e tokenizados, além de quaisquer arquivos, gráficos ou fontes referidos pelo documento. Todos esses conteúdos são acumulados em um único arquivo, resultando em uma saída PostScript composta.

#### Texto ####

O texto em PDF é representado por elementos de texto que são realmente exibidos com glifos de fontes. Um glifo é uma forma gráfica e está sujeito a todas as manipulações gráficas, como a transformação de coordenadas. Devido à importância do texto na maioria das descrições de página, o PDF oferece recursos de alto nível para descrever, selecionar e renderizar glifos de maneira conveniente e eficiente.

#### Gráficos ####

Os operadores gráficos usados em fluxos de conteúdo PDF descrevem a aparência das páginas que devem ser reproduzidas em um dispositivo de saída raster. As instalações destinam-se a aplicações de impressão e exibição. Os operadores gráficos formam seis grupos principais:

* Os operadores de estado gráfico manipulam a estrutura de dados chamada estado gráfico, a estrutura global dentro da qual os outros operadores gráficos são executados. O estado gráfico inclui a matriz de transformação atual (CTM), que mapeia as coordenadas do espaço do usuário usadas em um fluxo de conteúdo PDF nas coordenadas do dispositivo de saída. Também inclui a cor atual, o caminho de recorte atual e muitos outros parâmetros que são operandos implícitos dos operadores de pintura.
* Os operadores de construção de caminho especificam caminhos, que definem formas, trajetórias de linha e regiões de vários tipos. Eles incluem operadores para iniciar um novo caminho, adicionar segmentos de linha e curvas a ele e fechá-lo.
* Os operadores de pintura de caminho preenchem um caminho com uma cor, pintam um traço ao longo dele ou o usam como um limite de recorte.
* Outros operadores de pintura pintam certos objetos gráficos autodescritivos. Isso inclui imagens de amostra, sombreamentos definidos geometricamente e fluxos de conteúdo inteiros que, por sua vez, contêm sequências de operadores gráficos.
* Os operadores de texto selecionam e mostram glifos de caracteres de fontes (descrições de tipos de letra para representar caracteres de texto). Como o PDF trata os glifos como formas gráficas gerais, muitos dos operadores de texto podem ser agrupados com o estado gráfico ou operadores de pintura. No entanto, as estruturas de dados e mecanismos para lidar com descrições de glifos e fontes são suficientemente especializados.
* Os operadores de conteúdo marcado associam informações lógicas de nível superior a objetos no fluxo de conteúdo. Essas informações não afetam a aparência renderizada do conteúdo; é útil para aplicativos que usam PDF para intercâmbio de documentos.

## Referências ##

* [Formato de arquivo PDF: estrutura básica](https://resources.infosecinstitute.com/pdf-file-format-basic-structure/)
* [PDF - Wikipedia](https://en.wikipedia.org/wiki/PDF)
* [Referência de PDF - Adobe](https://www.adobe.com/devnet-apps/photoshop/fileformatashtml/)

