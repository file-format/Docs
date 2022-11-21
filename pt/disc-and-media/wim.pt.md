{
  "date" : "2021-08-11",
  "keywords" :[ "arquivo wim", "formato de arquivo wim", "o que é um arquivo wim", "arquivo", "exemplo wim", "extensão de arquivo wim","extensão", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo WIM e APIs que podem criar e abrir arquivos WIM.",
  "title" :"WIM - Arquivo de formato de imagem do Windows",
  "linktitle" : "WIM",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## O que é um arquivo WIM?
Os arquivos com extensões .wim foram vistos pela primeira vez no Windows Vista. O WIM pertence a um formato de imagem baseado em arquivo que foi normalmente introduzido no Microsoft Windows Vista. Ele permite que uma única imagem de disco seja implantada em várias plataformas de computador. Os arquivos WIM são usados para gerenciar arquivos como atualizações, drivers e componentes sem reinicializar a imagem do sistema operacional. O arquivo AQ WIM contém um conjunto de arquivos e metadados associados que são muito semelhantes a outros formatos de arquivo de disco.

## Formatos de arquivo WIM
O formato de arquivo WIM não é como os formatos baseados em setor, como VHD ou IS, na verdade, é baseado em arquivo, o que significa que a unidade fundamental de informação em um WIM é um arquivo. O benefício básico de ser baseado em arquivo é que um armazenamento de instância única de um arquivo referenciado várias vezes na árvore do sistema de arquivos e independência de hardware. Arquivo. Os arquivos WIM podem armazenar várias imagens de disco, que são referenciadas por seu nome exclusivo ou por seu índice numérico.
### Suporte para algoritmos de compressão
O WIM suporta as seguintes famílias de algoritmos de compressão em velocidade descendente e proporção ascendente:
- XPRESS
- LZX
- LZMS
- Compressão sólida.
As três primeiras famílias são baseadas em LZ77, enquanto a compactação sólida foi introduzida junto com LZMS no WIMGAPI Windows 8 e DISM Windows 8.1.
### Ferramentas para formato de arquivo WIM
As seguintes ferramentas geralmente suportam o formato de arquivo WIM:

- **ImageX**: uma ferramenta de linha de comando usada para editar, criar e implantar imagens de disco do Windows no Windows Imaging Format. Junto com o WIMGAPI relevante, é distribuído como parte do Kit de Instalação Automatizada do Windows gratuito. A partir do Windows Vista, a Instalação do Windows usa a API WAIK para instalar o Windows.
- **DISM**: uma ferramenta introduzida no Windows 7 e no Windows Server 2008 R2 que pode executar tarefas relacionadas ao serviço em uma imagem de instalação do Windows, seja uma imagem online ou uma imagem offline em uma pasta ou arquivo WIM. essa ferramenta era capaz de montar e desmontar imagens, adicionar um driver de dispositivo a uma imagem offline e consultar drivers de dispositivo instalados em uma imagem offline.
 




## Referências


* [Windows Imaging Format - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Imaging_Format)


