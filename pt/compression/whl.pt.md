{
  "date" : "2022-06-29",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" :"Formato de arquivo WHL - Arquivo de pacote roda Python",
  "description":"Saiba mais sobre o formato de arquivo WHL e APIs que podem criar e abrir arquivos WHL.",
  "linktitle" : "WHL",
  "menu" : {
    "docs" : {
      "parent" : "compression"
}
},
  "lastmod" : "2022-06-29"
}

## O que é um arquivo WHL?

Um arquivo WHL (Wheel) é um arquivo de pacote de distribuição salvo no formato wheel do Python. É uma instalação de formato padrão de distribuições Python e contém todos os arquivos e metadados necessários para a instalação. O arquivo WHL também contém informações sobre as versões e plataformas do Python suportadas por este arquivo wheel. Semelhante a um arquivo de configuração [MSI](/pt/executable/msi/), o formato de arquivo WHL é um formato pronto para instalar que permite executar o pacote de instalação sem compilar a distribuição de origem.

## Formato de arquivo WHL

O formato de arquivo WHL é um arquivo [ZIP](/pt/compression/zip/) (.zip) que contém todos os arquivos de instalação e metadados exigidos pelos instaladores para a instalação de um pacote. Esses arquivos WHL podem ser extraídos usando a opção de descompactação ou aplicativos de software de descompactação padrão, como WinZIP e WinRAR.

### Convenção de nome de arquivo WHL

Um arquivo WHL é nomeado de acordo com a convenção a seguir.

```
{dist}-{version}(-{build})?-{python}-{abi}-{platform}.whl
```

Um exemplo do nome do arquivo WHL é o seguinte.

```
cryptography-2.9.2-cp35-abi3-macosx_10_9_x86_64.whl
```

* `criptografia` é o nome do pacote.
* `2.9.2` é a versão do pacote de criptografia. Uma versão é uma string compatível com PEP 440, como 2.9.2, 3.4 ou 3.9.0.a3.
* `cp35` é a tag Python e denota a implementação e versão do Python que a roda exige.
* `abi3` é a tag ABI. ABI significa interface binária do aplicativo.
* `macosx_10_9_x86_64` é a tag da plataforma, que por acaso é um bocado.

## Referências

* [O que são rodas Python e por que você deve se importar?](https://realpython.com/python-wheels/)
* [Python Wheel](https://pypi.org/project/wheel/)

