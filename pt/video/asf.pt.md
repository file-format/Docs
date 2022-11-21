{
  "date" : "2021-02-15",
  "keywords" :[ "arquivo asf", "formato de arquivo asf", "o que é um arquivo asf", "arquivo", "exemplo asf", "extensão de arquivo asf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASF - Formato de arquivo de sistemas avançados",
  "description":"Saiba mais sobre o formato de arquivo ASF e APIs que podem criar e abrir arquivos ASF.",
  "linktitle" : "ASF",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## O que é um arquivo ASF?

Um arquivo com extensão .asf é um formato de arquivo multimídia para armazenar e reproduzir fluxos de mídia digital pela rede. É um formato de arquivo contêiner que pode ter conteúdo de vídeo e áudio para streaming online. Você raramente encontrará arquivos ASF e, mais provavelmente, encontrará os arquivos Windows Media Audio ([WMA](/pt/audio/wma/)) e Windows Media Video ([WMV](/pt/video/wmv/)) que especificam arquivos ASF tendo conteúdo codificado com os respectivos codecs. Os arquivos de mídia do Windows podem ser criados e lidos usando o SDK do Windows Media Format.

## Formato de arquivo ASF

Um arquivo ASF pode incluir vários fluxos independentes ou dependentes. Isso pode incluir vários fluxos de áudio para áudio multicanal ou vários fluxos de vídeo com taxa de bits. As múltiplas taxas de bits tornam os fluxos adequados para transmissão em diferentes larguras de banda. Além disso, os fluxos em um arquivo ASF podem estar em formato compactado ou não compactado. A melhor compactação é obtida com os codecs de áudio e vídeo do Microsoft Windows Media 9 Series. As especificações completas do formato de arquivo ASF estão disponíveis no [site da Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc).

### Estrutura de arquivo de nível superior ASF

Os arquivos ASF contêm logicamente três tipos de objetos de nível superior:

* `Header Object` - obrigatório e deve ser colocado no início de cada arquivo ASF
* `Data Object` - obrigatório e deve seguir o objeto de cabeçalho
* `Index Object(s)` - opcional, mas útil para fornecer acesso aleatório baseado em tempo em arquivos ASF

A imagem a seguir mostra a estrutura de arquivos de nível superior dos arquivos ASF.

![ASF File Structure](../asf.png "ASF File Structure")

#### Objeto de cabeçalho de nível superior ASF

O objeto Header fornece uma sequência de bytes bem conhecida no início dos arquivos ASF e, opcionalmente, pode conter metadados, como informações bibliográficas. Ele contém todas as informações necessárias para interpretar adequadamente as informações dentro do objeto de dados. O objeto de cabeçalho pode incluir vários objetos padrão, incluindo, mas não limitado a:

* Objeto Propriedades de Arquivo - Contém atributos globais de arquivo.
* Stream Properties Object - Define um fluxo de mídia digital e suas características.
* Header Extension Object - Permite que funcionalidades adicionais sejam adicionadas a um arquivo ASF enquanto mantém a compatibilidade com versões anteriores.
* Objeto Descrição de Conteúdo - Contém informações bibliográficas.
* Script Command Object - Contém comandos que podem ser executados na linha do tempo de reprodução.
* Marker Object - Fornece pontos de salto nomeados dentro de um arquivo.

O Header Object é representado usando a seguinte estrutura:

|Nome do campo |Tipo de campo |Tamanho (bits)|
---|---|---|
|ID do objeto| GUID| 128|
|Tamanho do objeto| QWORD| 64|
|Número de objetos de cabeçalho| DWORD| 32|
|Reservado1| BYTE| 8|
|Reservado2| BYTE| 8|

#### Objeto de dados de nível superior ASF

Todos os dados de mídia digital para um arquivo ASF estão contidos no objeto de dados e são armazenados na forma de pacotes de dados ASF. Cada pacote de dados tem um comprimento fixo e contém dados para um ou mais fluxos de mídia digital.

#### Objetos de índice de nível superior ASF

Os objetos de índice de nível superior ASF têm os dois tipos a seguir:

* `Simple Index Object` - Contém um índice baseado em tempo dos dados de vídeo em um arquivo ASF. O intervalo de tempo entre as entradas do índice é constante e é armazenado no Simple Index Object.
* `Index Object` - Refere-se ao Index Object, ao Media Object Index Object e ao Timecode Index Object, cujos formatos são semelhantes. Assim como o Simple Index Object, o Index Object indexa por tempo com um intervalo de tempo fixo, mas não se limita a fluxos de vídeo.

## Referências

* [Formato de arquivo ASF - Microsoft](https://download.microsoft.com/download/7/9/0/790fecaa-f64a-4a5e-a430-0bccdab3f1b4/ASF_Specification.doc)
* [QuickTime File Format - Wikipedia](https://en.wikipedia.org/wiki/QuickTime_File_Format)

