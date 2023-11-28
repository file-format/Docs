{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo MASTER - Formato de arquivo de página mestre ASP.NET",
  "description" :"Aprenda sobre o formato de arquivo MASTER e APIs para criar e abrir arquivos MASTER.",
  "linktitle" : "MASTER",
  "menu" : {
    "docs" : {
      "identifier":"web-master",
      "parent" : "web"
}
},
  "lastmod" : "2021-02-29"
}

## O que é um arquivo .MASTER?

Um arquivo MASTER é um arquivo de modelo de página da web mestre criado com ASP.NET. Ele é usado como ponto de partida para a criação de múltiplas páginas que possuem o mesmo layout e configurações do arquivo MASTER. O arquivo MASTER de modelo inclui configurações para cabeçalho, menus de navegação, rodapé, fonte e informações de estilo. Usar um arquivo MASTER ajuda a criar várias páginas da web rapidamente.

Você pode abrir um arquivo MASTER usando o Microsoft Visual Studio 2022 e superior.

## Formato de arquivo MASTER - Mais informações

Um arquivo MASTER é criado e salvo em formato de arquivo HTML e é semelhante a qualquer outro arquivo de página da web. É particionado em seções editáveis e não editáveis. As seções editáveis são aquelas que podem ser modificadas para atender às necessidades do usuário. As seções não editáveis ficam esmaecidas quando o arquivo MASTER é aberto no Microsoft Visual Studio.

As páginas mestras consistem em duas partes, ou seja, a própria página mestra e uma ou mais páginas de conteúdo.

### Pagina principal

A página mestra possui extensão .master e é feita em ASP.NET. Possui um layout predefinido que inclui texto estático, tags HTML e controles do lado do servidor. Em páginas .aspx comuns, a diretiva @ Page é usada. No caso de arquivos .master, isso é substituído pela diretiva @ Master.

### Páginas de conteúdo

Uma página de conteúdo representa o conteúdo dos controles de espaço reservado da página mestra. Estas são páginas .aspx que são, na verdade, o code-behind da página mestra. As páginas de conteúdo são vinculadas usando a diretiva @ Page incluindo um atributo MasterPageFile apontando para a página mestra a ser usada conforme mostrado abaixo.

```
<%@ Page Language="VB" MasterPageFile="~/MasterPages/Master2.master" Title="Content Page of Master File" %>
```

## Referências

* [Visão geral das páginas mestras do ASP.NET](https://learn.microsoft.com/en-us/previous-versions/aspnet/wtxbf3hh(v=vs.100))

