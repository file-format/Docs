{
  "date" : "2022-03-01",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo VPK - Formato de arquivo do pacote de aplicativos PlayStation Vita",
  "description":"Saiba mais sobre o formato de arquivo VPK e APIs que podem criar e abrir arquivos VPK.",
  "linktitle" : "VPK",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-03-01"
}

## O que é um arquivo VPK?

Um arquivo com extensão .vpk é um arquivo de pacote compactado usado para instalar aplicativos de terceiros no console de jogos Sony PlayStation Vita. Esses arquivos podem ser instalados apenas no jailbreak Vita PlayStation da HENkaku, que permitiu que o PS Vita e o PSTV usassem conteúdo personalizado criado pelo usuário. Um arquivo VPK contém todo o conteúdo que compõe o jogo, incluindo imagens como arquivos [PNG](/pt/image/png/), arquivos de configuração como [.bin](/pt/disc-and-media/bin/) e qualquer configuração no formato de arquivo [XML](/pt/web/xml/).

## Formato de arquivo VPK

Os arquivos VPK são salvos em disco como arquivos compactados padrão [ZIP](/pt/compression/zip/). Eles podem conter várias pastas e outros arquivos associados aos aplicativos de terceiros a serem instalados no Vita Gaming Console. Para visualizar o conteúdo do arquivo do pacote VPK, renomeie sua extensão de .vpu para .zip e extraia o conteúdo usando utilitários de descompactação padrão, como WinZip ou WinRAR.

A Valvesoftware tem informações detalhadas sobre o [formato de arquivo VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format) que podem ser referenciados da perspectiva do desenvolvedor.

## Como instalar arquivos VPK?

Os arquivos VPK podem ser instalados a partir do utilitário de linha de comando VPK.exe. No sistema operacional Windows, os arquivos podem ser descartados no arquivo vpk.exe que retorna um \*.vpk contendo todos os arquivos empacotados. Alternativamente, a ferramenta de linha de comando pode ser usada da seguinte maneira.

### Crie VPK e adicione arquivos

```
vpk <dirname>
```

### Extrair arquivos VPK

```
vpk x <vpkfile> <filename1> <filename2> ...
```

## Visualizador de VPK

* [VRF VPK Viewer](https://github.com/SteamDatabase/ValveResourceFormat)

## Referências

* [Formato de arquivo VPK](https://developer.valvesoftware.com/wiki/VPK_File_Format)
* [Arquivos VPK](https://developer.valvesoftware.com/wiki/VPK)

