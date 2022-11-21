{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PDF/VT",
  "description":"Saiba mais sobre o formato de arquivo PDF/VT e APIs que podem criar e abrir arquivos PDF/VT.",
  "linktitle" : "PDF/VT",
  "menu" : {
    "docs" : {
      "parent" : "pdf"
}
},
  "lastmod" : "2019-09-10"
}

# O que é PDF/VT? #

PDF/VT, publicado como [ISO 16612-2](https://www.iso.org/standard/46428.html) em agosto de 2010 como padrão, foi projetado para permitir a impressão de documentos variáveis (VDP) em uma variedade de ambientes. O padrão torna a informação variável e a impressão transacional como base para o padrão. A impressão de dados variáveis é utilizada onde parte da informação é diferente para cada destinatário do conteúdo. A impressão Transacional inclui faturas, extratos e outros documentos que combinam informações de cobrança com informações de marketing. Isso resulta em uma combinação de processamento aprimorado de imagens, texto e outros tipos de conteúdo. O PDF/VT permite o gerenciamento confiável e dinâmico de páginas para dados de impressão de saída transacional de alto volume (HVTO) usando o conceito de metadados de parte do documento (DPM). Arquivos PDF/VT podem ser abertos no visualizador do Adobe Acrobat sem a necessidade de adicionar qualquer outro componente.

## Hierarquia de Partes do Documento ##

A Hierarquia da Parte do Documento (DPart) é como uma estrutura em árvore de nós da parte do documento que se baseia em todas as páginas do documento. Os elementos desta árvore são chamados de nós DPart. Cada nó interno contém outros nós DPart e cada nó folha especifica uma ou mais páginas para um destinatário. Essencialmente, a hierarquia DPart especifica a sequência e o relacionamento de documentos ou partes de documentos em um arquivo PDF/VT. A estrutura em árvore dos nós DPart representa facilmente o conteúdo interno de um documento PDF/VT, pois pode conter subdocumentos para vários destinatários e cada parte do documento corresponde às páginas de um único destinatário. A hierarquia DPart é necessária em arquivos PDF/VT.

## Metadados de Parte do Documento (DPM) ##

O Document Part Metadata (DPM) está associado a cada nó na hierarquia de parte do documento e pode ser usado para comunicar informações sobre o subdocumento de um destinatário específico e suas partes. Em particular, o DPM pode conter informações sobre as propriedades ou informações sobre os destinatários em um formulário codificado.

## Níveis de conformidade ##

O PDF/VT é conferido nos três níveis de conformidade a seguir. Todos eles são baseados em [PDF](/pt/pdf/) 1.6.

* `PDF/VT-1` - É baseado em PDF/X-4 e contém todos os recursos necessários para renderizar um documento PDF.
* `PDF/VT-2` - Projetado para troca de vários arquivos, os documentos PDF/VT-2 podem fazer referência a intenções de saída externas, conteúdo externo ou ambos. Um documento PDF/VT e todos os seus arquivos PDF referenciados e intenções de saída externas são chamados coletivamente de conjunto de arquivos PDF/VT-2. Acrobat 9 e suportam este recurso.
* `PDF/VT-2s` - Suporta transmissão ao vivo de PDF/VT-2. Isso permite que seções segmentadas de dados sejam processadas.

## Referências ##

* [PDF/VT - Por Wikipedia](https://en.wikipedia.org/wiki/PDF/VT)
* [Tecnologia gráfica ISO 16612-2](https://www.iso.org/standard/46428.html)

