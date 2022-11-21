{
  "date" : "2019-10-11",
  "keywords" :[ "vcxproj", "arquivo", "extensão", "formato de arquivo", "Projeto Visual C++", "Guia de Programação" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VCXPROJ",
  "description":"Saiba mais sobre o formato de arquivo VCXPROJ e APIs que podem criar e abrir arquivos VCXPROJ.",
  "linktitle" : "VCXPROJ",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2020-09-10"
}

## O que é um arquivo VCXPROJ?

Um arquivo com extensão .vcxproj é um arquivo de projeto do Microsoft Visual C++ que armazena as informações do projeto [C++](/pt/programming/cpp/). Ele contém informações que são usadas pelo sistema de projeto MSBuild para compilar e compilar a saída final. VCXPROJ de projetos Visual C++ é o mesmo de [CSPROJ](/pt/programming/csproj/) para projetos .NET. Os arquivos VCXPROJ não contêm nenhum código, mas se referem a todas as classes, destinos e propriedades definidas para o projeto para construir o projeto. Eles podem ser abertos em editores de texto simples ou preferencialmente no Microsoft Visual Studio IDE.


## Formato de arquivo VCXPROJ - Mais informações

Os arquivos VCXPROJ são arquivos de texto criados no formato de arquivo [XML](/pt/web/xml/). Eles podem ser abertos em qualquer editor de texto, mas é altamente recomendável usar o Microsoft Visual Studio IDE para abrir e editar esses arquivos. Estes não foram projetados para edição manual. Erros podem fazer com que o IDE falhe ou se comporte de maneiras inesperadas.

O conteúdo de um arquivo VCXPROJ de amostra é o seguinte.

```
<Project DefaultTargets="Build" ToolsVersion="4.0" xmlns='http://schemas.microsoft.com/developer/msbuild/2003'>
  <ItemGroup Label="ProjectConfigurations" />
  <PropertyGroup Label="Globals" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.default.props" />
  <PropertyGroup Label="Configuration" />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.props" />
  <ImportGroup Label="ExtensionSettings" />
  <ImportGroup Label="PropertySheets" />
  <PropertyGroup Label="UserMacros" />
  <PropertyGroup />
  <ItemDefinitionGroup />
  <ItemGroup />
  <Import Project="$(VCTargetsPath)\Microsoft.Cpp.targets" />
  <ImportGroup Label="ExtensionTargets" />
</Project>
```
### Elementos do arquivo VCXPROJ

Um arquivo VCXPROJ típico contém vários elementos como pode ser visto no exemplo XML acima. A [estrutura VCXPROJ](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160) da Microsoft explica cada elemento de arquivo em detalhes e pode ser consultado do ponto de vista do desenvolvedor.

#### Elemento do projeto

Este é o nó raiz do arquivo VCXPROJ. O MSBuild usa esse elemento para ler a versão de compilação e o destino padrão para compilação.

#### Elemento ItemGroup de Configurações do Projeto

Ele contém as informações de configuração do projeto que podem incluir o método de compilação (Debug ou Release), compilação de 32 ou 64 bits, opções de otimização e outros. As informações neste grupo são usadas pelo IDE para carregar o projeto.

#### Elementos de configuração do projeto

Os elementos ProjectConfiguration em um arquivo VCXPROJ contêm informações sobre a compilação e a plataforma para a qual o projeto é carregado. Seu nome deve seguir o formato `$(Configuration)|$(Platform)`.

#### Elemento de grupo de propriedades globais

Esta seção contém configurações que fornecem informações para o nível do projeto, como:

* Guia do Projeto
* RootNamespace
* ApplicationType ou ApplicationTypeRevision


## Referências

* [Estrutura VCXPROJ - MSDN](https://docs.microsoft.com/en-us/cpp/build/reference/vcxproj-file-structure?view=msvc-160)
* [Arquivos de projeto C++](https://docs.microsoft.com/en-us/cpp/build/reference/project-files?view=msvc-160)

