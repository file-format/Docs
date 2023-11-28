{
  "date" : "2023-05-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo AXD - Formato de arquivo do manipulador da Web ASP.NET",
  "description" :"Aprenda sobre o que é um arquivo AXD e APIs que podem criar e abrir arquivos AXD.",
  "linktitle" : "AXD",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2023-05-23"
}

## O que é um arquivo .AXD?

Um arquivo AXD é um arquivo de configurações da web usado para manipular e recuperar solicitações de recursos incorporados no ASP.NET. É composto por instruções para recuperar recursos incorporados, como imagens, arquivos JavaScript ([.JS](/pt/web/js/)) e arquivos [.CSS](/pt/web/css/). Arquivos AXD são usados para injetar recursos em páginas do lado do cliente. Isso permite que as páginas do cliente acessem esses recursos no servidor de maneira padrão.

## Formato de arquivo AXD

Os arquivos AXD são armazenados como arquivos binários no lado do servidor. Refere-se a um arquivo Web Handler em ASP.NET que são componentes que geram respostas a solicitações específicas para um servidor web. Os arquivos AXD executam o processamento personalizado antes de gerar a resposta com base nas solicitações de página do cliente. Geralmente, eles são salvos como arquivos **WebResource.axd**.

### O que é o arquivo WebResource.axd?

A maioria dos projetos ASP.NET salva arquivos AXD como arquivos WebResource.axd que permitem que páginas do lado do cliente baixem recursos incorporados em um assembly. Seu aplicativo pode enfrentar desempenho lento caso você o execute no modo de depuração, pois o manipulador WebResources.axd não está armazenado em cache.

## Referências

* [WebResource.axd](https://social.msdn.microsoft.com/Forums/en-US/e6559555-5723-4590-9eb6-4b2af26a54cd/what-is-webresourceaxd?forum=aspgettingstarted)

