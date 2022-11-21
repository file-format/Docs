
{
  "date" : "2022-10-30",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo ADS - Formato de Arquivo de Especificação Ada",
  "description":"Saiba mais sobre o que é o formato de arquivo ADS com exemplos e APIs que podem criar e abrir arquivos ADS.",
  "linktitle" : "ADS",
  "menu" : {
    "docs" : {
      "identifier": "programming-ads",
      "parent" : "programming"
}
},
  "lastmod" : "2022-10-30"
}

## O que é um arquivo ADS?

Um arquivo ADS é um arquivo de especificação para um projeto de programação Ada. É semelhante a uma classe para Java, ou o par de cabeçalho e implementação no caso de C++. As especificações públicas e privadas do pacote Ada são armazenadas no arquivo .ads. O arquivo .adb, em contraste, contém a implementação ou corpos Ada. Assim como [C++](/pt/programming/cpp/), Ada oferece separação entre especificações e implementações independentes da OOP.

Os arquivos ADS podem ser abertos em qualquer editor de texto, como Microsoft Notepad, Notepad++ e Atom.

## Formato de arquivo ADS

Os arquivos ADS estão em formato de arquivo de texto simples e podem ser abertos/editados com qualquer editor de texto. Os pacotes Ada podem ser organizados em hierarquias. Uma unidade filho pode ser declarada da seguinte maneira:

```
-- root-child.ads

package Root.Child is
   --  package spec goes here
end Root.Child;

-- root-child.adb

package body Root.Child is
   --  package body goes here
end Root.Child;

```

## Referências

* [Pacotes Ada](https://learn.adacore.com/courses/Ada_For_The_CPP_Java_Developer/chapters/07_Packages.html)

