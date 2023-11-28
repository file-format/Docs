{
  "date" : "2023-01-31",
  "keywords" :["arquivo de execução", "o que é um arquivo de execução", "arquivo", "como abrir arquivo de execução", "extensão de arquivo de execução","extensão"],
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "description" :"Aprenda sobre o formato de arquivo RUN e APIs que podem criar e abrir arquivos RUN.",
  "title" :"Formato de arquivo RUN - arquivo executável do Linux",
  "linktitle" : "RUN",
  "menu" : {
    "docs" : {
      "identifier":"executable-run",
      "parent" : "executable"
}
},
  "lastmod" : "2023-01-31"
}

## O que é um arquivo .RUN?

O formato de arquivo .run é comumente usado para distribuição de software ou instaladores de aplicativos no ambiente Linux. Para instalar o software, você precisará tornar o arquivo executável, o que pode ser feito usando o seguinte comando:

```bash
chmod +x file_name.run 
```

Então, você pode executar o arquivo usando o seguinte comando:

```bash
./file_name.run 
```

O processo de instalação pode variar dependendo do arquivo e programa específico que você está tentando instalar.

O formato de arquivo .run é um tipo de script de shell usado para distribuir software ou instaladores de aplicativos no ambiente Linux. É um pacote independente que inclui tudo o que é necessário para instalar o software, incluindo arquivos binários, bibliotecas e arquivos de configuração.

É importante observar que os arquivos .run também podem conter código malicioso, por isso é sempre uma boa ideia verificar a origem do arquivo e verificar se há vírus antes de executá-lo.

Além disso, alguns arquivos .run podem exigir privilégios de root para serem executados e instalados, portanto, pode ser necessário usar o comando “sudo” para executar o arquivo com permissões elevadas:

```bash
sudo ./filename.run
```

## Como abrir o arquivo RUN?

Para abrir um arquivo .run, você precisa torná-lo executável, o que pode ser feito com o comando “chmod”:

```bash
chmod +x filename.run 
```

Depois que o arquivo se tornar executável, você pode executá-lo digitando:

```bash
./filename.run
```

Executar um arquivo .run não é o mesmo que abri-lo em um editor de texto. A execução de um arquivo .run executará suas instruções, que podem ser qualquer coisa, desde a instalação de um programa até a execução de um script. Para visualizar o conteúdo de um arquivo .run, você precisa abri-lo em um editor de texto, como nano ou vim:

```
nano filename.run
```
ou
```
vim filename.run
```

## Referências
* [Como executar arquivos .bin e .run no Ubuntu](https://vitux.com/how-to-execute-bin-and-run-files-in-ubuntu/)


