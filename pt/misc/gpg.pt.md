{
  "date" : "2022-02-17",
  "keywords" :["arquivo gpg", "formato de arquivo gpg", "o que é um arquivo gpg", "arquivo", "exemplo gpg", "extensão de arquivo gpg","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Arquivo GPG - Arquivo de chaveiro público do GNU Privacy Guard",
  "description":"Saiba mais sobre arquivos GPG e APIs que podem criar e abrir arquivos GPG.",
  "linktitle" : "GPG",
  "menu" : {
    "docs" : {
      "parent" : "misc"
}
},
  "lastmod" : "2022-02-17"
}

## O que é um arquivo GPG?

Um arquivo GPG é um arquivo de chave de criptografia/descriptografia usado pelo programa de criptografia GNU Privacy Guard (GnuPG). O próprio programa GnuPC é baseado no padrão OpenPGP conforme definido RFC4880 e também é conhecido como PGP. A chave para o uso bem-sucedido do GPG no sistema operacional moderno é seu sistema de gerenciamento de chaves versátil. O utilitário de linha de comando do GPG permite que ele se integre facilmente a outros aplicativos.

## Formato de arquivo GPG

Os arquivos GPG são salvos como arquivos binários criptografados e, claro, não são legíveis por humanos. Para descriptografar um arquivo GPG criptografado, você precisa usar a mesma chave segura. E é por isso que o formato de arquivo interno desses arquivos não é conhecido.

## Criptografar e descriptografar arquivos com GPG no Linux

O utilitário de linha de comando GPG pode ser usado para criptografar e descriptografar arquivos no Linux.

### Criptografando um arquivo

Um arquivo pode ser criptografado usando o comando gpg com a opção -c (criar) conforme mostrado abaixo.

```
gpg -c file1.txt
```
A execução deste comando pede uma frase-chave com a qual criptografar o conteúdo do arquivo original `file1.txt`. Isso resulta na criação do arquivo criptografado file1.txt.gpg.

### Descriptografando e extraindo um arquivo

Para descriptografar e extrair um arquivo criptografado, o comando a seguir pode ser usado.

```
gpg cfile.txt.gpg
```

## Referências

* [GNUPG](https://gnupg.org/)
* [HDF - Wikipedia](https://en.wikipedia.org/wiki/Hierarchical_Data_Format)

