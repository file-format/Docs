{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo dng", "formato de arquivo dng", "o que é um arquivo dng", "arquivo", "exemplo dng", "extensão de arquivo dng", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DNG - Formato de arquivo de imagem de câmera digital",
  "description":"Saiba mais sobre o formato de arquivo DNG e as APIs que podem criar e abrir arquivos DNG.",
  "linktitle" : "DNG",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DNG?

DNG é um formato de imagem de câmera digital usado para o armazenamento de arquivos raw. Foi desenvolvido pela Adobe em setembro de 2004. Foi desenvolvido basicamente para fotografia digital. DNG é uma extensão do formato padrão [TIFF](/pt/image/tiff/)/EP e usa metadados de forma significativa. Para manipular dados brutos de câmeras digitais com a facilidade de flexibilidade e controle artístico, os fotógrafos optam por arquivos camera raw. Os formatos JPEG e TIFF armazenam imagens que são processadas pela câmera, portanto, não há muito espaço para alteração nesses formatos.

## Histórico e versões do formato de arquivo DNG

Até agora, houve 5 versões da especificação DNG até agora. A versão 1.0.0.0 foi lançada em setembro de 2004 junto com o lançamento do "2.3" (ACR e DNG Converter). Em fevereiro de 2005 foi publicada a versão 1.1.0.0. Em maio de 2008 a versão 1.2.0.0 foi lançada e foi usada em "4.4". A versão 1.3.0.0 foi publicada em junho de 2009. A versão 1.4.0.0 apareceu em 2012.

## Formato de arquivo DNG

Enquanto os arquivos camera raw capturam dados não processados ou pouco processados diretamente do sensor. Como eles são semelhantes aos negativos de filme, os formatos camera raw também são conhecidos como “Negativos Digitais”. O benefício dos formatos brutos é o aumento do controle artístico para o usuário final. O usuário pode ajustar várias faixas de parâmetros de acordo com os requisitos, como balanço de branco, mapeamento de tom, redução de ruído, nitidez e assim por diante. Por outro lado, o arquivo camera raw deve ser processado para qualquer uso através de qualquer software ou através de um conversor.

Como não havia um formato padrão disponível para arquivos camera raw, isso criou vários problemas para o usuário final. Esses problemas foram resolvidos pela Adobe e definiram um formato não proprietário para arquivos camera raw. O formato é conhecido como Digital Negative ou DNG. O DNG pode ser usado por uma ampla variedade de hardware e software para o processamento de arquivos brutos. Além disso, o DNG também pode ser usado como um formato intermediário para armazenar imagens que foram capturadas originalmente por câmeras com seus próprios formatos raw proprietários.

### Especificações de formato de arquivo DNG

Nesta seção, descreveremos o formato DNG como uma extensão do TIFF 6.0.

* **Extensões de arquivo**: DNG usa extensões “.DNG” ou “.TIF”.
* **Árvores SubIFD**: O DNG não suporta cadeias SubIFD, em vez disso, o DNG recomenda o uso de árvores SubIFD conforme mencionado nas especificações TIFF-EP. A mais alta qualidade e resolução podem usar NewSubFileType de 0, enquanto as miniaturas de qualidade reduzida devem usar NewSubFileType igual a 1. Também é recomendado, embora não obrigatório, que o primeiro IFD tenha uma miniatura de baixa qualidade ou resolução.
* **Byte Order**: A ordem dos bytes deve ser suportada pelos leitores DNG, também para arquivos de um modelo de câmera específico.
* **Pixels mascarados**: a maioria dos sensores da câmera calcula pixels totalmente mascarados na borda do sensor por meio da codificação preta. Esses pixels podem ser incluídos ou cortados antes que a imagem seja armazenada no formato DNG. Se os pixels mascarados não forem aparados, a área desses pixels deve ser mencionada na tag ActiveArea. As informações coletadas desses pixels sobre o nível de codificação de preto devem ser usadas antes que os dados brutos sejam armazenados ou podem ser incluídos no arquivo DNG especificando o nível de preto.
* **Pixels defeituosos**: antes de armazenar dados brutos como DNG, os pixels defeituosos devem ser excluídos.
* **Metadados**: Os metadados podem ser incluídos no DNG de uma das seguintes maneiras:
** Usando tags de metadados TIFF-EP ou EXIF
** Através da tag de metadados IPTC (33723)
** Usando a tag de metadados XMP (700)
* **Dados proprietários**: Normalmente, os fornecedores incluem dados proprietários em arquivos brutos para serem usados por seus próprios conversores. O DNG armazena seus dados proprietários em tags privadas, IFDs privados e em um MakerNote privado. Os fornecedores devem usar as tags DNGPrivateData e MakerNoteSafety para garantir que os aplicativos que editam arquivos DNG preservem esses dados proprietários.

A seguir estão algumas restrições importantes e extensões de tags TIFF.

**BitsPorAmostra**

8 a 32 bits/amostra são suportados. Deve haver a mesma profundidade para cada amostra quando SamplesPerPixel não for igual a 1. Mas se BitsPerSample não for igual a 8 ou 16 ou 32, então os bits devem ser compactados em bytes usando o padrão TIFF FillOrder de 1 (big-endian).

**Compressão**

Dois valores de tag de compactação são compatíveis:

* Valor # 1: Dados não compactados.
* Valor # 7: dados compactados JPEG, seja DCT JPEG de linha de base ou compactação JPEG sem perdas.

**Interpretação Fotométrica**

Os seguintes valores são suportados apenas para IFDs de miniatura e visualização:

* 1 = PretoIsZero. Presume-se que esteja em um espaço de cores gama 2.2.
* 2 = RGB. Presume-se que esteja no espaço de cores sRGB.
* 6 = YCbCr. Usado para imagens de visualização codificadas JPEG.

Os valores a seguir são suportados para o IFD bruto e são considerados o espaço de cores nativo da câmera:

* 32803 # CFA (Color Filter Array).
* 34892 #LinearRaw.

**Orientação**

A tag de orientação é usada para navegadores de arquivos para que eles possam executar a rotação sem perdas de arquivos DNG. Os leitores DNG devem suportar todas as orientações possíveis, incluindo orientações espelhadas.

## Recursos na versão mais recente do DNG

O DNG Versão 1.4 de outubro de 2012 possui os seguintes recursos avançados.

* Corte de usuário padrão
* Transparência
* Ponto flutuante (HDR)
* Compressão com perda
* Procuradores

## Referências ##

* [Especificações DNG - Por Adobe](https://web.archive.org/web/20170829200857/http://wwwimages.adobe.com/content/dam/Adobe/en/products/photoshop/pdfs/dng_spec_1.4.0.0.pdf)
* [Digital Negative - Wikipedia](https://en.wikipedia.org/wiki/Digital_Negative)
* [DNG - O formato de arquivo público para dados brutos de câmeras digitais](https://helpx.adobe.com/photoshop/digital-negative.html)

