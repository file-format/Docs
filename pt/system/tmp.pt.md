{
  "date" : "2021-07-15",
  "keywords" :[ "TMP", "extensão", "arquivo", "formato", "sistema", "arquivo TMP", "documentos TMP", "arquivos TMP", "arquivo temporário", "aplicativo", "programas" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"TMP - Formato de arquivo temporário",
  "description":"Saiba mais sobre o formato de arquivo TMP e APIs que podem criar e abrir arquivos TMP.",
  "linktitle" : "TMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-15"
}

## O que é um arquivo TMP? ##

Um arquivo TMP refere-se a um backup transitório, armazenamento ou outro sistema de arquivos gerado por um programa de software. Ele é ocasionalmente criado como um arquivo invisível e é frequentemente destruído quando o programa é encerrado. Os arquivos TMP também podem ser usados para armazenar temporariamente informações enquanto um novo arquivo está sendo construído.

## Formato de arquivo TMP ##

Um arquivo TMP normalmente é composto de dados brutos que são utilizados como uma fase no processo de conversão de material de um estilo para outro. Microsoft Word e Apple Safari são dois aplicativos que podem produzir e usar o formato de arquivo TMP.

Os documentos TMP gerados devem, em teoria, ser removidos automaticamente quando o programa for fechado ou a máquina for desligada. Na prática, nem sempre é assim. Como resultado, ao navegar pelos documentos do seu programa, você pode encontrar arquivos temporários que não são usados ativamente pelo sistema ou por qualquer outro software.

### Memória auxiliar ###

A memória virtual é usada em sistemas operacionais, no entanto, programas que utilizam grandes volumes de informações podem precisar criar documentos temporários.

### Comunicação entre processos ###

A maioria dos sistemas operacionais fornece primitivos para passar dados entre programas, como pipes, soquetes ou memória principal, mas o método mais simples é transferir arquivos para um arquivo temporário e avisar o aplicativo receptor da localização do arquivo temporário.


## Especificação Técnica ##

A obtenção de nomes de documentos temporários distintos geralmente é fornecida por sistemas operacionais e programas de software.
Arquivos temporários podem ser gerados com segurança em sistemas POSIX usando as funções de biblioteca mkstemp ou tmpfile. Alguns sistemas incluem o aplicativo mktemp anterior POSIX (desde então). Esses arquivos geralmente são encontrados no diretório temporário regular em plataformas Unix em /TMP ou %TEMP% (é específico para login) em máquinas Windows.

Quando o programa para ou o documento é fechado, o arquivo transitório gerado com o tmpfile é removido automaticamente. GetTempFileName (Windows) ou tmpnam (POSIX) podem ser usados para criar um nome de arquivo temporário que durará mais do que o programa que o criou.

## Referência ##

* [TMP - Wikipedia](https://en.wikipedia.org/wiki/Temporary_file)
