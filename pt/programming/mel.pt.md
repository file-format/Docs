{
  "date" : "2019-10-11",
  "keywords" :[ ".mel", "Linguagem incorporada do Maya","arquivo", "extensão", "formato de arquivo", "Maya 3D", "Guia de programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MEL - Formato de arquivo de idioma incorporado do Maya",
  "description":"Saiba mais sobre o formato de arquivo MEL e APIs que podem criar e abrir arquivos MEL.",
  "linktitle" : "MEL",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-03-08"
}

## O que é um arquivo MEL?

Um arquivo com extensão .mel (Maya Embedded Language) é uma linguagem de script que é usada pelo Autodesk Maya para criar interfaces gráficas. Ele permite automatizar a criação de elementos gráficos usando scripts executáveis além da interface gráfica do Maya. O MEL permite que você crie interfaces gráficas sem aprender a programar. Isso é feito criando Macros e ações personalizadas que aceleram tarefas repetitivas. Esses procedimentos e scripts permitem criar modelagem, animações, dinâmicas e renderização de tarefas personalizadas. O Autodesk Maya 2020 pode ser usado para abrir e visualizar o conteúdo de um arquivo EML.

## Formato de arquivo MEL - Mais informações

Um [manual de referência](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865) do programador está disponível para desenvolvedores na seção de documentação do Maya. O MEL é baseado em comandos de script de shell, semelhantes ao UINX, para alcançar as coisas. Os comandos baseados em script o tornam irrelevante para programação convencional e orientada a objetos (OOP), resultando em nenhum uso de estruturas de dados, funções de chamada ou uso de OOP como em outras linguagens.

Alguns pontos-chave sobre MEL são os seguintes.

`Comments` - Toda instrução em MEL deve terminar com ponto e vírgula (;), mesmo no final de um bloco.

`Retornando Valores` - Declarar uma expressão que retorna um valor não imprime automaticamente o valor em MEL. Em vez disso, causa um erro.
```
3 + 5;
// Error: 3 + 5; //
// Error: Syntax error //
print(3+5);
8
```
`Comandos para criar, editar e excluir` - O mesmo comando é usado para criar coisas, editar coisas ou consultar informações sobre coisas existentes. No entanto, um sinalizador controla o que (criar, editar ou consultar) o comando faz.

```
// Create a sphere named "mySphere" with radius 5
sphere -radius 5 -name "mySphere";
// Edit the radius of mySphere
sphere -edit -radius "mySphere";
// Print the radius of mySphere
sphere -query -radius

```
`Return Value from Function` - A sintaxe da função retorna automaticamente um valor. Para obter um valor de retorno usando a sintaxe de comando, você deve colocar o comando entre aspas.

```
$a = getAttr("mySphere.translateX"); // Function syntax
$b = `getAttr mySphere.translateY`; // Command syntax
```

## Referências

* [MEL](https://download.autodesk.com/us/maya/2009help/index.html?url=Glossary_M_.mb_file_format.htm,topicNumber=d0e193865)

