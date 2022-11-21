{
  "date" : "2022-04-25",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo AHK e APIs que podem criar e abrir arquivos AHK.",
  "title" :"Formato de arquivo AHK - arquivo de script AutoHotkey",
  "linktitle" : "AHK",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2022-04-25"
}

## O que é um arquivo AHK?

Um arquivo AHK é um arquivo de script gerado com o aplicativo de software AutoHotkey que é usado para automação de tarefas no Microsoft Windows. Ele contém instruções para automação de tarefas usando teclas de atalho que podem ser usadas para realizar ações instantâneas. O arquivo é executado pelo AutoHotkey e todas as ações são executadas sequencialmente. Os arquivos AHK são poderosos o suficiente para realizar tarefas complexas usando as teclas de atalho definidas usando as teclas de atalho. Os arquivos AHK podem ser abertos com editores de texto como Microsoft Notepad e Notepad++.

## Formato de arquivo AHK

Os arquivos AHK são salvos em disco como arquivos de texto simples e contêm linhas de código que podem ser executadas pelo AutoHotkey. O AutoHotkey é uma linguagem de script gratuita e de código aberto e permite que os usuários criem scripts simples a complexos para executar ações como preenchimento de formulários, cliques automáticos, execução de macros etc. Um arquivo AHK no mínimo pode executar uma única ação e depois sair .

Existem ferramentas disponíveis que podem ser usadas para converter arquivos AHK para [Exe](/pt/executable/exe/).

### Exemplo AHK

O exemplo a seguir usa a tecla Win+Z para executar o Bloco de Notas da Microsoft ou trazê-lo para frente se já estiver em execução.

```
#z::Run https://www.autohotkey.com  ; Win+Z

^!n::  ; Ctrl+Alt+N
if WinExist("Untitled - Notepad")
    WinActivate
else
    Run Notepad
return
```

## Como crio um arquivo AHK?

As etapas a seguir podem ser usadas para criar um arquivo AHK. Eles assumem que o AutoHotkey já está instalado na máquina.

* Clique com o botão direito do mouse na área de trabalho.
* Encontre "Novo" no menu.
* Clique em "Script AutoHotkey" dentro do menu "Novo".
* Dê um novo nome ao script.
* Encontre o arquivo recém-criado em sua área de trabalho e clique com o botão direito nele.
* Clique em "Editar script".
* Uma janela deve ter aparecido, provavelmente o Bloco de Notas.
* Salve o arquivo.

## Referências

* [AutoHotkey](https://www.autohotkey.com/)
* [Arquivo de lote - por Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

