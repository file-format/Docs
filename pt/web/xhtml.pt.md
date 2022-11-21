{
  "date" : "2019-10-11",
  "keywords" :["xhtml", "Arquivo", "Extensão", "Formato de arquivo", "Extensão de arquivo", "html extensível"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XHTML - Formato de arquivo de linguagem de marcação de hipertexto extensível",
  "description":"Saiba mais sobre o que é formato de arquivo XHTML e APIs que podem criar e abrir arquivos XHTML.",
  "linktitle" : "XHTML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo XHTML?

O XHTML é um formato de arquivo baseado em texto com marcação no XML, utilizando uma reformulação do HTML 4.0. Esses arquivos são adequados para serem abertos ou visualizados em um navegador da web. XHTML foi projetado para ser mais estruturado, menos scripting, genérico; usando todas as facilidades existentes de XML e mais independente de dispositivo. XHTML fornece um conjunto de elementos e atributos geralmente valiosos, com opções de extensão em combinação com folhas de estilo. Os atributos são usados da coleção de atributos de metadados. XHTML fornece flexibilidade e acessibilidade subordinando todos os elementos de apresentação **[HTML](/pt/web/html/)** a folhas de estilo. As folhas de estilo são mais versáteis do que esses elementos de apresentação. As especificações para HTML 4.01, HTML5 e XHTML estão sendo desenvolvidas dinamicamente pelo World Wide Web Consortium (W3C).

## Breve História do Formato de Arquivo XHTML

A história do XHTML começa com um documento preliminar lançado em dezembro de 1998 pelo World Wide Web Consortium. Este documento refere-se à "Reformulação HTML em XML", uma especificação denominada XHTML 1.0. Esta nova especificação reformulou o HTML em XML utilizando os elementos ou atributos existentes. Em maio de 1999, o W3 Consortium declarou que o HTML 4.0 havia sido reformado como um aplicativo XML. ou seja, XHTML. Em 26 de janeiro de 2000, a primeira especificação que define XHTML 1.0 foi lançada pelo W3C. Além disso, em 31 de maio de 2001, o W3C anunciou o XHTML como uma linguagem independente e começou a trabalhar no desenvolvimento do HTML 5.0. No entanto, em 2005, foi formado um grupo de trabalho (WHATWG) que visava melhorar o HTML comum independente do XHTML. O WHATWG finalmente começou a trabalhar em HTML5 em paralelo com XHTML 2.

## Formato de arquivo XHTML

XHTML é um formato, que é uma coleção de diferentes tipos de documentos e módulos que imitam, categorizam e estendem o HTML 4. Os arquivos em XHTML são baseados em XML e visam trabalhar com os agentes de usuário baseados em XML. Os arquivos XHTML são compatíveis com XML. Ferramentas padrão XML são usadas para visualizar, editar e validar arquivos XHTML. Os aplicativos dependentes do Modelo de Objeto de Documento HTML ou do Modelo de Objeto de Documento XML [DOM] podem operar por meio de documentos XHTML. Optando pelo XHTML hoje, os desenvolvedores de conteúdo podem aproveitar todos os benefícios associados ao XML sem se preocupar com a compatibilidade de seu conteúdo com versões anteriores ou posteriores.

Um conjunto de elementos relacionados constrói um módulo em XHTML. Um formulário ou módulo de tabela pode conter vários elementos de formulário ou tabela que podem ser exibidos em uma página da web. A modularização visava isolar elementos HTML em conjuntos de vários elementos vinculados. Para que os desenvolvedores de conteúdo possam aproveitar a seleção de módulos para diferentes tipos de dispositivos. Além disso, os módulos permitem que os agentes de usuário selecionem elementos sem perder a consistência com o padrão XHTML. Os requisitos de análise do XHTML são os mesmos do XML, enquanto o HTML pratica seus próprios.

### Conformidade do Documento

XHTML2 oferece especificações em conformidade com documentos XHTML 1.0, que usa os elementos e atributos namespaces do XML e XHTML 1.0. A conformidade do documento é de dois tipos.

Um documento estritamente conforme é baseado em XML que precisa apenas de serviços obrigatórios definidos nesta especificação. Os seguintes critérios precisam ser atendidos para arquivos XHTML:

* Um arquivo deve estar em conformidade com as restrições definidas nas DTDs e no Apêndice B.
* O elemento base do arquivo deve ser html.
* O elemento base do arquivo deve conter declaração para o namespace XHTML e deve ser definido como:

```
http://www.w3.org/1999/xhtml.
```

* O elemento base pode ser escrito como:

```
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
```

Antes do elemento base, deve ser declarado um DOCTYPE, cujo identificador público deve fazer referência a uma das três definições de tipo de documento (DTDs). O identificador do sistema pode ser modificado para cumprir as convenções atuais do sistema.

```
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Transitional//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-transitional.dtd">
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Frameset//EN"
 "http://www.w3.org/TR/xhtml1/DTD/xhtml1-frameset.dtd">
```

Em documentos XML, não é necessário especificar declarações XML em todos os documentos; no entanto, os desenvolvedores de conteúdo são estimulados a usar declarações XML em todos os seus documentos XHTML. Essas declarações são obrigatórias quando a codificação de caracteres do documento é diferente de UTF-8 /16 ou nenhuma codificação foi especificada por um protocolo de controle. O exemplo a seguir de um documento XHTML define as declarações XML

```
<!DOCTYPE html
     PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"
    "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns#"http://www.w3.org/1999/xhtml" xml:lang#"en" lang#"en">
  <head>
    <title>Public Property</title>
  </head>
  <body>
    <p>changed to <a href#"http://sample.com/">sample.com</a>.</p>
  </body>
</html>
```

Um agente de usuário em conformidade deve cumprir as seguintes regras:

* A análise e avaliação do documento XHTML é feita por um agente de usuário que garante sua consistência com a Recomendação XML 1.0.
* Em caso de validação do agente usuário, deve-se verificar a validade dos documentos para suas DTDs referenciadas de acordo com o XML. Quando o arquivo XHTML é processado pelo agente do usuário como XML genérico, os recursos do tipo ID serão reconhecidos como identificadores de fragmentos.

Se um agente do usuário se deparar com um elemento não reconhecido, a seguir estão os critérios obrigatórios que ele deve cumprir

* processa o conteúdo desse elemento desconhecido
* ignore o atributo e seu valor
* Use o valor do atributo fornecido como padrão.

Quando o agente do usuário se deparar com uma declaração de referência de entidade que não foi processada anteriormente, ela deve ser processada como os caracteres (começando com o sinal “&” e terminando com o ponto e vírgula). Durante o processamento de conteúdo, caracteres ou referências a entidades de caracteres que são previsíveis pelo agente do usuário, mas não renderizáveis, podem usar qualquer renderização alternativa que produza o significado semelhante. Nesse caso, o documento deve ser exibido de maneira que deixe o usuário óbvio sobre o fato de que o processo de renderização não foi normal. Para o processamento de espaços em branco, o agente do usuário precisa procurar a definição de caracteres CSS [CSS2].

## Compatibilidade com versões anteriores de XHTML

A compatibilidade com versões anteriores de documentos XHTML 1. é bem versada com agentes de usuário HTML 4, se as regras apropriadas forem seguidas. O XHTML 1.1 é totalmente compatível, exceto as anotações ruby, embora elas sejam geralmente ignoradas pelos navegadores HTML 4. XHTML 2.0 é comparativamente menos compatível, no entanto, o problema foi resolvido até certo ponto através do uso de scripts.

## Referências

* [A History of XHTML: From the 1990s to Today](https://www.brighthub.com/internet/web-development/articles/109224.aspx)

