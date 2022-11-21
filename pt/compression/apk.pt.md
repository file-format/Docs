{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo apk", "formato de arquivo apk", "o que é um arquivo apk", "arquivo", "exemplo apk", "extensão de arquivo apk", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APK - O que é um arquivo APK?",
  "description":"Saiba saber o que é um arquivo APK e APIs que podem criar e abrir arquivos APK.",
  "linktitle" : "APK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-27"
}

## O que é um arquivo APK?

Um arquivo com extensão .apk é um arquivo de aplicativo do Google Android usado para instalar aplicativos (aplicativos) nos dispositivos Android. Ele é criado como um arquivo executável usando o IDE oficial Google Android Studio e é carregado na Google Play Store para ser baixado e instalado pelos usuários finais. Os arquivos APK podem ser gerados e disponibilizados para instalação manual também antes da publicação na Google Play Store. Isso ajuda a testar a funcionalidade e o comportamento do arquivo de pacote APK gerado. Portanto, é preciso ter certeza de que o arquivo APK é de uma fonte confiável e não contém nenhum malware.

## Formato de arquivo APK

Os arquivos APK são compactados no formato de arquivo [ZIP](/pt/compression/zip/) que pode ser aberto com qualquer software de abertura de arquivo ZIP. A extensão .apk desse arquivo pode ser renomeada para .zip e abrir o arquivo em qualquer aplicativo ZIP ou extrair seu conteúdo.

## Conteúdo do pacote APK

Um único arquivo APK contém todos os arquivos necessários para sua instalação e execução. Um arquivo APK, quando extraído com um aplicativo ZIP, contém os seguintes arquivos e pastas.

* `META-INF/`: Diretório que contém o arquivo de manifesto, assinatura e uma lista de recursos no arquivo
* `lib/`: Diretório contendo código compilado relacionado a plataformas específicas como armeabi-v7a, x86, arm64-v8a, etc.
* `res/`: Diretório contendo recursos não compilados, como imagens
* `assets/`: Diretório contendo ativos de aplicativos, que podem ser recuperados pelo AssetManager.
* `androidManifest.xml`: Contém o nome, informações de versão e conteúdo do arquivo APK
* `classes.dex`: São classes Java compiladas que podem ser executadas na máquina virtual Dalvik e pelo Android Runtime
* `resources.arsc`: arquivo de recursos compilado, como strings

## Como instalar o arquivo APK no dispositivo Android?

Para instalar um arquivo APK em seus dispositivos Android, as etapas a seguir podem ser usadas.

1. Baixe o APK usando o navegador da web
2. Toque nele - você poderá vê-lo baixando na barra superior do seu dispositivo
3. Depois de baixado, abra Downloads, toque no arquivo APK e toque em Sim quando solicitado.

Seguindo estas etapas, iniciará a instalação do aplicativo no seu dispositivo.

## Referências

* [Formato de arquivo APK](https://en.wikipedia.org/wiki/Android_application_package)

