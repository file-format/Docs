{
  "date" : "2022-04-01",
  "keywords" :[ "arquivo nkit", "formato de arquivo nkit", "o que é um arquivo nkit", "arquivo", "exemplo nkit", "extensão de arquivo nkit", "extensão", "formato", "rodapé nkit", "arquivo formato de nkit"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo NKIT e APIs que podem criar e abrir arquivos NKIT.",
  "title" :"NKIT - Formato de arquivo de imagem de disco",
  "linktitle" : "NKIT",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-04-01"
}

## O que é um arquivo NKIT?

Um arquivo NKIT é uma imagem de disco de dados extraídos de jogos NintendoWii e GameCube. NKIT é para o formato Nintendo Toolkit. O arquivo de compactação [ISO](/pt/compression/iso/) resultante utiliza os dados principais desses jogos para serem executados com programas emuladores como Dolphin, Swiss e Nintendont. O NKit vem em formatos de arquivo raw (iso) e compactados (gcz), que foram projetados tendo em vista a capacidade de reprodução e o tamanho.

## Formato de arquivo NKIT

O formato de arquivo NKit é um formato sem perdas e é usado para reduzir e restaurar imagens do Nintendo Wii e do GameCube. Os formatos estão disponíveis nos formatos de arquivo ISO e GCZ para cada um dos jogos GameCube e Wii.

|Sistema |Formato |Hardware suportado |Dolphin suportado |Restaurável 1:1 |Notas|
---|---|---|---|---|---|
|GameCube| nkit.iso| Sim |Sim| Sim |Igual à iso compactada do GameCube|
|GameCube| nkit.gcz| Não| Sim| Sim |GCZ é o próprio formato de compressão de bloco do Dolphin|
|Wii| nkit.iso| Não Sim| Sim| O formato RVT-H só pode ser reproduzido no Dolphin|
|Wii| nkit.gcz| Não Sim| Sim| RVT-H em GCZ jogável apenas em Dolphin|

### Cabeçalho NKIT

O cabeçalho do formato de arquivo NKIT é o seguinte.

|Deslocamento |Comprimento |Nome|
---|---|---|
|0x200 |0x4 |NKit Cabeçalho 'NKIT'|
|0x204 |0x4 |NKit Versão 'v01'|
|0x208 |0x4 |Imagem de origem original CRC32|
|0x20C |0x4 |NKit CRC - torna o arquivo NKit CRC32 igual ao CRC de origem em 0x208 (em 0x4 no GCZ)|
|0x210 |0x4 |Comprimento da imagem de origem|
|0x214 |0x4 |ID de lixo eletrônico forçado (quando o ID do disco é diferente - raro - apenas GameCube)|
|0x218 |0x4 |Wii Atualizar partição CRC32 se removido ao converter|

## Referências ##

* [Formato de arquivo NKIT - por gbatemp](https://wiki.gbatemp.net/wiki/NKit/NKitFormat)

