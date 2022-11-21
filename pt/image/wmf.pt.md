{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo wmf", "formato de arquivo wmf", "o que é um arquivo wmf", "arquivo", "exemplo wmf", "extensão de arquivo wmf","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"WMF - Formato de Meta-arquivo do Microsoft Windows",
  "description":"Saiba mais sobre o formato de arquivo WMF e APIs que podem criar e abrir arquivos WMF.",
  "linktitle" : "WMF",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo WMF?

Arquivos com extensão WMF representam o Microsoft Windows Metafile (WMF) para armazenar dados de imagens vetoriais e em formato de bitmap. Para ser mais preciso, o WMF pertence à categoria de formato de arquivo vetorial dos formatos de arquivo gráfico independente de dispositivo. A interface de dispositivo gráfico do Windows (GDI) usa as funções armazenadas em um arquivo WMF para exibir uma imagem na tela. Uma versão mais aprimorada do WMF, conhecida como Enhanced Meta Files (EMF), foi publicada posteriormente, tornando o formato mais rico em recursos. Praticamente, o WMF é semelhante ao SVG.

## Especificações de formato de arquivo WMF ##

Um arquivo WMF referido ao formato de arquivo de 16 bits no momento de sua inicialização com o Windows 3.0. O formato do arquivo consiste em uma série de registros de comprimento variável que contêm comandos de desenho gráfico, definições de objetos e propriedades. Como os arquivos WMF são baseados em comandos renderizados para o GDI para desenhar a imagem, também é conhecido como uma gravação digital da imagem que pode ser reproduzida para reproduzir essa imagem. As especificações completas de formato de arquivo do WMF estão disponíveis online e devem ser consultadas para o desenvolvimento de aplicativos para trabalhar com arquivos WMF. Um arquivo WMF é organizado em:

* Registro de cabeçalho WMF
* Registro(s) WMF
* Registro de fim de arquivo WMF

### Registro de cabeçalho WMF ###

O **META_HEADER Record** contém informações que definem as características do metarquivo, incluindo:

* O tipo do metarquivo
* A versão do metarquivo
* O tamanho do metarquivo
* O número de objetos definidos no metarquivo
* O tamanho do maior registro único no metarquivo

### Registro de cabeçalho posicionável WMF ###

O **META_PLACEABLE Record** contém informações estendidas sobre a imagem, incluindo:

* Um retângulo delimitador
* Tamanho da unidade lógica, para dimensionamento
* Uma soma de verificação, para validação

### Registro WMF ###

Os registros WMF têm um formato genérico, que é especificado no documento de especificações. Cada registro WMF contém as seguintes informações:

* O tamanho do registro
* A função de gravação
* Parâmetros, se houver, para a função de registro

## Referências ##

* [[MS-WMF]: Windows Metafile Format](https://msdn.microsoft.com/en-us/library/cc250370.aspx)
* [Windows MetaFile - Wikipedia](https://en.wikipedia.org/wiki/Windows_Metafile)

