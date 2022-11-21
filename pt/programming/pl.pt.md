{
  "date" : "2021-07-23",
  "keywords" :[ "PL", "arquivo", "extensão", "formato", "Perl", "linguagem Perl", "arquivos PL", "programação"],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo PL e APIs que podem criar e abrir arquivos PL.",
  "title" :"Arquivo PL - Formato de arquivo de script Perl",
  "linktitle" : "PL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-07-23"
}

## O que é um arquivo PL?

Um arquivo com extensão .pl é um arquivo Perl Script que é uma linguagem de script. Estes são compilados e executados usando o software Perl Interpreter. Um arquivo de script PL contém linhas de código, variáveis e comentários. As linguagens de script são comparativamente difíceis de
entender outros formatos de arquivo de programação, como [PHP](/pt/programming/php/). Os arquivos PL podem ser criados e são compatíveis com Windows, macOS e Linux.

## Breve História da Linguagem de Script Perl

Essa linguagem foi mantida em uso pela primeira vez em 1987, então esses arquivos tiveram sua origem naquele ano. Em 1989, o Perl 2 foi lançado. Mais tarde, foi atualizado e modificado até a versão 5.35, e a próxima versão está prevista para ser lançada no próximo ano.

Em cada atualização, foram adicionadas ferramentas sobre a funcionalidade, desempenho e aparência do idioma e dos arquivos. Houve muitas revisões sobre as versões nestes anos. Era originalmente uma linguagem de script básica, mas agora compreende muitos outros módulos também. Originalmente, era uma linguagem muito simples, mas os scripts dessa linguagem eram bastante difíceis de entender, pois eram compactos.

## Especificações de extensão de formato de arquivo Perl

Existem algumas propriedades ou especificações desses arquivos de programação, algumas delas são as seguintes:

* O código incluído nesses arquivos está em formato de texto simples e usado para desenvolvimento de scripts
* Scripting de servidor, análise de texto e administração de servidor são os principais aspectos que o script desta linguagem cobre
* Muitos programas populares associados a esta linguagem são Active state Active Perl e Bare Bones BBEdit (compatível com Mac OS)
* Esta linguagem é considerada uma linguagem de alto nível
* Para Win32, o usuário pode ter que instalar a distribuição binária nativa do idioma
* Requer algumas ferramentas de script para se tornar executável em vários Windows Resource Kits
* Visual Studio .NET é um framework famoso para o desenvolvimento de linguagens de programação. A ferramenta Active State conhecida como Visual Perl é usada para adicionar Perl ao Visual studio
* Nos arquivos, a primeira linha do código fonte descreve as informações do interpretador que está sendo utilizado. Os arquivos PL geralmente começam com a linha **#!/usr/bin/perl** que diz ao seu computador para executar este script usando um interpretador Perl instalado no computador


## Exemplos de script PL

```
#!/usr/bin/perl
print "Hello, world\n";
```

Isso irá imprimir

```
Hello, World
```

### Comentário de linha única ###

```
#!/usr/bin/perl
# This is a single line comment
print "Hello Perl\n";
```

### Comentário de várias linhas ###

```
#!/usr/bin/perl
=begin comment
This is a multiline comment.
Line 1
Line 2
=cut
print "Hello Perl\n";
```

### Atribuição de variável ###

```
#!/usr/bin/perl
$a = 10;
print "Variable a = $a\n";
```

### Atribuição de variável escalar ###

```
#!/usr/bin/perl
$age = 35; # Assigning an integer
$name = "Tony Stark"; # Assigning a string
$pi = 3.14; # Assigning a floating point
```

### Operações escalares simples ###

```
#!/usr/bin/perl
$constr = "hi" . "perl";# Concatenates two or more strings.
$add = 40 + 10; # addition of two numbers.
$prod = 4 * 51;# multiplication of two numbers.
$connumstr = $constr . $add;# concatenation of string and number.
```

## Referências ##

- [Python (linguagem de programação) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

