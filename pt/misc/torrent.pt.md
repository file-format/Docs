{
  "date" : "2022-05-16",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo torrent - arquivo BitTorrent",
  "description":"Saiba mais sobre arquivos TORRENT e APIs que podem criar e abrir arquivos TORRENT.",
  "linktitle" : "TORRENT",
  "menu" : {
    "docs" : {
      "identifier":"misc-torrent",
      "parent" : "misc"
}
},
  "lastmod" : "2022-01-12"
}

## O que é um arquivo TORRENT?

Um arquivo TORRENT é um arquivo de texto usado pelo BitTorrent e outros programas P2P (peer-to-peer) para download e troca de conteúdo. O conteúdo para download pode incluir documentos, vídeos, jogos, filmes e outras mídias disponíveis na Internet. Inclui informações de metadados sobre o conteúdo e a localização da mídia a ser baixada. Softwares como o BitTorrent usam informações desse arquivo, como nome, tamanho do arquivo e estrutura de pastas para download de dados. Os arquivos torrent podem ser convertidos para outros formatos de arquivo, como [PDF](/pt/pdf/) online.

## O que é Torrent? O formato de arquivo TORRENT para troca de dados

Torrenting é o conceito de troca (download e upload) de arquivos de dados usando a rede BitTorrent. Ao contrário dos servidores convencionais, onde os dados são carregados para outros acessarem e baixarem, os arquivos torrent são recuperados e enviados usando a rede torrent. Quando um usuário abre um arquivo .torrent em aplicativos como BitTorrent, o software inicia o download do conteúdo do arquivo bit a bit. Se vários usuários tiverem o mesmo arquivo, o BitTorrent divide os downloads entre todos os usuários para acelerar o processo de download. Ao mesmo tempo, o computador do usuário que está baixando o arquivo também se torna a fonte do arquivo para enviá-lo para outros usuários que também estão baixando o mesmo arquivo.

### Estrutura de um arquivo TORRENT

Um arquivo torrent é uma combinação de uma lista de arquivos e informações de metadados sobre todas as partes do arquivo a serem baixadas. Ele contém as seguintes informações na forma de chaves.

- `announce` — O URL do rastreador que é anunciado a outros peers para informar sobre a disponibilidade do arquivo
- `info` — Isso mapeia para um dicionário cujas chaves dependem se um ou mais arquivos estão sendo compartilhados:
  - files—a list of dictionaries each corresponding to a file (only when multiple files are being shared). Each dictionary has the following keys:
- `length` — tamanho do arquivo em bytes.
- `path` — uma lista de strings correspondentes aos nomes dos subdiretórios, o último dos quais é o nome real do arquivo
- `length` — o tamanho do arquivo em bytes (somente quando um arquivo está sendo compartilhado)
- `name` — nome do arquivo onde o arquivo deve ser salvo
- `piece length` — número de bytes por peça. Isso geralmente é 28 KiB = 256 KiB = 262.144 B.
- `pieces` — uma lista de hash que é uma concatenação do hash SHA-1 de cada peça.

## O torrent é seguro e legal?

O protocolo de torrent para troca de dados entre usuários P2P é seguro, pois é apenas o meio de compartilhar qualquer tipo de arquivo. Assim, o protocolo em si não é inseguro ou ilegal. No entanto, o conteúdo compartilhado pela rede pode conter arquivos ou mídia que podem violar o status legal dos documentos compartilhados. Nesse caso, a troca de tais dados pode causar ações legais contra as partes envolvidas no compartilhamento de tais arquivos publicamente.

## Referências

* [TORRENT File - wikipedia](https://en.wikipedia.org/wiki/Torrent_file)

