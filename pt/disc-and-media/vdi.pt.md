{
  "date" : "2021-08-11",
  "keywords" :[ "arquivo vdi", "formato de arquivo vdi", "o que é um arquivo vdi", "arquivo", "exemplo vdi", "extensão de arquivo vdi", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o formato de arquivo VDI e APIs que podem criar e abrir arquivos VDI.",
  "title" :"VDI - Arquivo de imagem de disco virtual do VirtualBox",
  "linktitle" : "VDI",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2021-08-11"
}

## O que é um arquivo VDI?
Um arquivo com extensão .vdi é uma imagem de disco virtual; específico para o programa de virtualização de desktop de código aberto da Oracle chamado VirtualBox. Os arquivos VDI são usados para iniciar a máquina virtual do VirtualBox. As VMs permitem que os usuários executem sistemas operacionais ou programas adicionais em um único computador. Portanto, o benefício dos arquivos VDI é que os usuários podem salvar esses arquivos de imagem de disco em seu disco rígido e executá-los usando emuladores sempre que precisarem.

## Formato de arquivo VDI
A imagem de disco virtual (VDI) é o formato de arquivo de disco principal para uma VM Oracle de código aberto e ativamente desenvolvida, conhecida como VirtualBox, que é um produto de virtualização de classe empresarial. O formato de arquivo VDI foi projetado para criar uma imagem de disco portátil que pode ser executada facilmente usando outros programas de virtualização. Ele suporta armazenamento alocado dinamicamente e de tamanho fixo. Ele permite expandir um arquivo de imagem depois de criado, mesmo que já contenha dados.

### Virtualização de disco
O sistema emula discos rígidos no formato de imagem de disco VDI. Uma VM do VirtualBox pode usar discos anteriores criados no Microsoft Virtual PC ou VMware, bem como seu próprio formato nativo. O VirtualBox também é capaz de se conectar a destinos iSCSI e particionamento bruto no host, usando como discos rígidos virtuais. O VirtualBox emula IDE (controladores PIIX4 e ICH6), SATA (controlador ICH8M), controladores SAS aos quais os discos rígidos podem ser conectados e SCSI.

O suporte está disponível para Open Virtualization Format (OVF) desde a versão 2.2.0 do VirtualBox. Os dispositivos físicos conectados ao host e as imagens ISO podem ser montados como unidades de CD ou DVD.
Por padrão, o VirtualBox suporta gráficos por meio de uma placa gráfica virtual personalizada compatível com VESA.

### Suporte de virtualização para Ethernet
O VirtualBox virtualiza as seguintes placas de interface de rede para um adaptador de rede Ethernet:
- AMD PCnet PCI II (Am79C970A)
- AMD PCnet-Fast III (Am79C973)
- Desktop Intel Pro/1000 MT (82540EM)
- Servidor Intel Pro/1000 MT (82545EM)
- Servidor Intel Pro/1000 T (82543GC)
- Adaptador de rede paravirtualizado (virtio-net)

As placas de rede emuladas permitem que os SOs convidados sejam executados sem a necessidade de pesquisar e instalar drivers para hardware de rede, pois eles estão disponíveis como parte do SO convidado. Um adaptador de rede paravirtualizado especial melhora o desempenho da rede reduzindo a necessidade de corresponder a uma interface de hardware específica. Portanto, requer suporte de driver especial no convidado.


## Referências

* [VirtualBox - por Wikipedia](https://en.wikipedia.org/wiki/VirtualBox#VirtualBox_Disk_Image)


