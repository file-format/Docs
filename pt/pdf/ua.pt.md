{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PDF/UA",
  "description":"Saiba mais sobre o formato de arquivo PDF/UA e APIs que podem criar e abrir arquivos PDF/UA.",
  "linktitle" : "PDF/UA",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# O que é arquivo PDF/UA? #

PDF/UA foi publicado como [ISO Standard 14289-1](https://en.wikipedia.org/wiki/ISO_14289) em agosto de 2012 e é de longe a primeira definição completa de um conjunto de requisitos para documentos PDF universalmente acessíveis. O termo "universalmente acessível" refere-se ao entendimento de que as informações contidas em um documento [PDF](/pt/pdf/) devem ser acessíveis de forma igual e independente a todos em geral e às pessoas com deficiência em particular. A introdução do padrão PDF/UA pode ser considerada um passo importante para a criação de ferramentas e aplicativos para criar e ler conteúdo PDF.

## Requisitos de formato de arquivo ##

O PDF/UA possui alguns requisitos definidos em sua base que atuam como a essência deste padrão. Essencialmente, eles são baseados na marcação de PDFs, o que significa que todos os documentos PDF/UA devem ser devidamente marcados. Também requer que as tags sejam semanticamente apropriadas e em ordem lógica. Isso garante que o documento final criado com a especificação PDF/UA seja mais confiável e acessível. Isso pode levar os autores de PDF a questionar se eles precisam saber tudo sobre todos esses requisitos? Felizmente, não é assim, pois as ferramentas de conformidade PDF/UA assumem a responsabilidade de adicionar e preservar a acessibilidade do PDF.

Os requisitos de formato de arquivo para PDF/UA são os seguintes.

* O conteúdo é categorizado de duas maneiras: conteúdo significativo e artefatos, como elementos decorativos da página. Todo conteúdo significativo deve ser marcado e integrado na árvore de estrutura de todas as tags dentro de um documento. Os artefatos, por outro lado, precisam apenas ser marcados como tal.
* O conteúdo significativo deve ser marcado com tags e, juntamente com as demais tags do documento, criar uma árvore de estrutura completa.
* O conteúdo significativo deve ser marcado com as tags semânticas apropriadas.
* A árvore de estrutura criada pelas tags do documento deve refletir a ordem lógica de leitura do documento.
* Somente as tags padrão definidas no PDF 1.7 podem ser utilizadas; se quaisquer outras tags forem usadas, uma entrada de atribuição de função deve registrar qual tag padrão cada uma representa.
* As informações não podem ser transmitidas apenas por meios visuais (por exemplo, contraste, cor ou posição na página).
* Nenhum conteúdo piscando, piscando ou piscando é permitido, seja como efeitos controlados por JavaScript ou como parte de qualquer vídeo incorporado ao PDF.
* Um título do documento deve ser fornecido e o documento deve ser configurado de forma que o título (em vez do nome do arquivo) apareça no título da janela.
* O idioma de todo o conteúdo deve ser anotado e as alterações de idioma devem ser explicitamente marcadas como tal.

## Conformidade PDF/UA ##

O padrão PDF/UA define especificações para conteúdo, leitores e tecnologia assistiva. Esses três aspectos estão ligados entre si com base no conteúdo do documento. Os requisitos de conformidade para cada um deles são os mencionados abaixo.

## Arquivos em conformidade ##

Os arquivos em conformidade com o padrão PDF/UA devem conter recursos válidos de acordo com as [especificações do PDF 1.7](https://opensource.adobe.com/dc-acrobat-sdk-docs/standards/pdfstandards/pdf/PDF32000_2008.pdf). No entanto, os recursos que são proibidos especificamente pelo PDF/UA devem ser excluídos.

## Leitores em conformidade ##

Um leitor em conformidade deve obedecer às regras escritas pelas especificações do PDF 1.7. Especificamente, deve suportar:

* todas as tags, atributos e valores-chave especificados para acessibilidade. Deve também ter a capacidade de processar e representar assinaturas digitais, anotações e Conteúdos Opcionais.
* processar e representar assinaturas digitais, anotações e conteúdo opcional
* navegar no documento por vários meios

## Tecnologia Assistiva em Conformidade ##

Uma tecnologia assistiva compatível é destinada ao suporte aos recursos PDF/UA. Eles incluem, por exemplo, recursos do conteúdo e do leitor, e devem permitir a navegação por rótulos de página, estrutura do documento ou esboço. Ele também deve permitir que o usuário substitua o zoom de navegação padrão.

## Referências ##

* [PDF/UA - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/UA)
* [PDF/UA em poucas palavras](http://www.pdfa.org/publication/pdfua-in-a-nutshell/)

