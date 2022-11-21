{
  "date" : "2022-04-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo HAML - Arquivo de código-fonte Haml",
  "description":"Saiba mais sobre o formato de arquivo HAML e APIs que podem criar e abrir arquivos HAML.",
  "linktitle" : "HAML",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-04-07"
}

## O que é um arquivo HAML?

Um arquivo HAML é um arquivo de linguagem de marcação de abstração HTML que contém código-fonte escrito na linguagem [Haml](https://haml.info/). Ele pode ser usado como um substituto para o ERB (scripts de template Ruby). O arquivo HAML contém o código-fonte do modelo para gerar o HTML de um documento da web. Os arquivos ERB podem ser substituídos simplesmente substituindo esses arquivos na pasta app/views para Haml, alterando a extensão do arquivo. Os arquivos HAML podem ser abertos com qualquer editor de texto, como Microsoft Notepad, Notepad++, Apple TextEdit,

## Formato de arquivo HAML

Os arquivos HAML são arquivos de origem salvos em disco como arquivos de texto simples. Ele contém código escrito em sintaxe HAML. O HAML substitui as tags **<>** pelo sinal **%** para tornar o código mais simples e fácil. Os arquivos ERB são substituíveis por HAML, conforme mostrado no exemplo simples a seguir.

```
app/views/account/login.html.erb → app/views/account/login.html.haml
```

### Exemplo HAML

A seguir está um exemplo Hello World de HAML.

```
%p{:class => "sample", :id => "welcome"} Hello, World!
%p.sample#welcome Hello, World!
```
que renderiza a seguinte saída HTML.

```
<p class="sample" id="welcome">Hello, World!</p>
```

## Referências

* [HAML - Github](https://github.com/haml/haml)

