{
"data": "07/03/2023",
  "keywords": [
"arquivo reg",
"o que é um arquivo reg",
"arquivo",
"extensão de arquivo reg",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo REG - Arquivo de registro do Windows",
  "description":"Aprenda sobre o formato REG e APIs que podem criar e abrir arquivos REG.",
"linktitle": "REG",
  "menu": {
    "docs": {
      "identifier": "system-reg",
"parent" : "system"
}
},
"último mod": "07/03/2023"
}

## O que é um arquivo .REG?

Um arquivo REG é um formato de arquivo usado para importar ou exportar dados do Registro do Windows. O Registro do Windows é um banco de dados hierárquico que armazena definições e opções de configuração para o sistema operacional Windows e aplicativos instalados. O registro contém informações como preferências do usuário, configurações de aplicativos, dados de configuração de hardware e software e muito mais.

Um arquivo REG normalmente tem uma extensão de arquivo “.reg” e é um arquivo de texto simples que contém uma série de entradas e valores de registro em um formato específico. O formato consiste em uma seção de cabeçalho que identifica o arquivo como um arquivo de registro, seguida por uma série de pares de chave e valor que representam entradas de registro.

## Formato de arquivo REG – Mais informações

Aqui está um exemplo de formato de arquivo reg:

```
[HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows\CurrentVersion\Run]
"Example"="C:\\Example.exe"

[HKEY_CURRENT_USER\Software\Microsoft\Windows\CurrentVersion\Explorer\Advanced]
"Hidden"=dword:00000001
```

A primeira linha do arquivo especifica a versão do editor de registro. As linhas a seguir contêm as entradas do registro no formato de um caminho de chave seguido por um nome de valor e dados de valor. Neste exemplo, o arquivo reg contém duas entradas: uma que adiciona um programa chamado "Example.exe" à lista de inicialização do Windows e outra que define o valor "Oculto" nas configurações avançadas do Windows Explorer como "true".

Os arquivos Reg podem ser criados e editados usando um editor de texto como o Bloco de Notas. Eles são frequentemente usados para fins de backup e restauração, bem como para configurar vários computadores com as mesmas configurações de registro.

## Importar ou exportar registro do Windows

Um arquivo REG é um tipo de arquivo usado para importar ou exportar dados do Registro do Windows. O Registro do Windows é um banco de dados hierárquico que armazena definições e opções de configuração para o sistema operacional Windows e aplicativos instalados. O registro contém informações como preferências do usuário, configurações de aplicativos, dados de configuração de hardware e software e muito mais.

Os arquivos Reg podem ser usados para criar ou modificar entradas de registro e geralmente são usados para fins de backup e restauração, bem como para configurar vários computadores com as mesmas configurações de registro. Veja como usar um arquivo reg para adicionar uma nova entrada de registro ao Registro do Windows:

1. Crie um novo arquivo de texto usando um editor de texto como o Bloco de Notas.
2. Digite a entrada do registro no formato correto. O formato consiste em uma seção de cabeçalho que identifica o arquivo como um arquivo de registro, seguida por uma série de pares de chave e valor que representam entradas de registro. Aqui está um exemplo:

```
Windows Registry Editor Version 5.00

[HKEY_CURRENT_USER\Software\Example]
"Setting1"="Value1"
```

Isso cria uma nova chave chamada "Exemplo" na chave "Software" na seção de registro do usuário atual e define o valor "Configuração1" como "Valor1".

3. Salve o arquivo com uma extensão .reg.
4. Clique duas vezes no arquivo .reg para adicionar a nova entrada de registro ao Registro do Windows.

Você será solicitado a confirmar que deseja adicionar a entrada ao registro. Depois de confirmar, a nova entrada será adicionada ao registro e você poderá verificá-la usando a ferramenta Editor do Registro.

## Referências
* [Registro do Windows](https://en.wikipedia.org/wiki/Windows_Registry)

