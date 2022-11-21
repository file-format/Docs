{
  "date" : "2019-12-12",
  "keywords" :[ "CBC", "extensão", "arquivo", "formato", "Histórias em quadrinhos", "Formato de arquivo de quadrinhos", "eBook" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo CBC e APIs que podem criar e abrir arquivos CBC.",
  "title" :"CBC - Formato de arquivo de coleção de quadrinhos",
  "linktitle" : "CBC",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-03"
}

## O que é um arquivo CBC?

Um arquivo com extensão .cbc é uma coleção compactada de arquivos de quadrinhos para eBooks e contém arquivos [CBZ](/pt/ebook/cbz/) e [CBR](/pt/ebook/cbr/). Ele é usado pelo [Calibre](https://calibre-ebook.com/), um aplicativo de conversão de e-books, que é um gerenciador de e-books de código aberto multiplataforma e permite gerenciar seus e-books e convertê-los em diferentes formatos . Um arquivo CBC contém um arquivo .txt, comics.txt, que lista outros arquivos que fazem parte do arquivo. Vários aplicativos estão disponíveis on-line que podem converter arquivos CBC para [AZW3](/pt/ebook/azw3), [EPUB](/pt/ebook/epub/), [FB2](/pt/ebook/fb2/), [MOBI](/pt/ebook/ mobi/), [TXT](/pt/word-processing/txt/), [PDF](/pt/pdf/) e outros formatos de arquivo populares.

## Formato de arquivo CBC

Os arquivos CBC são arquivos compactados que contêm CBZ, CBR e um arquivo de texto para listar o conteúdo. O arquivo de texto, comics.txt é codificado em UTF8 e contém uma lista dos arquivos CBC a serem usados pelos leitores para organizar suas coleções. Um arquivo CBC geralmente possui vários atributos que permitem a organização dessa coleção, como Quadrinhos, Categoria, Editora, Série, Edição e Artista.

O conteúdo de um arquivo CBC de amostra é listado da seguinte forma:

* comics.txt - Arquivo de texto que contém lista de arquivos CBR e CBZ
* 1.cbz
* 2.cbz
* 3.cbz
* Arquivo(s) CBZ

onde o arquivo comics.txt lista o conteúdo da seguinte forma:

* 1.cbz: Primeiro Capítulo
* 2.cbz: Segundo Capítulo
* 3.cbz: Terceiro Capítulo

Os leitores processam o arquivo comics.txt e geram o índice com base nos dados fornecidos.

## Referências

* [Calibre](https://calibre-ebook.com/)

