{
  "date" : "2019-10-11",
  "keywords" : [ "dae file", "dae file format", "what is an dae file", "file", "dae example", "dae file extension","extension", "format" ],
  "author" : {
    "display_name" : "Kashif Iqbal"
  },
  "draft" : "false",
  "toc" : true,
  "description":"Learn about DAE file format and APIs that can open and create DAE files.",
  "title" : "DAE - Digital Asset Exchange File Format",
  "linktitle" : "DAE",
  "menu" : {
    "docs" : {
      "parent" : "3d"
    }
  },
  "lastmod" : "2019-09-10"
}

## What is a DAE file?

A DAE file is a Digital Asset Exchange file format that is used for exchanging data between interactive 3D applications. This file format is based on the COLLADA (COLLAborative Design Activity) XML schema which is an open standard XML schema for the exchange of digital assets among graphics software applications. It has been adopted by ISO as a publicly available specification, ISO/pAS 17506. DAE files can be opened in applications such as Adobe Photoshop, AutoDesk Maya, AutoDesk AutoCAD, and APIs such as [Aspose.CAD](https://products.aspose.com/cad).

## DAE File Format

The DAE file format is based on the [COLLADA XML schema](https://www.khronos.org/files/collada_spec_1_5.pdf) where all the elements are defined as XML tags. It enables binding of diverse DCC and 3D processing tools into a production pipeline for 3D assets. It has comprehensive encoding of visual scenes including geometry, animation, shaders and physics. The format is open, archive-grade and retains meta information.

### COLLADA Tags

The COLLADA schema tag is as shown below.
```
<?xml version="1.0"?>
<COLLADA
  xmlns="http://www.collada.org/2005/11/COLLADASchema"
  version="1.4.1"
>
...
</COLLADA>
```
### Asset Tag

The asset tag describes the author and environment of the file

```
<asset>
  <author>alorino</author>
  <up_axis>Y_UP</up_axis>
</asset>
```

### Camera Library

COLLADA assets are contained inside libraries. The camera library contains unsurprisingly, cameras. Common cameras are perspective or orthographic. The camera library tag is defined as follow.
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
### Lights

Common lights are point, spot or directional
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

### Materials Instance

The Materials instance effects are defined as follow.
```
<library_materials>
    <material id="Blue" name="Blue">
      <instance_effect url="#Blue-fx"/>
    </material>
</library_materials>
```
### Common Effects

Common effects act like the OpenGL 1 state and can be defined as follow.

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

### Geometry Attributes

Geometry describes the OpenGL attributes and defined as follow.
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

### Visual Scenes

Visual scenes are like unity scenes and contain a hierarchy of nodes as follow.
```
<library_visual_scenes>
    <visual_scene id="VisualSceneNode" name="untitled">
        <node id="Camera" name="Camera">
        </node>
        ...
    </visual_scene>
</library_visual_scenes>
```

## References
 * [COLLADA 1.5.0 Specifications](https://www.khronos.org/files/collada_spec_1_5.pdf)
