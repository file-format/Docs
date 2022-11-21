{
  "date" : "2021-06-24",
  "keywords" :[ "arquivo bat", "o que é um arquivo bat", "arquivo", "exemplo de arquivo bat", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo BAT e APIs que podem criar e abrir arquivos BAT.",
  "title" :"BAT - Formato de arquivo em lote",
  "linktitle" : "BAT",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-24"
}

## O que é um arquivo BAT?
Um arquivo BAT é conhecido como um arquivo de lote executado com DOS e todas as versões do Windows, em cmd.exe. Ele consiste em uma série de comandos de linha em texto simples a serem executados pelo interpretador de linha de comando para realizar diferentes tarefas, como executar utilitários de manutenção no Windows ou iniciar programas típicos. Um arquivo de lote pode incluir qualquer comando que possa ser aceito pelo interpretador interativamente e usar a estrutura de código que permite ramificações e loops condicionais conforme escrito no arquivo de lote.
## Formato de arquivo BAT
Um formato de arquivo BAT é simplesmente um script incorporado para automatizar sequências de comandos que são repetitivas por natureza. O termo "lote" é usado para processamento em lote, pode ser considerado como "execução não interativa". Portanto, um arquivo em lote pode não processar um lote de vários dados. No antigo sistema operacional de disco (DOS), o arquivo em lotes era executado na interface de linha de comando digitando o nome do arquivo e a extensão .bat. O sistema operacional anterior baseado na interface gráfica da Microsoft, como o Microsoft Windows, dependia do DOS. Os usuários tinham que usar o DOS para realizar operações típicas como reparar, otimizar ou reinstalar o Windows. Mais tarde, a Microsoft introduziu o Windows NT, que não dependia do sistema operacional DOS. Portanto, os arquivos em lote podem ser executados usando o Prompt de Comando ou **cmd.exe** nos sistemas operacionais modernos da Microsoft.
### Parâmetros do arquivo em lote
O prompt de comando oferece suporte a várias variáveis especiais, como **%0, %1 a %9** para fazer referência ao nome e caminho do trabalho em lotes e aos nove parâmetros de chamada de dentro do trabalho em lotes. Parâmetros inexistentes são substituídos por uma string com comprimento zero. Embora, elas possam ser usadas de forma semelhante às variáveis de ambiente, mas não são salvas no ambiente. Microsoft e IBM referem-se a essas variáveis como parâmetros de substituição, enquanto Novell, Digital Research e Caldera introduziram o termo variáveis de substituição para elas.

Aqui estão alguns comandos úteis de arquivo em lote:
| Comando | Descrição |
------|------------|
| VER | Este comando em lote mostra a versão do MS-DOS que você está usando. |
|ASSOC| Este é um comando em lote que associa uma extensão a um tipo de arquivo (FTYPE), exibe associações existentes ou exclui uma associação. |
|CD| Este comando em lote ajuda a fazer alterações em um diretório diferente ou exibe o diretório atual. |
|CLS| Este comando em lote limpa a tela. |
|CÓPIA| Este comando em lote é usado para copiar arquivos de um local para outro. |
|EXCLUIR| Este comando em lote exclui arquivos e não diretórios. |
|DIR| Este comando em lote lista o conteúdo de um diretório. |
|DATA| Este comando em lote ajuda a encontrar a data do sistema. |
|ECO| Este comando em lote exibe mensagens ou ativa ou desativa o eco do comando. |
|SAÍDA| Este comando em lote sai do console do DOS. |
|MD| Este comando em lote cria um novo diretório no local atual. |
|MOVER| Este comando em lote move arquivos ou diretórios entre diretórios. |
|CAMINHO| Este comando em lote exibe ou define a variável de caminho. |
|PAUSA| Esse comando em lote avisa o usuário e aguarda a entrada de uma linha de entrada. |
|PROMPT| Esse comando em lote pode ser usado para alterar ou redefinir o prompt cmd.exe. |
|RD| Este comando em lote remove diretórios, mas os diretórios precisam estar vazios antes de serem removidos. |
|REN| Renomeia arquivos e diretórios |
|REM| Este comando batch é usado para comentários em arquivos batch, evitando que o conteúdo do comentário seja executado. |
|INICIAR| Este comando em lote inicia um programa em uma nova janela ou abre um documento. |
|HORA| Este comando em lote define ou exibe a hora. |
|TIPO| Este comando em lote imprime o conteúdo de um arquivo ou arquivos na saída. |
|VOL| Este comando em lote exibe os rótulos de volume. |
|ATTRIB| Exibe ou define os atributos dos arquivos no diretório curret |
|CHKDSK| Este comando em lote verifica se há problemas no disco. |
|ESCOLHA| Este comando em lote fornece uma lista de opções ao usuário. |
|CMD| Este comando em lote invoca outra instância do prompt de comando. |
|COMP| Este comando em lote compara 2 arquivos com base no tamanho do arquivo. |
|CONVERTER| Este comando em lote converte um volume do sistema de arquivos FAT16 ou FAT32 para o sistema de arquivos NTFS. |
|DRIVERQUERY| Este comando em lote mostra todos os drivers de dispositivo instalados e suas propriedades. |
| EXPANDIR| Este comando em lote extrai arquivos de arquivos de gabinete .cab compactados. |
|encontrar| Este comando em lote procura uma string em arquivos ou entrada, gerando linhas correspondentes. |
|FORMATO| Este comando em lote formata um disco para usar o sistema de arquivos suportado pelo Windows, como FAT, FAT32 ou NTFS, substituindo assim o conteúdo anterior do disco. |
|AJUDA| Este comando em lote mostra a lista de comandos fornecidos pelo Windows. |
|IPCONFIG| Este comando em lote exibe a configuração de IP do Windows. Mostra a configuração por conexão e o nome dessa conexão. |
|ETIQUETA| Este comando em lote adiciona, define ou remove um rótulo de disco. |
|MAIS| Este comando em lote exibe o conteúdo de um arquivo ou arquivos, uma tela por vez. |
|NET| Fornece vários serviços de rede, dependendo do comando usado. |
|PING| Este comando em lote envia pacotes de "eco" ICMP/IP pela rede para o endereço designado. |
|DESLIGAMENTO| Esse comando em lote desliga um computador ou faz logoff do usuário atual. |
|ORDENAR| Esse comando em lote recebe a entrada de um arquivo de origem e classifica seu conteúdo em ordem alfabética, de A a Z ou de Z a A. Ele imprime a saída no console. |
|SUBST| Este comando em lote atribui uma letra de unidade a uma pasta local, exibe as atribuições atuais ou remove uma atribuição. |
|SYSTEMINFO| Este comando em lote mostra a configuração de um computador e seu sistema operacional. |
|TASKKILL| Este comando em lote finaliza uma ou mais tarefas. |
|LISTA DE TAREFAS| Este comando em lote lista as tarefas, incluindo o nome da tarefa e o ID do processo (PID). |
|XCOPIA| Este comando em lote copia arquivos e diretórios de uma maneira mais avançada. |
|ÁRVORE| Este comando em lote exibe uma árvore de todos os subdiretórios do diretório atual para qualquer nível de recursão ou profundidade. |
|FC |Este comando em lote lista as diferenças reais entre dois arquivos. |
|DISKPART |Este comando batch mostra e configura as propriedades das partições de disco. |
|TITLE |Este comando em lote define o título exibido na janela do console. |
|CONFIGURAR | Exibe a lista de variáveis de ambiente no sistema atual. |

## Exemplo de arquivo BAT
Os scripts em lote geralmente são salvos como arquivos de texto simples; contendo comandos que são executados em uma sequência. Esses arquivos são salvos com extensão .bat; reconhecido e executado usando o software **Command Interpreter**. Este software está disponível nativamente no Microsoft Windows com o nome **cmd.exe**.

Aqui está um exemplo de script em lote que exclui todos os arquivos no diretório atual:
```
:: Deletes All files in the Current Directory With Prompts and Warnings
::(Hidden, System, and Read-Only Files are Not Affected)
:: @ECHO OFF
DEL . DR
```


## Referências

* [Script de lote - Guia rápido](https://www.tutorialspoint.com/batch_script/batch_script_quick_guide.htm)
* [Arquivo de lote - por Wikipewdia](https://en.wikipedia.org/wiki/Batch_file)

