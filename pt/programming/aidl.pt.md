{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo AIDL - Arquivo de linguagem de definição de interface Android",
  "description":"Saiba o que é o formato de arquivo AIDL com exemplos e APIs que podem criar e abrir arquivos AIDL.",
  "linktitle" : "AIDL",
  "menu" : {
    "docs" : {
      "identifier": "programming-aidl",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## O que é um arquivo AIDL?

Um arquivo AIDL (Android Interface Definition Language) permite que os desenvolvedores do Android estabeleçam comunicação entre diferentes aplicativos. Com base na interface de programação, o cliente e o serviço concordam em se comunicar usando a comunicação entre processos (IPC). O arquivo AIDL contém o código-fonte [Java](/pt/programming/java/) para definir essas interfaces e contratos para comunicação entre aplicativos.

Você pode abrir arquivos AIDL com o Google Android Studio ou qualquer editor de texto, como o Microsoft Notepad e o Notepad++.

## Formato de arquivo AIDL - Mais informações

AIDL são arquivos de texto que contêm as interfaces para comunicação entre aplicativos. O sistema operacional Android não permite que um processo acesse a memória de outro processo. Isso leva os processos a dividir seus objetos em primitivos para compreensão do sistema operacional subjacente e estabelecer o processo de estruturas de comunicação para o desenvolvedor.

### Quais tipos de dados são suportados pelo AIDL?

AIDL suporta os seguintes tipos de dados por padrão.

* Todos os tipos primitivos na linguagem de programação Java (como int, long, char, boolean e assim por diante)
* Corda
* Sequência de caracteres
* Lista
* Mapa

## Exemplo de arquivo AIDL

A seguir está um exemplo de arquivo AIDL.

```
// IRemoteService.aidl
package com.example.android;

// Declare any non-default types here with import statements

/** Example service interface */
interface IRemoteService {
    /** Request the process ID of this service, to do evil things with it. */
    int getPid();

    /** Demonstrates some basic types that you can use as parameters
     * and return values in AIDL.
     */
    void basicTypes(int anInt, long aLong, boolean aBoolean, float aFloat,
            double aDouble, String aString);
}

```
## Referências

* [Linguagem de definição de interface Android (AIDL)](https://stuff.mit.edu/afs/sipb/project/android/docs/guide/components/aidl.html)

