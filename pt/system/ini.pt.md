{
  "date" : "2021-07-07",
  "keywords" :[ "INI", "extensão", "arquivo", "formato", "sistema", "Iniciação", "extensão de diretório", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"INI - Formato de Arquivo de Iniciação",
  "description":"Saiba mais sobre o formato de arquivo INI e APIs que podem criar e abrir arquivos INI.",
  "linktitle" : "INI",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## O que é um arquivo INI? ##

Um arquivo INI é um documento de configuração de mensagens para programas de computador que contêm chaves públicas para características e seções que organizam os atributos em uma estrutura e gramática. Esses documentos de configuração de formato de arquivo do sistema obtêm seus nomes da extensão de diretório INI do sistema operacional MS-DOS, que significa iniciação. Ele popularizou essa forma de configuração de software. Muitos programas em outros aplicativos de software usam várias adições de nome de arquivo, como CONF e [CFG](/pt/system/cfg/), embora o formato tenha estabelecido um padrão não oficial em muitas situações de configuração.

## Breve História dos Arquivos INI##

Inicialmente, a principal técnica de configuração de programa do Windows era um formato de arquivo de texto que consistia em linhas de texto com um par crucial por linha, dividido em seções. Drivers de dispositivo, tipos de letra e inicializadores de inicialização foram todos armazenados neste formato. As configurações individuais também eram comumente armazenadas em arquivos INI por aplicativos.
Até o Windows 3.1x, o formato era suportado em plataformas Microsoft Windows de 16 bits. A partir do Windows 95, a Microsoft começou a incentivar os desenvolvedores a usar o Registro do Windows em vez de arquivos INI para configuração.

## Arquivo INI - Especificações de formato de arquivo

### Chaves/Propriedades ###

A chave/propriedade é o elemento mais básico de um arquivo INI. Um símbolo de igual (=) separa o nome e o valor de cada chave. À esquerda do sinal de igual é onde o nome é exibido. O símbolo de igual e o ponto e vírgula são letras discretas no sistema Windows, portanto, não podem ser usados na chave. Qualquer caractere pode ser usado no valor.

```
name=value
```

### Seções ###

O comentário da seção aparece entre colchetes ([]) em sua própria linha. Após a definição da seção, todas as chaves são vinculadas a essa seção. As seções terminam na próxima designação de seção ou no final do documento; não há um separador específico de "fim de seção". As seções não podem ser empilhadas; eles só podem ser nomeados uma vez e não precisam ser vinculados.

```
[section]
a=a
b=b
```

### Alterando recursos ###

O formato de arquivo INI não possui uma definição globalmente aceita. Muitos aplicativos de computador incluem funções além das já mencionadas. A lista abaixo inclui algumas características comuns que podem ou não ser incluídas em qualquer programa individual.

* Comentários
* Caracteres de escape
*Nomes duplicados


## Exemplo INI ##

O arquivo INI de exemplo tem a seguinte aparência:

```
[Settings]
 
#======================================================================
 
# Set detailed log for additional debugging info
 
DetailedLog=1
 
RunStatus=1
 
StatusPort=6090
 
StatusRefresh=10
 
Archive=1
 
# Sets the location of the MV_FTP log file
 
LogFile=/opt/ecs/mvuser/MV_IPTel/log/MV_IPTel.log
 
#======================================================================
 
Version=0.9 Build 4 Created July 11 2004 14:00
 
ServerName=Unknown

```

## Referência ##

* [DMP - Microsoft](https://docs.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

