{
"data": "16/05/2023",
  "keywords": [
"arquivo sami",
"o que é um arquivo sami",
"exemplo de arquivo sami",
"arquivo",
"extensão de arquivo sami",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo SAMI - arquivo de troca de legendas e metadados",
  "description":"Aprenda sobre o formato SAMI e APIs que podem criar e abrir arquivos SAMI.",
"linktitle": "SAMI",
  "menu": {
    "docs": {
      "identifier": "video-sami",
"parent" : "video"
}
},
"último mod": "16/05/2023"
}

## O que é um arquivo .SAMI?

Um arquivo com a extensão ".sami" normalmente se refere a um arquivo Subtitles And Metadata Interchange (SAMI). SAMI é um formato de legenda usado para exibir legendas ou legendas ocultas em vídeos. Foi originalmente desenvolvido pela Microsoft para o Windows Media Player.

Os arquivos SAMI contêm informações de tempo e conteúdo de texto para legendas ou legendas ocultas, permitindo que sejam sincronizados com a reprodução de vídeo. O formato oferece suporte a opções básicas de formatação, como estilo de fonte, cor e posicionamento das legendas na tela.

Os arquivos SAMI geralmente são arquivos de texto simples e podem ser abertos e editados usando um editor de texto. O conteúdo de um arquivo SAMI normalmente inclui uma seção de cabeçalho que fornece informações sobre o arquivo, seguida por entradas de legendas individuais com seus respectivos tempos e texto.

Aqui está um exemplo da aparência de um arquivo SAMI:

```
<SAMI>
<HEAD>
<TITLE>Example Subtitles</TITLE>
</HEAD>
<BODY>
<SYNC Start=100><P Class=ENCC>Subtitle 1</P></SYNC>
<SYNC Start=500><P Class=ENCC>Subtitle 2</P></SYNC>
<SYNC Start=1000><P Class=ENCC>Subtitle 3</P></SYNC>
</BODY>
</SAMI>
```

Os arquivos SAMI são comumente usados em conjunto com reprodutores de vídeo ou reprodutores de mídia que suportam exibição de legendas, como Windows Media Player ou VLC Media Player. O player lê o arquivo SAMI e sincroniza as legendas com o conteúdo do vídeo, permitindo que os espectadores leiam as legendas enquanto assistem ao vídeo.

## Tags HTML suportadas

Os arquivos SAMI (Subtitles And Metadata Interchange) suportam um conjunto limitado de tags semelhantes a HTML para formatar e estilizar as legendas. Aqui estão algumas das tags comumente usadas suportadas pelo SAMI:

- ``<SAMI> :`` O elemento raiz que encapsula todo o arquivo SAMI.
- ``<HEAD> :`` Contém informações de cabeçalho para o arquivo SAMI.
<html>- ``<TITLE> :`` Especifica o título do arquivo SAMI. </html>
- ``<BODY> :`` Inclui as entradas de legenda e suas informações de tempo.
- ``<SYNC> :`` Representa um ponto de sincronização para uma entrada de legenda. Especifica o momento em que a legenda deve ser exibida.
- ``<P> :`` Inclui o conteúdo de texto real de uma legenda. Geralmente é usado dentro de um<SYNC> bloquear.
<html>- `` <FONT>:`` Define propriedades de fonte para o texto incluído. Atributos como Cor, Face, Tamanho e Estilo podem ser usados para modificar a aparência da fonte.</font>
- ``<BR> :`` Insere uma quebra de linha dentro de uma legenda.
<html>- `` <B>:`` Renderiza o texto incluído em negrito.</b>
<html>- `` <I>:`` Renderiza o texto incluído em itálico.</i>
<html>- `` <U>:`` Renderiza o texto incluído sublinhado.</u>
- ``<C> :`` Especifica a posição ou alinhamento do texto da legenda na tela. Suporta atributos como Centro, Meio, Esquerda, Direita, Superior, Inferior e suas combinações.
- ``<LANG> :`` Especifica o código do idioma para o texto da legenda. Ajuda a identificar o idioma das legendas.

Estas são algumas das tags básicas suportadas pelos arquivos SAMI. É importante observar que o SAMI não oferece suporte a toda a gama de tags e atributos HTML. As tags suportadas concentram-se principalmente no estilo e no posicionamento das legendas, em vez de fornecer ampla estruturação ou interatividade do documento.

## Referências
* [SAMI](https://en.wikipedia.org/wiki/SAMI)

