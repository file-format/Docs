---
date: 2022-01-31
keywords: stp, .stp, formato de arquivo stp, como abrir arquivos stp, extensão .stp, extensão stp
autor:
  display_name: Kashif Iqbal
draft: false
toc: true
title: Formato de arquivo STP
linktitle: STP
description: "Saiba mais sobre o formato de arquivo STP e APIs que podem criar e abrir arquivos STP."
menu:
  docs:
    parent: "3d"
lastmod: 2022-01-31
---

## O que é um arquivo STP?

Um arquivo STP é um arquivo CAD 3D usado para troca de dados do produto entre aplicativos CAD e CAM. Ele contém informações sobre objetos 3D e é salvo de forma semelhante ao formato de arquivo **STEP**. Os arquivos STP facilitam a troca de dados entre aplicativos de acordo com os protocolos de aplicativo [STEP](/pt/3d/step/) ISO 10303-2xx. Esta ISO define o mecanismo de codificação para representação de dados na linguagem de modelagem de dados EXPRESS. Os arquivos STP podem ser abertos em aplicativos como o **Autodesk Fusion 360**.

## Formato de arquivo STP - Mais informações

Os arquivos STP são salvos em disco no formato de arquivo ASCII simples. Eles contêm informações de modelos 3D como texto simples que pode ser lido por aplicativos CAD/CAM para carregar esses modelos.

Os arquivos STP também são salvos com extensão .step e consistem em uma sequência de registros. Os recursos importantes sobre esses arquivos incluem:

* O conjunto de caracteres é definido como pontos de código da ISO 10646.
* "ISO-10303-21;" são os primeiros caracteres no primeiro registro.
* Os comentários estão entre os caracteres "/*" e "*/".
* O último registro contém "END-ISO-10303-21;" se o arquivo STEP estiver em conformidade com a versão 2002.
* Caso esteja em conformidade com a versão 2016, pode haver uma ou mais assinaturas digitais após o "END-ISO-10303-21;" o Exterminador do Futuro.
* As quebras de linha são indicadas por "\N\" e as quebras de página são indicadas por "\F\".

## Abrir arquivos STP

Os arquivos STP podem ser abertos em Visualizadores STP, bem como Editores de Texto.

### Abrir arquivos STP com visualizadores STP

Vários aplicativos CAD podem abrir arquivos STP para visualização no Windows, MacOS e Linux. Esses incluem:

* Autodesk Fusion 360 (plataforma cruzada)
* FreeCAD (plataforma cruzada)
* IMSI TurboCAD (Windows, Mac)
* Dassault Systems CATIA (Windows, Linux)

### Abrir arquivos STP com editores de texto

Os arquivos STP são salvos como arquivos de texto simples. Isso possibilita abrir arquivos STP com editores de texto. Editores de texto populares, como Notepad e Notepad++ no sistema operacional Windows, e o Apple TextEdit no MacOS podem abrir arquivos STP. Uma vez aberto em um editor de texto, o usuário pode editar as propriedades do arquivo STP. No entanto, pode levar à corrupção do arquivo em caso de atualização incorreta das propriedades.

## Como converter arquivos STP

Existem vários aplicativos que podem converter arquivos STP para outros formatos de arquivo. Os aplicativos CAD que podem converter arquivos STP incluem:

*Autodesk Fusion 360
* IMSI TurboCAD
* Siemens Solid Edge

Além desses, existem vários aplicativos online que podem converter arquivos STP para outros formatos de arquivo. Esses aplicativos online permitem que você carregue seu arquivo STP para servidores em nuvem, onde eles são convertidos para o formato desejado e devolvidos para download.

O Autodesk Fusion 360 pode converter arquivos STP para os seguintes formatos de arquivo 3D e CAD.

* [OBJ](/pt/3d/obj/)
* [3MF](/pt/3d/3mf/)
* [DWG](/pt/cad/dwg/)
* [DXF](/pt/cad/dxf/)
* [ASM](/pt/cad/asm/)
* [IGES](/pt/cad/iges/)
* [STL](/pt/cad/stl/)
* [FBX](/pt/3d/fbx/)
* F3D
* [USD](/pt/3d/usd/)

## Referências

* [ISO 10303-21 - Wikipedia](https://en.wikipedia.org/wiki/ISO_10303-21)
* [Autodesk Fusion 360](https://www.autodesk.com/products/fusion-360/overview)

