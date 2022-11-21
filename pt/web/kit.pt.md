{
  "date" : "2022-07-04",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo KIT e APIs que podem criar e abrir arquivos KIT.",
  "title" :"Formato de arquivo KIT - Arquivo CodeKit",
  "linktitle" : "KIT",
  "menu" : {
    "docs" : {
      "identifier":"web-kit",
      "parent" : "web"
}
},
  "lastmod" : "2022-07-04"
}

## O que é um arquivo KIT?

Um arquivo com extensão .kit é um arquivo HTML que é criado com o aplicativo de linguagem de programação [CodeKit](https://codekitapp.com/). Ele contém `imports` e `variables` além dos arquivos [HTML](/pt/web/html/) existentes, tornando-o ideal para sites estáticos. CodeKit compila arquivos KIT para HTML que podem ser facilmente usados como arquivos estáticos de sites.

## Formato de arquivo KIT

Os arquivos KIT são arquivos HTML que também incluem importações e variáveis. Eles são armazenados como arquivos de texto simples e podem ser abertos com qualquer editor de texto ou editor de arquivos da web.

### Importações de arquivos KIT

Quase qualquer tipo de arquivo pode ser importado para um arquivo Kit. A seguir está a sintaxe de importação usada para importar arquivos para um arquivo .kit.

```
<!-- @import "someFile.kit" -->
<!-- @import "file.html" -->
```

Quando uma importação é adicionada a um arquivo KIT e salva, ela é substituída pelo texto do arquivo que está sendo importado. Você também pode usar @include em vez de @import.

### Importações múltiplas em um arquivo KIT

Você também pode importar mais de um arquivo por vez usando uma lista separada por vírgulas:

```
<!-- @import someFile, otherFile.html, ../thirdFile.kit -->
```

## Referências

* [O que é Kit?](https://codekitapp.com/help/kit/)

