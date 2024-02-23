{
  "date" : "2022-12-19",
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "title" : "Arquivo MPK - Formato de arquivo do pacote ArcGIS Map",
  "description":"Aprenda sobre o formato de arquivo MPK e APIs que podem criar e abrir arquivos MPK.",
  "linktitle" : "MPK",
  "menu" : {
    "docs" : {
      "identifier":"gis-mpk-pt",
      "parent" : "gis"
}
},
  "lastmod" : "2022-12-19"
}

## O que é um arquivo .MPK?

Um arquivo MPK é um arquivo de pacote ArcGIS Map criado com ArcGIS. Ele contém um documento de mapa .mxd e dados relacionados. Além disso, contém informações adicionais, como camadas referenciadas, símbolos e outros recursos. O arquivo MPK é usado para compartilhar mapas e dados com outros usuários. Isso elimina a disponibilidade de terceiros que tenham a fonte de dados original e também ajuda a distribuir mapas para serem usados em um dispositivo móvel.

## Formato de arquivo MPX

Os detalhes do formato de arquivo interno dos arquivos MPX não estão disponíveis publicamente para referência do desenvolvedor.

### Criar arquivo MPK usando ArcGIS

Arquivos MPK podem ser criados usando ArcGIS. A opção Compartilhar como no menu Pacote de mapas pode ser usada para criar um arquivo .mpk que contém o documento do mapa e todos os seus dados e recursos referenciados. Este arquivo MPK pode então ser compartilhado com outras pessoas e pode ser aberto no ArcMap e ArcGIS Pro para visualizar o mapa e os dados.

### Criar arquivo MPK usando Python

```
import arcpy
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing_12"
arcpy.PackageMap_management('Exercise1_12.mxd', 'EditingExercise1_12.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```
### Usando Python para criar pacotes de mapas para todos os documentos de mapas em uma pasta

O código Python a seguir localiza e cria pacotes de mapas para todos os documentos de mapas que residem em uma pasta especificada.

```
# Name: PackageMap.py
# Description:  Find all the map documents that reside in a specified folder and create map packages for each map document.

# import system modules
import os
import arcpy

# Set environment settings
arcpy.env.overwriteOutput = True
arcpy.env.workspace = "C:/arcgis/ArcTutor/Editing"

# Loop through the workspace, find all the mxds and create a map package using the same name as the mxd
for mxd in arcpy.ListFiles("*.mxd"):
    print ("Packaging: {0}".format(mxd))
    arcpy.PackageMap_management(mxd, os.path.splitext(mxd)[0] + '.mpk', "PRESERVE", "CONVERT_ARCSDE", "#", "ALL")
```

## Referências

* [Mapa de pacote](https://desktop.arcgis.com/en/arcmap/10.3/tools/data-management-toolbox/package-map.htm)


