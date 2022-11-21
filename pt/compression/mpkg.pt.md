{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo mpkg", "formato de arquivo mpkg", "o que é um arquivo mpkg", "arquivo", "exemplo mpkg", "extensão de arquivo mpkg", "extensão", "formato" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo MPKG - arquivo de pacote meta",
  "description":"Saiba mais sobre o formato de arquivo MPKG e APIs que podem criar e abrir arquivos MPKG.",
  "linktitle" : "MPKG",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2021-04-02"
}

## O que é um arquivo MPKG?

Um arquivo com extensão .mpkg é um arquivo instalador de arquivo, encontrado principalmente em sistemas operacionais MacOS. Ele contém todos os arquivos de instalação necessários do aplicativo sem a necessidade de manter os arquivos associados separadamente. Um único arquivo MPKG pode conter arquivos de pacote [PKG](/pt/compression/pkg/) como um dos arquivos de instalação, além de outros arquivos. Os arquivos MPKG não podem ser abertos com nenhum software geral e são executados automaticamente no MacOS usando o Apple Installer.

## Formato de arquivo MPKG

Um arquivo MPKG contém diferentes tipos de arquivos necessários para a instalação de vários pacotes que ele contém. Isso pode ser visto na imagem abaixo, que é a estrutura em árvore de um arquivo MPKG de amostra. Esta estrutura de árvore é exportada usando o comando `tree` no terminal MacOS.

{{< figure src="../mpkg.png" alt="Formato de arquivo MPKG" >}}

A descrição dos diferentes elementos na imagem é a seguinte.

`Diretório de Pacotes` - armazena uma lista de arquivos pkg, ou seja, uma lista de sub-Pacotes
`Diretório de recursos` - armazena recursos usados pelo pkg, como recursos e imagens localizadas, documentos Rtf, documentos pdf, etc.
`Distribution.dist file` - Um documento xml contendo informações como subpacotes a serem instalados e scripts de tempo de execução

O arquivo XML de amostra para um arquivo MPKG pode ter a seguinte aparência, dependendo dos subpacotes associados.

```
<?xml version="1.0" encoding="utf-8" standalone="no"?>
<installer-script minSpecVersion="1.000000" authoringTool="com.apple.PackageMaker" authoringToolVersion="3.0.6" authoringToolBuild="201">
    <title>myframework installer</title>
    <options customize="never" allow-external-scripts="no" rootVolumeOnly="false"/>
    <installation-check script="pm_install_check();"/>
    <volume-check script="pm_volume_check();"/>
    <script>function pm_volume_check() {
  if(!(my.target.systemVersion &amp;&amp; /* &gt;= */ system.compareVersions(my.target.systemVersion.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}

function pm_install_check() {
  if(!(/pt/* &gt;= */ system.compareVersions(system.version.ProductVersion, '10.6') &gt;= 0)) {
    my.result.title = 'Failure';
    my.result.message = 'Installation cannot proceed, as not all requirements were met.';
    my.result.type = 'Fatal';
    return false;
  }
  return true;
}
</script>
    <choices-outline>
        <line choice="choice0"/>
    </choices-outline>
    <choice id="choice0" title="app">
        <pkg-ref id="com.macbook.myframeworkInstaller.pkg"/>
    </choice>
    <pkg-ref id="com.macbook.myframeworkInstaller.pkg" installKBytes="108" version="1.0" auth="Root">file:./Contents/Packages/app.pkg</pkg-ref>
</installer-script>
```
`app.pkg` - é o sub-pacote a ser instalado. É um diretório da estrutura Bundle no formato pkg. Ele contém um subdiretório Contents.

## Referências

* [Pacotes Planos OSX](https://matthew-brett.github.io/docosx/flat_packages.html)
* [C++ MPKG Package Manager](https://github.com/puellavulnerata/mpkg)

