{
  "date" : "2019-10-11",
  "keywords": [ "sh file", ".sh file", "extension", "format", "sh file example", "sh file format", "how to run sh file" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"SH - Arquivo de script do shell Bash",
  "description":"Saiba mais sobre o formato de arquivo SH e APIs que podem criar e abrir arquivos SH.",
  "linktitle" : "SH",
  "menu" : {
    "docs" : {
      "parent" : "programming"
}
},
  "lastmod" : "2021-05-21"
}

## O que é um arquivo SH?

Um arquivo com extensão .sh é um arquivo de comandos de linguagem de script que contém um programa de computador a ser executado pelo shell Unix. Ele pode conter uma série de comandos que são executados sequencialmente para realizar operações como processamento de arquivos, execução de programas e outras tarefas semelhantes. Eles são executados a partir da interface de linha de comando pelo usuário ou em lote para realizar várias operações ao mesmo tempo. Arquivos de script podem ser abertos em editores de texto como Notepad, Notepad++, Vim, Apple Terminal e outros aplicativos semelhantes no Windows, MacOS e Linux OS.

## Formato de arquivo SH

Os arquivos SH são escritos em texto simples seguindo a sintaxe definida. Esses arquivos de script suportam:

* `Comentários` - Os comentários começam com um # e são ignorados pelo shell.
* `Atalhos` - Estes podem ser usados para renomear um comando para execução curta e fácil.
* `Batch Jobs` - Vários comandos podem ser executados automaticamente que, de outra forma, precisariam ser inseridos manualmente. Isso elimina a necessidade de esperar que um usuário acione cada estágio da sequência.
* `Generalization` - Usando loops simples, muito mais generalização é alcançada para operações como conversão de imagens de um fromat para outro.

## Exemplo de arquivo SH

```
$ echo '#!/bin/sh' > my-script.sh
$ echo 'echo Hello World' >> my-script.sh
$ cat my-script.sh
#!/bin/sh
echo Hello World
$ chmod 755 my-script.sh
$ ./my-script.sh
Hello World
```
## Como executar o arquivo SH?
Os arquivos SH geralmente rodam no Linux, mesmo no Windows você precisa se conectar com um terminal Linux usando softwares como o Putty para rodar os arquivos sh. A seguir estão as etapas para executar um arquivo SH em um terminal Linux.

1. Abra o terminal Linux e vá para o diretório onde o arquivo SH está localizado.
2. Usando o comando `chmod`, defina a permissão de execução em seu script (se ainda não estiver definido).
3. Execute o script usando um dos seguintes
1. `./filename.sh`
2. `sh filename.sh`
3. `bash script-name-aqui.sh`

## Referências

* [Bashscripting for Beginners](https://help.ubuntu.com/community/Beginners/BashScripting)
* [Shellscript](https://www.shellscript.sh/)

