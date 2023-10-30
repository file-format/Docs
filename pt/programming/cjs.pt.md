{
  "date" : "2023-10-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo CJS - Arquivo de código CommonJS",
  "description":"O que é um arquivo .cjs e como abri-lo?",
  "linktitle" : "CJS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
    }
  },
  "lastmod" : "2023-10-29"
}

## O que é um arquivo CJS?

Um arquivo CommonJS (CJS) é um arquivo que contém código JavaScript escrito na sintaxe CommonJS. CommonJS é um sistema de módulo projetado para funcionar em ambientes além de navegadores front-end e é frequentemente usado em ambientes JavaScript do lado do servidor, como Node.js.

## Formato de arquivo CJS - Mais informações

Os arquivos CJS são escritos na sintaxe CommonJS e podem ser editados em qualquer editor de texto, como Microsoft Notepad ou Apple TextEdit. Os módulos CommonJS são normalmente armazenados em arquivos separados e destinam-se a encapsular e modularizar o código para melhor organização e manutenção. Esses módulos usam a função necessária para importar dependências e o objeto module.exports ou exports para expor valores e funções que podem ser usados por outras partes do código.

## Exemplo de código CJS

Os módulos CommonJS possuem uma sintaxe e estrutura específicas que incluem recursos como a função necessária para importar outros módulos e module.exports ou exporta objetos para exportar valores, funções ou objetos de um módulo. Esses módulos são usados para encapsular e separar partes de código, facilitando o gerenciamento e a manutenção de grandes bases de código JavaScript. Aqui está um exemplo básico de um módulo CommonJS:

```
// Module definition in a file named "myModule.js"
const someValue = 42;

function add(a, b) {
  return a + b;
}

module.exports = {
  someValue,
  add,
};

// Using the module in another file
const myModule = require('./myModule');
console.log(myModule.someValue); // 42
console.log(myModule.add(10, 20)); // 30
```

## Referências

* [Design Classes in Visual Studio](https://en.wikipedia.org/wiki/CommonJS)