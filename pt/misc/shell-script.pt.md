{
  "date" : "2023-08-07",
  "author" : {
    "display_name" : "Shakeel Faiz"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Shell script - Como executá-lo no Ubuntu e Linux",
  "description":"Aprenda sobre o que é Shell Script e como executá-lo no Ubuntu e Linux",
  "linktitle" : "SHELL SCRIPT",
  "menu" : {
    "docs" : {
      "identifier": "misc-shell-script-pt",
      "parent" : "misc"
}
},
  "lastmod" : "2023-08-07"
}

## O que é ShellScript?

O script Shell envolve escrever uma série de comandos em um arquivo de texto simples, geralmente chamado de **Shell Script**. Esses scripts são executados por um shell, que é um interpretador de linha de comando. As conchas mais comuns incluem

1. Bash (Bourne novamente SHell)
2. Zsh (concha Z)
3. Peixe.

Os scripts de shell podem variar de simples linhas a programas complexos e são usados para executar uma ampla variedade de tarefas, como manipulação de arquivos, administração de sistema e automação de tarefas repetitivas.

## Benefícios do Shell Script:

1.  **Automação:** Shell scripts permitem que os usuários automatizem tarefas repetitivas, economizando tempo e reduzindo a chance de erro humano.
    
2.  **Personalização:** Os usuários podem criar scripts adaptados às suas necessidades específicas, proporcionando um alto grau de personalização.
    
3.  **Processamento em lote:** Os scripts de shell são excelentes para lidar com tarefas de processamento em lote, onde vários comandos precisam ser executados em sequência.
    
4.  **Administração do sistema:** Os scripts de shell são comumente usados para tarefas de administração do sistema, como backups, rotação de logs e instalação de software.

## Escrevendo um script de shell simples:

Vamos criar um script de shell básico que imprima uma mensagem de saudação. Abra um editor de texto e crie um arquivo chamado `greeting.sh`. Adicione as seguintes linhas:

```
#!/bin/bash
# This is a simple shell script

echo "Hello, welcome to the world of shell scripting!"
```

Salve o arquivo e torne-o executável executando o seguinte comando no terminal:

```
chmod +x greeting.sh
```

Agora você pode executar o script:

```
./greeting.sh
```

A saída deve ser:

```
Hello, welcome to the world of shell scripting!
```

## Executando scripts Shell no Ubuntu e Linux:

Agora, discutiremos **como executar um arquivo .sh no Ubuntu e Linux**.

1.  **Tornar o script executável:** Antes de executar um script de shell, certifique-se de que ele seja executável. Use o comando `chmod` conforme mostrado anteriormente.
    
2.  **Navegue até o diretório de script:** Abra um terminal e use o comando `cd` para navegar até o diretório que contém seu script de shell.
    
3.  **Execute o script:** Execute o script digitando `./scriptname.sh` no terminal, substituindo scriptname pelo nome real do seu script.
    
```
cd path/to/script
./greeting.sh
``` 

4.  **Usando o comando Bash:** Se o seu script começar com `#!/bin/bash` (conhecido como **shebang**), você também pode executá-lo usando o comando `bash`.

```
bash greeting.sh
```

## O que significa $@ no Shell Script?

No shell script, `$@` representa todos os argumentos da linha de comando passados para o script. É frequentemente usado para fazer referência a listas de argumentos como entidades separadas. Quando usado entre aspas duplas, como `$@`, preserva argumentos individuais, contabilizando espaços e caracteres especiais.

Aqui está uma breve explicação:

- `$@`: Representa todos os parâmetros posicionais (argumentos) passados para script ou função. Cada argumento é tratado como uma palavra separada.
    
- `$@`: Quando colocado entre aspas duplas, preserva a separação dos argumentos, permitindo espaços ou caracteres especiais dentro de argumentos individuais.
    

Aqui está um exemplo simples para ilustrar:

```
#!/bin/bash

# Save this script as example.sh

echo "The total number of arguments is: $#"
echo "The arguments are: $@"
echo "The arguments with double quotes are: \"$@\""
```

Ao executar este script com argumentos, por exemplo:

```
bash example.sh arg1 "argument 2" arg3
```

A saída seria:

```
The total number of arguments is: 3
The arguments are: arg1 argument 2 arg3
The arguments with double quotes are: "arg1" "argument 2" "arg3"
```

Como você pode ver, `$@` representa todos os argumentos e `$@` preserva os argumentos individuais, mesmo que contenham espaços.

