{
  "date" : "2021-04-08",
  "keywords" :[ "arquivo dar", "formato de arquivo dar", "o que é um arquivo dar", "arquivo", "exemplo dar", "extensão de arquivo dar","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DAR - Formato de arquivo do arquivador de disco",
  "description":"Saiba mais sobre o formato de arquivo DAR e APIs que podem criar e abrir arquivos DAR.",
  "linktitle" : "DAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-09"
}

## O que é um arquivo DAR?

Um arquivo com extensão .dar é um arquivo compactado criado usando o arquivo DAR Disk. Ele pode criar backup/arquivo para disco completo ou um grupo de arquivos. Ele foi criado para substituir o formato de arquivo [TAR](/pt/compression/tar/) no sistema operacional UNIX e pode ser criado como arquivos divididos para um grande número de arquivos. O arquivo DAR suporta a opção de excluir arquivos do sistema que estão vinculados aos arquivos principais do arquivo. Seus recursos de fornecer backup diferencial, incremental e decremental o tornam superior aos arquivos TAR.

## Formato de arquivo DAR

Os arquivos DAR são arquivos compactados que podem usar qualquer compactação por arquivo, como [gzip](/pt/compression/gz/), [bzip2](/pt/compression/bz2/), lzo, xz ou lzma. O formato de arquivo exato de um arquivo DAR depende do tipo de formatação usado para compactar o conteúdo do arquivo. Ele também permite criptografia opcional Blowfish, Twofish, AES, Serpent, Camellia e criptografia e assinatura de chave pública (OpenPGP).

### Recursos DAR

Alguns dos recursos do formato de arquivo DAR são os seguintes.

* Cuida de qualquer tipo de inode (diretório, arquivos simples, links simbólicos, dispositivos especiais, pipes nomeados, soquetes, portas, ...)
* Cuida de inodes com link físico (arquivos simples com link físico, dispositivos char, dispositivos de bloco, links simbólicos com link físico)
* Cuida de arquivos esparsos
* Cuida dos atributos estendidos do arquivo Linux,
* Cuida do arquivo Linux ACL
* Cuida das bifurcações de arquivos do Mac OS X
* Cuida de alguns atributos específicos do sistema de arquivos, como data de nascimento do sistema de arquivos HFS + e atributos imutáveis, registro de dados, exclusão segura, fusão sem cauda, não excluível e noatime do sistema de arquivos ext2/3/4.
* Compressão por arquivo com gzip, bzip2, lzo, xz ou lzma (em oposição à compressão de todo o arquivo). Um indivíduo pode optar por não compactar arquivos já compactados com base em seu sufixo de nome de arquivo.
* Extração rápida de arquivos de qualquer lugar do arquivo
* Listagem rápida do conteúdo do arquivo salvando o catálogo de arquivos no arquivo
* Backup do sistema de arquivos ao vivo: detecta quando um arquivo foi modificado enquanto foi lido para backup e pode tentar salvá-lo até um determinado número máximo de tentativas
* Arquivo hash (MD5, SHA1 ou SHA-512) gerado on-fly para cada fatia, o arquivo resultante é compatível com md5sum ou sha1sum, para poder verificar rapidamente a integridade de cada fatia
* Independente do sistema de arquivos: pode ser usado para restaurar um sistema para uma partição de tamanho diferente e/ou para uma partição com um sistema de arquivos diferente[5]

## Referências

* [DAR](http://dar.linux.free.fr/)
* [DAR Disk Archiver](https://en.wikipedia.org/wiki/Dar_(disk_archiver))

