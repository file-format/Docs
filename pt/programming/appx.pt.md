{
  "date" : "2021-04-22",
  "keywords": [ "appx file", "extension", "format","how to open appx file","appx file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"APPX - O que é um arquivo APPX?",
  "description":"Saiba mais sobre o formato de arquivo APPX e APIs que podem criar e abrir arquivos APPX.",
  "linktitle" : "APPX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## O que é um arquivo APPX?

Um arquivo APPX é um formato de arquivo de pacote distribuível usado para distribuição e instalação de um aplicativo. Foi introduzido com o Windows 8 para ser publicado na Microsoft Windows Store. Ele contém todos os arquivos necessários para instalar um aplicativo do Windows. Isso inclui metadados, arquivos e informações de credenciais. Um formato de arquivo de empacotamento mais moderno é o MSIX, que atualmente é mais usado em comparação ao APPX.

## Formato de arquivo APPX - Mais informações

Os arquivos APPX são salvos como arquivos compactados no formato de arquivo [ZIP](/pt/compression/zip/). Isso torna o pacote inteiro como um arquivo morto com tamanho de arquivo reduzido que é fácil de ser carregado na Microsoft Store.

## Como visualizar arquivos em um arquivo APPX?

Para visualizar o conteúdo ou arquivos dentro de um arquivo APPX, as etapas a seguir devem ser seguidas.

1. Como os arquivos APPX são armazenados como arquivos ZIP compactados, renomeie o arquivo para a extensão .zip
1. Use qualquer ferramenta de descompactação como 7-Zip, WinZip ou WinRAR para extrair os arquivos contidos no arquivo APPX

## Como criar um arquivo APPX?

Existem dois métodos que podem ser usados para criar arquivos APPX.

1. Usando MakeApp.exe - [MakeApp.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool) é usado para criar ambos pacotes de aplicativos (.msix ou .appx) e arquivos de pacote de aplicativos .msixbundle ou .appxbundle). Além disso, ele pode extrair arquivos de um pacote de aplicativos. MakeApp.exe está disponível com o SDK do Windows 10 e pode ser usado no prompt de comando.
1. Usando o Microsoft Visual Studio - Os desenvolvedores geralmente [criam arquivos APPX](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview) usando o Microsoft Visual Studio. Quando o desenvolvimento do aplicativo estiver concluído e o aplicativo estiver pronto para ser publicado, o arquivo de pacote APPX pode ser criado publicando-o no Visual Studio.

## Referências

* [Crie um pacote ou pacote MSIX com MakeAppx.exe](https://learn.microsoft.com/en-us/windows/msix/package/create-app-package-with-makeappx-tool)
* [Crie arquivos APPX usando o Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

