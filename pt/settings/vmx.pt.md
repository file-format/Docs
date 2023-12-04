{
"data": "08/06/2023",
  "keywords": [
"arquivo vmx",
"o que é um arquivo vmx",
"exemplo de arquivo vmx",
"como abrir arquivo vmx",
"o que contém o arquivo vmx",
"qual é o formato do arquivo vmx",
"arquivo",
"extensão de arquivo vmx",
"extensão"
],
  "author": {
"display_name": "Shakeel Faiz"
},
"draft": "false",
"toc": true,
"title": "Formato de arquivo VMX - Arquivo de configuração de máquina virtual VMware",
  "description":"Aprenda sobre o formato VMX e APIs que podem criar e abrir arquivos VMX.",
"linktitle": "VMX",
  "menu": {
    "docs": {
      "identifier": "settings-vmx",
"parent" : "settings"
}
},
"último mod": "08/06/2023"
}

## O que é um arquivo .VMX?

Um arquivo VMX, também conhecido como arquivo de configuração de máquina virtual, é um arquivo de texto simples usado pelo software de virtualização VMware para definir configurações e configurações da máquina virtual (VM). Os arquivos VMX contêm informações como configuração de hardware da VM, mapeamentos de disco virtual, configurações de rede e outros parâmetros.

## Exemplo de arquivo VMX

Aqui está um exemplo da aparência de um arquivo VMX:

```
# version for configuration
config.version = "8"
# version for virtual machine (Regular version is 4)
virtualHW.version = "7"
# enable vnc
RemoteDisplay.vnc.enabled = "TRUE"
RemoteDisplay.vnc.port = "5900"
VMware, Inc. 3

# type of guest os
guestOS = "linux"
# display name for the VI Client/WebCenter
displayName = "RHEL3"
# scsi controller 0
scsi0.present = "true"
scsi0.virtualDev = "lsilogic"
# scsi hard drive
scsi0:0.present = "true"
scsi0:0.fileName = "/volumes/your-path/passthru.vmdk"
scsi0:0.deviceType = "scsi-hardDisk"
scsi0:0.redo = ""
# IDE CD drive
ide0:0.present ="true"
ide0:0.startConnected = "TRUE"
ide0:0.fileName = "/volumes/your-path/your-iso-image"
ide0:0.deviceType = "cdrom-image"
memsize = "512"
sched.mem.max = "512"
sched.mem.minsize = "512"
sched.swap.derivedName = "/volumes/your-path/passthru-12345.vswp"
svga.vramSize = "16777216"
```

## O que o arquivo VMX contém?

Um arquivo VMX contém várias definições de configuração para máquina virtual (VM). Aqui estão algumas das configurações comumente encontradas no arquivo VMX:

- `.encoding:` Especifica a codificação de caracteres usada no arquivo.
- `config.version:` Indica a versão do formato de arquivo VMX.
- `virtualHW.version:` Especifica a versão do hardware virtual para a VM.
- `guestOS:` Especifica o sistema operacional convidado instalado na VM.
- `memSize:` Define a quantidade de memória alocada para a VM.
- `displayName:` Define o nome de exibição ou rótulo da VM.
- `powerType:` Define o comportamento de energia para diferentes operações (desligar, ligar, reiniciar, suspender).
- `floppyX:` Definições de configuração relacionadas a unidades de disquete, como presença e mapeamentos de arquivos.
- `numvcpus:` Especifica o número de CPUs virtuais atribuídas à VM.
- `scsiX:` Definições de configuração para controladores SCSI e seus discos virtuais associados.
- `ethernetX:` Definições de configuração para adaptadores de rede, incluindo o tipo de dispositivo virtual, nome da rede e tipo de endereço.
- `ideX:` Definições de configuração para controladores IDE e seus discos virtuais associados.
- `usbX:` Definições de configuração para dispositivos USB, como presença e detalhes de conexão.
- `sound:` Definições de configuração para o adaptador de som virtual.
- `tools.syncTime:` Indica se a sincronização de horário com o sistema host está habilitada.
- `uuid.bios:` Especifica o UUID do BIOS da VM.
- `uuid.location:` Especifica o UUID de localização da VM.

## Como abrir o arquivo VMX?

Abrir um arquivo VMX manualmente não é recomendado. Quando você executa uma máquina virtual usando VMware Fusion, o software carrega automaticamente as informações do arquivo VMX.

No entanto, se quiser editar manualmente o arquivo VMX, você pode fazer isso usando qualquer editor de texto, por exemplo, Bloco de Notas (Windows) ou TextEdit (Mac).

## Qual é o formato do arquivo VMX?

Um arquivo VMX é um arquivo de texto simples com formato específico. O formato segue uma estrutura de par chave-valor onde cada linha representa uma opção de configuração separada.

O formato geral do arquivo VMX é o seguinte:

```
key1 = value1
key2 = value2
key3 = value3
```

Cada linha consiste em uma chave seguida do sinal de igual (=) e do valor correspondente. A chave representa uma definição de configuração específica e o valor representa o valor atribuído a essa configuração.

Por exemplo, `memSize = "8192"` no arquivo VMX especifica que o limite de memória da máquina virtual é 8192 MB de RAM.

O formato do arquivo VMX também pode incluir comentários, indicados por um sinal de cerquilha (#) no início da linha, que são ignorados pelo software VMware ao analisar o arquivo. Os comentários são frequentemente usados para fornecer informações adicionais ou explicações para configurações específicas.

## Referências
* [Exemplo de arquivo VMX](https://www.vmware.com/pdf/vsp_4_vmdirectpath_host.pdf)




