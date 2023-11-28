{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo ADMX - Formato de arquivo de modelo administrativo de política de grupo",
  "description":"Aprenda sobre o formato de arquivo ADMX e como abrir arquivos ADMX.",
  "linktitle" : "ADMX",
  "menu" : {
    "docs" : {
      "identifier" : "system-admx",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## O que é um arquivo .ADMX?

Um arquivo ADMX é um arquivo de configuração de política usado pelo software de Política de Grupo do Microsoft Windows que gerencia grupos de computadores em um grupo. É um arquivo de modelo administrativo baseado em XML e foi introduzido com o Windows Vista Service Pack 1. Os arquivos ADMX contêm definições de configuração para contas de usuário, configurações de sistema operacional e aplicativos. Os arquivos ADMX são usados para armazenar e implantar as configurações para o gerenciamento centralizado de muitos sistemas de computador.

Você pode criar ou editar arquivos ADMX usando qualquer editor de texto compatível com XML ou Editor de Objeto de Política de Grupo da Microsoft.

## Formato de arquivo ADMX - Mais informações

Os arquivos ADMX são armazenados no formato de arquivo universal [XML](/pt/web/xml/) que é legível por humanos. É um formato de arquivo multilíngue e permite que administradores de sistema de diferentes idiomas trabalhem com os mesmos arquivos ADMX. Os arquivos ADMX substituíram o antigo formato de arquivo [ADM](/pt/system/adm/), que é um formato de arquivo de texto formatado em Unicode. Os arquivos ADMX especificam as chaves do Registro que são alteradas quando uma determinada configuração de Política de Grupo é alterada.

### O que posso fazer com o arquivo ADMX?

Os arquivos ADMX definem quais ações devem ser permitidas aos computadores dos usuários que fazem parte de um grupo. A política de grupo impõe as regras definidas em combinação com o software Active Directory. Os arquivos ADMX são gerenciados no armazenamento central no sistema operacional Windows, que é um local central no domínio.

Um arquivo ADMX implantado em um ambiente de trabalho pode permitir que os administradores implementem políticas como:

*Controle o uso da internet
* Download de certos tipos de arquivos
* Uso de dispositivos removíveis nos sistemas

## Referências

* [Arquivos de modelo administrativo - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gerenciando arquivos de modelos administrativos](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

