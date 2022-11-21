{
  "date" : "2021-12-09",
  "keywords" :[ "asa",".asa", "formato de arquivo", "tipo de arquivo", "o que é um arquivo .asa" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ASA - Arquivo de configuração ASP",
  "description" :"Saiba mais sobre o que é um arquivo ASA e APIs que podem criar e abrir arquivos ASA.",
  "linktitle" : "ASA",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-12-09"
}

## O que é um arquivo ASA?

Um arquivo ASA é um arquivo de configuração, criado para projetos [ASP](/pt/web/asp/)/ASP.NET. Ele contém declarações de variáveis, contém e funções que devem ser acessíveis em nível global no aplicativo. Todas as páginas do projeto podem acessar essas variáveis e funções, evitando assim a necessidade de reescrevê-las. Um exemplo é a página Global.asa que é armazenada no diretório raiz para ser acessível por outras páginas do site ASP. Os arquivos Global.asa são opcionais, mas, se usados, cada aplicativo pode ter apenas um arquivo Global.asa.

## Formato de arquivo ASA - Mais informações

Os arquivos ASA são arquivos de texto simples com as seguintes informações.

* Eventos de aplicativos
* Eventos da sessão
* \<object> declarações
* Declarações TypeLibrary
* a diretiva #include

## Exemplo de arquivo ASA

Um arquivo Global.asa pode ser algo assim.

```
<script language="vbscript" runat="server">

sub Application_OnStart
'some code
end sub

sub Application_OnEnd
'some code
end sub

sub Session_OnStart
'some code
end sub

sub Session_OnEnd
'some code
end sub

</script>
```

## Referências

* [arquivo ASP Global.asa - w3schools](https://www.w3schools.com/asp/asp_globalasa.asp)

