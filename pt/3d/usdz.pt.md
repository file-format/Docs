{
  "date" : "2021-02-01",
  "keywords" :[ "usdz", "arquivo usdz", "formato de arquivo usdz", "formato de arquivo", "3d", "download de arquivo usdz"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"USDZ - Formato ZIP de Descrição de Cena Universal",
  "description":"Saiba mais sobre o formato de arquivo USDZ e APIs que podem abrir e criar arquivos USDZ.",
  "linktitle" : "USDZ",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2021-02-01"
}

## O que é um arquivo USDZ?

Um arquivo com .usdz é um arquivo ZIP descompactado e não criptografado para o formato de arquivo [USD](/pt/3d/usd/) (Universal Scene Description) que contém e proxies para arquivos de outros formatos (como texturas e animações) incorporados o arquivo e os executa diretamente com o tempo de execução do USD sem a necessidade de descompactar. Os arquivos USDZ são pacotes cujo design é baseado na nova abstração de nível Ar de um pacote. Usdz foi registrado na IANA e tem o nome do tipo de mídia do modelo e um nome do subtipo vnd.usd+zip e seus detalhes podem ser encontrados na [página de registro da IANA](https://www.iana.org/assignments/media- types/model/vnd.usdz+zip).

## Formato de arquivo USDZ

Os arquivos USDZ são baseados no formato de arquivo ZIP que arquiva arquivos individuais em seu contêiner. Isso permite que o receptor apenas descompacte o conteúdo e use os arquivos normais de descrição de cena do USD para trabalhar e inspecionar. Quase todos os sistemas operacionais fornecem suporte integrado para os formatos de arquivo ZIP e a escolha desse formato de arquivamento em vez de qualquer método personalizado torna fácil para os arquivos USDZ serem úteis como um protocolo de transporte simples.

### Restrições ZIP

O formato de arquivo USDZ usa o formato de arquivo ZIP sem qualquer `compressão` e `criptografia`. Isso foi projetado para atender a dois requisitos:

* Para um pacote já carregado na memória ou como um único arquivo em disco, as APIs estão disponíveis em USD para acessar os dados contidos na imagem
* Não deve haver necessidade de extrair arquivos para o disco ou alocar mais armazenamento heap

Com o USDZ, ambos os requisitos são atendidos, pois a maioria dos formatos de imagem permite esquemas de compactação internos, resultando em tamanho de arquivo compacto.

### Requisitos de layout

Os pacotes USDZ exigem que o layout dos arquivos dentro do pacote seja que os dados de cada arquivo comecem em um múltiplo de 64 bytes desde o início do pacote. No entanto, o pacote deve começar com um arquivo nativo [USD](/pt/3d/usd/) no caso de direcionar o pacote com uma referência simples. Nesse caso, esse primeiro arquivo USD é chamado de Camada Padrão. Os clientes que desejam fornecer "conteúdo de streaming" também podem considerar outras restrições de layout.

## Download do arquivo USDZ
Como os arquivos usdz são embalados com outras imagens de alta qualidade e arquivos usd, eles podem ocupar mais espaço de armazenamento em disco. Aqui você pode encontrar um arquivo de exemplo USDZ simples e menor para download:

- [Amostra.usdz](../amostra.usdz)

## Referências

* [Especificações de formato de arquivo USDZ](https://graphics.pixar.com/usd/docs/Usdz-File-Format-Specification.html)

