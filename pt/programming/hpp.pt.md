{
"data": "08/06/2023",
  "keywords": [
"arquivo hpp",
"o que é um arquivo hpp",
"o que contém o arquivo hpp",
"exemplo de arquivo hpp",
"qual é o formato do arquivo hpp",
"arquivo",
"extensão de arquivo hpp",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo HPP - Arquivo de cabeçalho C++",
  "description":"Aprenda sobre o formato HPP e APIs que podem criar e abrir arquivos HPP.",
"linktitle": "HPP",
  "menu": {
    "docs": {
      "identifier": "programming-hpp",
"parent" : "programming"
}
},
"último mod": "08/06/2023"
}

## O que é um arquivo .HP?

O formato de arquivo ".hpp" é comumente usado para arquivos de cabeçalho na linguagem de programação C++. Os arquivos de cabeçalho normalmente contêm declarações e definições de funções, classes, variáveis e constantes que são usadas por outros arquivos de código-fonte no projeto C++.

O objetivo do uso de arquivos de cabeçalho é fornecer uma maneira de compartilhar código comum em vários arquivos de código-fonte sem duplicar o próprio código. Quando o arquivo de origem C++ precisa acessar declarações ou definições do arquivo de cabeçalho, ele inclui o arquivo de cabeçalho usando a diretiva de pré-processador `#include`.

A extensão de arquivo ".hpp" é frequentemente usada para indicar que um arquivo é um arquivo de cabeçalho C++. Não é obrigatório usar esta extensão específica para arquivos de cabeçalho, e você também pode encontrar arquivos de cabeçalho com “.h” ou outras extensões. A escolha da extensão é em grande parte uma questão de convenção e preferência pessoal.

Quando um arquivo de origem C++ inclui o arquivo de cabeçalho usando `#include`, o compilador combina efetivamente o conteúdo do arquivo de cabeçalho com o arquivo de origem antes de compilá-lo como uma unidade. Isso permite que o arquivo fonte acesse declarações e definições no arquivo de cabeçalho, fornecendo as informações necessárias para que o compilador execute a verificação de tipo e geração de código.

## O que o arquivo HPP contém?

Aqui estão alguns conteúdos comuns que você pode encontrar no arquivo ".hpp":

- **Declarações de funções:** Os arquivos de cabeçalho geralmente incluem declarações de funções sem suas implementações reais. Essas declarações fornecem informações sobre o nome da função, tipo de retorno e parâmetros, permitindo que outros arquivos de código-fonte usem a função sem a necessidade de saber detalhes de implementação.
- **Declarações de classe:** Os arquivos de cabeçalho podem conter declarações de classe, incluindo nome de classe, variáveis de membro, funções de membro e especificadores de acesso. Ao incluir a declaração de classe no arquivo de cabeçalho, outros arquivos de código-fonte podem criar objetos dessa classe e acessar seus membros.
- **Declarações constantes:** Os arquivos de cabeçalho podem definir constantes, como variáveis globais ou valores enum que devem ser compartilhados entre vários arquivos de código-fonte. Essas constantes podem ser acessadas incluindo o arquivo de cabeçalho em outros arquivos de origem, permitindo-lhes usar as constantes definidas.
- **Definições de tipo:** Os arquivos de cabeçalho podem conter definições de tipo usando a palavra-chave "typedef" ou aliases de tipo usando a palavra-chave "using". Essas definições criam novos nomes para tipos existentes, tornando o código mais legível e de fácil manutenção.
- **Definições de funções embutidas:** Em alguns casos, os arquivos de cabeçalho podem conter definições de funções embutidas. Funções embutidas são pequenas funções que são expandidas no site de chamada em vez de serem chamadas como funções separadas. Incluir a definição de função embutida no arquivo de cabeçalho permite que o compilador substitua a chamada de função diretamente pelo corpo da função, melhorando potencialmente o desempenho.

## Exemplo de arquivo HPP

```
#ifndef PERSON_HPP
#define PERSON_HPP

#include <string>

class Person {
private:
    std::string name;
    int age;

public:
    Person();
    Person(const std::string& name, int age);
    void setName(const std::string& newName);
    void setAge(int newAge);
    std::string getName() const;
    int getAge() const;
    void printInfo() const;
};

#endif

```

## Qual é o formato do arquivo HPP?

HPP é um arquivo de texto simples, mas segue as regras gerais e a sintaxe da linguagem de programação C++. Aqui está uma análise do formato geral e da estrutura do arquivo ".hpp":

- **Proteções de cabeçalho:** Normalmente, um arquivo ".hpp" começa com proteções de cabeçalho para evitar múltiplas inclusões do mesmo arquivo. Isso é conseguido usando diretivas de pré-processador como `#ifndef`, `#define` e `#endif`. A proteção do cabeçalho garante que o conteúdo do arquivo seja incluído apenas uma vez durante o processo de compilação.
- **Incluir instruções:** Após os protetores de cabeçalho, você pode incluir outros arquivos de cabeçalho necessários usando a diretiva `#include`. Eles podem incluir cabeçalhos de biblioteca padrão ou outros cabeçalhos personalizados exigidos pelo seu código.
- **Declarações e Definições:** O conteúdo principal do arquivo ".hpp" são as declarações e, em alguns casos, definições de classes, funções, constantes, aliases de tipo e outros elementos. Por exemplo, você pode declarar classes usando a palavra-chave `class`, funções usando seu tipo de retorno, nome e lista de parâmetros e constantes usando a palavra-chave `const` seguida de seu tipo e nome.
- **Definições de funções inline:** Em certos casos, você pode incluir definições de funções inline diretamente no arquivo ".hpp". Funções inline são geralmente definidas dentro do corpo da classe, o que significa que a definição da função é incluída junto com sua declaração. Isso pode ser feito prefixando a definição da função com a palavra-chave `inline`.
- **Declarações de namespace:** Se você estiver usando namespaces em seu código, poderá declará-los no arquivo ".hpp". Isso é feito usando a palavra-chave `namespace` seguida pelo nome do namespace e colocando o código relevante dentro do bloco de namespace.

## Referências
* [Arquivos de cabeçalho (C++)](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

