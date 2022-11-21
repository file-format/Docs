{
  "date" : "2021-02-15",
  "keywords" :[ "arquivo vp6", "formato de arquivo vp6", "o que é um arquivo vp6", "arquivo", "exemplo vp6", "extensão de arquivo vp6","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"VP6 - Arquivo de vídeo TrueMotion",
  "description":"Saiba mais sobre o formato de arquivo VP6 e APIs que podem criar e abrir arquivos VP6.",
  "linktitle" : "VP6",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-02-16"
}

## O que é um arquivo VP6?

VP6 é um formato de vídeo de compressão com perdas que foi introduzido pelas tecnologias On2 em maio de 2003. Faz parte de uma série de codecs de vídeo desenvolvidos pela TrueMotion, incluindo V3, V4 e V5. O formato foi usado rapidamente no campo de transmissão, como com relatórios da BBC e software QuickLink. O VP6 foi sucedido pelo VP7 Codec em janeiro de 2005 com melhor compatibilidade de compressão.

## Formato de arquivo VP6

As especificações completas para arquivos V6 não estão disponíveis publicamente. A On2 tornou as especificações públicas inicialmente, mas logo elas ficaram indisponíveis para usuários em geral. Uma documentação não oficial do formato de arquivo VP6 está disponível em [wiki multimídia](https://wiki.multimedia.cx/index.php?title=On2_VP6) que pode ser consultada para referência do desenvolvedor.

### Macroblocos (MB)

Semelhante ao MPEG-2, MPEG-4 partes 2 e 10, cada quadro de vídeo de um arquivo VP6 é composto por uma matriz de macroblocos (MB) de 16x16. Cada MB pode estar em um dos seguintes modos:

* IntraMB
* Inter MB, MV nulo, referência de quadro anterior
* Inter MB, MV diferencial, referência de quadro anterior
* Inter MB, quatro MVs, referência de quadro anterior
* Inter MB, MV 1, referência de quadro anterior
* Inter MB, MV 2, referência de quadro anterior
* Inter MB, MV nulo, referência de quadro marcada
* Inter MB, MV diferencial, referência de quadro marcada
* Inter MB, MV 1, referência de quadro marcada
* Inter MB, MV 2, referência de quadro marcada

### Cabeçalho do quadro

O cabeçalho do quadro de um VP6 é como mostrado abaixo, que segue o empacotamento de bits big-endian.

|Sintaxe|Número de bits|Tipo|Symantecs|
---|---|---|---|
|frame_mode|1|Enum|0x0 significa um intraframe|
|qp |6 |Não assinado |Intervalo válido do parâmetro de quantificação 0..63|
|marcador| 1| Constante| 0=VP61/62, 1=VP60|
|if (modo_quadro == 0) { | 0 | |igual a INTRA_FRAME|
|versão |5| Constante| 6=VP60/61, 7=VP60(Electronic Arts), 8=VP62|
|versão2 |2| Constante |0=VP60, 3=VP61/62|
|entrelaçar |1| Boolean |true (1) significa que o entrelaçamento será usado|
|if (marcador==1 ou versão2==0) {||||
|deslocamento |16 |Não assinado| deslocamento do buffer secundário (bytes relativos ao início do buffer)|
|}||||
|dim_y |8| Não assinado| Altura do macrobloco de vídeo|
|dim_x |8| Não assinado| Largura do macrobloco de vídeo|
|render_y |8 |Não assinado |Exibir altura do vídeo|
|render_x |8 |Não assinado |Largura de exibição do vídeo|
|}outra{||||
|if (marcador==1 ou versão2==0) {||||
|deslocamento |16 |Não assinado |Deslocamento do buffer secundário (bytes relativos ao início do buffer)|
|}||||
|}||||

## Referências

* [VP6 Wikipedia](https://en.wikipedia.org/wiki/VP6#:~:text=On2%20TrueMotion%20VP6%20is%20a,Video%2C%20and%20JavaFX%20media%20files.)

