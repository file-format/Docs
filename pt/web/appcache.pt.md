{
  "date" : "2022-08-05",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo APPCACHE - Formato de arquivo de manifesto de cache HTML5",
  "description" :"Saiba mais sobre o que é um arquivo APPCACHE e APIs que podem criar e abrir arquivos APPCACHE.",
  "linktitle" : "APPCACHE",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-08-05"
}

## O que é um arquivo APPCACHE?

Um arquivo APPCACHE é um arquivo de texto que contém a lista de recursos a serem armazenados em cache pelos navegadores para acesso offline aos aplicativos da web. Isso é útil quando não há conexão com a Internet. Nessa situação, o navegador usa os recursos de cache offline para fornecer acesso ao conteúdo da web. O arquivo APPCACHE contém recursos da web, como imagens (por exemplo, **[PNG](/pt/image/png/)**, **[WEBP](/pt/image/webp/)** etc.), folhas de estilo **([ CSS])(/pt/web/css/)** e arquivos de script (como arquivos Javascript **[JS](/pt/web/js/)**).

Os aplicativos que podem **abrir arquivos APPCACHE** incluem navegadores da Web, como Google Chrome, Safari e Firefox.

## Formato de arquivo APPCACHE - Mais informações

Os arquivos APPCACHE são arquivos de texto simples, fornecendo acesso offline a páginas da Web para execução sem conexão com a Internet. A presença de APPCACHE designa uma página como disponível offline.

### Como referenciar um arquivo APPCACHE?

Em sua página HTML, um arquivo APPCACHE é referenciado da seguinte forma.

```
<html manifest="example.appcache">
  ...
</html>
```

## Estrutura de um arquivo de manifesto APPCACHE

Um arquivo de manifesto APPCACHE simples tem a seguinte aparência.

```
CACHE MANIFEST
index.html
stylesheet.css
images/logo.png
scripts/main.js
http://cdn.example.com/scripts/main.js
```

Este é um exemplo mais simples e pode haver estruturas mais complexas presentes também.

## Vantagens do manifesto APPCACHE

O uso da interface de cache oferece aos aplicativos da Web as seguintes vantagens.

1. Navegação offline - A interface de cache permite que os usuários finais naveguem em seu site completo quando estiverem offline
1. Velocidade - o cache permite acesso de alta velocidade ao conteúdo offline diretamente do disco
1. Acessibilidade o tempo todo - Caso seu site fique inativo, os usuários ainda terão acesso ao conteúdo da web e poderão obter a experiência offline

## Referências

* [A Beginner Guide to AppCache Manifest](https://web.dev/appcache-beginner/)

