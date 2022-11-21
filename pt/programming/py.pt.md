---
date: 2019-10-11
keywords: py, python, .py, formato de arquivo py, como abrir arquivo py, como executar arquivos py, como executar arquivos python, como executar python
autor:
  display_name: Muhammad Ahmad Chishti
draft: false
toc: true
title: Formato de arquivo PY
linktitle: PY
description: "Saiba mais sobre o formato de arquivo PY e as APIs que podem criar e abrir arquivos PY."
menu:
  docs:
    parent: "programming"
lastmod: 2020-25-11
---

## O que é um arquivo PY? ##

Os arquivos com a extensão .py contêm o código-fonte do Python. A linguagem Python se tornou uma linguagem muito famosa nos dias de hoje. Ele pode ser usado para scripts de sistema, desenvolvimento de software e web e matemática. Python suporta compatibilidade entre plataformas; significa que os aplicativos desenvolvidos em Python podem funcionar em diferentes plataformas como Windows, MAC, Linux, Raspberry Pi, etc. O Python fornece uma sintaxe simples e de fácil leitura, semelhante à do idioma inglês. Os desenvolvedores podem escrever um aplicativo de software razoável escrevendo algumas linhas de código Python. Como o Python é executado em um sistema interpretador, o código pode ser executado assim que for escrito, o que o torna muito bom para prototipagem.

## Breve história ##

Python foi concebido no final dos anos 80 por Guido van Rossum como um sucessor da linguagem de programação ABC. Sua implementação começou em dezembro de 1989 com Van Rossum como o único desenvolvedor líder. Ele trabalhou em python até 12 de julho de 2018. Em janeiro de 2019, os desenvolvedores do núcleo ativo do Python elegeram um "Conselho Diretor" de cinco membros composto por Nick Coghlan, Brett Cannon, Carol Willing, Barry Warsaw e Van Rossum para liderar o projeto.

### Versões ###

- Python 2.0 foi lançado em 16 de outubro de 2000.
- Python 3.0 foi lançado em 3 de dezembro de 2008.

## Como executar o arquivo py ##

Para verificar a versão do Python instalada, você pode usar o seguinte comando:

```cmd
python --version
```

Isso produzirá a versão no console como

```cmd
Python 3.7.4
```

Se o Python não estiver instalado em sua máquina, você pode acessar [python.org](https://www.python.org/) e baixar e instalar o Python para seu sistema operacional relevante.

Para executar um script Python, você pode usar o seguinte comando:

```cmd
python helloworld.py
```

*helloworld.py* é um arquivo de script que contém o seguinte código

```py
print("Hello World from Python")
```

Isso imprimirá o seguinte na janela do console.

```cmd
Hello World from Python
```

Observação: se você usa IDEs, eles fornecem botões na tela ou atalhos de teclado diferentes para executar o Python. Por exemplo, um botão play é mostrado na sarjeta com o editor no PyCharm que permite executar o script Python.

## Formato de arquivo PY ##

Python foi projetado para facilitar a leitura e tem semelhanças com inglês e matemática. Python usa novas linhas para indicar o comando completo em oposição a ponto e vírgula ou parênteses usados em outras linguagens. Para escopos, loops e funções, o Python conta com recuo e espaços em branco, em oposição às chaves usadas em outras linguagens.

### Sintaxe ###

Veja a seguir um exemplo de sintaxe do Python.

```py
print("Hello World")

#Variables
name = "John"
age = 25
print(name)
print(age)

#While Loop
i = 1
while i < 3:
  print(i)
  i += 1
  
#For Loop
names = ["John", "Harry", "Tom"]
for name in names:
  print(name)
```

## Referências ##

- [Python (linguagem de programação) - Wikipedia](https://en.wikipedia.org/wiki/Python_(programming_language))

