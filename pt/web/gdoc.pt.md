{
  "date" : "2022-01-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo GDOC - Atalho do Google Docs",
  "description":"Saiba mais sobre o que é um arquivo GDOC e APIs que podem criar e abrir arquivos GDOC.",
  "linktitle" : "GDOC",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-01-23"
}

## O que é um arquivo GDOC?

Um arquivo GDOC é um arquivo de atalho que aponta para um arquivo localizado no Google Drive, um serviço de armazenamento de documentos baseado em nuvem. Quando o cliente do Google Drive é instalado em um computador e um documento é criado dentro dele, o drive cria um documento no armazenamento em nuvem on-line e grava o [URL](/pt/web/url/) desse documento no arquivo GDOC no Google local Pasta da unidade. Quando esse arquivo de atalho é clicado duas vezes, o navegador da Web padrão abre o documento a partir do local [URL](/pt/web/url/). Se este arquivo de atalho for movido para fora desta pasta, o link para o documento online será quebrado.

## Formato de arquivo GDOC - Mais informações

O arquivo GDOC contém um atalho para o documento online escrito no formato de arquivo [JSON](/pt/web/json/). O navegador que abre os arquivos GDOC lê as informações de URL e abre o documento vinculado para exibição, desde que o usuário esteja conectado a esta conta do Google onde o documento está armazenado. Os arquivos GDOC não contêm o conteúdo do documento.

### Exemplo de arquivo GDOC

O arquivo GDOC pode ser aberto em um editor de texto e seu conteúdo se parece com o seguinte.

```
{"url": "https://docs.google.com/a/test.com/spreadsheet/ccc?key=01234567898765432123456789&usp=docslist_api", "resource_id": "spreadsheet:0A12345B678HJK9TZPL9078767"}
```

Como pode ser visto, o conteúdo é formatado em JSON tendo a URL de um documento e o ID do documento associado.

## Referências

* [O Google Docs não abre arquivos gdoc ou docx](https://support.google.com/docs/thread/8408691/google-docs-not-opening-either-gdoc-or-docx-files?hl=en )

