{
  "date" : "2019-10-11",
  "keywords" :[ "arsc", ".arsc","o que é um arquivo arsc","como abrir um arquivo arsc", "extensão", "arquivo", "arquivo arsc","formato de arquivo arsc", "extensão de arquivo arsc" ,"exemplo de arquivo arsc"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"ARSC - Arquivo de tabela de recursos do pacote Android",
  "description":"Saiba mais sobre o formato de arquivo ARSC e APIs que podem criar e abrir arquivo ARSC.",
  "linktitle" : "ARSC",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-06-22"
}

## O que é um arquivo ARSC?

Um arquivo ARSC é um arquivo de tabela de recursos do Android que contém a lista de recursos do aplicativo em um formato de tabela. Ele contém informações como nomes de recursos, propriedades e IDs. Os arquivos ARSC fazem parte dos pacotes APK usados para instalar esses aplicativos Android. Todos os recursos como imagens, layouts, estilos e strings, em um aplicativo Android são convertidos em arquivos binários quando o arquivo APK é gerado. O arquivo ARSC também é gerado no mesmo, contendo lista de todos os recursos compilados do programa e seus IDs.

## Formato de arquivo ARSC

Os arquivos de extensão .arsc são arquivos binários gerados após o compilador, como ANT (Eclipse) ou Gradle (AS), compilar o código do aplicativo Android para produzir o arquivo [APK](/pt/compression/apk/). Você pode extrair o arquivo APK usando qualquer utilitário de arquivamento, como o WinZip, para visualizar seu conteúdo, que são os arquivos de classe java compilados, ou seja, classes.dex. Além destes, contém também este arquivo ARSC que contém meta-informações sobre:

* Os nós XML
* Os atributos
* Os IDs de recursos

Os recursos em um arquivo APK são referidos pelos IDs de recursos, enquanto os atributos são resolvidos para um valor em tempo de execução. A ferramenta aapt do Android coleta todos os recursos definidos nos arquivos no momento da compilação e atribui IDs de recursos a eles. Depois que os identificadores são atribuídos aos recursos compilados, um arquivo R.java é gerado a partir do código-fonte, bem como do arquivo resources.arsc.

## Referências

* [Estrutura da tabela de recursos binários](https://stackoverflow.com/questions/27548810/android-compiled-resources-resources-arsc)

