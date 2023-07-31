{
  "date" : "2021-04-22",
  "keywords": [ "msix file", "extension", "format","how to open msix file","msix file format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"MSIX - O que é um arquivo MSIX?",
  "description":"Saiba mais sobre arquivos MSIX e APIs que podem criar e abrir arquivos MSIX.",
  "linktitle" : "MSIX",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-12-16"
}

## O que é um arquivo MSIX?

Um arquivo MSIX é um formato de empacotamento de aplicativo do Windows usado para criar e distribuir aplicativos no Windows 10. Este é o formato de arquivo de pacote moderno em comparação com o [APPX](/pt/programming/appx/) e o MSI que serão finalmente eliminados para este novo formato de arquivo. Ele pode ser usado para implantação de aplicativos Win32, WPF e Windows Forms. Os arquivos MSIX são confiáveis e visam a otimização de espaço em disco e rede. Os desenvolvedores os usam para distribuir programas aos usuários finais por meio da Microsoft Store (anteriormente conhecida como Windows Store).

## Formato de arquivo MSIX - Mais informações

Os arquivos MSIX são compactados em [ZIP](/pt/compression/zip/), com todos os arquivos incluídos dentro do arquivo empacotado. Além dos arquivos relacionados ao aplicativo, o arquivo MSIX contém arquivos de configuração [.xml](/pt/web/xml/) que contêm informações relacionadas à instalação do aplicativo.

## O que há dentro de um pacote MSIX?

Um pacote MSIX consiste nos seguintes arquivos.

* `AppxBlockMap.xml` - Conhecido como arquivo de mapa de blocos do pacote, é um documento XML que contém uma lista de arquivos do aplicativo com índices e hashes criptográficos para cada bloco de dados armazenado no pacote.
* `AppxManifest.xml` - Um documento XML que contém as informações necessárias para a implantação, exibição e atualização de um aplicativo MSIX. Essas informações incluem identidade do pacote, dependências do pacote, recursos necessários, elementos visuais e pontos de extensibilidade.
* `AppxSignature.p7x` - Um arquivo que é gerado quando o pacote é assinado. Todos os pacotes MSIX precisam ser assinados antes da instalação. Com o AppxBlockmap.xml, a plataforma consegue instalar o pacote e ser validada.

## Referências

* [Visão geral do MSIX](https://learn.microsoft.com/en-us/windows/msix/overview)
* [Crie arquivos APPX usando o Microsoft Visual Studio](https://learn.microsoft.com/en-us/windows/msix/desktop/vs-package-overview)

