{
  "date" : "2021-09-13", 
  "keywords" :[ "ici", "arquivo", "extensão", "formato de arquivo", "implementação de ICI", "Guia de Programação", "exemplo de ICI", "linguagem de programação ICI", "módulos de ICI", "modelo de dados de ICI ", "documentação do ICI", "idioma do ICI" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ICI - Arquivo de linguagem de programação",
  "description":"Saiba mais sobre o formato de arquivo ICI e APIs que podem criar e abrir arquivos ICI.",
  "linktitle" : "ICI",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-09-13"
}

## O que é um arquivo ICI?

Uma linguagem de programação de uso geral que é interpretada e contém vários recursos, como tipagem dinâmica junto com os tipos de dados flexíveis, é conhecida como linguagem de programação ICI (não um acrônimo). É considerado semelhante à linguagem [Perl](/pt/programming/pl/). Essa linguagem ICI compreende construções de controle de fluxo e também contém alguns operadores da linguagem C. Não é uma linguagem orientada a objetos, mas alguns dos recursos da OOP podem ser obtidos por um método de herança específico conhecido como superestruturas. Semelhante a [C](/pt/programming/c), esta linguagem de programação ICI possui a mesma interface do sistema e uma biblioteca padrão para funções integradas.


## Breve história ##

No final dos anos 80, foi desenvolvido por Tim Long como uma linguagem de programação interpretada de propósito geral. A maioria dos recursos desta linguagem é semelhante ao C e também pode alcançar alguns dos recursos aplicando alguns métodos especiais. Esta linguagem é de domínio público e está disponível como uma linguagem revenda e ninguém é obrigado a mencionar de onde obteve o código-fonte. A documentação da ICI está sob os direitos autorais da Canon Information System Research Australia.

## Especificação Técnica ##

Existem dois tipos de dados diferentes usados nesta linguagem. Esses dois são tipos de dados primitivos e agregados. Ambos incluem diferentes expressões de acordo com sua composição pré-definida na linguagem. Diferentes módulos como aninhados e sub-rotinas são suportados por esta linguagem. Como algumas de suas propriedades são semelhantes ao Perl, ele possui uma integração estrita com as expressões regulares.

Os conjuntos são confinados a serem heterogêneos e aninhados. Esses conjuntos fornecem suporte para operações de conjunto comumente usadas, como União e Interseção, etc. É usado principalmente como uma linguagem para implementação central para aplicativos pertencentes a organizações multinacionais.

Quase todos os tipos de programas podem ser escritos nesta linguagem e principalmente os programas específicos que envolvem estruturas de dados complexas são escritos na linguagem de programação ICI. Os aplicativos podem envolver a implementação do ICI de uma forma que devem ser escritos nele. Partes funcionais do aplicativo podem ser implementadas pelos módulos do ICI. A linguagem do ICI se assemelha um pouco à linguagem C, mas o modelo de dados do ICI é de nível bastante superior e diferente com tipos como dicionários (struct), conjuntos, matrizes dinâmicas, expressões regulares e strings (reais).


## Exemplo de formato de arquivo ICI ##

```

printf("Hello world.\n");

```

```
s = [set 200, 300, "a string"];
if (s[200])
	printf("200 is in the set\n");
if (s[400])
	printf("400 is in the set\n");
if (s["a string"])
	printf("\"a string\" is in the set\n");
s[200] = 0;
if (s[200])
	printf("200 is in the set\n");

```

```

forall (colour in [array "red", "green", "blue"])
	printf("%s\n", colour);

```

## Referência ##

* [Linguagem de programação ICI](http://atrn.org/ici/doc/ici.html)



