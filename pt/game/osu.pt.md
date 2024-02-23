{
  "date" : "2023-01-18",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Aprenda sobre o formato de arquivo OSU e APIs que podem criar e abrir arquivos OSU.",
  "title" : "Arquivo OSU - Osu! Formato de arquivo de script",
  "linktitle" : "OSU",
  "menu" : {
    "docs" : {
      "identifier":"game-osu-pt",
      "parent" : "game"
}
},
  "lastmod" : "2023-01-18"
}

## O que é um arquivo .OSU?

Um arquivo OSU é um script de jogo escrito para osu! jogo de ritmo. Ele contém informações sobre um beatmap usado no jogo, como o nível de dificuldade, a música a ser tocada e os tempos dos objetos atingidos com os quais o jogador deve sincronizar com a música. Ele permite que jogadores de jogos de ritmo desenvolvam desafios personalizados e compartilhem com a comunidade do jogo.

**Tipo MIME de formato de arquivo OSR:** x-osu-beatmap

## Formato de arquivo OSU

Os arquivos OSU são salvos como arquivos de texto simples em disco e sua estrutura é claramente definida no [OSU file format](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29) do osu!.

### Seções no arquivo OSU

Um arquivo OSU típico possui as seguintes seções.

|Seção |Descrição |Tipo de conteúdo|
---|---|---|
|[Geral]| Informações gerais sobre o beatmap| chave: pares de valores |
|[Editor]| Configurações salvas para o editor de beatmap | chave: pares de valores |
|[Metadados] |Informações usadas para identificar o beatmap| chave: pares de valores |
|[Dificuldade] |Configurações de dificuldade| chave: pares de valores |
|[Eventos]| Eventos gráficos de beatmap e storyboard | Listas separadas por vírgula|
|[Pontos de tempo]| Pontos de tempo e controle | Listas separadas por vírgula|
|[Cores]| Combo e cores de pele| chave: pares de valores |
|[HitObjects]| Acertar objetos | Listas separadas por vírgula|

## Referências

* [OSU! Jogo de ritmo](https://osu.ppy.sh/home)

* [Formato de arquivo OSU](https://osu.ppy.sh/wiki/en/Client/File_formats/Osu_%28file_format%29)


