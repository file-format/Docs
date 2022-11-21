{
  "date" : "2022-06-23",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo PET - Arquivo de pacote de instalação do Puppy Linux",
  "description":"Saiba mais sobre o formato de arquivo PET e APIs que podem criar e abrir arquivos PET.",
  "linktitle" : "PET",
  "menu" : {
    "docs" : {
      "identifier":"compression-pet",
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-23"
}

## O que é um arquivo PET do Linux?

Um arquivo PET é um arquivo de pacote de instalação de aplicativo criado e usado com a variante PuppyLinux do sistema operacional Linux. Ele é criado como um arquivo compactado [TGZ](/pt/compression/tgz/) que reduz o tamanho do arquivo compactado. A integridade do formato de arquivo PET é garantida pela soma de verificação md5sum que é anexada ao final do arquivo para verificação na extremidade remota. Os arquivos PET podem ser extraídos usando o extrator de arquivos padrão TGZ e o WinRAR. Os arquivos PET substituíram os antigos arquivos de instalação do pacote [PUP](/pt/compression/pup/).

## Formato de arquivo PET

Os arquivos PET são salvos em disco como arquivos compactados em formato de arquivo binário. No entanto, os detalhes do formato de arquivo interno do formato de arquivo PET não são conhecidos. Semelhante aos arquivos de instalação do pacote [.exe](/pt/executable/exe/) e [.msi](/pt/executable/msi/), os arquivos PET iniciam uma instalação quando são executados.

## Referências

* [PuppyLinux](https://en.wikipedia.org/wiki/Puppy_Linux)
* [Índice de pacotes PET do PuppyLinux](https://distro.ibiblio.org/puppylinux/pet-packages-lucid/)

