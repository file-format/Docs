{
"data": "31/05/2023",
  "keywords": [
"arquivo da área de trabalho",
"o que é um arquivo de desktop",
"o que contém o arquivo da área de trabalho",
"exemplo de arquivo da área de trabalho",
"como abrir arquivo da área de trabalho",
"qual é o formato do arquivo desktop",
"arquivo",
"extensão de arquivo da área de trabalho",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo DESKTOP - Arquivo de entrada da área de trabalho",
  "description":"Aprenda sobre o formato DESKTOP e APIs que podem criar e abrir arquivos DESKTOP.",
"linktitle": "DESKTOP",
  "menu": {
    "docs": {
      "identifier": "settings-desktop",
"parent" : "settings"
}
},
"último mod": "31/05/2023"
}

## O que é um arquivo .DESKTOP?

Um arquivo .desktop é um arquivo de configuração usado por ambientes de desktop Linux para definir atalhos e inicializadores de aplicativos. Ele fornece metadados sobre um aplicativo, como nome, ícone, comando para executar e outras propriedades. Esses arquivos são normalmente usados para criar atalhos em menus de aplicativos, inicializadores de desktop ou painéis em sistemas baseados em Linux.

## O que contém o arquivo DESKTOP?

Um arquivo .desktop segue um formato específico e contém vários campos-chave:

- **[Desktop Entry]:** Este é o cabeçalho da seção principal do arquivo .desktop.
- **Nome:** Especifica o nome do aplicativo.
- **Comentário:** Fornece uma breve descrição ou comentário sobre a aplicação.
- **Exec:** Define o comando a ser executado ao iniciar o aplicativo.
- **Ícone:** Especifica o caminho para o arquivo de ícone associado ao aplicativo.
- **Terminal:** Especifica se o aplicativo deve ser executado em uma janela de terminal.
- **Tipo:** Especifica o tipo de entrada, como "Aplicativo" ou "Link".
- **Categorias:** Especifica categorias ou grupos sob os quais o aplicativo deve ser exibido no menu.
- **StartupNotify:** Especifica se o ambiente de área de trabalho deve mostrar uma notificação de inicialização para o aplicativo.
- **NoDisplay:** Especifica se o aplicativo deve ser ocultado dos menus.
- **Ações:** Define ações adicionais que podem ser executadas no aplicativo, como abrir um arquivo específico.

## Exemplo de arquivo DESKTOP

Aqui está um exemplo de arquivo .desktop para um editor de texto fictício chamado "MyTextEditor":

```
[Desktop Entry]
Name=MyTextEditor
Comment=A simple text editor
Exec=mytexteditor %F
Icon=/path/to/icon.png
Terminal=false
Type=Application
Categories=TextEditor;Utility;
StartupNotify=true
NoDisplay=false
Actions=OpenNewWindow;OpenExistingFile;

[Desktop Action OpenNewWindow]
Name=Open New Window
Exec=mytexteditor

[Desktop Action OpenExistingFile]
Name=Open Existing File
Exec=mytexteditor %U
```

Neste exemplo, o arquivo .desktop define o aplicativo "MyTextEditor" com suas propriedades associadas. Também inclui duas ações adicionais, “Abrir nova janela” e “Abrir arquivo existente”, que podem ser acessadas no menu de contexto do inicializador de aplicativos.

Ao colocar um arquivo .desktop em diretórios específicos como `/usr/share/applications` ou `~/.local/share/applications`, o ambiente de desktop irá reconhecê-lo e exibir o aplicativo adequadamente nos menus ou permitir que ele seja iniciado a partir de Área de Trabalho.

## Como abrir o arquivo DESKTOP?

Vários programas de software podem abrir e manipular arquivos .desktop. Esses programas são normalmente gerenciadores de arquivos ou ambientes de desktop em sistemas baseados em Linux. aqui estão alguns exemplos:

- **Nautilus (Arquivos):** O gerenciador de arquivos padrão para o ambiente de área de trabalho GNOME.
- **Nemo:** O gerenciador de arquivos para o ambiente de desktop Cinnamon.
- **Dolphin:** O gerenciador de arquivos padrão para o ambiente de desktop KDE Plasma.
- **Thunar:** O gerenciador de arquivos padrão para o ambiente de desktop Xfce.
- **Editor de Menu KDE:** Uma ferramenta específica para o ambiente de desktop KDE Plasma que permite visualizar e editar arquivos .desktop.

Esses gerenciadores de arquivos e ambientes de desktop fornecem interface gráfica para gerenciar arquivos .desktop. Eles permitem visualizar e editar propriedades de arquivos .desktop, criar inicializadores de aplicativos e organizar atalhos em menus de aplicativos ou na área de trabalho.

Os arquivos .desktop são arquivos de texto simples, portanto você também pode abri-los e editá-los com um editor de texto de sua preferência. Basta clicar com o botão direito no arquivo .desktop e selecionar “Abrir com” ou “Abrir com outro aplicativo” para escolher um editor de texto na lista de programas instalados.

## Qual é o formato do arquivo DESKTOP?

O formato de arquivo .desktop segue estrutura e formato específicos. É um arquivo de texto simples com um conjunto de pares de valores-chave organizados em seções. Aqui está uma visão geral do formato:

- **Cabeçalhos de seção:** Cada seção começa com um cabeçalho entre colchetes ([]). A seção principal normalmente é chamada [Desktop Entry], que contém os metadados principais do aplicativo ou inicializador.
- **Pares de valores-chave:** Em cada seção, você define propriedades usando pares de valores-chave. O formato é "Chave=Valor". A chave identifica a propriedade e o valor fornece os dados correspondentes.
- **Sintaxe da propriedade:** Os valores das propriedades podem ser de diferentes tipos, incluindo strings, valores booleanos, caminhos de arquivos ou listas. O formato de cada valor de propriedade depende do seu tipo.
- **Comentários:** Você pode incluir comentários no arquivo .desktop usando o símbolo '#'. Qualquer coisa após '#' on-line é considerada um comentário e é ignorada.

## Referências
* [Arquivos de entrada da área de trabalho](https://www.baeldung.com/linux/desktop-entry-files)

