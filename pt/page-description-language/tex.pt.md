{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo TEX",
  "description":"Saiba mais sobre o formato de arquivo TEX e APIs que podem criar e abrir arquivos TEX.",
  "linktitle" : "TEX",
  "menu" : {
    "docs" : {
      "parent" : "page-description-language"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo TEX? ##

**TeX** é uma linguagem que inclui recursos de programação e marcação, usados para compor documentos. Donald Knuth, da Universidade de Stanford, é o criador deste engenhoso sistema de composição. Em todo o mundo, o TeX é a melhor escolha de autores e editores para produzir documentos técnicos de alta qualidade. O TeX realiza um excelente trabalho de formatação de expressões matemáticas complexas. Em conjunto com uma fotocompositora de alta qualidade, o TeX concorre com os resultados gerados pelos melhores sistemas tradicionais de composição. Portanto, considerados os sistemas tipográficos digitais mais elegantes.

Os arquivos de entrada do TeX são baseados em código ASCII, permitindo assim o compartilhamento de manuscritos entre escritores, gerentes de publicação e críticos. Uma grande variedade de ambientes de computação, quase todas as plataformas modernas e muitas plataformas mais antigas suportam o TeX. Além disso, o TeX é um software gratuito, disponível para uma ampla gama de consumidores. Muitas instalações UNIX usam tanto o UNIX troff quanto o TeX como seu sistema de formatação para diferentes propósitos. Outras tarefas de composição são executadas tremendamente na forma de LaTeX, ConTeXt e outros pacotes de macros.

## Breve história ##

O TeX foi projetado e escrito por Donald Knuth em 1978. Guy Steele do Massachusetts Institute of Technology revisou a entrada/saída do TeX para fazê-lo rodar sob o sistema operacional Incompatível como o Timesharing System (ITS). A primeira versão do TeX foi desenvolvida sob o sistema operacional WAITS de Stanford na linguagem de programação (SAIL) e testada para rodar em um PDP-10. Knuth introduziu a ideia de programação alfabetizada para versões avançadas. A programação alfabetizada é uma maneira de gerar código fonte compilável e tipografia (em TeX) para documentação com links cruzados usando o arquivo original. A linguagem usada para desenvolver essas versões avançadas do TeX é chamada WEB, uma mistura de programas DEC PDP-10 Pascal para garantir a portabilidade.

Uma nova versão revisada do TeX foi publicada em 1982 e foi chamada de TeX82. A principal mudança é a substituição do algoritmo de hifenização original pelo algoritmo recém-escrito por Frank Liang. Para garantir a portabilidade em diferentes plataformas, em vez de usar ponto flutuante, o TeX82 usa aritmética de ponto fixo junto com uma linguagem de programação real e completa. Em 1989, foram lançadas novas versões do TeX e Metafont. Assim, a versão 3.0 do TeX facilita as entradas de 8 bits, permitindo 256 caracteres diferentes no texto. Após a versão 3, as atualizações são indicadas pela adição de um dígito extra no final do decimal, por exemplo, a versão atual do TeX é indicada como 3.14159265. Esta versão foi atualizada pela última vez em 12-1-2014.

## Entrada TeX ##

Um arquivo de entrada para TEX pode ser preparado com um editor de texto usando texto comum. Ao contrário de um processador de texto típico, este arquivo de entrada não permite caracteres de controle invisíveis. Um arquivo pode ser incorporado em outro arquivo, contendo definições de macro e definições auxiliares que aprimoram os recursos do TeX. Se uma instalação do TeX vier com algum arquivo de macro, as informações locais sobre o TeX demonstram o uso de arquivos de macro. A forma padrão do TeX integra uma combinação de macros e outras definições conhecidas como TEX simples.

Com base no conhecimento preciso dos tamanhos de todos os caracteres e símbolos, ele calcula a organização ideal de letras por linha e linhas por página. No momento do processamento do documento, é gerado um arquivo .dvi, onde “dvi” significa “independente do dispositivo”. Os programas de driver de dispositivo são necessários para imprimir ou visualizar o documento com uma extensão dvi. Hoje em dia, a geração dvi é contornada por um pdf-TeX comumente usado. Nenhum conhecimento prévio de fontes está disponível na instalação do TeX, portanto, arquivos de fontes externas, que fazem parte do ambiente local do TeX, são usados para obter informações para o documento.

## Sistema de composição ##

Cerca de 300 primitivas (comandos) podem ser compreendidas pelo sistema TeX básico. Primitivos são comandos de baixo nível, portanto, um usuário comum raramente os usa diretamente e a maioria das funcionalidades é executada por arquivos de formato. Esses arquivos de formato são imagens de memória pré-carregadas do TeX que são seguidas pelo carregamento de grandes coleções de macros. O formato padrão original da linguagem, ou seja, o TeX simples adiciona cerca de 600 comandos.

Uma barra invertida agrupada com chaves denota o início dos comandos do TeX. Como o TeX é uma linguagem baseada em macros e tokens, quase todas as características sintáticas do TeX podem ser alteradas em tempo de execução, incluindo as definidas pelo usuário, exceto os tokens não expansíveis que são então executados. A expansão em si é praticamente livre de problemas. Alguns comandos precisam vir depois de argumentos que ajudam a explicar a função de um comando. Por exemplo, o comando \vskip direciona o TEX para pular para baixo/subir a página seguido por um argumento determinando quanto espaço pular.

## Versões ##

LaTeX é o formato mais usado originalmente desenvolvido por Leslie Lamport. O LaTeX integra diferentes estilos de documentos para arquivos, cartas, livros e slides e oferece referência e numeração automática para diferentes seções e expressões matemáticas. AMS-TeX é outro formato popular, desenvolvido pela American Mathematical Society.

O AMS-TeX oferece muito mais comandos amigáveis, que podem ser redefinidos pelos periódicos para se adequarem ao seu estilo local. O LaTeX pode aproveitar os benefícios do AMS-TeX usando os "pacotes" do AMS, que são então denominados como AMS-LaTeX. ConTeXt é outro formato escrito por Hans Hagen usado principalmente para editoração eletrônica.

O software TeX oferece diversos recursos que não estavam disponíveis, ou de qualidade inferior, em outros sistemas tipográficos no momento de sua criação. Algumas das características inovadoras desta linguagem são baseadas em algoritmos interessantes derivados das teses dos alunos de Knuth. Enquanto outros programas de composição estão incorporando recursos úteis do TeX em seus programas.

## Referências ##

* [Sistema de composição TeX](https://en.wikipedia.org/wiki/TeX)

