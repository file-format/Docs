{
  "date" : "2021-09-08",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo OSR e APIs que podem criar e abrir arquivos OSR.",
  "title" : "Arquivo OSR - osu! Formato de arquivo de repetição",
  "linktitle" : "OSR",
  "menu" : {
    "docs" : {
      "identifier":"game-osr-pt",
      "parent" : "game"
}
},
  "lastmod" : "2021-09-08"
}

## O que é um arquivo .OSR?

An OSR file is a game replay file created by the [osu! game](https://osu.ppy.sh/home). Osu! is a rhythm game where users match mouse clicks with the music. The song played by the user, hits and misses, time and date of song played, and overall ranking is recorded in the OSR file. This OSR file can then be shared with others for replay purpose. OSR file requires the beatmap file to be present in the "Songs" folder.

**Tipo MIME de formato de arquivo OSR:** x-osu-replay

## Formato de arquivo OSR

Os arquivos OSR são salvos como arquivos binários com campos de dados de comprimento fixo e variável.

|Tipo de dados| Formato|
---|---|
|Byte |Modo de jogo do replay (0 = osu! Standard, 1 = Taiko, 2 = Catch the Beat, 3 = osu!mania)|
|Inteiro |Versão do jogo quando o replay foi criado (ex. 20131216)|
|String |osu! hash MD5 do mapa de batida |
|Sequência| Nome do jogador|
|Sequência| osu! hash MD5 de repetição (inclui certas propriedades da repetição)|
|Curto| Número de 300 |
|Curto| Número de 100 no padrão, 150 no Taiko, 100 no CTB, 100 no mania |
|Curto| Número de 50 no padrão, fruta pequena no CTB, 50 no mania|
|Curto| Número de Gekis no padrão, Max 300 na mania |
|Curto| Número de Katus no padrão, 200 na mania |
|Curto| Número de erros |
|Inteiro| Pontuação total exibida no relatório de pontuação |
|Curto| Maior combinação exibida no relatório de pontuação|
|Byte| Combinação perfeita/completa (1 = sem erros e sem quebras de controle deslizante e sem controles deslizantes finalizados antecipadamente) |
|Inteiro| Modos usados. Veja abaixo a lista de valores mod.|
|Sequência| Gráfico de barras de vida: pares separados por vírgula u/v, onde u é o tempo em milissegundos da música e v é um valor de ponto flutuante de 0 a 1 que representa a quantidade de vida que você tem em um determinado momento (0 = barra de vida é vazio, 1= barra de vida está cheia)|
|Longo| Carimbo de hora (tiques do Windows) |
|Inteiro| Comprimento em bytes de dados de reprodução compactados |
|Byte |Array Dados de reprodução compactados|
|Longo| ID de pontuação on-line |
|Duplo| Informações adicionais sobre mods. Presente apenas se a prática de tiro ao alvo estiver habilitada.|

## Referências

* [OSU! Jogo de ritmo](https://osu.ppy.sh/home)

* [Formato de arquivo OSR](https://osu.ppy.sh/wiki/en/Client/File_formats/Osr_%28file_format%29#data-types)


