{
  "date" : "2021-04-21",
  "keywords": [ "what is a HS file", "tutorials on HS","HS means","HS", "HS files", "extension", "format", "HS tutorial", ".hs", "HS example","hs file extension" ,"how to open a hs file"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"HS - Formato de arquivo de script Haskell",
  "description":"Saiba mais sobre o que é um formato de arquivo HS e APIs que podem criar e abrir arquivos HS.",
  "linktitle" : "HS",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-15"
}

# HS - Formato de arquivo Java HelpSet

## O que é um arquivo Java HS?

Um arquivo com extensão .hs na linguagem de programação Java é um arquivo de documentação de ajuda usado pelo sistema JavaHelp quando ativado por um aplicativo. Ele define o helpset para o aplicativo específico instalado e compreende vários subconjuntos como parte da ajuda do sistema para o aplicativo. O programa Java deve ser capaz de localizar o arquivo helpset cujo nome termina com a extensão .hs.

## Informações do Conjunto de Ajuda Java

Um arquivo .hs pode conter as seguintes informações.

|Informações|Descrição|
---|---|
|Arquivo de Mapa|O arquivo de mapa é empregado para associar IDs de tópicos com o localizador de recursos uniforme ou nome de caminho de arquivos de tópicos de linguagem de marcação de hipertexto.|
|Visualizar Informações|Informações que descrevem os navegadores que estão sendo empregados no helpset. os navegadores de qualidade são: índice, índice e pesquisa de texto completo. outros navegadores incluem o gloss e também os navegadores favoritos. os dados relativos aos navegadores personalizados estão incluídos aqui.|
<html>|Título do conjunto de ajuda|O \<title> é descrito no arquivo helpset (.hs). Este título parece ser o mais alto da janela e de todas as janelas secundárias descritas em seu arquivo de ajuda.| </html>
|ID inicial|O título do ID (padrão) exibido quando o observador de assistência é chamado sem indicar um ID.|
|Apresentação|As janelas para mostrar os assuntos de assistência. Esta pode ser uma inclusão moderna do programa de computador JavaHelp 2 que é retratado com mais detalhes abaixo de \<presentation> .|
|Sub-helpsets|Esta área discricionária incorpora estaticamente outros helpsets utilizando a tag. Os helpsets mostrados por esta tag são combinados naturalmente no helpset que contém a tag. Mais pontos de interesse sobre blending podem ser encontrados em Blending Helpsets.|
|Implementação|Este segmento discricionário faz um registro que fornece mapeamento de informações chave para caracterizar a classe HelpBroker a ser utilizada dentro do método HelpSet.createHelpBroker. O registro também determina o visualizador de conteúdo para o cliente para uma determinada classificação Emular.|

## Formato de arquivo Java HS

Os arquivos Java HS estão no formato de arquivo XML e são baseados na recomendação proposta da linguagem de marcação estendida do World Wide Web Consortium (W3C) [PR-xml-971208](http://www.w3.org/TR/PR-xml- 971208). Isso significa que um arquivo Java HS está no formato de arquivo XML legível por humanos que pode ser aberto em qualquer aplicativo leitor de XML.

### Exemplo de formato de arquivo Java HS

Veja a seguir um exemplo de arquivo de helpset a partir da [documentação do Oracle Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html).

```html
<?xml version='1.0' encoding='ISO-8859-1' ?>
<!DOCTYPE helpset
  PUBLIC "-//Sun Microsystems Inc.//DTD JavaHelp HelpSet Version 2.0//EN"
         "http://java.sun.com/products/javahelp/helpset_2_0.dtd">
<helpset version="2.0">
   <!-- title -->
   <title>Java Development Environment - Help</title>

   <!-- maps -->
   <maps>
     <homeID>top </homeID>
     <mapref location="Map.jhm" />
   </maps>

   <!-- views -->
   <view xml:lang="en" mergetype="javax.help.UniteAppendMerge">
      <name>TOC</name>
      <label>Table Of Contents</label>
      <type>javax.help.TOCView</type>
      <data>IdeHelpTOC.xml</data>
   </view>

   <view xml:lang="en" mergetype="javax.help.SortMerge">
      <name>Index</name>
      <label>Index</label>
      <type>javax.help.IndexView</type>
      <data>IdeHelpIndex.xml</data>
   </view>

   <view xml:lang="en">
      <name>Search</name>
      <label>Search</label>
      <type>javax.help.SearchView</type>
         <data engine="com.sun.java.help.search.DefaultSearchEngine">
         JavaHelpSearch
         </data>
   </view>

   <!-- A glossary navigator -->
   <view  mergetype="javax.help.SortMerge">
      <name>glossary</name>
      <label>Glossary</label>
      <type>javax.help.GlossaryView</type>
      <data>glossary.xml</data>
   </view>

   <!-- A favorites navigator -->
   <view>
      <name>favorites</name>
      <label>Favorites</label>
      <type>javax.help.FavoritesView</type>
   </view>

   <!-- presentation windows -->

   <!-- This window is the default one for the helpset.
     *  Its title bar says "Project X Help". It
     *  is a tri-paned window because displayviews, not
     *  defined, defaults to true and because a toolbar is defined.
     *  The toolbar has a back arrow, a forward arrow, and
     *  a home button that has a user-defined image.
   -->
   <presentation default=true>
       <name>main window</name>
       <size width="400" height="400" />
       <location x="200" y="200" />
       <title>Project X Help</title>
       <toolbar>
           <helpaction>javax.help.BackAction</helpaction>
           <helpaction>javax.help.ForwardAction</helpaction>
           <helpaction image="homeicon">javax.help.HomeAction</helpaction>
       </toolbar>
   </presentation>

   <!-- This window is simpler than the main window.
     *  It's intended to be used a secondary window.
     *  It has no navigation pane or toolbar.
   -->
   <presentation displayviews=false>
       <name>secondary window</name>
       <size width="200" height="200" />
       <location x="200" y="200" />
   </presentation>

   <!-- subhelpsets -->
   <subhelpset location="file:/c:/Foobar/HelpSet2.hs" />

   <!-- implementation section -->
   <impl>
      <helpsetregistry helpbrokerclass="javax.help.DefaultHelpBroker" />
      <viewerregistry viewertype="text/html"
         viewerclass="com.sun.java.help.impl.CustomKit />
      <viewerregistry viewertype="text/xml"
         viewerclass="com.sun.java.help.impl.CustomXMLKit />
   </impl>
</helpset>
```

## Referências
* [Arquivo Oracle Java Helpset](https://docs.oracle.com/cd/E19253-01/819-0913/author/helpset.html)

# HS - Formato de arquivo de script Haskell

## O que é um arquivo HS?

Um arquivo com extensão .hs é um arquivo Haskell Script escrito em [Haskell](https://wiki.haskell.org/Haskell), uma linguagem de programação avançada de código aberto puramente funcional. Código escrito em arquivo HS é puramente baseado em funções, ao contrário de [C](/pt/programming/c/), [C++](/pt/programming/cpp/) e similares, que seguem os princípios de desenvolvimento rápido de software robusto e conciso. Haskell fornece simultaneidade e paralelismo integrados, juntamente com APIs ricas, criadores de perfil e depuradores para produzir aplicativos flexíveis e de alta qualidade.

## Formato de arquivo HS

Como qualquer linguagem de programação, os arquivos HS são escritos em formato de texto simples que pode ser lido por humanos. Estes podem ser criados, editados e visualizados com qualquer ferramenta de texto disponível. O arquivo de código fonte .hs é compilado com um compilador Haskell, gerando o arquivo binário executável.

### Exemplo de formato de arquivo HS

O código pode ser escrito em um arquivo .hs e compilado usando um compilador Haskell como [GHC](https://haskell.org/ghc). A linha de código a seguir é salva como `HelloWorld.hs` conforme mostrado no exemplo a seguir.

```
main = putStrLn "Hello, World!"
```

Isso é compilado usando o comando:

```
$ ghc -o hello hello.hs
```
e o arquivo executável resultante pode ser executado como:

```
$ ./hello
```
Isso imprime a mensagem "Hello, World!" declaração para a saída.

## Referências

* [Haskell](https://wiki.haskell.org/Haskell)
* [Haskell em 5 etapas fáceis](https://wiki.haskell.org/Haskell_in_5_steps)

