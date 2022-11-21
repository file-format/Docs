{
  "date" : "2021-08-10",
  "keywords" :[ "arquivo .ova", "formato de arquivo", "o que é um arquivo .ova", "arquivo", "extensão de arquivo"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
   "toc" : true,
  "description" :"Saiba mais sobre o que é um formato de arquivo .ova e APIs que podem criar e abrir arquivos ova.",
  "title" :"Formato de arquivo OVA - Abrir arquivo de dispositivo virtual",
  "linktitle" : "OVA",
  "menu" : {
    "docs" : {
      "parent" : "disc-and-media"
}
},
  "lastmod" : "2022-01-03"
}

## O que é um arquivo OVA?

Um arquivo OVA (Open Virtual Appliance) é um diretório OVF salvo como um arquivo usando o formato de arquivamento .tar. É um arquivo de pacote de dispositivo virtual que contém arquivos para distribuição de software executado em uma máquina virtual. Um pacote OVA contém um arquivo descritor [.ovf](/pt/disc-and-media/ovf/), arquivos de certificado, um arquivo opcional [.mf](/pt/programming/mf/) junto com outros arquivos relacionados. Os arquivos OVA têm o tipo de mídia como application/ovf.

## Formato de arquivo OVA

Conforme mencionado, um arquivo OVA é um arquivo que é criado usando o diretório OVF no formato de arquivo TAR. O arquivo em si é salvo como um arquivo binário. A maioria das plataformas de virtualização, como VMware, Microsoft, Oracle e Citrix, pode instalar dispositivos virtuais a partir de um arquivo OVF que é um arquivo descritor com os detalhes da imagem a ser carregada na máquina virtual.

## Vantagens de um arquivo OVA

* Os arquivos OVA são compactados, permitindo downloads mais rápidos.
* O vSphere Client valida um arquivo OVA antes de importá-lo e garante que ele seja compatível com o servidor de destino pretendido. Se o appliance for incompatível com o host selecionado, ele não poderá ser importado e uma mensagem de erro será exibida.
* OVA pode encapsular aplicativos multicamadas e mais de uma máquina virtual.

## Referências

* [Formatos e modelos de arquivo OVA](https://docs.vmware.com/en/VMware-vSphere/7.0/com.vmware.vsphere.vm_admin.doc/GUID-AE61948B-C2EE-436E-BAFB-3C7209088552.html )
* [Especificações de formato de arquivo OVF](https://products.conholdate.app/viewer/view/3XKCLQbwAw/open-virtualization-format-specification-dsp0243_1-1-0.pdf)

