{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo tbz", "formato de arquivo tbz", "o que é um arquivo tbz", "arquivo", "exemplo tbz", "extensão de arquivo tbz","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TBZ - Bzip Compressed Tar Archive",
  "description":"Saiba mais sobre o formato de arquivo TBZ e APIs que podem criar e abrir arquivos TBZ.",
  "linktitle" : "TBZ",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-05"
}

## O que é um arquivo TBZ?

Um arquivo com extensão .tbz é um arquivo compactado que usa compactação BZIP para reduzir o tamanho dos arquivos de conteúdo. Os arquivos TBZ são, na verdade, arquivos arquivados UNIX [TAR](/pt/compression/tar/) que são compactados com BZIP. A compactação de segundo nível mais recente é [BZIP2](/pt/compression/bz2/) que substituiu o BZIP. O formato de arquivo TBZ é adequado para transferir arquivos grandes. Os arquivos TBZ podem ser abertos/extraídos usando aplicativos de software como 7-Zip, PeaZip e jZip. Os usuários de Linux e macOS também podem abrir um TBZ com o comando BZIP2 em uma janela de terminal.

## Formato de arquivo TBZ

Os arquivos TBZ são, na verdade, arquivos compactados criados com compactação BZIP/[BZIP2](/pt/compression/bz2). Não há especificações formais disponíveis para este formato de arquivo. No entanto, [especificações de engenharia reversa] não oficiais (https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf) mostram que um fluxo .bz2 consiste em um cabeçalho de 4 bytes que é seguido por zero ou mais blocos compactados.

## Referências ##

* [Especificações do formato BZIP2](https://github.com/dsnet/compress/blob/master/doc/bzip2-format.pdf)

