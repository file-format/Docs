{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo tar", "formato de arquivo tar", "o que é um arquivo tar", "arquivo", "exemplo tar", "extensão do arquivo tar", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TAR - Formato de arquivo de arquivo Unix",
  "description":"Saiba mais sobre o que é um arquivo Tar e APIs que podem criar e abrir arquivos TAR.",
  "linktitle" : "TAR",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo TAR?

Arquivos com extensão .tar são arquivos criados com utilitário baseado em Unix para coletar um ou mais arquivos. Vários arquivos são armazenados em um formato não compactado com o suporte de adicionar arquivos e pastas ao arquivo. O utilitário TAR no Unix é baseado em comandos, mas os arquivos criados são suportados pela maioria dos sistemas de arquivamento de arquivos em quase todos os sistemas operacionais. Foi criado pela primeira vez em 1979 pelos Laboratórios AT&T Bell e as versões subsequentes foram publicadas com o passar do tempo.

## Formato de arquivo TAR

TAR é um formato de arquivo aberto com especificações completas disponíveis para referência do desenvolvedor. Sua estrutura de arquivos foi padronizada no POSIX.1-1988 e posteriormente no POSIX.1-2001. Os conjuntos de dados criados pelo tar retêm informações sobre os parâmetros do sistema de arquivos, como:

* Nome
* Carimbos de tempo
* Propriedade
* Permissões de acesso a arquivos
* Organização do diretório

Um arquivo Tar não tem nenhum número mágico. Ele contém uma série de blocos onde cada bloco é de bytes BLOCKSIZE.

Cada arquivo arquivado é representado por um bloco de cabeçalho que descreve o arquivo, seguido por zero ou mais blocos que fornecem o conteúdo do arquivo. No final do arquivo há dois blocos de 512 bytes preenchidos com zeros binários como marcador de final de arquivo. Um sistema razoável deve escrever tal marcador de fim de arquivo no final de um arquivo, mas não deve assumir que tal bloco existe ao ler um arquivo. Em particular, o GNU tar sempre emite um aviso se não encontrá-lo.

Os blocos podem ser bloqueados para operações físicas de E/S. Cada registro de n blocos (onde n é definido pela opção blocking-factor = 512-size para tar) é gravado com uma única operação "write()". Em fitas magnéticas, o resultado de tal gravação é um único registro. Ao escrever um arquivo, o último registro de blocos deve ser escrito em tamanho real, com os blocos após o bloco zero contendo todos os zeros. Ao ler um arquivo, um sistema razoável deve tratar adequadamente um arquivo cujo último registro seja mais curto que o restante, ou que contenha registros de lixo após um bloco zero.

### Cabeçalho de alcatrão

Como qualquer outro cabeçalho de arquivo, o registro de cabeçalho do arquivo tar contém metadados sobre um arquivo e é mostrado na tabela a seguir.


|Deslocamento do campo|Tamanho do campo (Bytes)|Campo
---|---|---|
|0|100|Nome do arquivo
|100|8|Modo de arquivo
|108|8|ID de usuário numérico do proprietário
|116|8|ID de usuário numérico do grupo
|124|12|Tamanho do arquivo em bytes (base octal)
|136|12|Hora da última modificação no formato numérico Unix (octal)
|148|8|Soma de verificação para registro de cabeçalho
|156|1|Indicador de link (tipo de arquivo)
|157|100|Nome do arquivo vinculado

Os campos não utilizados são preenchidos com bytes NUL. Um cabeçalho é composto por 257 bytes que são preenchidos com bytes NUL para preencher o registro de 512 bytes.

## Referências ##

* [TAR - Por Wikipedia](https://en.wikipedia.org/wiki/Tar_(computing))
* [Formato Básico TAR](https://www.gnu.org/software/tar/manual/html_node/Standard.html)

