{
  "date" : "2021-06-09",
  "keywords" :[ "cda", "arquivo", "extensão", "formato", "o que é um arquivo cda", "música", "formato de arquivo cda", "especificação de formato de arquivo cda"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo CDA e APIs que podem criar, converter e abrir arquivos CDA.",
  "title" :"CDA - CD Audio Track Shortcut File",
  "linktitle" : "CDA",
  "menu" : {
    "docs" : {
      "parent" : "audio"
}
},
  "lastmod" : "2021-06-09"
}

## O que é um arquivo CDA?

Um arquivo com extensão .cda é um pequeno arquivo stub gerado pelo Microsoft Windows para cada faixa de áudio em um CD de áudio. Esses arquivos contêm informações típicas, como tempos de faixa e um atalho do Windows que permite aos usuários acessar as faixas de áudio específicas. Os arquivos CDA não são música, mas estão apontando para um arquivo de música existente em algum lugar no armazenamento. Podemos dizer isso como um atalho de um arquivo de áudio que está localizado em um CD.

## Formato de arquivo CDA

O formato de arquivo CDA é usado para informar a um computador qual arquivo de áudio deve ser reproduzido em um CD. Assim, os arquivos CDA tornam-se inúteis separados de um CD que representam. Os arquivos CDA são comumente considerados como recursos RIFF. Existe apenas um pedaço chamado "CDDA" e contém apenas um bloco de dados chamado "FMT" na versão atual do arquivo .cda. Este bloco tem 24 bytes. O identificador criado pelo Windows é usado pela unidade de CD relacionada ao Windows 95 e ao Windows 98 e seu player não pode se conectar ao FreeDB ou CDDB. Para que ele possa exibir o título da música e o nome do artista, você deve inserir manualmente essas informações no arquivo cdplayer.ini.

### Organização de um arquivo CDA

A tabela a seguir mostra as informações sobre deslocamentos típicos:
| deslocamento | comprimento | conteúdo |
---|---|---|
| 0x00 | 4 | os 4 caracteres ASCII "RIFF" |
| 0x04 | 4 | o tamanho do seguinte pedaço: sempre 36 (44 - 8), em 4 bytes (ordem Intel) |
| 0x08 | 4 | identificador de bloco: os 4 caracteres ASCII "CDDA" |
| 0x0C | 4 | os 3 caracteres ASCII "fmt" seguidos de um espaço |
| 0x10 | 4 | comprimento do pedaço: sempre 24, em 4 bytes (ordem Intel) |
| 0x14 | 2 | versão do formato CD, em 2 bytes (ordem Intel). Em maio de 2006, sempre igual a 1. |
| 0x016 | 2 | número do intervalo, em 2 bytes (ordem Intel). A primeira faixa tem o número 1. |
| 0x18 | 4 | identificador calculado pelo Windows para cdplayer.exe. |
| 0x1c | 4 | deslocamento de intervalo, em número de quadros (ordem Intel) |
| 0x20 | 4 | duração da faixa, número total de quadros (ordem Intel) |
| 0x24 | 1 | posição do intervalo: quadros |
| 0x25 | 1 | posição do intervalo: segundos |
| 0x26 | 1 | posição do intervalo: minutos |
| 0x27 | 1 | um byte nulo (valor binário 0) |
| 0x28 | 1 | duração da trilha: quadros |
| 0x29 | 1 | duração da faixa: segundos |
| 0x2a | 1 | duração da pista: minutos |
| 0x2b | 1 | um byte nulo (valor binário 0) |

## Referências

* [arquivo .cda - Por Wikipedia](https://en.wikipedia.org/wiki/.cda_file)

