{
  "date" : "2021-07-12",
  "keywords" :[ "arquivo cmd", "o que é um arquivo cmd", "arquivo", "exemplo cmd", "extensão do arquivo cmd", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo CMD e APIs que podem criar e abrir arquivos CMD.",
  "title" :"CMD - Formato de arquivo de comando do Windows",
  "linktitle" : "CMD",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-07-12"
}

## O que é um arquivo CMD?
Um arquivo CMD consiste em um script contendo um ou vários comandos na forma de texto simples que são executados para executar várias tarefas. É semelhante a um arquivo [BAT](/pt/executable/bat/), que geralmente também é usado para armazenar um lote de comandos executáveis. Os arquivos CMD são amplamente utilizados no sistema operacional Microsoft Windows. Esses arquivos foram introduzidos quase na década de 90, mas ainda são usados no sistema operacional Windows mais recente. Esses arquivos geralmente são gravados para executar mais de um comando em uma sequência.

## Formato de arquivo CMD
CMD é um formato de arquivo usado por programas executáveis no estilo CP/M. Geralmente é comparável com [COM](/pt/executable/com/) no CP/M-80 e [EXE](/pt/executable/exe/) no DOS. Um arquivo CMD contém de 1 a 8 grupos de código ou dados e um cabeçalho de 128 bytes. Cada grupo pode ter até 1 MB de tamanho. Os arquivos CMD também podem conter informações de realocação e Extensões de Sistema Residentes (RSXs) em suas versões posteriores. O CMD é um recém-chegado em comparação com o arquivo [BAT](/pt/executable/bat/); usado para MS-DOS antes do lançamento do Windows No MS-DOS. Embora ainda seja possível salvar arquivos com extensão .bat hoje, muitas pessoas usam a extensão .cmd para salvar seus scripts executáveis.

### Especificação do formato CMD

O início do cabeçalho contém a lista dos grupos presentes no arquivo junto com seus tipos. Cada tipo pode ser usado uma vez no máximo. Esses tipos são:

- Código
- Dados
- Adicional
- Pilha
- Usuário 1
- Usuário 2
- Usuário 3
- Usuário 4
- Código compartilhado

Da mesma forma que o prefixo de segmento de programa no DOS, os primeiros 256 bytes do grupo de dados são zero. Eles serão preenchidos pelo CP/M-86 com a página zero. Se não houver grupo de dados, os primeiros 256 bytes do grupo de código serão usados.
## Exemplo de arquivo CMD
A seguir está um exemplo de um script CMD para mostrar informações de sistemas.
```
@ECHO OFF

:: This CMD script provides you with your operating system, hardware and network information.

TITLE My System Info

ECHO Please wait... Gathering system information.

ECHO =========================

ECHO OPERATING SYSTEM

systeminfo | findstr /c:"OS Name"

systeminfo | findstr /c:"OS Version"

ECHO =========================

ECHO BIOS

systeminfo | findstr /c:"System Type"

ECHO =========================

ECHO MEMORY

systeminfo | findstr /c:"Total Physical Memory"

ECHO =========================

ECHO CPU

wmic cpu get name

ECHO =========================

ECHO NETWORK ADDRESS

ipconfig | findstr IPv4

ipconfig | findstr IPv6

PAUSE
```



## Referências

* [Como escrever um script CMD](https://smallbusiness.chron.com/write-cmd-script-53226.html)
* [arquivo CMD (CP/M) - pela Wikipedia](https://en.wikipedia.org/wiki/CMD_file_(CP/M))

