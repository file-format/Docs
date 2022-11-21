{
  "date" : "2021-06-29",
  "keywords" :[ "DLL", "extensão", "arquivo", "formato", "sistema", "Biblioteca de vínculo dinâmico", "configurações", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DLL - Biblioteca de links dinâmicos",
  "description":"Saiba mais sobre o formato de arquivo DLL e APIs que podem criar e abrir arquivos DLL.",
  "linktitle" : "DLL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo DLL? ##

Um arquivo DLL ou Dynamic Link Library é um tipo de arquivo executável. É um dos arquivos de extensão mais comumente encontrados em seu dispositivo e geralmente é armazenado na pasta System32 em seu Windows. O arquivo de extensão DLL foi desenvolvido pela Microsoft e é popularmente usado por eles. Tem uma classificação de usuário de alta popularidade. A DLL funciona como uma prateleira que contém os *drivers/procedures/functions/properties* que são projetados e aplicados para um programa/aplicativo pelo servidor Windows. Um único arquivo DLL também pode ser compartilhado entre vários programas do Windows. Esses arquivos de extensão são vitais para o bom funcionamento dos programas do Windows em seu dispositivo, pois são responsáveis por habilitar e executar várias funções no programa, como gravar e ler arquivos, conectar-se a outros dispositivos externos à sua configuração.
Esses arquivos, no entanto, só podem ser abertos em um dispositivo que suporte qualquer versão do Windows (windows 7/windows 10/etc.) e, portanto, não podem ser abertos diretamente em um dispositivo que suporte o Mac OS. (Se você deseja abrir um arquivo DLL no Mac OS, vários aplicativos externos podem ajudar a abri-los.)


## Formato de arquivo DLL ##

O arquivo DLL foi desenvolvido pela Microsoft e possui a extensão ".dll" que representa o tipo. Ele tem sido parte integrante do servidor Windows 1.0 e além. É um tipo de arquivo binário e suportado por todas as versões do Microsoft Windows. Este tipo de arquivo foi criado como meio de criar um sistema de biblioteca compartilhada dentro dos programas do Windows, para permitir edições ou alterações separadas e independentes nas bibliotecas do programa sem a necessidade de revincular os programas.


## Exemplo de DLL ##

O código de exemplo para um ponto de entrada de DLL pode ser encontrado abaixo:

```
BOOL APIENTRY DllMain(
HANDLE hModule,// Handle to DLL module
DWORD ul_reason_for_call,// Reason for calling function
LPVOID lpReserved ) // Reserved
{
    switch ( ul_reason_for_call )
    {
        case DLL_PROCESS_ATTACHED: // A process is loading the DLL.
        break;
        case DLL_THREAD_ATTACHED: // A process is creating a new thread.
        break;
        case DLL_THREAD_DETACH: // A thread exits normally.
        break;
        case DLL_PROCESS_DETACH: // A process unloads the DLL.
        break;
}
    return TRUE;
}

```

## Referência ##

* [DLL - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/deployment/dynamic-link-library)
