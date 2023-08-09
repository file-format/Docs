{
  "date" : "2019-10-11",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo BML - arquivo de linguagem de marcação Bean",
  "description":"Saiba mais sobre o formato de arquivo BML e APIs que podem criar e abrir arquivos BML.",
  "linktitle" : "BML",
  "menu" : {
    "docs" : {
      "parent" : "web"
}
},
  "lastmod" : "2021-08-12"
}

## O que é um arquivo BML?

Um arquivo com extensão .bml é um arquivo Bean Markup Language que armazena classes Java para oferecer suporte a aplicativos Java. Isso permite o acesso a objetos e métodos Java e não precisa criar novas funcionalidades usando classes Java. Especifica como os componentes são conectados uns aos outros para executar tarefas úteis. BML foi desenvolvido pela IBM alphaWorks para descrever as estruturas e relacionamentos de componentes. Os arquivos BML podem ser abertos e visualizados usando qualquer editor de texto, como navegadores da Web, Microsoft Notepad e Notepad++.

## Formato de arquivo BML

O website IBM alphaworks forneceu duas implementações de BML. A primeira implementação é um interpretador que 'toca' um script BML para gerar a hierarquia de bean desejada. A segunda implementação é um compilador que compila qualquer script BML em código Java sem reflexão. Isso é vantajoso no sentido de que permite capturar a estrutura entre componentes do aplicativo usando uma linguagem projetada para esse propósito específico com a capacidade adicional de compilá-la em código Java 'regular'.

## Etiquetas BML

A seguir está uma explicação de algumas das tags usadas na linguagem BML:

### O<bean> marcação:

o<bean> O elemento é usado para criar novos beans ou procurar beans por nome. o<bean> tag está no formato:
```
<bean class = "classname or serialized file" [id = "name"]>
</bean>
```
O "id" na tag está associado ao registro de objeto para o JavaBean.

### O<string> marcação

Há duas maneiras de usar a tag string:

1. Para criar uma string não vazia:

```
<string [value = "value of string"]> [value of string]
</string>
```
2. Para criar uma string vazia:

```
<string/>
```
## Referências

* [Mensagens orientadas a objetos com XML](https://docs.oracle.com/cd/A87860_01/doc/appdev.817/a86030/adx16nt5.htm)
* [A Linguagem de Marcação Física](http://web.mit.edu/mecheng/pml/standards.htm)


