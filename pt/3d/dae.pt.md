{
  "date" : "2019-10-11",
  "keywords" :[ "arquivo dae", "formato de arquivo dae", "o que é um arquivo dae", "arquivo", "exemplo dae", "extensão de arquivo dae","extensão", "formato"],
  "author" : {
    "display_name" : "Kashif Iqbal"
},
  "draft" : "false",
  "toc" : true,
  "description":"Saiba mais sobre o formato de arquivo DAE e APIs que podem abrir e criar arquivos DAE.",
  "title" :"DAE - Formato de arquivo de troca de ativos digitais",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
}
},
  "lastmod" : "2019-09-10"
}

## O que é um arquivo DAE?

Um arquivo DAE é um formato de arquivo Digital Asset Exchange usado para trocar dados entre aplicativos 3D interativos. Este formato de arquivo é baseado no esquema XML COLLADA (COLLAborative Design Activity), que é um esquema XML de padrão aberto para a troca de ativos digitais entre aplicativos de software gráfico. Foi adotado pela ISO como uma especificação publicamente disponível, ISO/pAS 17506. Os arquivos DAE podem ser abertos em aplicativos como Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD e APIs como [Aspose.CAD](https://products .aspose.com/cad).

## Formato de arquivo DAE

O formato do arquivo DAE é baseado no [esquema COLLADA XML](https://www.khronos.org/files/collada_spec_1_5.pdf) onde todos os elementos são definidos como tags XML. Ele permite vincular diversas ferramentas de processamento DCC e 3D em um pipeline de produção para ativos 3D. Possui codificação abrangente de cenas visuais, incluindo geometria, animação, shaders e física. O formato é aberto, de nível de arquivo e retém informações meta.

### Etiquetas COLLADA

A tag do esquema COLLADA é mostrada abaixo.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Etiqueta de recurso

A etiqueta de recurso descreve o autor e o ambiente do arquivo

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Biblioteca de câmeras

Os ativos COLLADA estão contidos em bibliotecas. A biblioteca de câmeras contém, sem surpresa, câmeras. As câmeras comuns são perspectiva ou ortográfica. A tag da biblioteca de câmeras é definida como segue.
```
<library_cameras>
    <camera id="PerspCamera" name="PerspCamera">
      <optics>
        <technique_common>
          <perspective>
            <yfov>37.8493</yfov>
            <aspect_ratio>1</aspect_ratio>
            <znear>10</znear>
            <zfar>1000</zfar>
          </perspective>
        </technique_common>
      </optics>
    </camera>
</library_cameras>
```
### Luzes

As luzes comuns são pontuais, pontuais ou direcionais
```
<library_lights>
    </light>
    <light id="pointLightShape1-lib" name="pointLightShape1">
      <technique_common>
        <point>
          <color>1 1 1 </color>
          <constant_attenuation>1</constant_attenuation>
          <linear_attenuation>0</linear_attenuation>
          <quadratic_attenuation>0</quadratic_attenuation>
        </point>
      </technique_common>
    </light>
</library_lights>
```

### Instância de materiais

Os efeitos de instância de Materiais são definidos a seguir.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Efeitos comuns

Os efeitos comuns agem como o estado OpenGL 1 e podem ser definidos como segue.

```
<library_effects>
    <effect id="Blue-fx">
      <profile_COMMON>
        <technique sid="common">
          <phong>
            <emission>
              <color>0 0 0 1 </color>
            </emission>
            ...
            <index_of_refraction>
              <float>0</float>
            </index_of_refraction>
          </phong>
        </technique>
      </profile_COMMON>
    </effect>
</library_effects>
```

### Atributos de geometria

A geometria descreve os atributos do OpenGL e os define a seguir.
```
<library_geometries>
    <geometry id="box-lib" name="box">
      <mesh>
        <source id="box-lib-positions" name="position">
        </source>
        <source id="box-lib-normals" name="normal">
        </source>
        ...
        <vertices id="box-lib-vertices">
          <input semantic="POSITION" source="#box-lib-positions"/>
        </vertices>
        <polylist count="6" material="BlueSG">
          <input offset="0" semantic="VERTEX" source="#box-lib-vertices"/>
          <input offset="1" semantic="NORMAL" source="#box-lib-normals"/>
          <vcount>4 4 4 4 4 4 </vcount>
          <p>0 0 2 1 3 2 1 3 0 4 1 5 5 6 4 7 ...</p>
        </polylist>
      </mesh>
    </geometry>
</library_geometries>
```

### Cenas visuais

Cenas visuais são como cenas de unidade e contêm uma hierarquia de nós como segue.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## Referências
* [Especificações COLLADA 1.5.0](https://www.khronos.org/files/collada_spec_1_5.pdf)

