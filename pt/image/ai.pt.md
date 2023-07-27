{
  "date" : "2021-01-21",
  "keywords" :[ "arquivo ai", "formato de arquivo ai", "o que é um arquivo ai", "arquivo", "exemplo ai", "extensão de arquivo ai", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"AI - Arquivo de arte do Adobe Illustrator",
  "description":"Saiba mais sobre o formato de arquivo AI e APIs que podem criar e abrir arquivos AI.",
  "linktitle" : "AI",
  "menu" : {
    "docs" : {
      "parent" : "image"
}
},
  "lastmod" : "2021-01-21"
}

## O que é um arquivo AI?

Um arquivo com extensão .ai é um arquivo de arte do Adobe Illustrator que contém gráficos vetoriais em uma única página. ele usa pontos para criar caminhos para exibir os dados da imagem, evitando assim a perda de qualidade da imagem se for ampliada. O formato de arquivo AI é baseado no formato de arquivo PGF, que é semelhante aos arquivos AI. O formato AI encontra seu maior uso para logotipos e mídia impressa, e suas versões iniciais foram consideradas semelhantes às dos arquivos [EPS](/pt/page-description-language/eps/). Os arquivos AI podem ser abertos com as ferramentas Adobe Illustrator, Adobe Acrobat DC, PaintShop Pro e CorelDraw Graphics.

## Formato de arquivo AI

AI é o formato de arquivo proprietário do Adobe Illustrator e usa a abordagem de caminho duplo semelhante ao PGF para salvar arquivos compatíveis com EPS. As [especificações do formato de arquivo do Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf) fornecem uma descrição detalhada referência do desenvolvedor para detalhes internos deste formato de arquivo. Todos Os documentos (arquivos) criados pelo Adobe Illustrator são documentos em linguagem PostScript e possuem duas partes principais em conformidade com as Convenções de Estruturação de Documentos: um `prolog` e um `script`.

### Prólogo

A seção prólogo encapsula as informações necessárias para a interpretação do arquivo. Um exemplo seria a caixa delimitadora que contém todas as marcas na página. Ele também contém informações de recursos, como fontes e definições de procedimentos. Esses recursos são agrupados logicamente em conjuntos chamados procsets e contêm métodos explícitos para inicializar e encerrar seus procedimentos.

### Roteiro

Os elementos gráficos na página são descritos pelo script. Um script contém referências aos operadores e procedimentos no prólogo, juntamente com operandos e dados. As três seções lógicas de um script incluem:

* Sequência de Configuração - que inicializa e ativa os recursos definidos no prólogo
* Sequência de operadores descritivos
* Trailer que desativa recursos

Operadores no script são sequências de elementos gráficos escritos na linguagem definida por procsets no prólogo. Essas sequências consistem em coleções de elementos de dados, definições de atributos gráficos e chamadas para os procedimentos definidos nos procsets.

### Tags de objeto

As tags de objeto são usadas para anexar informações personalizadas a um objeto de arte do Adobe Illustrator. As etiquetas consistem em:

*Identificador de tags
* Tipo de etiqueta
* Dados

## Referências
* [Especificações de formato de arquivo do Adobe Illustrator](https://web.archive.org/web/20150906044646/http://partners.adobe.com/public/developer/en/illustrator/sdk/AI7FileFormat.pdf)
* [Formato de arquivo AI por PaintShopPro](https://www.paintshoppro.com/en/pages/ai-file/)

