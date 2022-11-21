{
  "date" : "2021-06-30",
  "keywords" :[ "arquivo msi", "formato de arquivo MSI", "o que é um arquivo msi", "arquivo", "exemplo msi", "extensão de arquivo msi", "extensão", "formato" ],
  "author" : {
    "display_name" : "Muhammad Umar"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo MSI e APIs que podem criar e abrir arquivos MSI.",
  "title" :"MSI - Arquivo de pacote do Windows Installer",
  "linktitle" : "MSI",
  "menu" : {
    "docs" : {
      "parent" : "executable"
}
},
  "lastmod" : "2021-06-30"
}

## O que é um arquivo MSI?
Um arquivo MSI usado para instalar e iniciar programas do Windows; um pacote completo para Microsoft Windows que contém informações de instalação de um programa de software típico, incluindo arquivos essenciais a serem instalados e informações sobre o local de instalação. Os arquivos MSI também podem conter o pacote para atualizações de software. Os arquivos MSI são semelhantes a [EXE](/pt/executable/exe/), mas o EXE às vezes pode não incluir as informações do instalador e o programa de software pode ser executado diretamente ao executar o arquivo EXE.

## Formato de arquivo MSI
O Windows Installer é na verdade uma API (Application Programming Interface) e um componente de software do Microsoft Windows usado para a instalação, remoção e manutenção de um programa de software. As informações de instalação e os arquivos opcionais são empacotados como pacotes de instalação e bancos de dados pouco relacionais estruturados como COM Structured Storages; bem conhecidos como **arquivos MSI**, com a extensão de arquivo .msi. Os pacotes com a extensão de arquivo **.mst** contêm **Transformation Scripts** do Windows Installer, os arquivos com a extensão **.msm** contêm **Merge Modules** e a extensão de arquivo **.pcp** é usado para **Propriedades de Criação de Patch**. O Windows Installer se torna mais avançado depois de sofrer alterações significativas em relação às versões anteriores, a API de instalação. Uma estrutura de GUI e geração automática da sequência de desinstalação são os novos recursos do Windows Installer. Ele foi considerado agora como uma alternativa para estruturas de instalador executáveis autônomos.

### Estrutura lógica dos pacotes MSI
Um pacote designa a instalação de um ou mais produtos completos e geralmente é identificado por um **GUID**. Um produto é composto por um ou vários componentes e agrupado em vários recursos. O Windows Installer não lida com dependências entre vários produtos simultaneamente. A estrutura lógica dos pacotes consiste nos seguintes elementos:

- **Produtos**: Um único programa instalado e em funcionamento ou um conjunto de vários programas combinados é um produto. Um produto é identificado por um GUID exclusivo.
- **Recursos**: Pode conter qualquer número de componentes e outros sub-recursos. Pacotes menores podem consistir em um único recurso.
- **Componentes**: O componente é tratado pelo Windows Installer como uma unidade; pode conter arquivos de programa, pastas, chaves de registro, componentes COM e atalhos.
- **Caminhos de chave**: um caminho de chave é um arquivo específico, fonte de dados ODBC ou chave de registro que o autor do pacote especifica como crítico para um determinado componente.

## Referências

* [Windows Installer - pela Wikipedia](https://en.wikipedia.org/wiki/Windows_Installer)


