{
  "date" : "2022-02-03",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo WSDL - Arquivo de linguagem de descrição de serviços da Web",
  "description":"Saiba mais sobre o que é um arquivo WSDL e APIs que podem criar e abrir arquivos WSDL.",
  "linktitle" : "WSDL",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2022-02-03"
}

## O que é um arquivo WSDL?

Um arquivo WSDL é um arquivo Web Services Description Language escrito em linguagem XML para descrever serviços da Web. Ele contém informações sobre os terminais ou interfaces para conectividade com o mundo externo em um formato universalmente aceito. [Especificações de formato de arquivo WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/) (mantido por W3C.org) definem os termos para publicação de feeds de dados para troca de dados para ter acesso remoto a aplicativos em portas e endpoints.

## Formato de arquivo WSDL - Mais informações

Os arquivos WSDL são salvos como arquivos XML que podem ser lidos por humanos e podem ser abertos em qualquer editor de texto para visualizar o conteúdo.

## Descrição do serviço WSDL

As especificações de formato de arquivo WSDL 2.0 descrevem o serviço WSDL como composto de dois estágios:

- Palco abstrato
- Palco de concreto

A reutilização da descrição e projetos independentes de preocupação é regida por um serviço da Web. Isso é obtido usando vários tipos diferentes de elementos, incluindo tipos (definições de tipo de dados), mensagens (os dados comunicados), operações (ações) e protocolos usados pelo serviço. Tudo isso é gerenciado em nível abstrato. A vinculação dos detalhes do formato de transporte e ligação é especificada pela vinculação, que agrupa os pontos de extremidade para implementar uma interface comum.

### Quais tecnologias podem ser usadas para fazer interface com serviços WSDL?

Várias tecnologias diferentes podem ser usadas para fazer interface com serviços WSDL, incluindo aplicativos ASP.NET, C/C++ e Java.

## Exemplo de WSDL

```
<message name="getTermRequest">
  <part name="term" type="xs:string"/>
</message>

<message name="getTermResponse">
  <part name="value" type="xs:string"/>
</message>

<portType name="glossaryTerms">
  <operation name="getTerm">
    <input message="getTermRequest"/>
    <output message="getTermResponse"/>
  </operation>
</portType>
```

Neste exemplo, o portType "glossaryTerms" define uma operação unidirecional chamada "setTerm".

## Referências

* [WSDL XML](https://www.w3schools.com/xml/xml_wsdl.asp)
* [especificações de formato de arquivo WSDL](https://www.w3.org/TR/2007/REC-wsdl20-20070626/)

