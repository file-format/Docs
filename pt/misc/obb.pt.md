{
  "date" : "2022-02-16",
  "keywords" :[ "arquivo obb", "formato de arquivo obb", "o que é um arquivo obb", "arquivo", "exemplo obb", "extensão de arquivo obb","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo OBB - arquivo de blob binário opaco do Android",
  "description":"Saiba mais sobre o formato de arquivo OBB e APIs que podem criar e abrir arquivos OBB.",
  "linktitle" : "OBB",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-16"
}

## O que é um arquivo OBB?

Um arquivo OBB é um arquivo de expansão que contém dados adicionais que estão além do arquivo Android [APK](/pt/compression/apk/). A Google Play Store não permite ter um arquivo APK Android com tamanho superior a 100 MB. Mas alguns aplicativos podem exigir que gráficos de alta definição, arquivos de mídia ou outros ativos grandes sejam hospedados além dos arquivos APK. É aí que entram os tipos de arquivo OBB. O Google Play permite anexar esses arquivos de expansão como um complemento ao arquivo APK.

## Formato de arquivo OBB

Os arquivos OBB são salvos como arquivos binários junto com os arquivos APK. Quando um APK acompanha os arquivos OBB, o Google Play hospeda os arquivos de expansão em seu servidor e nenhum custo adicional é cobrado do desenvolvedor. Esses arquivos adicionais são armazenados no armazenamento compartilhado do dispositivo no cartão SD ou partição montável em USB quando o aplicativo é baixado para instalação.

Os arquivos OBB são baixados e instalados após o download. Mas, em alguns casos, eles são baixados para instalação quando o aplicativo é executado pela primeira vez.

### Tamanho máximo do arquivo OBB

A Google Play Store permite que você carregue arquivos de expansão OBB de tamanho de até 2 GB. Arquivos de tamanho grande são recomendados para serem carregados como arquivos compactados [ZIP](/pt/compression/zip/) para um upload eficiente via internet.

Esses arquivos de expansão podem ser hospedados como arquivo de expansão principal **principal** para recursos adicionais exigidos pelo aplicativo ou como um arquivo de expansão de patch opcional destinado a pequenas atualizações no arquivo de expansão principal.

## Referências

* [Desenvolvedores Android - Arquivos de expansão](https://developer.android.com/google/play/expansion-files)

