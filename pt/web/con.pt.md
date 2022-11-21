{
  "date" : "2022-08-24",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo CON - Formato de arquivo de origem do aplicativo de conceito",
  "description" :"Saiba mais sobre o que é um arquivo CON e APIs que podem criar e abrir arquivos CON.",
  "linktitle" : "CON",
  "menu" : {
    "docs" : {
      "identifier":"web-con",
      "parent" : "web"
}
},
  "lastmod" : "2022-08-24"
}

## O que é um arquivo CON?

Um arquivo CON é um arquivo de código-fonte para o aplicativo desenvolvido para o **Concept Application Server**. É usado para escrever aplicativos para troca de dados entre o servidor e o usuário. Os arquivos CON hospedados no servidor são acessíveis com um navegador da Web, desde que o Concept Client esteja instalado no usuário final. Conceito Servidor de aplicativos é um servidor web com linguagem de programação de pequena escala que pode ter um mecanismo de banco de dados de subconjunto [SQL](/pt/database/sql/) (TinDB).

Os arquivos CON podem ser abertos/executados com o RadGs Concept Application Server.

## Formato de arquivo CON - Mais informações

Os arquivos CON são hospedados no servidor e são acessados usando o navegador da web na máquina do usuário. Conceitos [URLs](/pt/web/url/) são diferentes dos URLs HTTP normais e começam com **concept://**.

### Exemplo de URL do arquivo CON

Um arquivo CON hospedado no Concept Application Server pode ser acessado via navegador da web usando URLs como:

```
concept://domain.server.com/web_application/main.con.
```
## Referências

* [Concept Application Server](https://github.com/Devronium/ConceptApplicationServer)

