{
  "date" : "2024-02-08",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo TIME - O que é arquivo .time? Hora em que o arquivo foi criado no Linux",
  "description" : "Aprenda sobre o arquivo TIME e descubra a hora em que o arquivo foi criado no Linux",
  "linktitle" : "TIME",
  "menu" : {
    "docs" : {
      "identifier" : "data-en-time-pt",
      "parent" : "data"
}
},
  "lastmod" : "2024-02-08"
}

## O que é um arquivo .TIME?

O formato de arquivo TIME foi usado por um sistema web chamado LIGHT, que ajudava os usuários a registrar, organizar e compartilhar suas vidas. Essencialmente, ele armazenava uma coleção de postagens e representava uma pasta na página de vida do usuário dentro do sistema.

## Como descobrir quando um arquivo foi criado no Linux

No Linux, você pode usar o comando `stat` para descobrir quando um arquivo foi criado. Aqui está como você pode fazer isso:

Abra um terminal e digite o seguinte comando:

```
stat <file_path>
```

Substitua `<file_path> ` com o caminho para o arquivo de seu interesse. Por exemplo:

```
stat /path/to/your/file.txt
```

Este comando exibirá várias informações sobre o arquivo, incluindo a hora de criação. Procure a linha que começa com Nascimento” ou Arquivo:”. A hora de Nascimento indica quando o arquivo foi criado no sistema de arquivos.

Aqui está um exemplo de como a saída pode ser:

```
  File: /path/to/your/file.txt
  Size: 1024       	Blocks: 8          IO Block: 4096   regular file
Device: 801h/2049d	Inode: 1643318     Links: 1
Access: (0644/-rw-r--r--)  Uid: ( 1000/   user)   Gid: ( 1000/   user)
Access: 2024-01-31 12:34:56.789012345 +0000
Modify: 2024-01-31 12:34:56.789012345 +0000
Change: 2024-01-31 12:34:56.789012345 +0000
 Birth: 2024-01-31 12:34:56.789012345 +0000
```

Neste exemplo, a hora de Nascimento” indica quando o arquivo foi criado.

