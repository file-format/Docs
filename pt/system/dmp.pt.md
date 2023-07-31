{
  "date" : "2021-07-07",
  "keywords" :[ "DMP", "extensão", "arquivo", "formato", "sistema", "MemoryDump", "Minidump", "programas", "computador", "aplicativo" ],
  "author" : {
    "display_name" : "Sami Cheema"
},
  "draft" : "false",
  "toc" : true,
  "title" :"DMP - Formato de arquivo MemoryDump",
  "description":"Saiba mais sobre o formato de arquivo DMP e as APIs que podem criar e abrir arquivos DMP.",
  "linktitle" : "DMP",
  "menu" : {
    "docs" : {
      "parent" : "system"
}
},
  "lastmod" : "2021-07-07"
}

## O que é um arquivo DMP? ##

O arquivo DMP está associado principalmente ao formato de arquivo MemoryDump ou Minidump. Ele é usado no sistema operacional Microsoft Windows para armazenar dados que foram despejados do espaço de memória do computador. Normalmente, os arquivos DMP são criados quando um arquivo falha ou ocorre um erro. Às vezes, os arquivos DMP são muito importantes para especialistas técnicos ou usuários avançados de computador para solucionar os problemas que você está enfrentando e resolver qualquer tipo de problema de aplicativo. Os arquivos DMP são armazenados como um formato proprietário na Microsoft, que é usado pelo sistema operacional para depurar qualquer aplicativo instalado no sistema.


## Especificação técnica do formato de arquivo DMP

No Windows, a ferramenta de sistema "savedump.exe" gera arquivos .dmp que podem ser processados por vários utilitários de depuração disponíveis. O mini dump (64/128 Kb) é armazenado pelo Windows no diretório '%SystemRoot%\Minidump'. Por outro lado, a memória do kernel e os despejos de memória completos são armazenados na raiz do sistema como arquivos 'Memory.dmp'. Os arquivos de despejo de memória são arquivos relativamente grandes, portanto, podem ocupar uma quantidade suficiente de espaço de armazenamento. Portanto, é aconselhável que os arquivos .dmp inúteis que você acha que não serão úteis para solucionar problemas, apague-os.

Você pode excluir arquivos .dmp manualmente ou usando o "assistente de limpeza de disco" padrão em seu computador. As extensões DMP são usadas pelos produtos de banco de dados Oracle para usar os arquivos .dmp em arquivos de banco de dados de backup e recuperação criados e usados. Os arquivos DMP criados pelo Oracle são backups de banco de dados que podem ser usados para importar ou restaurar em uma instância de banco de dados em execução por meio de um servidor de banco de dados. Na maioria dos casos, os arquivos .dmp têm carimbos de data e hora como seus nomes de arquivo.

### Conteúdo do arquivo DMP

Um arquivo de despejo de memória contém:

* A instrução stop e seus parâmetros;
* Uma lista de drivers carregados;
* O contexto do processador (PRCB) para os processos que interromperam a operação normal do Windows;
* O contexto do kernel e informações do processador (EPROCESSES) para os processos que foram interrompidos;
* O contexto do kernel e informações do processador (ETHREAD) para o segmento que parou;
* A pilha de chamadas do modo kernel para o encadeamento que encerrou a execução do processo.


## Exemplo de DMP

O erro de parada 0XC0000218 (Registry_File_Failure) cria um arquivo DMP da seguinte forma:

```
Symbol search path is: srv*
Executable search path is:
Windows XP Kernel Version 2600 (Service Pack 1) UP Free x86 compatible
Product: WinNt, suite: TerminalServer SingleUserTS
Built by: 2600.xpsp2.030422-1633
Kernel base = 0x804d4000 PsLoadedModuleList = 0x80543530
Debug session time: Fri Jun 11 10:22:46 2004
System Uptime: 0 days 0:00:24.187
Loading Kernel Symbols
.................................................
Loading unloaded module list

Loading User Symbols
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Use !analyze -v to get detailed debugging information.

BugCheck C0000218, {e144c418, 0, 0, 0}

Probably caused by : ntoskrnl.exe ( nt!ExRaiseHardError+13c )

Followup: MachineOwner
---------

kd> !analyze -v
*******************************************************************************
* *
* Bugcheck Analysis *
* *
*******************************************************************************

Unknown bugcheck code (c0000218)
Unknown bugcheck description
Arguments:
Arg1: e144c418
Arg2: 00000000
Arg3: 00000000
Arg4: 00000000

Debugging Details:
------------------


BUGCHECK_STR: 0xc0000218

ERROR_CODE: (NTSTATUS) 0xc0000218 - {Registry File Failure} The registry cannot load the hive (file): %hs or its log or alternate. It is corrupt, absent, or not writable.

DEFAULT_BUCKET_ID: DRIVER_FAULT

LAST_CONTROL_TRANSFER: from 8062be87 to 804f4103

STACK_TEXT:
f96f0870 8062be87 0000004c c0000218 f96f09d4 nt!KeBugCheckEx+0x19
f96f0a20 805e9f96 c0000218 00000001 00000001 nt!ExpSystemErrorHandler+0x44c
f96f0bcc 805ea21c c0000218 00000001 00000001 nt!ExpRaiseHardError+0x9a
f96f0c3c 805fb94c c0000218 00000001 00000001 nt!ExRaiseHardError+0x13c
f96f0dac 805aa2b6 00000000 00000000 00000000 nt!CmpLoadHiveThread+0x16a
f96f0ddc 805319c6 805fb7e2 00000001 00000000 nt!PspSystemThreadStartup+0x34
00000000 00000000 00000000 00000000 00000000 nt!KiThreadStartup+0x16


FOLLOWUP_IP:
nt!ExRaiseHardError+13c
805ea21c 837dfc00 cmp dword ptr [ebp-0x4],0x0

SYMBOL_STACK_INDEX: 3

FOLLOWUP_NAME: MachineOwner

SYMBOL_NAME: nt!ExRaiseHardError+13c

MODULE_NAME: nt

IMAGE_NAME: ntoskrnl.exe

DEBUG_FLR_IMAGE_TIMESTAMP: 3ea80977

STACK_COMMAND: kb

BUCKET_ID: 0xc0000218_nt!ExRaiseHardError+13c

Followup: MachineOwner

```

## Referência ##

* [DMP - Microsoft](https://learn.microsoft.com/en-us/troubleshoot/windows-client/performance/read-small-memory-dump-file)

