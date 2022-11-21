{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"PCL",
  "description":"Saiba mais sobre o formato de arquivo PCL e APIs que podem criar e abrir arquivos PCL.",
  "linktitle" : "PCL",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo PCL? ##

PCL significa Printer Command Language, que é uma linguagem de descrição de página introduzida pela Hewlett Packard (HP). A HP criou o PCL para fornecer uma maneira eficiente de controlar os recursos da impressora em vários dispositivos de impressão diferentes. O formato foi originalmente desenvolvido para as impressoras matriciais e jato de tinta da HP, mas com o passar do tempo fez parte de várias impressoras térmicas, matriciais e de página. O formato passou por várias revisões diferentes, resultando em diferentes versões onde cada versão foi aprimorada para atender às demandas de tempo em relação aos recursos de controle da impressora. Hoje, PCL é a linguagem de impressora mais difundida no mercado de impressoras de última geração.

## Versões PCL ##

As versões PCL diferem em funcionalidade (por exemplo, suporte ao tipo de fonte: fontes bitmap, fontes escaláveis (Intellifonts, fontes TrueType), métodos de compactação de gráficos raster, suporte gráfico HP-GL/2).

**PCL 1:** por volta de 1980 - A funcionalidade Imprimir e Espaço é o conjunto básico de funções fornecidas para saída de estação de trabalho simples, conveniente e de usuário único.

**PCL 2:** por volta de 1980 - A funcionalidade EDP (Processamento Eletrônico de Dados)/Transação é um superconjunto de PCL 1. As funções foram adicionadas para impressão de sistema multiusuário de uso geral.

**PCL 3**: 1984 - A funcionalidade Office Word Processing é um superconjunto do PCL 2. Foram adicionadas funções para produção de documentos de escritório de alta qualidade e aumento de dpi até 300 dpi. Ele permitia o uso de um número limitado de fontes e gráficos de bitmap e suportava HP-GL. O PCL 3 foi amplamente imitado por outros fabricantes de impressoras e foi referido por essas empresas como “LaserJet Plus Emulation”.
(Impressoras: família HP DeskJet, impressora série HP LaserJet, impressora série HP LaserJet Plus)

**PCL3+:** Usado pela família de impressoras DeskJet e DesignJet.

**PCL3c:** Usado pela família de impressoras DeskJet e DesignJet.

**PCL3e**: Usado pela família de impressoras DeskJet e DesignJet. Agora usado no PhotoSmart também.

**PCL3GUI**: Usa RTL e é usado pela família de impressoras DeskJet e DesignJet.

**PCLSLEEK**: Usa RTL e é usado pela família de impressoras DeskJet e DesignJet.

**PCL 4**: 1985 - A funcionalidade de formatação de página é um superconjunto de PCL 3. Macros compatíveis, fontes de bitmap maiores e gráficos. (Impressoras: HP LaserJet II, HP LaserJet IIP (PCL 4.5))

**PCL 5:** 1990 - A funcionalidade Office Publishing é um superconjunto do PCL 4. Os novos recursos de publicação incluem dimensionamento de fonte e gráficos HP-GL/2 (vetor). (Impressoras: HP LaserJet III)

**PCL 5e:** 1994 - Esta é uma revisão importante, que inclui novos recursos como Adaptive Compression System, codificação de caracteres de 2 bytes, suporte para fontes vetoriais e comandos de configuração bidirecional. Inclui operações lógicas (corresponde a GDI ROPs) para melhorar o suporte do Windows antes de cortar caminhos. (Impressoras: HP LaserJet 4)

**PCL 5j:** novos recursos, como suporte a caracteres de 2 bytes para fontes escaláveis residentes em japonês, escrita vertical, tamanhos de papel em japonês e strings de tipo de letra. (Impressoras: HP LaserJet 4PJ)

**PCL 5c:** 1995 - O suporte a cores e operações lógicas foi adicionado ao PCL5. PCL5c antecede PCL5e. Alguns modelos também suportam caminhos de recorte. (Impressoras: HP Color LaserJet, HP PaintJet 300 XL (primeira impressora com PCL5c), HP DeskJet 1200C/1600C (esses números de modelo foram reutilizados e os modelos mais recentes não são PCL 5c)

**PCL 5ce:** suporta fontes escaláveis Agfa Microtype. (Impressoras: Impressora HP 2500c Pro)

**PCL 6 / XL:** 1996 - PCL 6 ou PCL XL é um novo formato introduzido em 1995, que não é compatível com nenhuma versão anterior do PCL. (Impressoras: HP LaserJet 5, 5M e 5N)

## Visão geral do PCL 6 ##

A HP introduziu o PCL 6 em 1996, que foi a próxima evolução da linguagem PCL e tecnologias relacionadas. Tem os seguintes componentes:

**PCL 6 Enhanced:** fornece versão otimizada para impressão a partir de interfaces gráficas de usuário (GUIs) como MS Windows e OS/2

**PCL 6 Standard:** oferece compatibilidade retroativa completa com impressoras HP LaserJet anteriores

**Síntese de fontes PCL:** fornece fontes escalonáveis, gerenciamento de fontes e armazenamento de formulários e fontes.

A versão estendida PCL XL está mais próxima do GDI que muitos aplicativos usam. Ele garante que menos traduções ocorram, resultando em recursos WYSIWYG aprimorados e melhor desempenho com aplicativos que suportam escapes implementados pelo driver aprimorado. A saída do driver Enhanced (PCL XL) pode não ser igual à saída do driver Standard. Se a saída não for a esperada, escolha o driver Padrão (PCL5e).

Os comandos PCL 6 Enhanced foram projetados para corresponder de maneira ideal aos requisitos de impressão de gráficos para aplicativos baseados em GUI. Na maioria dos casos, para cada comando de impressão de gráficos que uma GUI deseja executar, há um comando PCL 6 Enhanced correspondente. Isso reduz o número de comandos necessários para descrever uma página de gráficos. Cada comando no PCL 6 Enhanced foi projetado para exigir uma transferência mínima de dados do PC host para a impressora. Isso reduz a quantidade de dados necessários para descrever uma página.

O Windows Printing System para a maioria das impressoras HP LaserJet fornece dois drivers separados: Standard e Enhanced. O driver Standard oferece compatibilidade com versões anteriores usando comandos PCL 6 Standard (PCL5e) para imprimir texto simples ou texto misto e páginas gráficas. O driver Enhanced utiliza os comandos PCL 6 Enhanced que foram otimizados para imprimir páginas gráficas complexas.

## Revisões de Classe PCL 6 ##

#### Classe 1.1 ####

**Ferramentas de desenho:** suporte para desenhar linhas, arcos/elipses/acordes, retângulos (arredondados), polígonos, caminhos de Bézier, caminhos recortados, imagens rasterizadas, linhas de varredura, operações rasterizadas.
**Manuseio de cores:** Suporta paletas de 1/4/8 bits, espaço de cores RGB/cinza. Suporta padrões de meio-tom personalizados (máximo de 256 padrões).
**Compressão:** é compatível com RLE.
**Unidades de medida:** Polegada, milímetro, décimo de milímetro.
**Manuseio de papel:** Suporta conjuntos personalizados ou predefinidos de tipos de papel, incluindo comum Carta, Ofício, A4, etc. Pode escolher papel de alimentação manual, bandejas, cassetes. O papel pode ser duplexado horizontalmente ou verticalmente. O papel pode ser orientado em retrato, paisagem ou rotação de 180 graus dos dois primeiros.
**Fonte:** suporta fontes bitmap ou TrueType, pontos de código de 8 ou 16 bits. A escolha do conjunto de caracteres usa um código de conjunto de símbolos diferente do PCL 5. Quando a fonte bitmap é usada, muitos comandos de dimensionamento ficam indisponíveis. Quando a fonte TrueType é usada, descritores de comprimento variável, blocos de continuação não são suportados. A fonte de contorno pode ser girada, dimensionada ou cortada.

#### Classe 2.0 ####

**Compressão:** foi adicionada uma compressão JPEG proprietária chamada JetReady.
**Manuseio de papel:** a mídia pode ser redirecionada para diferentes bandejas de saída (até 256). Adicionados tamanhos de mídia predefinidos A6 e japonês B6. Adicionado terceiro pré-ajuste de cassete, 248 fontes de mídia de bandeja externa.
**Fonte:** o texto pode ser escrito verticalmente.

#### Classe 2.1 ####

**Manuseio de cores:** Adicionado recurso de correspondência de cores.
**Compressão:** Linha Delta adicionada.
**Manuseio de papel:** Orientação, tamanho da mídia são opcionais ao declarar uma nova página. Adicionados tipos de papel B5, JIS 8K, JIS 16K, JIS Exec.

#### Classe 3.0 ####

**Manuseio de cores:** permite o uso de diferentes configurações de meio-tom para gráficos vetoriais ou raster, texto. Suporta meio-tom adaptável.
**Protocolo:** suporta passagem PCL, permitindo que recursos PCL 5 sejam usados por fluxos PCL 6. No entanto, alguns estados PCL 6 não são preservados ao usar esse recurso.
**Fonte:** compatível com fontes PCL.
**Visualizador/Conversor:** PCLReader (freeware) pode visualizar, converter ou imprimir qualquer nível de PCL 6 (incluindo JetReady) em qualquer impressora.

## Referências ##

* [PCL - Por Wikipedia](https://en.wikipedia.org/wiki/Printer_Command_Language)

