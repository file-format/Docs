{
  "date" : "2021-03-08",
  "keywords" :[ "RB", "dispositivo Rocket eBook da Nuvo Media", "arquivo", "extensão", "formato", "eBook" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo RB para o dispositivo Rocket eBook da Nuvo Media e as APIs que podem criar e abrir arquivos RB.",
  "title" :"RB - Arquivo eBook Rocket",
  "linktitle" : "RB",
  "menu" : {
    "docs" : {
      "parent" : "ebook"
}
},
  "lastmod" : "2021-03-08"
}

## O que é um arquivo RB?

O arquivo com extensão .rb contém o conteúdo do Rocket eBook. O Rocket eBook é na verdade um dispositivo feito pela Nuvo Media; eles lançaram este dispositivo em 1998. Embora o Rocket eBook seja capaz de exibir imagens, mas apenas em preto e branco. Ele tem uma tela de 106 dpi ou 480 x 320 pixels em uma tela sensível ao toque de 4,5 x 3 polegadas. O Rocket eBook se conecta a um computador através de uma conexão de porta serial para baixar eBooks no formato de arquivo RB. Os arquivos RB são capazes de usar DRM, mas essa tecnologia não está sendo usada em eBooks modernos. O arquivo RB convencionalmente contém um arquivo HTML com as imagens e um arquivo pseudo-OPF com todos os metadados (.info).

## Especificação Técnica do Formato de Arquivo RB ##

Um número mágico (em hexadecimal) aparece nos primeiros 4 bytes do arquivo: B0 0C B0 0C.

Parece que os próximos dois bytes são um número de versão, como "02 00", que significa versão principal 2 e versão secundária 0.

Os próximos quatro bytes contêm o texto "NUVO", seguido de 4 bytes de 00h.

Os próximos 4 bytes são a data em que o livro foi criado, codificado como int16. Isso nos coloca no deslocamento 0Eh. A versão antiga do ORocketLibrary codificava o valor total do ano (ou seja, 1999 era "CF 07", 2000 era "D0 07"). Na versão recente, tm_year é armazenado literalmente, ou seja, 100 para o ano 2000 ("64 00"). Após o ano vem um int8 representando o número do mês relativo 1 e um int8 representando o dia do mês.

Os próximos 6 bytes são 00h. Para ajuste de tempo, estes podem ser reservados.

O deslocamento absoluto do "Índice" está contido em um int32 no deslocamento 18h.

Depois disso, há um int32 contendo o comprimento do arquivo .rb. Isso é usado para determinar se os arquivos estão completos ou não.

Todo esse pedaço de bytes (20h a 128h) parece ser necessário apenas para um título criptografado. Em títulos não criptografados, eles são sempre zero.

Na maioria dos casos, segue o índice (no deslocamento 128). Ele começa com uma contagem int32 do número de entradas de "página" (seções de arquivo .rb) no ToC. Cada entrada consiste em um nome (preenchido com zeros até 32 bytes), seguido por 3 int32s: o comprimento do segmento de dados, a posição no arquivo .rb e um sinalizador para essa entrada. A partir de hoje, os valores conhecidos são: 1 (criptografado), 2 (página de informações) e 8 (deflacionado). Os nomes são todos adaptados, conforme necessário, para garantir que sejam todos exclusivos.

## Referências

* [E-Reader - Por MobileRead](https://en.wikipedia.org/wiki/E-reader)

