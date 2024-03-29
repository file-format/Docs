{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo rtf", "formato de arquivo rtf", "o que é um arquivo rtf", "arquivo", "exemplo rtf", "extensão de arquivo rtf", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"RTF - Formato Rich Text",
  "description":"Saiba mais sobre o formato de arquivo RTF e APIs que podem criar e abrir arquivos RTF.",
  "linktitle" : "RTF",
  "menu" : {
    "docs" : {
      "parent" : "word-processing"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo RTF?

Introduzido e documentado pela Microsoft, o Rich Text Format (**RTF**) representa um método de codificação de texto e gráficos formatados para uso em aplicativos. O formato facilita a troca de documentos entre plataformas com outros Produtos da Microsoft, servindo assim ao propósito de interoperabilidade. Essa capacidade o torna um padrão de transferência de dados entre softwares de processamento de texto e, portanto, o conteúdo pode ser transferido de um sistema operacional para outro sem perder a formatação do documento. As especificações de formato de arquivo estão disponíveis pela Microsoft para download público e podem ser consultadas da perspectiva do desenvolvedor.

## Breve Histórico do Formato de Arquivo RTF ##

O formato de arquivo RTF passou por várias revisões desde sua publicação. Sua versão oficial para leitura/gravação foi publicada como parte do Microsoft Word 3.0 para Macintosh com especificações da versão 1.0. A versão final das especificações, 1.9.1, foi publicada pela Microsoft em março de 2008. Não foram feitas mais melhorias nas especificações depois disso. Atualmente, quase todos os sistemas operacionais têm aplicativos mais ricos em recursos que minimizaram/erradicaram o uso do formato de arquivo RTF.

## Especificações de formato de arquivo RTF ##

O RTF serve como um padrão de transferência de dados entre software de processamento de texto e transferência de conteúdo de um sistema operacional para outro. Isso é feito usando palavras de controle que foram introduzidas pelo Microsoft Office Word até 2007. Um arquivo RTF padrão consiste em ASCII para representar rich text e com caracteres não ASCII que são convertidos em valores de código apropriados. Versões mais recentes do Word podem ler arquivos RTF gerados com versões anteriores, enquanto as versões mais antigas ignoram palavras de controle e grupos que não entendem.

### Entendendo os fundamentos do RTF ###

Os arquivos RTF usam texto simples ASCII de 7 bits, consistindo em:

* palavras de controle
* símbolos de controle e
* grupos.

Estes atuam como os blocos de construção para a representação de dados RTF como texto compreensível e codificação de caracteres.

#### Palavra de controle ####

Eles representam comandos especialmente formatados usados para marcar caracteres para exibição e não podem ter mais de 32 letras. Uma palavra de controle é definida por:

\<ASCII Letter Sequence> //<//Delimiter//> //

Cada palavra de controle diferencia maiúsculas de minúsculas e começa com uma barra invertida. A sequência de letras ASCII pode conter alfabetos ASCII (a a z e A a Z). o<Delimite> marca o final do nome da palavra de controle e pode ser um dos seguintes:

* Um espaço. Isso serve apenas para delimitar uma palavra de controle e é ignorado no processamento subsequente.
* Um dígito numérico ou um sinal de menos ASCII, que indica que um parâmetro numérico está associado à palavra de controle. A seqüência digital subsequente é então delimitada por qualquer caractere que não seja um dígito ASCII (geralmente outra palavra de controle que começa com uma barra invertida). O parâmetro pode ser um número decimal positivo ou negativo. O intervalo dos valores para o número é nominalmente –32768 a 32767, ou seja, um inteiro de 16 bits com sinal. Um pequeno número de palavras de controle assume valores no intervalo‌ -2.147.483.648 a 2.147.483.647 (inteiro com sinal de 32 bits). Essas palavras de controle incluem **\binN**, **\revdttmN//**, **\rsidN** palavras de controle relacionadas e algumas propriedades de imagem como **\bliptagN**. Aqui **N** representa o parâmetro numérico. Um analisador RTF deve permitir até 10 dígitos opcionalmente precedidos por um sinal de menos. Se o delimitador for um espaço, ele é descartado, ou seja, não é incluído no processamento posterior.
* Qualquer caractere que não seja uma letra ou um dígito. Neste caso, o caractere delimitador termina a palavra de controle e não faz parte da palavra de controle. Como uma barra invertida “\”, que significa que uma nova palavra de controle ou um símbolo de controle segue.

#### Símbolo de controle ####

Um símbolo de controle representa uma ocorrência especial que tem um significado específico dependendo de seu conteúdo. Consiste em uma barra invertida seguida de um caractere especial (caractere não alfabético) e não possui delimitadores.

#### Grupo ####

Um grupo pode consistir em texto, palavras de controle ou símbolos de controle entre chaves (**{ }**). A chave de abertura (**{** ) indica o início do grupo e a chave de fechamento ( **}**) indica o fim do grupo. Cada grupo especifica o texto afetado pelo grupo e os diferentes atributos desse texto.

### Estrutura do arquivo RTF ###

Um arquivo RTF tem a seguinte sintaxe padrão:

Introduzido e documentado pela Microsoft, o Rich Text Format (**RTF**) representa um método de codificação de texto e gráficos formatados para uso em aplicativos. O formato facilita a troca de documentos entre plataformas com outros Produtos da Microsoft, servindo assim ao propósito de interoperabilidade. Essa capacidade o torna um padrão de transferência de dados entre softwares de processamento de texto e, portanto, o conteúdo pode ser transferido de um sistema operacional para outro sem perder a formatação do documento. As especificações de formato de arquivo estão disponíveis pela Microsoft para download público e podem ser consultadas da perspectiva do desenvolvedor.

#### Cabeçalho RTF ####

Um cabeçalho RTF tem a seguinte representação.

|Campo|Descrição
---|---|
|\<header> |**\rtf1\fbidis**? \<character set> \<from> ? \<deffont> \<deflang> \<fonttbl> ? \<filetbl> ? \<colortbl> ? \<stylesheet> ? \<stylerestrictions> ? \<listtables> ? \<revtbl> ? \<rsidtable> ? \<mathprops> ? \<generator> ?

As tabelas de cabeçalho devem aparecer nesta ordem se existirem. O arquivo RTF pode incluir grupos para fontes, estilos, cores da tela, imagens, notas de rodapé, comentários (anotações), cabeçalhos e rodapés, informações de resumo, campos, marcadores, propriedades de formatação de documentos, seções, parágrafos e caracteres, matemática, imagens e objetos. Se a fonte, arquivo, estilo, cor, marca de revisão e grupos de informações de resumo e propriedades de formatação de documento estiverem incluídos no arquivo, eles deverão aparecer no cabeçalho RTF, que precede o corpo RTF. Se o conteúdo de qualquer grupo não for usado, o grupo poderá ser omitido. Qualquer grupo que use as propriedades definidas em outro grupo deve aparecer após o grupo que define essas propriedades. Por exemplo, as propriedades de cor e fonte devem preceder o grupo de estilos.

#### Versão RTF ####

Um documento RTF deve começar com estes seis caracteres:

```
{\rtf1
```
onde o 1 mostra o número da versão RTF.

#### Conjunto de caracteres ####

Após o {\rtf1, o documento deve declarar qual conjunto de caracteres ele usa. A maneira de declarar um conjunto de caracteres é com um destes comandos:

`\ansi` - O documento está no conjunto de caracteres ANSI, também conhecido como Code Page 1252, o conjunto de caracteres usual do MSWindows.

`\mac` - O documento está no conjunto de caracteres MacAscii, o conjunto de caracteres usual em versões antigas (pré-10) do Mac OS.

`\pc` - O documento está em DOS Code Page 437, o conjunto de caracteres padrão para MS-DOS. Datilógrafos com boa memória muscular notarão que este é o conjunto de caracteres que ainda é usado para interpretar códigos “Alt numéricos” – ou seja, quando você mantém pressionado Alt e digita “130” no teclado numérico, ele produz um é, porque o caractere 130 em CP437 é um é. Esse é o único uso que o CP437 vê nos dias de hoje.

`\pca` - O documento está em DOS Code Page 850, também conhecido como MS-DOS Multilingual Code Page.

#### Comando de fonte ####

A definição do conjunto de caracteres é seguida pelo comando `\deffN`. Isso define que o número da fonte N é a fonte padrão para este documento. O número da fonte N é referido na tabela de fontes. O comando `\deffN` é tecnicamente opcional, mas deve estar no lado seguro como um prólogo comum, como a seguir, escolhe a fonte 0 como a fonte padrão.

`{\rtf1\ansi\deff0`

#### Tabela de fontes ####

Todas as fontes que podem ser usadas em um documento são listadas em uma tabela de fontes onde cada fonte é representada por um número de fonte. O documento deve ter uma tabela de fontes, embora alguns programas funcionem sem isso também.

A sintaxe para uma tabela de fontes é {\fonttbl //...declarations//...}, em que cada declaração tem esta sintaxe básica:

`{\fnumber\familycommand Fontname;}`

Uma tabela de fontes com quatro declarações é a seguinte:

```
{\fonttbl
{\f0\froman Times;}
{\f1\fswiss Arial;}
{\f2\fmodern Courier New;}
}
```

Em um documento com essa tabela de fontes, `{\f2 stuff}` imprimiria “coisas” em Courier New. Uma fonte não pode ser usada em um documento até que esteja listada na tabela de fontes.

### Fim do documento ###

Todo documento RTF deve terminar com um }, para fechar o grupo aberto pelo { que é o primeiro caractere do documento. Nada pode seguir o } final, exceto possivelmente uma nova linha.

## Referências ##
* [Formato Rich Text](https://en.wikipedia.org/wiki/Rich_Text_Format)
