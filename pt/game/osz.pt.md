{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo OSZ e APIs que podem criar e abrir arquivos OSZ.",
  "title" : "Arquivo OSZ - osu! Formato de arquivo Beatmap",
  "linktitle" : "OSZ",
  "menu" : {
    "docs" : {
      "identifier":"game-osz-pt",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## O que é um arquivo .OSZ?

Um arquivo OSZ é um formato de arquivo compactado usado pelo jogo de ritmo osu! para armazenar dados de beatmap. Beatmaps são essencialmente níveis do jogo e incluem informações como a música, o tempo da batida e a localização dos objetos atingidos na tela do jogo. Os arquivos OSZ permitem fácil distribuição de beatmaps e normalmente são baixados da Internet e importados para o jogo. OSU! também tem o formato de arquivo [OSR](/game/osr/) que é um arquivo de repetição de jogo e pode ser reproduzido por jogadores.

**Tipo MIME de formato de arquivo OSR:** x-osu-replay

## Formato de arquivo OSZ

Os detalhes internos do formato de arquivo dos tipos de arquivo OSZ não estão disponíveis publicamente. Ele contém dados compactados em [ZIP](/compression/zip/) que contêm informações para tocar a música, mostrar gráficos e exibir aos jogadores sobre os eventos quando eles devem interagir com o jogo.

## Como criar um arquivo OSZ?

OSU! tem instruções detalhadas para arquivos [creating OSZ](https://osu.ppy.sh/wiki/en/Client/File_formats#creating-.osz-and-.osk-files) e OSK. As etapas a seguir podem ser usadas para criar um arquivo OSZ usando OSU!.

1. Abra um beatmap através do editor.
1. No menu superior, selecione Arquivo > Exportar pacote....
1. O arquivo .osz será colocado na pasta Exports dentro do osu! pasta.

## Referências

* [OSU! Jogo de ritmo](https://osu.ppy.sh/home)


