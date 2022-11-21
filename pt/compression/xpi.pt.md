{
  "date" : "2022-06-07",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"XPI - Arquivo de pacote do instalador multiplataforma",
  "description":"Saiba mais sobre o formato de arquivo XPI e APIs que podem criar e abrir arquivos XPI.",
  "linktitle" : "XPI",
  "menu" : {
    "docs" : {
    "identifier": "compression-xpi",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-07"
}

## O que é um arquivo XPI?

Um arquivo XPI é um arquivo de instalação compactado para reduzir o tamanho do arquivo. Ele é usado pelos aplicativos Mozilla para instalação de plugins e arquivos de complemento. Ele contém um script de instalação ou um manifesto na raiz do arquivo junto com vários arquivos de dados. Um arquivo XPI pode conter temas, kit de ferramentas ou plugins do Firefox que o usuário pode instalar para se tornar parte do navegador Firefox, Thunderbird ou SeaMonkey.

## Formato de arquivo XPI - Mais informações

Os arquivos XPI são salvos em disco como arquivos [ZIP](/pt/compression/zip/) que combinam vários arquivos em um único arquivo compactado. Os arquivos dentro de um arquivo XPI podem incluir arquivo de script de instalação como JS e arquivos da web como [CSS](/pt/web/css/), [HTML](/pt/web/html/) e [JSON](/pt/web/json/ ). Às vezes, também pode conter arquivos de imagem [PNG](/pt/image/png/) para serem usados como ícones pelo complemento.

### Como visualizar o conteúdo do arquivo XPI?

Um arquivo XPI é praticamente um arquivo ZIP cujo conteúdo pode ser visualizado seguindo as etapas a seguir.

* Altere a extensão do arquivo de XPI para ZIP
* Extraia o conteúdo do arquivo usando qualquer utilitário de descompactação padrão, como WinZip (Windows, Mac), 7-Zip (Windows) ou Apple Archive Utility (Mac).

### Instale o arquivo XPI no Firefox Android

Principalmente as pessoas estão curiosas para saber se os arquivos XPI podem ser instalados no Firefox em dispositivos Android. No Android, você pode instalar o complemento de um arquivo XPI localizando o arquivo e abrindo-o com o Firefox.

## Referências

* [XPInstall - Wikipedia](https://en.wikipedia.org/wiki/XPInstall)
* [Como posso abrir uma extensão de arquivo XPI?](https://support.mozilla.org/en-US/questions/1009049)

