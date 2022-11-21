{
  "date" : "2019-12-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo ZIM - Arquivo de arquivo OpenZIM",
  "description":"Saiba mais sobre o formato de arquivo ZIM e APIs que podem criar e abrir arquivos ZIM.",
  "linktitle" : "ZIM",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-12-09"
}

## O que é um arquivo ZIM? ##

Arquivos com extensão .zim são arquivos criados para armazenar o conteúdo do Wiki offline. É considerado o formato de arquivo aberto mais adequado para armazenar a Wikipedia em um USB. Ele armazena o conteúdo do site em um formato compacto. Seu nome vem de "Zeno IMproved", que era o formato de arquivo Zeno anterior. O ZIM é mantido pelo projeto [openZIM ](https://openzim.org/) que é patrocinado pela Wikimedia CH e apoiado pela Wikimedia Foundation. Os arquivos ZIM podem ser abertos por aplicativos como Kiwix e ZIMReader. O projeto OpenZIM hospedou a implementação do formato de arquivo ZIM no [Github](https://github.com/openzim) para contribuição da comunidade OpenSource.

## Especificações de formato de arquivo ZIM

O formato de arquivo ZIM foi desenvolvido em cima do [formato de arquivo Zeno](https://openzim.org/wiki/Zeno_file_format) e não é compatível com versões anteriores. As especificações de formato do formato de arquivo ZIM estão [disponíveis online](https://openzim.org/wiki/ZIM_file_format) por openZIM para referência do desenvolvedor. OpenZIM forneceu implementação de código aberto C++, [LibZim](https://openzim.org/wiki/Zimlib), para leitura e gravação de arquivos ZIM.

O formato de arquivo ZIM usa a compactação LZMA2 para tornar o conteúdo compacto.

{{< figure src="../ZIM_File_Format.jpeg" alt="Formato de arquivo ZIM" >}}


### Cabeçalho ZIM

Um arquivo ZIM começa com um cabeçalho que está no deslocamento 0. Todos os constituintes são baseados em little-endian e todos os inteiros são inteiros sem sinal, ou seja, uint_16, uint_32, uint_64.

|Nome do campo |Tipo| Deslocamento| Comprimento| Descrição|
---|---|---|---|---|
|magicNúmero| inteiro| 0| 4| Número mágico para reconhecer o formato do arquivo, deve ser 72173914 (0x44D495A)|
|majorVersion| inteiro| 4| 2| Versão principal do formato de arquivo ZIM (5 ou 6)|
|menorVersão| inteiro| 6| 2| Versão secundária do formato de arquivo ZIM|
|uuid| inteiro| 8| 16| id exclusivo deste arquivo zim|
|Contagem de artigos| inteiro| 24| 4| número total de artigos|
|Contagem de clusters| inteiro| 28| 4| número total de clusters|
|urlPtrPos| inteiro| 32| 8| posição da lista de ponteiros de diretório ordenada por URL|
|titlePtrPos| inteiro| 40| 8| posição da lista de ponteiros de diretório ordenada por Title|
|clusterPtrPos| inteiro| 48| 8| posição da lista de ponteiros de cluster|
|mimeListPos| inteiro| 56| 8| posição da lista de tipos MIME (também tamanho do cabeçalho)|
|Página principal| inteiro| 64| 4| página principal ou 0xffffffff se não houver página principal|
|página de layout| inteiro| 68| 4| página de layout ou 0xffffffffff se não houver página de layout|
|checksumPos| inteiro| 72| 8| ponteiro para o md5checksum deste arquivo sem o próprio checksum. Isso aponta sempre 16 bytes antes do final do arquivo.|

## Referências ##

* [OpenZIM](https://openzim.org/)
* [C++ LibZim](https://openzim.org/wiki/Zimlib)

