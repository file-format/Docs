{
  "date" : "2021-06-24",
  "keywords": [ "GADGET file", "what is a gadget file", "extension", "format", "what is a GADGET file", "archive" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo GADGET e APIs que podem criar e abrir arquivos GADGET.",
  "title" :"GADGET - Arquivo de CD virtual",
  "linktitle" : "GADGET",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-06-24"
}

## O que é um arquivo GADGET?

Um arquivo GADGET consiste em um pequeno programa de software que é executado na barra lateral do Windows Vista ou Windows 7. Ele comprime vários arquivos baseados na web e os arquivos podem incluir os arquivos [.html](/pt/web/html), [.css](/pt/web/css) ou [.js](/pt/web/js), bem como outros arquivos da web. Os arquivos GADGET são usados para pequenos componentes, como ferramentas de pesquisa, feeds de notícias, utilitários do sistema e pequenos jogos. Embora os GADGETs sejam hospedados pela Barra Lateral, não são específicos da área da Barra Lateral; eles podem ser desencaixados e movidos para a área de trabalho conforme desejado.

## Formato de arquivo GADGET

O arquivo GADGET é um arquivo [ZIP](/pt/compression/zip) renomeado que contém uma coleção de arquivos HTML, XML, JScript e CSS (Cascading Style Sheets). A instalação contém o download do arquivo .gadget e a ativação do processo de download para instalar o componente ou o salvamento do arquivo .gadget no sistema local e um clique duplo para iniciar o processo de instalação.

Basicamente, um GADGET contém dois arquivos:

1. **Gadget.xml**: O manifesto, um arquivo XML que consiste em informações gerais de apresentação e configuração do gadget.
2. **name.html**: um arquivo HTML, no qual o nome é especificado no<name> do manifesto do gadget associado, que fornece o wrapper para a interface do usuário do gadget e compreende a funcionalidade principal do gadget.

Várias instâncias de um arquivo GADGET podem ser executadas simultaneamente. Por exemplo, se alguém quiser saber a hora em vários fusos horários, poderá executar várias instâncias do gadget de relógio configurando cada relógio para um fuso horário específico.

### Descontinuação do GADGET

Como a plataforma Windows Sidebar no Windows 7 possui sérias vulnerabilidades, os Gadgets não estão mais disponíveis no site oficial da Microsoft. Mais tarde, a Microsoft retirou esse recurso em versões mais recentes do Windows. O GADGET pode ser explorado para acessar os arquivos de um computador, danificar um computador, revelar conteúdo censurável ou alterar seu comportamento a qualquer momento.

## Referências

* [Barra Lateral do Windows - da Microsoft](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-entry)
* [Desenvolvendo um Gadget para Windows Sidebar Parte 1](https://docs.microsoft.com/en-us/previous-versions/windows/desktop/sidebar/-sidebar-overview-gdo)

