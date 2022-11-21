{
  "date" : "2019-10-11",
  "keywords" :[ "JAR", ".jar","o que é um arquivo jar","como abrir um arquivo jar", "extensão", "arquivo", "arquivo jar","formato de arquivo jar", "extensão .jar "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"JAR - Formato de arquivo de arquivo Java",
  "description":"Saiba mais sobre o formato de arquivo JAR e as APIs que podem criar e abrir o arquivo JAR.",
  "linktitle" : "JAR",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo JAR?

Um arquivo com extensão .jar é um arquivo Java Archive que contém muitos arquivos diferentes relacionados a aplicativos como um único arquivo. Este formato de arquivo foi criado para reduzir a velocidade de carregamento de um Java Applet baixado no navegador via transação HTTP, evitando a criação de múltiplas conexões HTTP. Um único arquivo JAR pode conter arquivos de classe Java ([.class](/pt/programming/class/)), [images](/pt/image/) e [sounds](/pt/audio/). Itens individuais dentro de um arquivo JAR podem ser assinados digitalmente pelo desenvolvedor do aplicativo para autenticar sua origem. Os arquivos JAR são usados regularmente para criar APIs funcionais que contêm funcionalidades específicas relacionadas a essa API.

## Formato de arquivo JAR

Os arquivos JAR são baseados no popular [formato de arquivo ZIP](/pt/compression/zip/) que arquiva seus arquivos de conteúdo individuais em um único arquivo. O formato de arquivo JAR suporta compactações, resultando em um tamanho de arquivo menor para download e, portanto, melhora ainda mais o tempo de download. O artigo [especificações do arquivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jar.html) da Oracle fornece detalhes completos sobre as especificações internas dos arquivos JAR.

### O arquivo de manifesto

Quando um arquivo JAR é criado, um arquivo de manifesto é criado automaticamente dentro dele que contém as informações de metadados sobre o conteúdo do arquivo JAR. Este arquivo mostra o conteúdo que está empacotado dentro do arquivo JAR. Um arquivo de manifesto típico tem a seguinte aparência, que mostra as pastas e classes incluídas no arquivo JAR.

```
META-INF/
META-INF/MANIFEST.MF
pack/
pack/class1.class
pack/class2.class
..
..
```

#### Especificações do manifesto

As especificações do manifesto são definidas pela Oracle da seguinte forma.

`manifest-file`: nova linha da seção principal \*seção individual

`main-section`: nova linha de informação da versão \*main-attribute

`version-info`: Manifest-Version : version-number

`version-number`: digit+{.digit+}*

`main-attribute`: (qualquer atributo principal legítimo) nova linha

`individual-section`: Nome: valor nova linha \*perentry-attribute

`perentry-attribute`: (qualquer atributo de perentry legítimo) nova linha

`nova linha` : CR LF | LF | CR (não seguido por LF)

`digit`: {0-9}

### JAR executável

Os arquivos JAR também podem incluir um aplicativo que pode ser executado pela Java Virtual Machine (JVM) semelhante a qualquer outro aplicativo no sistema operacional Microsoft Windows. Nesse caso, a JVM precisa saber sobre o ponto de entrada do aplicativo que é qualquer classe com um método main public static void. O arquivo de manifesto identifica tal classe com o cabeçalho `Main-Class` no seguinte formato:

```
Main-Class: com.example.MyClassName
```



## Referências

* [Visão geral do arquivo JAR](https://docs.oracle.com/javase/8/docs/technotes/guides/jar/jarGuide.html)
* [Formato de arquivo JAR](https://en.wikipedia.org/wiki/JAR_(file_format)#:~:text=A%20JAR%20(Java%20ARchive)%20is,into%20one%20file%20for% 20distribution.&text=Eles%20são%20construídos%20em%20a extensão jar%20file%20.)

