{
  "date" : "2023-02-14",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo ADM - Formato de arquivo de modelo administrativo",
  "description":"Aprenda sobre o formato de arquivo ADM e como abrir arquivos ADM.",
  "linktitle" : "ADM",
  "menu" : {
    "docs" : {
      "identifier" : "system-adm",
      "parent" : "system"
}
},
  "lastmod" : "2023-02-14"
}

## O que é um arquivo .ADM?

Um arquivo ADM é um arquivo de modelo usado pelo software de Políticas de Grupo da Microsoft para especificar o local das configurações de política baseadas em registro no arquivo de registro. É usado pelos administradores do sistema para definir a política de gerenciamento de um grupo de computadores que fazem parte do grupo. Essas informações passam a fazer parte dos Objetos de Política de Grupo (GPOs) criados para gerenciamento do grupo.

Você pode abrir arquivos ADM usando o Editor de objetos de política de grupo da Microsoft.

## Formato de arquivo ADM – Mais informações

Os arquivos ADM são armazenados como arquivos de texto formatados em Unicode. Eles foram usados principalmente para descrever a localização das configurações de política baseadas no registro no registro do Windows Vista e do Windows 7.

Os arquivos ADM não são mais suportados e foram substituídos pelos arquivos [ADMX](/pt/system/admx/). O GPA ignora os seguintes arquivos ADM padrão em computadores que executam o Microsoft Windows Vista Service Pack 1 ou posterior.

* sistema.adm
* inetres.adm
*conf.adm
* wmplayer.adm
* wuau.adm

## Referências

* [Arquivos de modelo administrativo - ADMX](https://learn.microsoft.com/en-us/mem/intune/configuration/administrative-templates-windows)
* [NetIQ - Gerenciando arquivos de modelos administrativos](https://www.netiq.com/documentation/group-policy-administrator-69/grouppolicyadministratoruserguide/data/administrativetemplatefiles.html)
* [SSDT](https://wiki.osdev.org/SSDT)

