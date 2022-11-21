{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo mst", "formato de arquivo mst", "o que é um arquivo mst", "arquivo", "exemplo mst", "extensão de arquivo mst", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
	

},
  "draft" : "false",
  "toc" : true,
  "title" :"LBR - LU Library Archive Format",
  "description":"Saiba mais sobre o formato de arquivo LBR e as APIs que podem criar e abrir arquivos LBR.",
  "linktitle" : "LBR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-19"
}

## O que é um arquivo LBR?

Um arquivo com extensão .lbr é um arquivo criado com o programa LU e usado em sistemas operacionais CP/M e DOS durante a década de 1980. Ele não está mais sendo usado e foi substituído por formatos de arquivo de arquivamento modernos. O formato não compacta os arquivos membros e atua como um arquivo de contêiner para eles. O recurso de arquivamento foi usado principalmente para transferência de arquivos arquivados pela Internet. Como o LBR não oferecia compactação, outros utilitários como SQ ou CRUNCH foram usados para compactar o pré-arquivamento dos arquivos membros ou o arquivo resultante pós-arquivamento para reduzir seu tamanho.

## Formato de arquivo LBR

O formato de arquivo LBR foi projetado por Gary P. Novosielski e não possui detalhes técnicos disponíveis publicamente. Os arquivos LBR começam com um byte 0x00, seguido por 11 espaços (0x20), depois dois bytes 0x00 e dois bytes que não são ambos 0x00. Sendo o formato de arquivo container, pode ser extraído utilizando o LU.COM e o NULU.COM.

## Referências

* [LBR - Wikipedia](https://en.wikipedia.org/wiki/LBR_(file_format))

