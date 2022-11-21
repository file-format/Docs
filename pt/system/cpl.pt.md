{
  "date" : "2021-06-29",
  "keywords" :[ "CPL", "extensão", "arquivo", "formato", "sistema", "Arquivo do Painel de Controle", "Windows", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"CPL - Arquivo do Painel de Controle",
  "description":"Saiba mais sobre o formato de arquivo CPL e APIs que podem criar e abrir arquivos CPL.",
  "linktitle" : "CPL",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-06-29"
}

## O que é um arquivo CPL? ##

Um arquivo CPL é um tipo de arquivo "sistema". É usado pelo sistema operacional Windows. Um arquivo CPL é a abreviação de arquivo do painel de controle. Esses arquivos são arquivos binários que se abrem com o painel de controle em um sistema operacional Microsoft Windows e são usados para representar e abrir as ferramentas disponíveis no painel de controle, como Mouse, Displays, Networking, entre outras. Os arquivos CPL normalmente são armazenados na pasta do sistema em seu dispositivo. Esses arquivos não devem ser abertos manualmente.


## Formato de arquivo CPL ##

Diferentes arquivos CPL em seu sistema operacional Windows estão conectados para representar diferentes itens do painel de controle. Todos os itens do painel de controle estão vinculados a um arquivo CPL e têm o sufixo “.cpl” anexado aos seus itens.

Alguns tipos comuns de arquivos CPL com seus formatos são:

* Inetcpl.cpl – Para propriedades da Internet no seu dispositivo
* Appwiz.cpl – Para adicionar ou remover propriedades de programas no seu dispositivo
* Desk.cpl – Para as propriedades de exibição
* Main.cpl – Para propriedades relacionadas a Mouse, Fontes, Teclado e Impressoras.
* Netcpl.cpl – Para propriedades relacionadas à rede
* System.cpl – Para propriedades relacionadas ao sistema e para adicionar novo assistente de hardware
* TimeDate.cpl – Para propriedades de data ou hora
* Mlcfg32.cpl – Para propriedades do Microsoft Exchange ou Windows Messaging
* Intl.cpl – Isso se refere às propriedades de configurações regionais
* Modem.cpl – Para propriedades relacionadas ao modem
* Themes.cpl – Armazena temas e propriedades da área de trabalho.
* Password.cpl – Para propriedades de senha
* Mmsys.cpl – Para propriedades multimídia
* Wgpocpl.cpl – Pertence ao Microsoft Mail Post Office

## Breve história ##

O tipo de arquivo CPL foi desenvolvido pelo Microsoft Windows e é parte integrante do sistema operacional Windows desde o Windows 1.0. Ele ainda é usado em todas as versões do Windows e todas as propriedades do item do painel de controle são armazenadas usando esse tipo de arquivo.

## Exemplo de CPL ##

Um exemplo de arquivo CPL pode ser visto abaixo:

```
<!-- Copyright (c) Microsoft Corporation -->
<assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0">
<assemblyIdentity name="Microsoft.Windows.Net.ncpa" processorArchitecture="x86" version="5.1.0.0" type="win32"/>
<description>NCPA CPL</description>
<dependency>
    <dependentAssembly>
        <assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="x86" 
            publicKeyToken="6595b64144ccf1df"
            language="*"
        />
    </dependentAssembly>
</dependency>
<trustInfo xmlns="urn:schemas-microsoft-com:asm.v3">
    <security>
        <requestedPrivileges>
            <requestedExecutionLevel level="asInvoker" uiAccess="false"/>
        </requestedPrivileges>
    </security>
</trustInfo>
</assembly>

```
