{
  "date" : "2021-07-08",
  "keywords" :[ "SYS", "extensão", "arquivo", "formato", "sistema", "Driver", "Arquivo de sistema", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SYS - Formato de arquivo do sistema",
  "description":"Saiba mais sobre o formato de arquivo SYS e APIs que podem criar e abrir arquivos SYS.",
  "linktitle" : "SYS",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-08"
}

## O que é um arquivo SYS? ##

Os arquivos SYS são "arquivos de sistema" usados em aplicativos Windows OS e MS-DOS. Esses arquivos não podem ser abertos diretamente e consistem no driver e na configuração do dispositivo. Os arquivos SYS são responsáveis por conter arquivos de funções centrais do sistema operacional. Estes são considerados arquivos críticos do driver do dispositivo e também podem ser usados quando qualquer problema do driver de corrida deve ser resolvido. Estes são responsáveis pelo bom funcionamento de um sistema de computador, e os arquivos .sys devem estar corretos e completos.


## Especificação Técnica ##

Os arquivos .sys são, na verdade, o subconjunto do formato [BMP](/pt/image/bmp), pois só permite combinações específicas. O formato usual desses arquivos é como LOGOS.SYS, LOGOW.SYS e LOGO.SYS. Quaisquer outros arquivos não possuem este formato.

Esses arquivos são usados principalmente no diretório *C* do Windows no momento da instalação. A maioria dos problemas que giram em torno de drivers de dispositivo são resolvidos com a atualização do sistema operacional Windows. Os detalhes e informações desses arquivos podem ser visualizados usando os programas internos do sistema operacional Windows. Estes também incluem as referências a diferentes módulos em um sistema operacional.
Alguns dos exemplos de arquivos do sistema são:

* IO.SYS (Estes armazenam drivers de dispositivo do sistema operacional de disco)
* MSDOS.SYS (contêm o kernel ou o código central do sistema operacional)
* CONFIG.SYS (contêm várias opções de configuração)
* KEYBOARD.SYS (contêm informações relacionadas ao layout do teclado)
* COUNTRY.SYS (Estas informações relacionadas ao país e à página de código)

## Formato de arquivo SYS ##

A Microsoft desenvolveu os arquivos com extensões .sys. Variáveis e funções estão incluídas nos arquivos SYS. Estes são usados principalmente pelo sistema operacional da Microsoft. Esses arquivos estão localizados principalmente no diretório raiz do disco:

* C:\Windows\system32\drivers
* C:\Windows\WinSxS

Alguns avisos comuns sobre arquivos SYS são os seguintes:

* Os nomes desses arquivos não devem ser alterados, pois esses arquivos são responsáveis pelas principais funções e variáveis do sistema operacional
* Esses arquivos não devem ser excluídos, pois a ausência desses arquivos pode causar erros
* Os arquivos .sys não devem ser baixados da internet até que você tenha certeza sobre a legitimidade da fonte
* Não se deve mexer com esses arquivos, pois alterá-los ou mexer com eles causa sérios erros de sistema
* Se esses arquivos forem corrompidos por algum vírus ou malware, eles devem ser reinstalados

## Exemplo SYS ##

Veja a seguir um exemplo de um arquivo simples de configuração do sistema SYS:

```
DEVICE=C:\Windows\HIMEM.SYS
DOS=HIGH,UMB
DEVICE=C:\Windows\EMM386.EXE NOEMS
FILES=30
STACKS=0,0
BUFFERS=20
DEVICEHIGH=C:\Windows\COMMAND\ANSI.SYS
DEVICEHIGH=C:\MTMCDAI.SYS /D:123
```
