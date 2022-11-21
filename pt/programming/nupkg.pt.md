{
  "date" : "2022-03-09",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo NUPKG - Arquivo de pacote NuGet",
  "description":"Saiba mais sobre o formato de arquivo NUPKG e APIs que podem criar e abrir arquivos NUPKG.",
  "linktitle" : "NUPKG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-09"
}

## O que é um arquivo NUPKG?

Um arquivo NUPKG é um arquivo de pacote que contém o código-fonte a ser usado pelo software NuGet para criar pacotes a serem usados em projetos .NET. O componente NuGet Package Manager é instalado como parte do Microsoft Visual Studio para buscar pacotes do repositório de hospedagem de pacotes online. Os arquivos NUPKG ajudam os desenvolvedores a buscar os pacotes mais recentes do [Nuget.org](https://nuget.org) usando o NuGet Package Manager em vez de baixar e instalar manualmente os pacotes de desenvolvimento. Os arquivos NUPKG são construídos a partir de arquivos NUSPEC e, quando obtidos, instalam o pacote no sistema do usuário.

## Formato de arquivo NUPKG

Os arquivos NUPKG são arquivos [ZIP](/pt/compression/zip/) que contêm as bibliotecas empacotadas dentro dele. Quando baixado, ele pode ser renomeado para .zip e extraído com qualquer utilitário zip padrão, como WinZIP, 7-Zip e Apple Archive Utility.

## Referência

* [Nuget.org](https://nuget.org)
* [Início rápido: instalar e usar um pacote no Visual Studio (somente Windows)](https://docs.microsoft.com/en-us/nuget/quickstart/install-and-use-a-package-in-visual- estúdio)
* [Como criar e publicar um pacote Nuget](https://docs.microsoft.com/en-us/nuget/quickstart/create-and-publish-a-package-using-visual-studio?tabs=netcore- CLI)

