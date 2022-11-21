{
  "date" : "2019-10-11",
  "keywords" :["xml", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "linguagem de marcação extensível"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo XML",
  "description":"Saiba mais sobre o formato de arquivo XML e APIs que podem criar e abrir arquivos XML.",
  "linktitle" : "XML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo XML?

XML significa Extensible Markup Language que é semelhante a **[HTML](/pt/web/html/)**, mas diferente no uso de tags para definir objetos. A ideia por trás da criação do formato de arquivo XML era armazenar e transportar dados sem depender de ferramentas de software ou hardware. Sua popularidade se deve ao fato de ser tanto humano quanto legível por máquina. Isso permite criar protocolos de dados comuns na forma de objetos a serem armazenados e compartilhados em uma rede, como a World Wide Web (WWW). O "X" em XML é extensível, o que implica que a linguagem pode ser estendida a qualquer número de símbolos conforme os requisitos do usuário. É para esses recursos que muitos formatos de arquivo padrão fazem uso dele, como Microsoft Open XML, LibreOffice OpenDocument, **[XHTML](/pt/web/xhtml/)** e **[SVG](/pt/page-description-language /svg/)**.

## Formato de arquivo XML

O formato de arquivo XML é baseado no XML Document Object Model (DOM) que é uma API de programação para documentos HTML e XML. O XML DOM define um método padrão para acessar e manipular os elementos do documento XML. Faz uma visualização de estrutura em árvore de um documento XML que pode ser usado para acessar todos os elementos através da árvore DOM. Elementos existentes podem ser modificados/excluídos assim como novos elementos podem ser criados na árvore XML. Cada elemento de um documento XML é chamado de nó. O XML DOM é conforme mostrado na imagem a seguir.

{{< figure src="../XML DOM.png" alt="XML DOM" >}}

### Abordagem universal de XML

O poder do XML o torna uma linguagem universal para comunicação de dados pela rede, simplificando o transporte de dados e as alterações de plataforma. Isso também garante a troca de dados entre sistemas incompatíveis, armazenando dados em formato de texto simples. HTML é para representação de dados na web, enquanto XML é para troca de dados. Os pares de tags de marcação usados dentro do XML definem os elementos-chave da estrutura a serem utilizados pelos aplicativos de leitura.

## Exemplo de XML

A seguir, um exemplo simplificado de um catálogo de CDs, onde cada registro contém informações sobre os CDs, como artista, país, empresa, preço e ano de produção.

```
<CATALOG>
  <CD>
    <TITLE>Empire Burlesque</TITLE>
    <ARTIST>Bob Dylan</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>Columbia</COMPANY>
    <PRICE>10.90</PRICE>
    <YEAR>1985</YEAR>
  </CD>
  <CD>
    <TITLE>Hide your heart</TITLE>
    <ARTIST>Bonnie Tyler</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>CBS Records</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1988</YEAR>
  </CD>
  <CD>
    <TITLE>Greatest Hits</TITLE>
    <ARTIST>Dolly Parton</ARTIST>
    <COUNTRY>USA</COUNTRY>
    <COMPANY>RCA</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1982</YEAR>
  </CD>
  <CD>
    <TITLE>Still got the blues</TITLE>
    <ARTIST>Gary Moore</ARTIST>
    <COUNTRY>UK</COUNTRY>
    <COMPANY>Virgin records</COMPANY>
    <PRICE>10.20</PRICE>
    <YEAR>1990</YEAR>
  </CD>
  <CD>
    <TITLE>Eros</TITLE>
    <ARTIST>Eros Ramazzotti</ARTIST>
    <COUNTRY>EU</COUNTRY>
    <COMPANY>BMG</COMPANY>
    <PRICE>9.90</PRICE>
    <YEAR>1997</YEAR>
  </CD>
  <CD>
</CATALOG>
```

## Referências

* [XML - Por Wikipedia](https://en.wikipedia.org/wiki/XML)

