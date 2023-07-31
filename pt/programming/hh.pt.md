{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".hh","o que é um arquivo .hh","como abrir um arquivo .hh", "extensão", "arquivo", "arquivo .hh",".hh formato de arquivo", " .hh extensão de arquivo",".Exemplo de arquivo HH"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HH - Formato de arquivo de cabeçalho C++",
  "description":"Saiba mais sobre o formato de arquivo HH e as APIs que podem criar e abrir o arquivo HH.",
  "linktitle" : "HH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-20"
}

## O que é um arquivo HH?

Um arquivo com extensão .hh é um arquivo de cabeçalho C++ que inclui a declaração de variáveis, constantes e funções. Essas declarações são usadas pelos arquivos de implementação C++ correspondentes, geralmente salvos como arquivos [.cpp](/pt/programming/cpp/) que contêm a implementação real da lógica do usuário. Os arquivos de cabeçalho .hh são referenciados nos arquivos CPP de implementação usando a diretiva `#include`. Você pode adicionar o máximo possível de arquivos de cabeçalho ao seu projeto C++ para incluir declarações de nível de projeto.

## Formato de arquivo .HH

Um arquivo .hh é um arquivo de texto simples que é criado mantendo em vista as regras de definição do arquivo de cabeçalho. As informações mais comuns declaradas em um arquivo .hh incluem o seguinte.

**`Variables`** - No caso de Programação Orientada a Objetos (OOP), um arquivo de cabeçalho de classe contém definições de todas as variáveis de nível de classe que são acessíveis nos arquivos de código-fonte de implementação
**`Declaração de Métodos`** - Todas as declarações de métodos são incluídas nos arquivos de cabeçalho .h para serem acessíveis em vários arquivos de implementação.
**`Definições de Função Não Inline`** - Arquivos de cabeçalho também podem conter definições de métodos não embutidos.
**`Message Maps`** - Um arquivo de cabeçalho também pode conter mapas de mensagens no caso de uma implementação de código-fonte MFC. Nesse caso, os mapas de mensagens estão vinculados à implementação da funcionalidade que está vinculada aos elementos da interface do usuário, como botão, caixa de seleção, botões de opção, etc.

## Diferença entre arquivos .H e .HH

Aparentemente, não existe essa diferença entre os arquivos de cabeçalho .h e .hh além da maneira recomendada de usá-los para as respectivas linguagens, ou seja, [C](/pt/programming/c/) ou C++. Nomear seus arquivos de cabeçalho de acordo com essas linguagens ajuda a distinguir entre eles em um projeto grande que pode ser uma mistura de implementações C e C++.

Além disso, se os cabeçalhos forem separados por extensão, seu editor poderá aplicar a formatação apropriada automaticamente para respectivamente.

No geral, a diferenciação desses dois formatos de arquivo não causará nenhum dano, mas será vantajosa, e é incentivada a seguir a distinção entre C e C++.

### Protetores de cabeçalho

Os arquivos de cabeçalho podem gerar erros complexos em que várias declarações são incluídas no mesmo arquivo como resultado da adição de outros arquivos de cabeçalho. Essas definições duplicadas geram erros do compilador. Essa situação problemática pode ser evitada por meio de um mecanismo chamado proteção de cabeçalho, que são diretivas de compilação condicional, conforme mostrado abaixo.

```
#ifndef ANY_UNIQUE_NAME_HERE_HPP
#define ANY_UNIQUE_NAME_HERE_HPP

// your declarations (and certain types of definitions) here

#endif
```
Com este cabeçalho, o pré-processador verifica se o `ANY_UNIQUE_NAME_HERE_HPP` já foi definido. Se o cabeçalho for incluído repetidamente no mesmo arquivo, o conteúdo do cabeçalho será ignorado.

## Referências

* [Arquivadores de cabeçalho - Microsoft](https://learn.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)
* [Diferença entre os formatos de arquivo .h e .hh](https://stackoverflow.com/questions/10354321/c-reason-why-using-hh-as-extension-for-c-header-files)

