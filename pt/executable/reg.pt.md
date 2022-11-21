{
  "date" : "2021-08-02",
  "keywords" :[ "arquivo reg", "formato de arquivo reg", "o que é um arquivo reg", "arquivo", "exemplo reg", "extensão de arquivo reg","extensão", "formato"],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo REG e APIs que podem criar e abrir arquivos REG.",
  "title" :"REG - Arquivo de Registro do Windows",
  "linktitle" : "REG",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-08-02"
}

## O que é um arquivo REG?
Um arquivo REG é simplesmente um arquivo de texto com a extensão .reg. Esses arquivos geralmente são criados exportando chaves típicas do Registro. Esses arquivos também podem ser usados como backup do registro (especialmente esta etapa é importante antes de fazer alterações!). Você pode ver que alguns os disponibilizaram como arquivos para download nos mesmos sites que mostram como executar um hack do Registro. Um arquivo REG é útil para fazer alterações manuais no Registro e exportar essas alterações. Basta limpar um pouco o arquivo e compartilhá-lo com outras pessoas.

## Formato de arquivo REG
O formato de arquivo REG foi projetado para exportar e importar partes do registro do Windows usando uma sintaxe baseada em INI. O Registro do Windows é um banco de dados relacional ou hierárquico que mantém as configurações de baixo nível para o sistema operacional Microsoft Windows e outros aplicativos que usam o registro do Windows. Alternativley, podemos dizer, o registro ou Registro do Windows consiste em informações, opções, configurações e outros valores para programas e hardwares instalados em todas as versões dos sistemas operacionais Microsoft Windows.
### Sintaxe do arquivo REG
Aqui estão alguns elementos-chave como parte de uma sintaxe de arquivo REG:
- **RegistryEditorVersion**: Por exemplo, "Windows Registry Editor Version 5.00" para Windows 2000, Windows XP e Windows Server 2003.
- **Linha em branco**: Identifica o início de um novo caminho de registro.
- **RegistryPathx**: O caminho da subchave que contém o primeiro valor que você está importando.
- **DataItemNamex**: o nome do item de dados que você deseja importar.
- **DataTypex**: O tipo de dados para o valor do Registro.

As chaves são armazenadas em arquivos .reg usando a seguinte sintaxe:
```
[<Hive name>\<Key name>\<Subkey name>]
"Value name"=<Value type>:<Value data>
```
Você pode editar o valor padrão de uma chave usando "@" em vez de "Nome do valor":
```
[<Hive name>\<Key name>\<Subkey name>]
@=<Value type>:<Value data>
```
### Exemplo
Aqui está um exemplo de arquivo REG
```
Windows Registry Editor Version 5.00

[HKEY_LOCAL_MACHINE\SOFTWARE\Foobar]
"Value A"="<String value data with escape characters>"
"Value B"=hex:<Binary data (as comma-delimited list of hexadecimal values)>
"Value C"=dword:<DWORD value integer>
"Value D"=hex(0):<REG_NONE (as comma-delimited list of hexadecimal values)>
"Value E"=hex(1):<REG_SZ (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value F"=hex(2):<Expandable string value data (as comma-delimited list of hexadecimal values representing a UTF-16LE NUL-terminated string)>
"Value G"=hex(3):<Binary data (as comma-delimited list of hexadecimal values)> ; equal to "Value B"
"Value H"=hex(4):<DWORD value (as comma-delimited list of 4 hexadecimal values, in little endian byte order)>
"Value I"=hex(5):<DWORD value (as comma-delimited list of 4 hexadecimal values, in big endian byte order)>
"Value J"=hex(7):<Multi-string value data (as comma-delimited list of hexadecimal values representing UTF-16LE NUL-terminated strings)>
"Value K"=hex(8):<REG_RESOURCE_LIST (as comma-delimited list of hexadecimal values)>
"Value L"=hex(a):<REG_RESOURCE_REQUIREMENTS_LIST (as comma-delimited list of hexadecimal values)>
"Value M"=hex(b):<QWORD value (as comma-delimited list of 8 hexadecimal values, in little endian byte order)>
```

## Referências

* [Registro do Windows - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Registry)
* [Como adicionar, modificar ou excluir subchaves e valores do registro usando um arquivo .reg](https://support.microsoft.com/en-us/topic/how-to-add-modify-or-delete- Registry-subkeys-and-values-by-using-a-reg-file-9c7f37cf-a5e9-e1cd-c4fa-2a26218a1a23)


