{
"data": "02/02/2023",
  "keywords": [
"arquivo do aplicativo",
"o que é um arquivo de aplicativo",
"arquivo",
"como abrir arquivo de aplicativo",
"extensão de arquivo de aplicativo",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
  "description":"Aprenda sobre o formato de arquivo APP e APIs que podem criar e abrir arquivos APP.",
"title": "Formato de arquivo APP - pacote de aplicativos macOS",
"linktitle": "APLICATIVO",
  "menu": {
    "docs": {
      "identifier": "executable-app",
"parent": "executável"
}
},
"último mod": "02/02/2023"
}

## O que é um arquivo .APP?

Um arquivo .app no macOS é um tipo especial de diretório que contém todos os arquivos necessários para executar um aplicativo específico, incluindo código executável, recursos e metadados. A extensão .app sinaliza ao sistema operacional que esse diretório deve ser tratado como uma unidade única, em vez de uma coleção de arquivos separados, e que pode ser iniciado diretamente do Finder ou do Dock.

Finder é o aplicativo gerenciador de arquivos padrão no macOS. Ele permite que você navegue e organize os arquivos e diretórios do seu computador. O Dock é um recurso do macOS que fornece acesso rápido a aplicativos e documentos usados com frequência. Tanto o Finder quanto o Dock permitem que você inicie aplicativos clicando em seus arquivos .app, que abrirão o pacote de aplicativos correspondente. Quando você inicia um aplicativo, o código executável do pacote .app é executado, disponibilizando o aplicativo para uso. O arquivo .app é a representação do aplicativo no sistema de arquivos e fornece uma maneira para o usuário acessar e iniciar o aplicativo.

Ao clicar com o botão direito em um arquivo .app no Finder em um sistema macOS e selecionar "Mostrar conteúdo do pacote", você poderá ver a estrutura interna do pacote de aplicativos. Isso é útil se você quiser acessar recursos ou arquivos usados pelo aplicativo ou se quiser inspecionar o conteúdo do aplicativo para fins de solução de problemas. O conteúdo do pacote de um arquivo .app normalmente inclui diretórios para recursos como imagens e sons, bem como o código executável do aplicativo. Ao explorar o conteúdo de um arquivo .app, você pode obter insights mais profundos sobre como o aplicativo é montado e o que ele faz.

## Como abrir o arquivo APP?

Para abrir um arquivo .app no macOS, basta clicar duas vezes no arquivo no Finder. Isso iniciará o aplicativo contido no pacote .app. Se o aplicativo estiver instalado em seu sistema e tiver sido associado ao tipo de arquivo .app, clicar duas vezes no arquivo deverá iniciar o aplicativo automaticamente. Se o aplicativo não estiver associado ao tipo de arquivo .app, pode ser necessário clicar com o botão direito do mouse no arquivo e selecionar "Abrir com" para escolher um aplicativo apropriado para abri-lo.

Você pode abrir um arquivo .app no Terminal do macOS usando o comando “open”. Para fazer isso, navegue até o diretório onde o arquivo .app está localizado usando o comando “cd” e execute o seguinte comando:

```
open <AppName>.app 
```

onde<AppName> é o nome do aplicativo que você deseja iniciar. Isso iniciará o aplicativo como se você tivesse clicado duas vezes nele no Finder. O comando “open” é um utilitário de uso geral que pode ser usado para abrir muitos tipos diferentes de arquivos, incluindo aplicativos, documentos e diretórios. Quando você usa o comando “open” em um arquivo .app, ele inicia o aplicativo contido no pacote.

## Referências
* [Bundle (macOS)](https://en.wikipedia.org/wiki/Bundle_(macOS))
