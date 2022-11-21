{
  "date" : "2021-08-27",
  "keywords" :[ "arquivo wsh", "formato de arquivo wsh", "o que é um arquivo wsh", "arquivo", "exemplo wsh", "extensão de arquivo wsh","extensão", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo WSH e APIs que podem criar e abrir arquivos WSH.",
  "title" :"WSH - Arquivo de script do Windows",
  "linktitle" : "WSH",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-27"
}

## O que é um arquivo WSH?
Um arquivo com extensão .wsh contém propriedades e parâmetros para um determinado script de linguagem de programação como VB ou VBS etc. A real necessidade do WSH é utilizá-los para customizar a execução de determinados scripts. WScript ou CScript são necessários para serem executados e ambos estão incluídos no sistema operacional Windows. Os arquivos WSH foram inicialmente fornecidos no Windows 95 nos discos de instalação como um opcional configurável e instalável para o Painel de Controle e, em seguida, um componente padrão do Windows 98.

## Formato de arquivo WSH
WSH (Windows Script Host) pode ser usado para diversos fins, incluindo administração, scripts de logon e automação geral. O WSH estabelece um ambiente para a execução de scripts. ele invoca o mecanismo de script adequado e aloca um conjunto de serviços e objetos para o script trabalhar. Esses scripts podem ser executados em modo GUI, a partir de um objeto COM ou modo de linha de comando, proporcionando flexibilidade ao usuário para scripts interativos ou não interativos.

### Exemplos
Aqui está um exemplo muito simples que mostra algum VBScript que usa o objeto raiz WSH COM "WScript" para exibir uma mensagem com um botão 'OK'. Quando esse script for iniciado, o mecanismo CScript ou WScript será chamado e o ambiente de tempo de execução será estabelecido.

```
WScript.Echo "Hello world"
WScript.Quit
```


## Referências

* [Windows Script Host - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Script_Host)



