{
  "date" : "2019-12-12",
  "keywords" :[ "JT", "arquivo", "extensão", "formato", "3D fbx", "" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo JT e APIs que podem criar e abrir arquivos JT.",
  "title" :"JT - Formato de arquivo de mosaico de Júpiter",
  "linktitle" : "JT",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo JT?

**JT** (Jupiter Tessellation) é um formato de dados 3D padrão ISO flexível, eficiente e focado no setor desenvolvido pela Siemens PLM Software. Os domínios de CAD mecânico da indústria aeroespacial, automotiva e de equipamentos pesados usam JT como seu formato de visualização 3D mais líder.

O formato JT é um gráfico de cena que suporta os atributos e nós específicos do CAD. Técnicas de compressão sofisticadas são usadas para armazenar dados de facetas (triângulos). Esse formato é estruturado para oferecer suporte a atributos visuais, informações de produto e fabricação (PMI) e metadados. Há um bom suporte para streaming assíncrono de conteúdo. Na indústria mecânica pesada, os profissionais usam o arquivo JT em suas soluções CAD e programas de software de gerenciamento do ciclo de vida do produto (PLM) para examinar a geometria de mercadorias complicadas.

Como o JT suporta quase todos os formatos CAD 3D importantes, sua montagem pode lidar com uma variedade de combinações conhecidas como "multi-CAD". Esta montagem multi-CAD é sempre bem gerenciada e atualizada porque a sincronização entre os arquivos de descrição do produto CAD nativo com seus arquivos JT associados ocorre automaticamente. Os arquivos JT são originalmente leves, portanto, considerados adequados para colaborações na Internet. Empresas Colaboram enviando visualizações 3D pela mídia com muito mais facilidade em comparação com arquivos CAD originais "pesados". Além disso, os arquivos JT garantem muitos recursos de segurança que tornam o compartilhamento de propriedade intelectual mais seguro.

## Breve História do Formato de Arquivo JT

Engineering Animation, Inc. e Hewlett Packard foram os designers originais da JT, que desenvolveram esse formato como o kit de ferramentas Direct Model. Depois que a EAI foi adquirida pela UGS Corp. JT tornou-se parte do conjunto da UGS. No início de 2007, a UGS anunciou o JT como seu formato 3D mestre. No mesmo ano, a Siemens AG comprou a UGS e se tornou a Siemens PLM Software. A Siemens usa JT como formato comum de interoperabilidade e formato de arquivamento de dados. Em 2009, a ISO aceitou a especificação JT para publicação como uma especificação disponível publicamente (PAS). cenários de troca. Em 2012, JT foi oficialmente declarado como um formato de visualização 3D padronizado pela ISO (ISO 14306:2012 (ISO JT V1)).

## Formato de arquivo JT ##

Todos os objetos no formato JT são representados por meio de um identificador de objeto e as referências entre objetos são tratadas por meio do identificador do objeto referenciado. A integridade dessas referências de objeto pode ser mantida por meio de ponteiros unwizzling/swizzling.

Um arquivo JT é organizado como uma série de blocos e o bloco de cabeçalho é sempre o primeiro bloco de dados no arquivo. Uma série de segmentos de dados e um segmento TOC seguem imediatamente o bloco de cabeçalho. O único segmento de dados (6 segmentos LSG) possui um arquivo JT compatível com referência sempre existe. O segmento TOC contém as informações de localização de todos os outros segmentos de dados desse arquivo.

{{< figure src="../JT-1.png" alt="Formato de arquivo JT" >}}

### Cabeçalho do arquivo ###

File Header é o primeiro bloco na hierarquia de dados do arquivo JT. As informações de versão e as informações de localização do TOC estão incluídas no cabeçalho, o que facilita os carregadores na leitura do arquivo. O conteúdo do cabeçalho do arquivo é organizado da seguinte forma.

### Segmento TOC ###

O segmento TOC deve existir dentro de um arquivo e conter informações de identificação e localização de todos os outros segmentos de dados. A localização real do segmento TOC é especificada pelo campo TOC Offset do cabeçalho do arquivo. Cada segmento de dados endereçável individualmente é representado pela entrada TOC em um segmento TOC.

### Segmento de dados ###

O arquivo JT define todos os dados armazenados em um segmento de dados. Alguns segmentos de dados podem compactar todos os bytes de dados de informações que permaneceram no segmento. Os segmentos de dados têm a seguinte estrutura:

![alt text](../JT-2.png "JT Data Segment")

A tabela a seguir descreve diferentes tipos de segmentos de dados:

|Nome|Descrição
---|---|
|Segmento LSG|Compreende uma coleção de objetos vinculados por meio de referências direcionadas para formar LSG (estrutura gráfica acíclica direcionada)
|Shape LOD segment|contém os dados de definição para as formas geométricas (por exemplo, vértices, normais, polígonos, etc)
|Segmento JT B-Rep|Tendo elemento para os dados representarem o limite geométrico preciso para uma porção individual no formato JT B-Rep.
|Segmento XT B-Rep|Tendo elemento para os dados representarem o limite geométrico preciso para uma porção individual no formato de representação de limite
|Segmento de estrutura de arame|Os dados representam uma estrutura de arame 3D precisa para uma parte específica definida por um elemento contido neste segmento.
|Segmento de Metadados|Permite armazenar metadados em segmentos endereçáveis distintos.
|Segmento JT ULP|Tendo elemento para que os dados representem o limite geométrico semipreciso de uma porção individual no formato JT ULP.
|Segmento JT LWPA|Contém um elemento que define dados analíticos para uma determinada peça. O LWPA inclui a coleção de superfícies analíticas na definição b-rep da peça.

## Compressão ##

Os requisitos de transmissão e armazenamento de modelos 3D são mais exigentes, portanto, os arquivos JT podem se beneficiar da compactação. Um modelo de dados JT pode ser composto de diferentes arquivos usando diferentes técnicas de compactação, mas o processo de compactação é transparente para o usuário de dados JT.

Até agora, o JT Open Toolkit (como padrão) e a compactação avançada são duas técnicas de compactação usadas pelos arquivos JT. O JT Open Toolkit emprega um algoritmo de compactação fácil e sem perdas, enquanto a compactação avançada emprega uma técnica de compactação mais refinada e específica do domínio que leva à compactação de geometria com perdas. Os aplicativos cliente preferem a compactação avançada em vez de usar a compactação padrão, pois a compactação avançada gera taxas de compactação bastante altas. A compatibilidade com versões anteriores com aplicativos comuns de visualização de arquivos JT é mantida através do fornecimento de compactação padrão. O formulário de compactação deve ser compatível com a versão do formato de arquivo JT que pode ser visto quando um arquivo JT é aberto usando o editor de texto e incluído nas informações do cabeçalho ASCII.

## Referências ##

* [Referência de formato de arquivo JT](https://www.plm.automation.siemens.com/en_us/Images/JT-v10-file-format-reference-rev-B_tcm1023-233786.pdf)
* [JT (formato de visualização)](https://en.wikipedia.org/wiki/JT_(formato de visualização)#Data_model)

