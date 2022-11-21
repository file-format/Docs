{
  "date" : "2019-10-11",
  "keywords" :[ "AVI", "Vídeo de áudio compactado", "Arquivo", "Extensão", "Formato de arquivo", "Contêiner de multimídia", "XVid", "DivX", "Codecs", "Formato de arquivo de intercâmbio de recursos", "RIFF "],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo AVI - um arquivo de intercalação de áudio e vídeo",
  "description":"Saiba mais sobre o formato de arquivo AVI e APIs que podem criar e abrir arquivos AVI.",
  "linktitle" : "AVI",
  "menu" : {
    "docs" : {
      "parent" : "video"
}
},
  "lastmod" : "2021-04-23"
}

## O que é um arquivo AVI? ##

O formato de arquivo **AVI** é um formato de arquivo de contêiner multimídia de áudio e vídeo que foi introduzido pela Microsoft. Ele contém os dados de áudio e vídeo criados e compactados usando vários codecs (Codificadores/Decodificadores), como **XVid** e **DivX**. Como diferentes codecs podem ser usados para codificar o conteúdo AVI, os aplicativos de recuperação, ou seja, players AVI, devem ser capazes de abri-los somente se tiverem os codecs necessários instalados com os quais o conteúdo AVI foi criado. O formato é suportado por padrão em todas as plataformas do **Microsoft Windows**, bem como em quase todas as outras plataformas principais. Vários aplicativos e APIs fornecem a capacidade de criar/salvar, ler e converter AVI para outros formatos populares, como MP4, MOV, WMV, etc.

## Formato de arquivo AVI ##

Um arquivo com extensão .avi é um arquivo AVI. É um subformato do Resource Interchange File Format (RIFF). O RIFF organiza os dados em blocos, ou "pedaços", que são identificados com uma tag FourCC. Um arquivo AVI é simplesmente um "pedaço" em um arquivo formatado em RIFF.

No primeiro sub-chunk, o cabeçalho do arquivo é identificado pela tag "hdrl"; seu conteúdo inclui a largura, a altura e a taxa de quadros do vídeo. No segundo sub-chunk, a tag de movimento representa a taxa de quadros do vídeo. O vídeo AVI é composto pelos dados audiovisuais reais neste pedaço. Há também um terceiro subchunk opcional com a tag "idx1", que indica a posição dentro do arquivo dos blocos de dados individuais que pertencem ao arquivo.

### Limitações ###

* As informações de proporção de aspecto não podem ser codificadas na especificação AVI original, embora a especificação OpenDML posterior (AVI 2.0) ofereça um método padronizado
* Embora os arquivos AVI sejam amplamente usados na pós-produção de filmes e televisão, várias abordagens para adicionar um código de tempo a eles estão competindo, afetando a usabilidade do formato.
* Um arquivo de vídeo codificado em AVI não pode usar uma técnica de compactação que exija dados de quadros futuros além do quadro que está sendo codificado (quadro B)
* É problemático usar arquivos AVI com taxas de bits variáveis (VBR) (como áudio MP3 em taxas de amostragem abaixo de 32 kHz)
* Um arquivo AVI com codificação de longa-metragem de definição padrão, como normalmente usado, provavelmente incorrerá em sobrecarga de cerca de 5 MB por hora, dependendo de como o arquivo é usado
* As legendas devem ser codificadas no fluxo de vídeo ou distribuídas em um arquivo separado, caso os arquivos AVI não possam acomodar anexos como fontes e legendas

## Breve história ##

O AVI foi introduzido pela Microsoft em 1992 com o objetivo de fornecer um formato de arquivo de áudio e vídeo mais robusto e avançado. O formato rapidamente se tornou popular com o uso da internet, permitindo que indivíduos compartilhem arquivos de vídeo direta e indiretamente por meio de armazenamento de mídia baseado em nuvem.

## Referências ##

* [AVI - Por Wikipedia](https://en.wikipedia.org/wiki/Audio_Video_Interleave)

