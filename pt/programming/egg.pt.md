{
  "date" : "2022-03-15",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"EGG File Format - Python Distribution File",
  "description":"Saiba mais sobre o formato de arquivo EGG e APIs que podem criar e abrir arquivos EGG.",
  "linktitle" : "EGG",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2022-03-15"
}

## O que é um arquivo EGG?

Um arquivo EGG, também conhecido como ovos Python, é um formato de distribuição mais antigo das distribuições Python. É um arquivo compactado [ZIP](/pt/compression/zip/) com extensão .egg e contém os arquivos de origem do aplicativo Python junto com as informações meta sobre a distribuição. Os arquivos EGG são alternativos a um arquivo Windows Executable [EXE](/pt/executable/exe/), mas é multiplataforma. Esse formato antigo para distribuições Python foi substituído pelo formato de arquivo Wheel (WHL) mais recente no início de 2010.

## Formato de arquivo EGG

Os arquivos EGG são salvos como arquivos ZIP compactados. Isso significa que, se você substituir a extensão .egg por .zip, poderá abri-la com utilitários de descompactação padrão, como Corel WinZIP, Microsoft Explorer ou RARLAB WinRAR.

Os arquivos EGG podem ser criados usando o pacote **distutils** disponível pelo Python. Outra ferramenta que pode criar e abrir arquivos EGG é o **SetupTools**. Os arquivos EGG podem ser instalados como um pacote usando **easy_install**.

`NOTA - O formato de arquivo EGG foi obsoleto em favor do novo formato de arquivo WHL da roda.`

## Referência ##

* [OVOS Python](https://python101.pythonlibrary.org/chapter38_eggs.html)

