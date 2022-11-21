{
  "date" : "2021-02-10",
  "keywords" :[ "arquivo jpx", "formato de arquivo jpx", "o que é um arquivo jpx", "arquivo", "exemplo jpx", "extensão de arquivo jpx","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JPX - Formato de arquivo de imagem",
  "description":"Saiba mais sobre o formato de arquivo JPX e APIs que podem criar e abrir arquivos JPX.",
  "linktitle" : "JPX",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-02-10"
}

## O que é um arquivo JPX? ##

Um arquivo com extensão .jpx é uma extensão do formato de arquivo JPEG 2000. Ele usa principalmente a compactação JPEG 2000 e também fornece recursos avançados, como várias camadas para uma imagem, vários espaços de cores, opacidade e fluxos de código fragmentados. O JPX também permite outras compactações, como JBIG, CCITT Group3, CCITT Group4, etc., além da compactação JPEG 2000. O formato de arquivo JPX foi aprovado como padrão [ISO/IEC 15444-2](https://www.iso.org/standard/33160.html), mas não pôde receber uma recepção calorosa devido ao uso extensivo de [JPEG ](/pt/imagem/jpeg/) formato de arquivo. Os aplicativos que podem abrir arquivos JPX incluem Corel PaintShop Pro, Adobe Photoshop 2020, Adobe Illustrator 2020 e CorelDraw Graphics Suite 2020.

## Breve história

Em 2000, o comitê do Joint Photographic Experts Group projetou o JP2 com o objetivo de melhorar seu próprio padrão JPEG baseado em transformada de cosseno discreto com este novo método baseado em wavelet. O comitê do JPEG pretendia fornecer seus métodos básicos livres de taxas de licença. Na licença JP2, ganhando concorrência entre 20 empresas, eles venceram por um triz. O JPEG 2000 foi declarado como um padrão ISO, embora a maioria dos navegadores da Web não esteja pronta para dar uma mão ao JPEG 2000 desde 2017. Em 2004, o formato ISO/IEC 15444-2 foi aceito publicamente como extensão do formato de arquivo JP2.

## Formato de arquivo JPX

O formato de arquivo JPX foi formulado para atender aos requisitos de aplicativos que precisavam de estruturas de dados além da funcionalidade definida pelo formato de arquivo [JP2](/pt/image/jp2/). Um arquivo JP2 com extensões não compatíveis pode causar confusão no mercado, onde alguns leitores podem interpretar alguns arquivos JP2, mas não outros. JPX é a resposta para evitar esses problemas em aplicativos.

### Identificação do arquivo

Os arquivos JPX são armazenados como [JPF](/pt/image/jpf/) quando armazenados no sistema de arquivos de computador tradicional. É por isso que o termo JPX é menos usado em comparação com o JPF. Um arquivo JPX começa com os seguintes bytes:

`00 00 00 0c 6a 50 20 20 0d 0a 87 0a ?? ?? ?? ?? 66 74 79 70 6a 70 78 20`

### Organização de arquivos

Semelhante ao JP2, um arquivo JPX é uma coleção de caixas com uma estrutura binária com as caixas organizadas em ordem contígua. A primeira caixa dá o início ao arquivo com seu primeiro byte e o último byte da última caixa representa o último byte do arquivo.
A estrutura binária de uma caixa em um arquivo JPX é idêntica àquela definida no formato de arquivo [JP2](/pt/image/jp2/).

### Armazenamento de CodeStream em JPX

O formato de arquivo JPX permite que o fluxo de código da imagem seja dividido em fragmentos. Isso possibilita modificar um único bloco da imagem e gravar o bloco modificado no final do arquivo sem reescrever o arquivo inteiro. O formato de arquivo original [JP2](/pt/image/jp2/) restringe todo o fluxo de código a ser armazenado em uma parte contígua do arquivo, o que pode ser problemático para aplicativos de edição de imagem que desejam modificar um único bloco da imagem e obter a capacidade de suporte acima pelo formato de arquivo JPX. A fragmentação do fluxo de código da imagem torna o formato de arquivo JPX superior ao formato de arquivo JP2. Além disso, o formato de arquivo JPX permite que vários fluxos de código sejam combinados e produzam resultados renderizados. Codestreams podem ser combinados como composição e animação.

## Referências ##

* [Visão geral do JPEG 2000](https://jpeg.org/jpeg2000)

