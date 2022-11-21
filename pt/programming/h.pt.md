{
  "date" : "2019-10-11",
  "keywords" :[ "h", ".h", "o que é um arquivo h", "como abrir um arquivo h", "extensão", "arquivo", "arquivo h", "formato de arquivo h", "extensão de arquivo h", "Exemplo de arquivo H"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"H - Formato de arquivo de cabeçalho C/C++",
  "description":"Saiba mais sobre o formato de arquivo H e as APIs que podem criar e abrir o arquivo H.",
  "linktitle" : "H",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-07"
}

## O que é um arquivo H?

Um arquivo salvo com **h extensão de arquivo** é um arquivo de cabeçalho usado em arquivos C/C++ para incluir a declaração de variáveis, constantes e funções. Eles são referidos pelos arquivos de implementação [C++](/pt/programming/cpp/) que contêm a implementação real dessas funções. Um arquivo de cabeçalho .h também pode incluir informações adicionais, como definições de macro. Esses arquivos de cabeçalho são referenciados nos arquivos C/C++ usando a diretiva `#include`.

Um novo projeto C++ geralmente contém um arquivo de cabeçalho especial chamado arquivo **stdafx.h** que é o ponto de partida para todas as cadeias de compilação e todos os arquivos de cabeçalho podem ser incluídos nesse único arquivo. Um arquivo .h pode ser aberto com qualquer editor de texto, Eclipse IDE, Microsoft Visual Studio IDE, compilador Borland C++ e muitos outros aplicativos.

## Formato de arquivo .H

Um arquivo .h é um arquivo de texto simples que possui suas próprias regras para definir a sintaxe. Os arquivos de cabeçalho podem conter as seguintes informações.

**`Variables`** - No caso de Programação Orientada a Objetos (OOP), um arquivo de cabeçalho de classe contém definições de todas as variáveis de nível de classe que são acessíveis nos arquivos de código-fonte de implementação
**`Declaração de Métodos`** - Todas as declarações de métodos são incluídas nos arquivos de cabeçalho .h para serem acessíveis em vários arquivos de implementação.
**`Definições de Função Não Inline`** - Arquivos de cabeçalho também podem conter definições de métodos não embutidos.
**`Message Maps`** - Um arquivo de cabeçalho também pode conter mapas de mensagens no caso de uma implementação de código-fonte MFC. Nesse caso, os mapas de mensagens estão vinculados à implementação da funcionalidade que está vinculada aos elementos da interface do usuário, como botão, caixa de seleção, botões de opção, etc.


### Protetores de cabeçalho

Os arquivos de cabeçalho podem gerar erros complexos em que várias declarações são incluídas no mesmo arquivo como resultado da adição de outros arquivos de cabeçalho. Essas definições duplicadas geram erros do compilador. Essa situação problemática pode ser evitada por meio de um mecanismo chamado proteção de cabeçalho, que são diretivas de compilação condicional, conforme mostrado abaixo.

```
#ifndef ANY_UNIQUE_NAME_HERE
#define ANY_UNIQUE_NAME_HERE

// your declarations (and certain types of definitions) here

#endif
```
Com este cabeçalho, o pré-processador verifica se o `ANY_UNIQUE_NAME_HERE` já foi definido. Se o cabeçalho for incluído repetidamente no mesmo arquivo, o conteúdo do cabeçalho será ignorado.

## Exemplo de arquivo H

```
// sample.h
#pragma once
#include <vector> // #include directive
#include <string>

namespace N  // namespace declaration
{
    inline namespace P
    {
        //...
}

    enum class colors : short { red, blue, purple, azure };

    const double PI = 3.14;  // const and constexpr definitions
    constexpr int MeaningOfLife{ 42 };
    constexpr int get_meaning()
    {
        static_assert(MeaningOfLife == 42, "unexpected!"); // static_assert
        return MeaningOfLife;
}
    using vstr = std::vector<int>;  // type alias
    extern double d; // extern variable

#define LOG   // macro definition

#ifdef LOG   // conditional compilation directive
    void print_to_log();
#endif

    class my_class   // regular class definition,
    {                // but no non-inline function definitions

        friend class other_class;
    public:
        void do_something();   // definition in my_class.cpp
        inline void put_value(int i) { vals.push_back(i); } // inline OK

    private:
        vstr vals;
        int i;
    };

    struct RGB
    {
        short r{ 0 };  // member initialization
        short g{ 0 };
        short b{ 0 };
    };

    template <typename T>  // template definition
    class value_store
    {
    public:
        value_store<T>() = default;
        void write_value(T val)
        {
            //... function definition OK in template
    }
    private:
        std::vector<T> vals;
    };

    template <typename T>  // template declaration
    class value_widget;
}
```

## Referências

* [Arquivadores de cabeçalho - Microsoft](https://docs.microsoft.com/en-us/cpp/cpp/header-files-cpp?view=msvc-160)

